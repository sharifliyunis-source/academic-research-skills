---
name: bibliography-search
description: "Systematic literature search and annotated bibliography agent. 3-agent pipeline for rigorous, reproducible literature searches with APA 7.0 annotated bibliographies. 4 modes: full systematic search, quick search, bibliography update, and citation check. Covers search strategy design, source screening (PRISMA-compliant), source quality assessment, and APA 7.0 citation formatting. Triggers on: bibliography, literature search, find sources, annotated bibliography, cite, citations, APA, references, systematic search, find papers, find articles, 文獻搜尋, 參考文獻, 書目, 引用格式, 系統性搜尋."
metadata:
  version: "1.0"
  last_updated: "2026-03-21"
  author: "Cheng-I Wu"
  license: "CC-BY-NC 4.0"
---

# Bibliography Search — Systematic Literature Search & Annotated Bibliography

A focused, 3-agent tool for systematic, reproducible literature searches and APA 7.0 annotated bibliographies. Use this when you need sources — not a full research report.

## Quick Start

**Minimal command:**
```
Find sources on the impact of retrieval-augmented generation on hallucination in LLMs
```

**With mode:**
```
/bibliography-search full: barriers to technology adoption in rural healthcare
/bibliography-search quick: mindfulness interventions for student burnout
/bibliography-search update: [paste existing bibliography]
/bibliography-search cite-check: [paste reference list]
```

---

## Trigger Conditions

### Trigger Keywords

**English**: bibliography, literature search, find sources, find papers, find articles, annotated bibliography, cite, citations, APA format, APA 7, references, reference list, systematic search, source list, literature review sources

**繁體中文**: 文獻搜尋, 找文獻, 找論文, 找資料, 參考文獻, 書目, 引用格式, APA格式, 系統性搜尋, 來源清單, 文獻清單

### Does NOT Trigger

| Scenario | Use Instead |
|----------|-------------|
| Full research report needed | `deep-research` |
| Writing a paper | `academic-paper` |
| Reviewing a paper | `academic-paper-reviewer` |
| Full research-to-paper pipeline | `academic-pipeline` |

### Quick Mode Selection Guide

| Your Situation | Recommended Mode |
|----------------|-----------------|
| Need comprehensive bibliography (10+ sources) | `full` |
| Need a quick source list (5–8 sources, fast) | `quick` |
| Have existing bibliography, need new sources added | `update` |
| Need to fix/verify APA 7.0 formatting | `cite-check` |

---

## Agent Team (3 Agents)

| # | Agent | Role | Phase |
|---|-------|------|-------|
| 1 | `bibliography_agent` | Search strategy design, source screening, annotated bibliography | Phase 1–2 |
| 2 | `source_quality_agent` | Evidence hierarchy grading, predatory journal screening, quality scoring | Phase 2 |
| 3 | `citation_formatter_agent` | APA 7.0 compliance checking, citation correction, reference list formatting | Phase 3 |

---

## Mode Reference

### `full` Mode — Systematic Search (Default)

Full systematic search following PRISMA-style documentation. Produces a complete annotated bibliography with search strategy and quality assessment.

**Minimum outputs**:
- Search strategy (databases, keywords, Boolean, date range)
- PRISMA flow (records identified → included)
- Annotated bibliography (≥ 10 sources)
- Source quality matrix
- APA 7.0 formatted reference list

**Time estimate**: Comprehensive

### `quick` Mode — Rapid Source List

Streamlined search for when you need sources fast. Fewer databases, less documentation overhead.

**Minimum outputs**:
- Condensed search strategy
- Annotated bibliography (5–8 sources)
- APA 7.0 formatted reference list

**Time estimate**: Fast

### `update` Mode — Add to Existing Bibliography

Accepts an existing bibliography and identifies new sources published after the original search date, or fills gaps in coverage.

**Input required**: Existing bibliography (APA format preferred)

**Minimum outputs**:
- Gap analysis (what was missing or outdated)
- New sources with annotations
- Updated combined bibliography
- Date of update documented

### `cite-check` Mode — APA 7.0 Verification

Accepts a reference list and verifies/corrects APA 7.0 formatting. Does not search for new sources.

**Input required**: Reference list (any format)

**Minimum outputs**:
- Error report (what was wrong and why)
- Corrected reference list in APA 7.0
- Formatting notes for recurring issues

---

## Orchestration Workflow

