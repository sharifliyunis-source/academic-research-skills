# Search Strategy Template

## Purpose

Document your search strategy before executing it. A complete search strategy record enables reproducibility and is required for systematic review registration (PROSPERO, OSF).

---

## Search Strategy Record

### Administrative Information

**Research Question**: [Precise, answerable RQ or topic scope]
**Prepared by**: [Agent/researcher]
**Date prepared**: YYYY-MM-DD
**Date executed**: YYYY-MM-DD (fill after execution)
**Mode**: [full / quick / update]

---

### Database Selection

| Database | Rationale | Search Date | Hits |
|----------|-----------|-------------|------|
| [Database 1] | [Why this DB for this topic] | YYYY-MM-DD | ___ |
| [Database 2] | [Why this DB for this topic] | YYYY-MM-DD | ___ |
| [Database 3] | [Why this DB for this topic] | YYYY-MM-DD | ___ |
| Google Scholar | Supplementary / grey literature | YYYY-MM-DD | ___ |

**Total hits before deduplication**: ___

---

### Keyword Development

**Step 1: Identify core concepts**

Break the RQ into 2–4 core concepts:
- Concept A: [e.g., "intervention"]
- Concept B: [e.g., "population"]
- Concept C: [e.g., "outcome"]
- Concept D: [optional]

**Step 2: Generate synonyms for each concept**

| Concept A | Concept B | Concept C | Concept D |
|-----------|-----------|-----------|-----------|
| [term 1] | [term 1] | [term 1] | [term 1] |
| [synonym] | [synonym] | [synonym] | [synonym] |
| [MeSH/thesaurus] | [MeSH/thesaurus] | [MeSH/thesaurus] | — |

**Step 3: Construct Boolean string**

```
(Concept A term 1 OR Concept A synonym 1 OR Concept A synonym 2)
AND
(Concept B term 1 OR Concept B synonym 1 OR Concept B synonym 2)
AND
(Concept C term 1 OR Concept C synonym 1)
[AND NOT exclusion term if needed]
```

**Database-specific adaptations**:

| Database | Adapted String | Notes |
|----------|---------------|-------|
| PubMed | `[exact string]` | MeSH terms added: [...] |
| Scopus | `[exact string]` | TITLE-ABS-KEY() field |
| Web of Science | `[exact string]` | TS= field |
| [Other] | `[exact string]` | — |

---

### Date Range

**Range**: YYYY to YYYY (or "no restriction")

**Rationale**:
> [Explain why this date range. Examples: "The intervention was introduced in YYYY"; "Post-[event] research only"; "Field is rapidly evolving — limiting to last 5 years"; "No restriction — foundational papers from 1960s are still cited"]

**Seminal paper exceptions** (if any):
- [Author, Year] — included despite predating range because [reason]

---

### Language Selection

**Languages included**: [English / English + Spanish / etc.]

**Rationale** (if restricted):
> [Explain why restriction applied. If English-only, acknowledge as limitation]

---

### Inclusion/Exclusion Criteria

**Inclusion Criteria** (all must be met for a source to be included):
| Code | Criterion | Decision Rule |
|------|-----------|---------------|
| IC1 | | Include if: ___ |
| IC2 | | Include if: ___ |
| IC3 | | Include if: ___ |
| IC4 | | Include if: ___ |

**Exclusion Criteria** (any one causes exclusion):
| Code | Criterion | Decision Rule |
|------|-----------|---------------|
| EC1 | | Exclude if: ___ |
| EC2 | | Exclude if: ___ |
| EC3 | | Exclude if: ___ |

---

### Screening Protocol

**Pass 1 — Title/Abstract Screening**
- Apply: IC1, IC2, EC1, EC2, EC3 (criteria determinable from abstract)
- When uncertain: **include** (conservative approach)
- Record reason for exclusion by batch

**Pass 2 — Full-Text Screening**
- Apply: all remaining criteria
- Record specific exclusion reason per article (E1–E10 codes)
- Retain borderline decisions with notes

---

### Search Execution Log

For each database, record:

```
DATABASE: ___
Date: YYYY-MM-DD
String used:
  [paste exact string used, including field tags]
Hits: ___
Notes: [any deviations from planned string; database errors; filter applications]
```

---

### Deduplication

**Method**: [Manual / Reference manager (Zotero, Mendeley, EndNote) / Other]
**Duplicates removed**: ___
**Basis for duplicate identification**: [exact DOI match / title + author + year / other]

---

### PRISMA Flow (Fill During Execution)

```
Records identified: ___
  └─ [DB 1]: ___  └─ [DB 2]: ___  └─ [DB 3]: ___  └─ Other: ___
Duplicates removed: ___
Title/Abstract screened: ___
  └─ Excluded: ___ (reasons below)
Full-text assessed: ___
  └─ Excluded: ___ (reasons below)
INCLUDED: ___
```

**T/A exclusion breakdown**:
- E1 (irrelevant): ___
- E6 (date): ___
- E7 (not peer-reviewed): ___
- Other: ___

**Full-text exclusion breakdown**:
- E1 (irrelevant): ___
- E5 (wrong design): ___
- E9 (no access): ___
- Other: ___

---

### Strategy Evaluation

Before executing: answer these questions.

**Recall check**: Have I included all likely synonyms? Could key papers use different terminology?

**Precision check**: Is the search specific enough to avoid thousands of irrelevant hits? Consider adding a Concept C to narrow.

**Database coverage check**: Have I selected databases that cover:
- [ ] The primary discipline?
- [ ] Interdisciplinary work at the boundary of the topic?
- [ ] Grey literature (if relevant)?
- [ ] Non-English sources (if required)?

**Feasibility check**: Is the expected number of hits manageable for screening?
- < 200 hits: Manageable for solo screener
- 200–1000: Systematic but manageable; allow 2–5 hours for screening
- > 1000: Consider narrowing strategy or adding exclusion terms
