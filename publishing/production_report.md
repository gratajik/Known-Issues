# Production Report — known-issues

_Generated 2026-07-12 by BookForge._

## The book

| | |
|---|---|
| Chapters | 18 |
| Words | 55,254 |
| Pages (≈250 words/page) | ~221 |
| Review passes | 7 |
| Converged | yes |

## Cost

| | |
|---|---|
| As-if-API (every call at list price) | $17.86 |
| — writing | $7.81 |
| — review + audit | $9.91 |
| — publishing | $0.14 |
| Actually paid (itemized metered calls) | $0.00 |

_0 of 54 logged review calls used the metered API; unlogged phases (writing, fixes, verifies) run proxy-first and their metered fallbacks, if any, are not itemized — treat 'actually paid' as a floor._

## Time by phase

| Phase | Duration | Commits |
|---|---|---|
| Write | 1h 31m | 19 |
| Review | 1h 32m | 13 |
| Audit | 35m | 1 |
| **Total** | **3h 39m** | |

_Derived from git commit timestamps; gaps between runs (cold proxy waits, operator pauses) are included in the phase that followed them._

## Tokens

| | |
|---|---|
| Output tokens, logged review calls | 130,584 |
| Input tokens, logged (metered calls only) | 0 |
| Cache write / read, logged | 0 / 0 |
| Estimated total output tokens, all phases | ~714,563 |

_Estimate backs total output out of the as-if-API cost at $25/MTok; proxy calls do not meter input._

## Outstanding issues

**No blocking issues** — the audit gate is clear.

Also on record: 12 non-blocking issue(s) shipped with the book; 14 claim(s) refuted with quote-verified evidence (see tracking/known_issues.md).