```
User: "Find sources on [topic]"
     |
=== Phase 1: SEARCH STRATEGY ===
     |
     +-> [bibliography_agent] -> Search Parameters
         - Define research question (if not provided)
         - Select databases appropriate to field
         - Generate keywords + synonyms + MeSH/controlled vocabulary
         - Design Boolean search strings
         - Set date range with justification
         - Define inclusion/exclusion criteria
         ** Present strategy to user for confirmation (full mode) **
     |
=== Phase 2: SEARCH & SCREEN ===
     |
     |-> [bibliography_agent] -> Source Corpus
     |   - Execute search across databases
     |   - Record hits per database (PRISMA)
     |   - Pass 1: Title + Abstract screening
     |   - Pass 2: Full-text assessment
     |   - Build annotated bibliography (APA 7.0)
     |   - Document exclusion reasons
     |
     +-> [source_quality_agent] -> Quality-Graded Sources
         - Assign evidence hierarchy level (I–VII) to each source
         - Flag predatory journals (Beall's list criteria)
         - Check for retractions (Retraction Watch)
         - Assess conflict-of-interest disclosures
         - Score methodological quality
         - Produce source quality matrix
     |
=== Phase 3: FORMATTING & DELIVERY ===
     |
     +-> [citation_formatter_agent] -> Final Output
         - Verify all citations against APA 7.0 rules
         - Correct formatting errors
         - Organize by theme (or alphabetical if unthemed)
         - Produce final annotated bibliography
         - Produce clean reference list (for copy-paste use)
```

---

## Output Format

```markdown
## Annotated Bibliography: [Topic]

**Search Date**: YYYY-MM-DD
**Mode**: [full / quick / update / cite-check]
**Total Sources**: N

---

### Search Strategy

**Research Question**: [RQ or topic scope]
**Databases Searched**: [list]
**Keywords**: [primary terms] AND/OR [secondary terms] AND/OR [synonyms]
**Boolean String**: [full string used]
**Date Range**: [YYYY–YYYY] — [justification]
**Language**: [included languages]
**Document Types**: [types included]

**Inclusion Criteria**:
- [criterion 1]
- [criterion 2]

**Exclusion Criteria**:
- [criterion 1]
- [criterion 2]

---

### PRISMA Flow

Records identified: ___
  └─ [Database A]: ___
  └─ [Database B]: ___
  └─ Other sources: ___

After duplicate removal: ___
Screened (title/abstract): ___
  └─ Excluded: ___ ([reason])
Full-text assessed: ___
  └─ Excluded: ___ ([reason])
**Included: ___**

---

### Sources (N = X)

#### [Theme 1: Theme Name]

**1. [APA 7.0 Citation]**
- **Relevance**: [How it relates to the research question]
- **Key Findings**: [2–3 main findings or arguments]
- **Methodology**: [Brief description of research design]
- **Evidence Level**: [I–VII] — [e.g., RCT, systematic review, case study]
- **Quality Notes**: [Strengths and limitations]
- **Contribution**: [What this source uniquely adds]

**2. ...**

#### [Theme 2: Theme Name]
...

---

### Source Quality Matrix

| # | Author (Year) | Level | Peer-Reviewed | Retracted | COI Disclosed | Score |
|---|--------------|-------|--------------|-----------|---------------|-------|
| 1 | [Author, Year] | II | ✓ | No | Yes | High |
| 2 | ... | | | | | |

---

### Reference List

[Author, A. A., & Author, B. B. (Year). ...]
[...]

---

### Search Limitations
- [limitation 1]
- [limitation 2]
```

---

## Quality Standards

| Standard | Full Mode | Quick Mode |
|----------|-----------|------------|
| Minimum sources | 10 | 5 |
| Peer-reviewed % | ≥ 60% | ≥ 50% |
| Sources ≤ 5 years old | ≥ 70% | ≥ 60% |
| APA 7.0 compliance | 100% verified | 100% verified |
| Search documented | Full PRISMA | Condensed |
| Quality graded | All sources | All sources |

---

## Handoff to `deep-research`

The annotated bibliography produced by this skill can serve as a direct input to `deep-research` Phase 2 (Investigation), bypassing the bibliography_agent step.

**Handoff materials**:
- Annotated bibliography with APA citations
- Search strategy documentation
- Source quality matrix

See `shared/handoff_schemas.md` for the full handoff schema.
