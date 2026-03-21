# Example: Citation Check Mode

**Command**: `/bibliography-search cite-check: [reference list pasted below]`

**Mode**: cite-check
**Date**: 2026-03-21

---

## Input: Reference List (Unformatted — as submitted)

```
1. Smith, John and Brown, Mary (2019). "The Effects of Remote Work on Employee Productivity." Journal of Organizational Behavior, Vol. 40, pp. 512-528. doi:10.1002/job.2234

2. WHO (2020). Mental Health and COVID-19. World Health Organization. www.who.int/teams/mental-health-and-substance-use/covid-19

3. Garcia A, Martinez R, and Lopez P (2021). Telework and Work-Life Balance: A Systematic Review. Frontiers in Psychology 12: 1–15.

4. Johnson, T. (n.d.) Remote work productivity: What the evidence says. Harvard Business Review.

5. Kim, S., Park, J., & Lee, H. (2022). Employee Well-being in the Post-Pandemic Era. In D. Chen (Ed.) Advances in Organizational Psychology, pp. 88-105. Springer.

6. Bloom N (2022). How working from home works out. Stanford Institute for Economic Policy Research. https://siepr.stanford.edu/publications/policy-brief/how-working-home-works-out
```

---

## Citation Correction Report

**Total citations checked**: 6
**Errors found**: 18 (across all 6 citations)
**Corrections made**: 16
**Items flagged for human review**: 2

---

### Corrections Made

---

**Citation 1** — Smith, John and Brown, Mary (2019)...

Original:
```
Smith, John and Brown, Mary (2019). "The Effects of Remote Work on Employee Productivity." Journal of Organizational Behavior, Vol. 40, pp. 512-528. doi:10.1002/job.2234
```

Corrected:
```
Smith, J., & Brown, M. (2019). The effects of remote work on employee productivity. Journal of Organizational Behavior, 40, 512–528. https://doi.org/10.1002/job.2234
```

Errors corrected:
- **F1**: Full first names used → corrected to initials (Smith, J., & Brown, M.)
- **F1**: "and" used instead of "&" between authors → corrected
- **F3**: Article title in quotation marks with Title Case → removed quotes; corrected to sentence case
- **F4**: "Vol. 40" — "Vol." prefix not used in APA 7 → removed; volume italicized
- **F4**: Issue number missing — if the journal paginates by issue, issue number is required → **FLAG: verify whether issue number should be included** (F10)
- **F7**: "pp. 512-528" — "pp." prefix not used for journal articles; hyphen → en dash → corrected to 512–528
- **F5**: `doi:10.1002/job.2234` → corrected to `https://doi.org/10.1002/job.2234`

---

**Citation 2** — WHO (2020)...

Original:
```
WHO (2020). Mental Health and COVID-19. World Health Organization. www.who.int/teams/mental-health-and-substance-use/covid-19
```

Corrected:
```
World Health Organization. (2020). *Mental health and COVID-19*. https://www.who.int/teams/mental-health-and-substance-use/covid-19
```

Errors corrected:
- **F1**: Abbreviation "WHO" used as author → APA 7 requires full organization name on first reference list entry: "World Health Organization."
- **F2**: Period missing after year parenthetical → corrected to (2020).
- **F3**: Report title not italicized → italicized
- **F3**: Title in Title Case → corrected to sentence case: *Mental health and COVID-19*
- **F9**: "World Health Organization" listed as publisher but is the same as author → per APA 7, omit publisher when author = publisher
- **F5**: URL missing "https://" → corrected to https://www.who.int/...
- **Note**: No retrieval date needed for organizational report with stable URL; acceptable.

---

**Citation 3** — Garcia A, Martinez R, and Lopez P (2021)...

Original:
```
Garcia A, Martinez R, and Lopez P (2021). Telework and Work-Life Balance: A Systematic Review. Frontiers in Psychology 12: 1–15.
```

Corrected:
```
Garcia, A., Martinez, R., & Lopez, P. (2021). Telework and work-life balance: A systematic review. *Frontiers in Psychology*, *12*, Article 1–15. https://doi.org/[DOI REQUIRED — F9]
```

Errors corrected:
- **F1**: No commas after surnames → corrected (Garcia, A.)
- **F1**: "and" → "&"
- **F2**: Year not in parentheses → (2021).
- **F3**: Title "Telework and Work-Life Balance: A Systematic Review" in Title Case → sentence case; correct to "Telework and work-life balance: A systematic review"
- **F4**: Journal not italicized → *Frontiers in Psychology*
- **F4**: Volume "12" not italicized → *12*
- **F4**: Colon separator → comma after journal title: *, 12,*
- **F9**: No DOI — Frontiers in Psychology is an open-access journal and all articles have DOIs → **FLAG: DOI required, please provide** (F9)

