# SynBioHub Issues — September 2026 Community Findings

## v3 (The Future) — Active Development

### 🔴 Critical: Swagger API (#1106)
- **Filed:** Sep 3, 2026 by cjmyers
- **Milestone:** SBH 3.0.0
- **Assignee:** pagarap57
- **Why it matters:** This is the API that could fix iBioSim's broken SynBioHub upload integration (#639, #632). A proper Swagger-documented API would enable reliable tool-to-platform integration and unlock third-party clients.

### 🟡 UX Research Issues (SBH 2.0.0)
- #1107: Update Collections Page (Sep 4, 2026 — BroD54)
- #1093: Add owner modal (Aug 2026)
- #1092: Sharing — visibility of status (Aug 2026)
- #1091: Add owner list of users (Aug 2026)
- #1060: Search Suggestions (Jul 2026)
- #1062: Create 2 boxes when applying filters (Jul 2026)

### 🔵 Bug: Search Quality
- #1108: Dev2 doesn't show any similar parts (Sep 12, 2026 — cl117)

## v1 (Legacy) — Final Maintenance (Milestone SBH 1.6.2)

### Data Integrity
| Issue | Title | Date | Status |
|---|---|---|---|
| #1756 | SubCollections missing from public graph | Sep 3, 2026 | ✅ Fixed (7c6c191) |
| #1753 | OMEX download missing SBML attachments | Aug 21, 2026 | 🔴 Open (2 comments) |

### Workflow Gaps
| Issue | Title | Date |
|---|---|---|
| #1755 | Recursive download doesn't follow linked collections | Aug 30, 2026 |
| #1746 | Incremental updates not working with SBOLExplorer | Jul 19, 2026 |

### Infrastructure
| Issue | Title | Date |
|---|---|---|
| #1754 | Legacy data in Virtuoso should be deleted | Aug 23, 2026 |
| #1752 | Private-to-public visibility resets prefix | Aug 19, 2026 |
| #1744 | Backend lacks OR request parsing | Jul 16, 2026 |
| #1745 | Root collection filter — SBOLCanvas layout | Jul 16, 2026 |

## Key Takeaway

The v1-to-v3 migration is the defining infrastructure story. Issue #1753 (OMEX/SBML export) reveals the root cause of the interoperability crisis: `Model->source` references aren't traversed during export. The fix is structural — restructuring SBML files as direct Model attachments — not a patch.

Meanwhile, v3's Swagger API (#1106) is the bridge that could connect desktop tools (iBioSim) and web tools (GENtle2) to the redesigned platform.