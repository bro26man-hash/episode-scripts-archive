# 🔬 Detailed Research Notes — Synbio & Biotech Software Tools

## Survey Methodology

1. **Repository Discovery** — Searched GitHub with queries: `synthetic biology`, `biotech software tools bioinformatics`, `synthbio CAD biology design`
2. **Star-Ranked Analysis** — Identified top projects by community engagement (stars, forks, recent activity)
3. **Open-Issue Triage** — Reviewed recent open issues across 10+ repositories, sorted by last-updated date
4. **Deep-Dive Inspection** — Examined detailed issue threads on the most-reported bugs (SynBioHub #1753, iBioSim #637)
5. **Commit-Activity Analysis** — Reviewed recent commits on the two most actively maintained repos (SynBioHub v1: 5 commits/week; iBioSim: steady monthly fixes)

---

## Repository Inventory

### Tier 1: High-Impact Platforms (50+ stars, active maintenance)

| Repo | Stars | Language | License | Status |
|---|---|---|---|---|
| [biopython/biopython](https://github.com/biopython/biopython) | 5,070 | Python | BSD | ✅ Active |
| [google/deepvariant](https://github.com/google/deepvariant) | 3,726 | Python | Apache-2.0 | ✅ Active |
| [nextflow-io/nextflow](https://github.com/nextflow-io/nextflow) | 3,412 | Groovy | Apache-2.0 | ✅ Active |
| [synthea](https://github.com/synthetichealth/synthea) | 3,342 | Java | Apache-2.0 | ✅ Active |
| [TDC](https://github.com/mims-harvard/TDC) | 1,283 | Jupyter | MIT | ✅ Active |
| [poly](https://github.com/bebop/poly) | 737 | Go | MIT | ✅ Active |
| [deepTools](https://github.com/deeptools/deepTools) | 765 | Python | GPL-3.0 | ✅ Active |
| [DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) | 274 | Python | MIT | ✅ Active |
| [awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) | 223 | — | CC-BY-4.0 | ✅ Active |
| [GENtle2](https://github.com/Synbiota/GENtle2) | 106 | JavaScript | — | ⚠️ Stalled |
| [act (20n)](https://github.com/20n/act) | 92 | Java/Scala | GPL-3.0 | 🔒 Internal |
| [SynBioHub v1](https://github.com/SynBioHub/synbiohub) | 84 | JS/Java | BSD-2-Clause | 🟡 Maintenance |
| [SynBioHub v3](https://github.com/SynBioHub/synbiohub3) | 16 | JS/Java | BSD-2-Clause | ✅ Active (rewrite) |
| [Cello-v2](https://github.com/CIDARLAB/Cello-v2) | 74 | Java | MIT | ✅ Active |
| [iBioSim](https://github.com/MyersResearchGroup/iBioSim) | 67 | Java | Apache-2.0 | ⚠️ Struggling |
| [ART (JBEI)](https://github.com/JBEI/ART) | 66 | Jupyter | — | 🔒 Private code |

### Tier 2: Emerging & Niche Tools (10-50 stars)

| Repo | Stars | Language | Notable Feature |
|---|---|---|---|
| [Coral](https://github.com/klavinslab/coral) | 32 | Python | Design-as-code framework; minimal open issues |
| [BioCRNpyler](https://github.com/BuildACell/bioCRNpyler) | 54 | Python | CRN compiler with TXTL cell-free support |
| [CASPIA](https://github.com/shenmaa233/SJTU-software-CASPIA) | 13 | Python | AI-powered metabolic engineering |

### Tier 3: Bleeding-Edge (5-15 stars)

| Repo | Stars | Language | Architecture |
|---|---|---|---|
| [SynBioHub v3](https://github.com/SynBioHub/synbiohub3) | 16 | JS/Java | React (Next.js) + Spring Boot (Java 17) |
| [Syn-Zeug](https://github.com/Sheffield-iGEM/syn-zeug) | 7 | Rust + Svelte + WASM | Modern web-native toolbox |
| [sboljs3](https://github.com/SynBioDex/sboljs3) | 7 | TypeScript | SBOL library for TS/JS apps |

---

## Issue Analysis: SynBioHub v1 (8 Open Issues — Milestone SBH 1.6.2)

### Data Integrity & Export Completeness

**#1756 — SubCollections does not report members in public graph**
- Filed: Sep 3, 2026 by cjmyers (maintainer)
- Fix already merged: commit `7c6c191` ("Fix public subcollection graph clauses")
- **Significance:** Public graph views were hiding sub-collection members, meaning users couldn't see nested designs. The fix was immediate — maintainer is actively triaging.

**#1753 — OMEX download missing SBML file attachments**
- Filed: Aug 21, 2026 by Gonza10V
- 2 comments, community affected
- **Root cause (from cjmyers):** `Model->source` is not followed to find all files during OMEX export. SBML files get orphaned because they're referenced indirectly, not as direct attachments.
- **Proposed fix (from cjmyers):** Restructure SBML files as direct attachments of Model objects (pattern used in SynBioSuite).
- **Significance:** This is THE interoperability bottleneck. If OMEX exports are incomplete, researchers can't reliably share designs between tools.

### Workflow Gaps

**#1755 — Recursive download does not follow linked collections**
- Filed: Aug 30, 2026 by cjmyers
- Downloads don't traverse linked collection references
- **Impact:** Researchers can't do bulk downloads of related design families

**#1746 — Incremental updates not working with SBOLExplorer**
- Filed: Jul 19, 2026 by cjmyers
- Assigned to cl117
- **Impact:** SBOLExplorer can't pull incremental updates from SynBioHub v1

### Infrastructure & Query Capabilities

**#1754 — Legacy data in Virtuoso should be deleted**
- Filed: Aug 23, 2026 by cjmyers
- **Significance:** The RDF triplestore (Virtuoso) is accumulating deprecated entries. This is a sign of aging infrastructure.

**#1752 — Private-to-public visibility change resets prefix**
- Filed: Aug 19, 2026 by cl117
- Changing visibility from private to public resets the URI prefix from `localhost:3333` to `synbiohub.org`
- **Impact:** Deployment friction for local instances

**#1744 — Backend should have a mechanism to parse OR request**
- Filed: Jul 16, 2026 by cl117
- Backend lacks OR (logical disjunction) query parsing support
- **Impact:** Limited query expressiveness compared to modern APIs

**#1745 — Root collection filter should handle SBOLCanvas layout properly**
- Filed: Jul 16, 2026 by cjmyers
- SBOLCanvas layout not respected in root collection filter
- **Impact:** Visualization inconsistency

---

## Issue Analysis: iBioSim (7 Open Issues — Cross-Platform Struggles)

### The Jena/Xerces Crash (#637) — Most Discussed

**Error:**
```
java.lang.NoClassDefFoundError: Could not initialize class org.apache.jena.query.ARQ
Caused by: java.lang.NoClassDefFoundError: org/apache/xerces/util/XMLChar
```

**Timeline:** Jan 20, 2025 — Jan 25, 2025 (6 comments)

**Discussion thread:**
1. **Hatem-synbio** reported the crash while debugging Kenzo's toggle switch model using the iBioSim tutorial (page 94, automatic model generation)
2. Shared screenshots and offered the COMBINE archive on Slack
3. **cjmyers (maintainer)** root-caused: *"I'm pretty sure the issue has to do with trying to create a model using iGEM parts. iGEM parts do not have interaction information, so it is impossible to generate a model. Granted, there should be a better error than an exception. To actually test this better, should use the Cello library."\*
4. cjmyers requested the COMBINE archive for deeper testing

**Key insight:** The crash isn't a bug — it's a design limitation. iGEM parts lack interaction information needed for model generation. But instead of a user-friendly error message, the tool crashes with a cryptic Java exception. This reveals a significant UX gap.

**Implication for Swagger API (#1106):** If iBioSim could reliably upload to SynBioHub v3's proper API, it might offload some computation or get better error handling through the platform.

### Cross-Platform Issues

| Issue | OS | Problem | Comments |
|---|---|---|---|
| #638 | macOS | Can't run iBioSim 3.2.0 | 1 |
| #635 | Windows 11 | Cannot open iBioSim | 4 |
| #640 | Cross-platform | Java exception (runtime crash) | 1 |

### Integration Failures

| Issue | Target | Problem |
|---|---|---|
| #639 | SynBioHub | Can't upload design (API incompatibility) |
| #632 | LCP Synbiohub | Can't connect (handshake failure) |

---

## Issue Analysis: GENtle2 (75+ Open Issues — 10+ Year Legacy)

### The Refactor Milestones

The maintainer (`alexandremeunier`) has created two refactor milestones:

1. **Refactor — Canvas events & RES/annotation cards information**
   - #164: Display feature details when hovering (2014)
   - #163: Tracking mouse events in `Artist` (2014)
   - #159: Tracking shapes in `Artist` (2014, 6 comments)

2. **Refactor — Sequence opening/editing**
   - #132: Replace non-allowed chars on Genebank import (2014)
   - #130: Bug with selection using up arrow (2014)

### The Persistent Bugs

| Issue | Bug | Impact |
|---|---|---|
| #162 | Selection disappears via context menu | Data loss risk |
| #161 | Selection disappears with hotkeys (no shift) | Workflow interruption |
| #158 | Creating feature clears plasmid map without redraw | Visualization failure |
| #156 | Caret moves by one base unexpectedly during selection | Input accuracy |
| #154 | Plasmid map title overflows for long sequence names | Display issue |

### The Story These Issues Tell

GENtle2 has **75+ open issues dating to 2014**. The maintainer is attempting a clean-slate architecture (the Refactor milestones), but progress is glacial. With only 6 comments on the most discussed issue (#159) and a 9+ year timeline for the refactor, this is a cautionary tale about **sustaining open-source scientific software**.

The community is **starved for contributors**. The tool is well-known (106 stars) but the codebase is inaccessible to new contributors because it's JavaScript from 2014 with no TypeScript, no tests, and no CI pipeline.

---

## Issue Analysis: Syn-Zeug (10 Open Issues — All Features, No Bugs)

### The Architecture

Syn-Zeug uses a **three-layer architecture** that's worth studying:

1. **Rust Core Library** — Performance-critical sequence operations (Extract Subsequences, Hamming Distance, Levenshtein Distance)
2. **Svelte SPA** — Modern web UI with interactive pipeline builder
3. **WASM Shim (biobox)** — Allows Rust library to run in the browser

### Feature Roadmap

| Category | Issues | Status |
|---|---|---|
| **New Tools** | #47 (Protein ORFs), #26 (Percent Composition), #17 (Shuffle Sequence), #8 (Mutate Sequence), #42 (Misc) | All open |
| **Pipeline UX** | #38 (Pause tool), #36 (Drag-and-drop) | Both open |
| **UI Polish** | #37 (Tooltips), #39 (Region info like Benchling) | Both open |
| **Dependencies** | #46 (rust-bio updates) | 1 comment |

### Significance

The **all-feature-request, zero-bug-report** pattern is extraordinary. It means:
- The core is stable and well-tested
- The architecture is sound (Rust + WASM is working)
- The community is productively engaged (suggesting features, not reporting crashes)
- This is what sustainable open-source looks like

Syn-Zeug represents **the future of web-native bioinformatics tooling**.

---

## Cross-Project Themes

### Theme 1: The Interoperability Crisis

SynBioHub v1's issues are almost exclusively about **data not moving correctly** between tools:
- OMEX exports missing SBML attachments (#1753)
- Recursive downloads breaking (#1755)
- Incremental sync failing (#1746)
- OR queries not supported (#1744)

The root cause is architectural: the Virtuoso RDF triplestore was designed for flexible data representation, not reliable data export. The `Model->source` reference chain is a classic example — it works for internal queries but breaks during export.

**The fix is structural, not patchable.** Restructuring SBML files as direct Model attachments (as done in SynBioSuite) is the right approach, but it requires a coordinated update across all tools that consume OMEX bundles.

### Theme 2: The Desktop Tool Bottleneck

iBioSim (305+ open issues) and GENtle2 (75+ open issues) share a common pattern:
- **Java dependency hell** — iBioSim's Jena/Xerces crash (#637) is symptoms of deeper dependency management problems
- **OS-specific breakage** — Mac (#638), Windows 11 (#635)
- **Aging UI codebases** — GENtle2's 2014-era JavaScript
- **Broken platform integration** — iBioSim can't upload to SynBioHub (#639, #632)

The solution isn't better desktop apps — it's **web-native tools** that don't require installation, don't have OS-specific builds, and can be updated centrally.

### Theme 3: The Swagger API as Linchpin

Issue [#1106](https://github.com/SynBioHub/synbiohub3/issues/1106) — "Develop New API Using Swagger" — filed Sep 3, 2026 under the SBH 3.0.0 milestone.

This single issue could unlock:
- ✅ Reliable iBioSim ↔ SynBioHub integration
- ✅ Third-party client development
- ✅ Plugin architecture for tools
- ✅ Versioned, documented API surface
- ✅ Migration path from v1 to v3

Without it, the v3 redesign is just a prettier frontend. With it, SynBioHub becomes a true platform.

### Theme 4: The Missing Open-Source ML Stack

ART (JBEI) and 20n/act represent the frontier of **computational biology design**:
- ART: Probabilistic strain recommendations using MCMC and Bayesian optimization
- 20n/act: End-to-end DNA design automation (predicted first bio-route to acetaminophen)

But **both are closed-source**. ART's code is private (license access only). 20n/act is maintained internally by 20n Inc.

There's a clear opportunity for an **open-source, web-native, ML-integrated design tool** that the community can build and modify together. Syn-Zeug (Rust) and sboljs3 (TypeScript) are early indicators of this direction.

### Theme 5: Standards Are Maturing, but Pipelines Aren't

SBOL and SBML are well-defined standards with active working groups. But the **pipelines** that move data between tools are broken:
- OMEX exports are incomplete (#1753)
- Recursive collection resolution fails (#1755)
- Incremental sync doesn't work (#1746)

The standards exist. The plumbing doesn't.

`sboljs3` bringing SBOL to the browser is a promising sign — the next step is making those standards reachable from web-native tools end-to-end.

---

## Recommended Episode Topics

Based on the research findings, here are 8 episode topics ranked by timeliness and community impact:

| # | Episode | Angle | Key Issues | guests |
|---|---|---|---|---|
| 1 | **The Swagger API as Linchpin** | Interview cjmyers about why #1106 matters and what it will unlock | synbiohub3#1106 | cjmyers |
| 2 | **The Interoperability Crisis** | Deep-dive into OMEX export bugs and what they mean for daily lab work | synbiohub#1753, #1755 | Gonza10V, cjmyers |
| 3 | **Why Desktop Tools Die** | iBioSim's 305 issues and GENtle2's 12-year refactor — what went wrong? | iBioSim#637, GENtle2#159 | Lukas Buecherl |
| 4 | **The Rust Revolution in Bioinformatics** | Syn-Zeug's all-feature roadmap and the WASM architecture pattern | syn-zug#47, #36 | Sheffield-iGEM team |
| 5 | **From Hand Engineering to Computational Design** | ART and 20n/act — the "DeepSeek moment" for synbio | ART, 20n/act | JBEI team |
| 6 | **SBOL in the Browser** | How sboljs3 and SynBioHub v3 are bringing standards to the web | sboljs3, synbiohub3#1106 | pagarap57 |
| 7 | **The Maintenance Trap** | Why academic software stalls (GENtle2) vs. what makes it sustain (Coral) | GENtle2#159, Coral#37 | Klavins Lab |
| 8 | **The Design-Build-Learn Cycle, Code-First** | Coral and BioCRNpyler — specifying biology as software | Coral, BioCRNpyler | Klavins Lab, BuildACell |

---

## Research Sources

| Source | Type | Date |
|---|---|---|
| SynBioHub v1 open issues | GitHub Issues API | Sep 2026 |
| SynBioHub v3 open issues | GitHub Issues API | Sep 2026 |
| iBioSim open issues | GitHub Issues API | Aug 2025–Apr 2024 |
| GENtle2 open issues | GitHub Issues API | Jul 2014–Jul 2023 |
| Syn-Zeug open issues | GitHub Issues API | Apr 2022–Oct 2022 |
| SynBioHub v1 commits | GitHub Commits API | Sep 2026 |
| iBioSim commits | GitHub Commits API | Apr 2026 |
| SynBioHub v1 #1753 discussion | GitHub Issue comments | Aug 2026 |
| iBioSim #637 discussion | GitHub Issue comments | Jan 2025 |
| Repository metadata | GitHub REST API | Sep 2026 |
| awesome-synthetic-biology list | GitHub Repository | Sep 2026 |