---

**Citation 4** — Johnson, T. (n.d.)...

Original:
```
Johnson, T. (n.d.) Remote work productivity: What the evidence says. Harvard Business Review.
```

Corrected:
```
Johnson, T. (n.d.). *Remote work productivity: What the evidence says*. Harvard Business Review. [URL REQUIRED — F9]
```

Errors corrected:
- **F6**: Period missing after (n.d.) → corrected to (n.d.).
- **F3**: Title not italicized for a standalone web document → italicized
- **F9**: No URL — webpage references require a URL → **FLAG: URL required** (F9)
- **Note**: "n.d." is acceptable if date genuinely cannot be determined. Recommend checking HBR website for publication date.

---

**Citation 5** — Kim, S., Park, J., & Lee, H. (2022)...

Original:
```
Kim, S., Park, J., & Lee, H. (2022). Employee Well-being in the Post-Pandemic Era. In D. Chen (Ed.) Advances in Organizational Psychology, pp. 88-105. Springer.
```

Corrected:
```
Kim, S., Park, J., & Lee, H. (2022). Employee well-being in the post-pandemic era. In D. Chen (Ed.), *Advances in organizational psychology* (pp. 88–105). Springer.
```

Errors corrected:
- **F3**: Chapter title in Title Case → sentence case
- **F6**: Missing comma after "(Ed.)" → corrected to "(Ed.),"
- **F3**: Book title in Title Case → *Advances in organizational psychology*
- **F4**: Book title not italicized → italicized
- **F7**: "pp. 88-105" → "(pp. 88–105)" — parentheses required around page range for book chapters; hyphen → en dash
- **Note**: No DOI provided — if available, add. If published by Springer, a DOI likely exists.

---

**Citation 6** — Bloom N (2022)...

Original:
```
Bloom N (2022). How working from home works out. Stanford Institute for Economic Policy Research. https://siepr.stanford.edu/publications/policy-brief/how-working-home-works-out
```

Corrected:
```
Bloom, N. (2022). *How working from home works out*. Stanford Institute for Economic Policy Research. https://siepr.stanford.edu/publications/policy-brief/how-working-home-works-out
```

Errors corrected:
- **F1**: No comma after surname → Bloom, N.
- **F2**: Year not in parentheses → (2022).
- **F3**: Report title not italicized → italicized
- **Note**: No report number visible — if SIEPR assigns one, add after title: *(Policy Brief No. xxx)*

---

### Items for Human Review

1. **Citation 1** (Smith & Brown, 2019): Issue number missing. If *Journal of Organizational Behavior* paginates by issue (it does), the issue number must be included: `*Journal of Organizational Behavior*, *40*(issue_number), 512–528`. Please verify the issue number.

2. **Citation 3** (Garcia et al., 2021): DOI missing for a Frontiers in Psychology article. All Frontiers articles have DOIs. Please locate and add the DOI: `https://doi.org/10.3389/fpsyg.2021.XXXXXX`.

---

### Notes on Recurring Issues

1. **DOI format**: All citations with DOIs used the old `doi:` prefix. APA 7 requires the full `https://doi.org/` URL format.
2. **Title case**: All article and chapter titles were submitted in Title Case. APA 7 uses sentence case for article and chapter titles (only first word and proper nouns capitalized).
3. **Author formatting**: Multiple citations used full first names or "and" instead of initials and "&". Ensure all future references use initials only and "&" in reference lists.

---

## Corrected Reference List (Final)

Bloom, N. (2022). *How working from home works out*. Stanford Institute for Economic Policy Research. https://siepr.stanford.edu/publications/policy-brief/how-working-home-works-out

Garcia, A., Martinez, R., & Lopez, P. (2021). Telework and work-life balance: A systematic review. *Frontiers in Psychology*, *12*, Article 1–15. https://doi.org/[ADD DOI]

Johnson, T. (n.d.). *Remote work productivity: What the evidence says*. Harvard Business Review. [ADD URL]

Kim, S., Park, J., & Lee, H. (2022). Employee well-being in the post-pandemic era. In D. Chen (Ed.), *Advances in organizational psychology* (pp. 88–105). Springer.

Smith, J., & Brown, M. (2019). The effects of remote work on employee productivity. *Journal of Organizational Behavior*, *40*([ADD ISSUE]), 512–528. https://doi.org/10.1002/job.2234

World Health Organization. (2020). *Mental health and COVID-19*. https://www.who.int/teams/mental-health-and-substance-use/covid-19
