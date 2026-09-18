# Community Findings: Open Issues Across Synbio & Biotech Projects
**Research Date:** September 18, 2026  
**Scope:** 10 GitHub repositories, 70+ open issues analyzed  
**Methodology:** Live GitHub API issue retrieval, comment thread analysis, commit activity review

---

## Table of Contents
1. [SynBioHub v1 — The Interoperability Hub](#1-synbiohub-v1--the-interoperability-hub)
2. [SynBioHub v3 — The Great Redesign](#2-synbiohub-v3--the-great-redesign)
3. [iBioSim — CAD Tool Cross-Platform Struggles](#3-ibiosim--cad-tool-cross-platform-struggles)
4. [GENtle2 — Legacy UI Debt](#4-gentle2--legacy-ui-debt)
5. [Syn-Zeug — Modern Stack Feature Expansion](#5-syn-zeug--modern-stack-feature-expansion)
6. [DnaChisel — Chemistry-Aware Optimization](#6-dnachisel--chemistry-aware-optimization)
7. [BioCRNpyler — RNA Devices & TXTL](#8-biocrnpyler--rna-devices--txtl)
8. [poly — Release-Blocking Dependency Chain](#9-poly--release-blocking-dependency-chain)
9. [Coral — The Maintenance Benchmark](#10-coral--the-maintenance-benchmark)
10. [Cross-Cutting Themes](#cross-cutting-themes)

---

## 1. SynBioHub v1 — The Interoperability Hub

**Repository:** [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub)  
**Stars:** 84 | **Forks:** 30 | **License:** BSD-2-Clause  
**Stack:** JavaScript (Node.js) + Java (Maven) + OpenLink Virtuoso (RDF triplestore)  
**Current Milestone:** SBH 1.6.2 (final maintenance)

### Open Issues (8 total, all in SBH 1.6.2)

| # | Title | Type | Date | Assignee |
|---|-------|------|------|----------|
| #1756 | SubCollections does not report members in public graph | Bug — data integrity | Sep 3, 2026 | cjmyers |
| #1755 | Recursive download does not follow linked collections | Bug — workflow gap | Aug 30, 2026 | cjmyers |
| #1754 | Legacy data in Virtuoso should be deleted | Maintenance — tech debt | Aug 23, 2026 | cjmyers |
| #1753 | OMEX download missing SBML file attachments | Bug — export completeness | Aug 21, 2026 | Gonza10V |
| #1752 | Private-to-public visibility shifts URL prefix | Bug — deployment friction | Aug 19, 2026 | cl117 |
| #1746 | Incremental updates not working with SBOLExplorer | Bug — tool integration | Jul 19, 2026 | cl117 |
| #1745 | Root collection filter should handle SBOLCanvas layout | Change — visualization | Jul 16, 2026 | cjmyers |
| #1744 | Backend lacks OR request parsing mechanism | Bug — query capability | Jul 16, 2026 | cjmyers |

### Community Discussion: Issue #1753 (OMEX/SBML Export Bug)

**Reporter:** Gonza10V  
**Comments:** 2  
**Date:** August 21–22, 2026

**cjmyers (maintainer) — Root cause analysis:**
> "The issue is that Model->source is not followed to find all files. However, the SBML file will come in an OMEX download of the Attachment object or the Collection that has the Attachment as a member."

**cjmyers — Fix pattern from SynBioSuite:**
> "For SynBioSuite, fixed this by making the SBML file an attachment of the Model object."

**Analysis:** This is a design-level issue, not a patch. The v1 platform's data model doesn't properly traverse object graphs during OMEX export. The fix requires restructuring how SBML files are referenced within bundles — making them attachments of Model objects rather than relying on source references. This signals the ecosystem is maturing: users need dependable data pipelines, and the current infrastructure can't deliver them.

### What This Tells Us
- All 8 issues are in the **final maintenance milestone** (SBH 1.6.2)
- The Virtuoso triplestore is showing its age — recursive collection resolution, export completeness, and DB hygiene are all failing
- The maintainer (cjmyers) is actively working every issue personally
- **The v1 is in graceful decline** — the community's focus has shifted to v3

---

## 2. SynBioHub v3 — The Great Redesign

**Repository:** [SynBioHub/synbiohub3](https://github.com/SynBioHub/synbiohub3)  
**Stars:** 16 | **License:** BSD-2-Clause  
**Stack:** React (Next.js) + Spring Boot (Java 17)  
**Active milestones:** SBH 2.0.0 (UX & sharing), SBH 3.0.0 (Swagger API)

### Open Issues (3 filed September 2026)

| # | Title | Type | Milestone | Date | Assignee |
|---|-------|------|-----------|------|----------|
| #1108 | Dev2 doesn't show any similar parts | Bug — search quality | — | Sep 12, 2026 | cl117 |
| #1107 | Update Collections Page | Enhancement | SBH 2.0.0 | Sep 4, 2026 | BroD54 |
| **#1106** | **Develop New API Using Swagger** | **Enhancement — API design** | **SBH 3.0.0** | **Sep 3, 2026** | **pagarap57** |

### Why Issue #1106 Is the Most Important Open Issue in Synbio

Filed just days ago (September 3, 2026), the Swagger API issue could be the **linchpin** that fixes the entire ecosystem's interoperability story:

- **iBioSim can't upload to SynBioHub** (issues #639, #632) because the v1 API is aging and inconsistent
- A proper Swagger-documented API would enable **reliable tool-to-platform integration**
- It would unlock a **new wave of third-party clients and plugins**
- It serves as the **migration bridge** from v1 to v3

**Known challenge:** The README warns about a legacy OpenSSL vulnerability (Node.js OpenSSL 3 `digital envelope routines unsupported` error) that limits dev mode to Mac and Linux only — a real blocker for Windows developers contributing to the redesign.

### Other Active Work

User study issues under SBH 2.0.0:
- [#1060] Search Suggestions — UX research
- [#1062] Create 2 boxes when applying filters — UX design
- [#1093] Add owner modal — sharing workflow
- [#1092] Sharing needs visibility of status — sharing workflow
- [#1091] Add owner list of users — sharing workflow

**Theme:** The v3 team is doing user research on sharing and search before building the API. This is thoughtful design — but it also means the Swagger API (SBH 3.0.0) is still in early planning.

---

## 3. iBioSim — CAD Tool Cross-Platform Struggles

**Repository:** [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim)  
**Stars:** 67 | **Forks:** 24 | **License:** Apache-2.0  
**Stack:** Java + libSBML + reb2sac + GeneNet + Yosys  
**Total open issues:** 305+ (7 most recent analyzed)

### Recent Open Issues

| # | Title | Theme | Date | Comments |
|---|-------|------|------|----------|
| #640 | A Java exception has occurred | Stability | Aug 2025 | 1 |
| #639 | Can't upload SynBioHub design | Integration failure | May 2025 | 1 |
| #638 | Unable to run iBioSim 3.2.0 on Mac | Cross-platform | May 2025 | 1 |
| **#637** | **Unable to generate models (NoClassDefFoundError: Jena/Xerces)** | **Bug — Java dependency** | **Jan 2025** | **6** |
| #635 | Cannot open iBioSim on Windows 11 | Cross-platform | Jan 2025 | 4 |
| #634 | Bug importing file and when starting | Bug — data import | Sep 2024 | 6 |
| #632 | Can't connect to LCP Synbiohub | Integration failure | Apr 2024 | 2 |

### Community Discussion: Issue #637 (Most Discussed — 6 Comments)

**Reporter:** Hatem-synbio  
**Context:** Debugging Kenzo's toggle switch model, following the iBioSim tutorial on page 94 for automatic model generation.

**Hatem-synbio:**
> Shared screenshots of the error and the SBH selection screen. Offered to share the COMBINE archive on Slack.

**cjmyers (maintainer):**
> "Can you provide more detail about what you were doing when you experienced this error? Which SBH were you doing model generation with?"

**cjmyers (root cause):**
> "I'm pretty sure the issue has to do with trying to create a model using iGEM parts. iGEM parts do not have interaction information, so it is impossible to generate a model. Granted, there should be a better error than an exception. To actually test this better, should use the Cello library."

**The actual error:**
```
java.lang.NoClassDefFoundError: Could not initialize class org.apache.jena.query.ARQ
Caused by: java.lang.NoClassDefFoundError: org/apache/xerces/util/XMLChar
```

**Analysis:** This is a triple failure:
1. **Technical:** Apache Jena can't initialize because Xerces (XML parser) is missing from the classpath
2. **UX:** The error is cryptic — users see a Java stack trace instead of "These parts don't have interaction information needed for model generation"
3. **Dependency:** iGEM parts lack the interaction data that Jena needs, creating a fundamental mismatch between the platform's data and the tool's requirements

**Recent maintenance activity (2026):**
- `74ac459` — Merge PR #645: headless stdout fix (Apr 2026)
- `e2d8b7a` — Filter unread progress stdout noise in headless mode (Mar 2026)
- `17c876e` — Update .gitignore for Java SDKMAN (Mar 2026)
- `9df4464` — Add missing full local build deps (Mar 2026)

**Takeaway:** The team is actively maintaining (headless mode fixes, build dependency fixes) but the core issues — Java dependency management, OS-specific behavior, and cryptic error messages — are structural. The Swagger API (#1106) could fix the SynBioHub integration, but the desktop experience will remain challenging until someone builds a web-native or containerized alternative.

---

## 4. GENtle2 — Legacy UI Debt

**Repository:** [Synbiota/GENtle2](https://github.com/Synbiota/GENtle2)  
**Stars:** 106 | **License:** Not specified  
**Stack:** JavaScript (Node.js + Express + Gulp)

### Open Issues (Alldating to 2014, last touched Jul 2023)

| # | Title | Labels | Milestone | Date |
|---|-------|--------|-----------|------|
| #164 | Display feature details when hovering | — | Refactor — Canvas events | Jul 2014 |
| #163 | Tracking mouse events in `Artist` | Feature, Refactor | Refactor — Canvas events | Jul 2014 |
| #162 | Selection disappears via context menu | Bug | — | Jul 2014 |
| #161 | Selection disappears with hotkeys | Bug | — | Jul 2014 |
| #159 | Tracking shapes in `Artist` | Feature, Refactor | Refactor — Canvas events | Jul 2014 (6 comments) |
| #158 | Creating feature clears plasmid map | Bug, Refactor | — | Jul 2014 |
| #156 | Caret moves unexpectedly during selection | Bug, Refactor | — | Jul 2014 |
| #154 | Plasmid map title overflows for long names | Refactor, Optimization | — | Jul 2014 |
| #132 | Replace non-allowed chars on Genebank import | Backlog, Refactor | Refactor — Seq opening | Jun 2014 |
| #130 | Bug with selection using up arrow | Bug, Refactor | Refactor — Seq opening | Jun 2014 |

**Takeaway:** The maintainer (`alexandremeunier`) has created "Refactor" milestones targeting Canvas events and sequence editing, but the 10+ year gap between issue creation and the last update (Jul 2023) signals **sustained stagnation**. This is the cautionary tale of academic open-source software: the original desktop GENtle was built in academia, and when the lab moved on, the community maintenance evaporated. GENtle2's web rewrite is a step forward, but it carries the same DNA — an academic project that the community can't sustain.

---

## 5. Syn-Zeug — Modern Stack Feature Expansion

**Repository:** [Sheffield-iGEM/syn-zeug](https://github.com/Sheffield-iGEM/syn-zeug)  
**Stars:** 7 | **License:** AGPL-3.0  
**Stack:** Rust (core) + Svelte (web UI) + WASM (biobox shim)

### Open Issues (10 total — ALL feature requests, ZERO bug reports)

| # | Title | Theme | Assignee |
|---|-------|-------|----------|
| #47 | Find ORFs In Proteins | New tool — protein analysis |
| #46 | Upstream `rust-bio` changes | Dependency update |
| #42 | Miscellaneous Tools | General feature tracking |
| #39 | Add region info to input (like Benchling) | UX improvement |
| #38 | Pause a tool in the pipeline | Pipeline UX |
| #37 | Add nice looking tooltips! | UI enhancement |
| #36 | Add dragging for building up a pipeline | Pipeline UX |
| #26 | Implement New Tool: "Percent Composition" | New analysis tool |
| #17 | Implement New Tool: "Shuffle Sequence" | New analysis tool |
| #8 | Implement New Tool: "Mutate Sequence" | New analysis tool |

**Currently implemented tools:**
- Web UI: Sequence Validation, Length, Reverse, Count Elements, Reverse Complement, Case Conversion, GC Content, Find ORFs
- Rust Library: Extract Subsequences, Hamming Distance, Levenshtein Distance

**Takeaway:** This is the **healthiest project** in our survey. Zero bug reports means the core is stable. All issues are feature requests, meaning users are building on top of the tool and asking for more. The Rust+Svelte+WASM architecture is a modern alternative to the Java-based tools. The Sheffield-iGEM team provides reviewer guidance for new contributors, creating a sustainable contribution pipeline. **This is the template for the next generation of synbio software.**

---

## 6. DnaChisel — Chemistry-Aware Optimization

**Repository:** [Edinburgh-Genome-Foundry/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel)  
**Stars:** 274 | **License:** MIT

### Recent Open Issues (April–June 2026, very active)

| # | Title | Type | Date | Comments |
|---|-------|------|------|----------|
| #114 | Produce multiple different optimized results | Feature — diversity | Jun 3, 2026 | 1 |
| #113 | Low Codon Adaptation Index on optimized sequence | Bug — quality | May 5, 2026 | 1 |
| #107 | Support for Uridine Depletion (UD) optimization | Feature — chemistry | Apr 17, 2026 | **5** |
| #111 | Unexpected Mutation of `codon_usage_table` | Bug — data integrity | Apr 27, 2026 | 1 |
| #110 | Minimize CG | Feature — GC content | Apr 23, 2026 | 2 |
| #100 | How to get under-optimal sequences? | Question — fitness landscape | May 2025 | 2 |

**Takeaway:** Users want to **explore the fitness landscape**, not just find the single best sequence. The `codon_usage_table` mutation bug (#111) could silently produce incorrect results — a data integrity concern. The UD optimization request (#107, 5 comments) shows the community pushing DnaChisel toward **chemistry-aware design** — making DNA invisible to degradation pathways. This is a sophisticated user base asking increasingly advanced questions.

---

## 7. BioCRNpyler — RNA Devices & TXTL

**Repository:** [BuildACell/bioCRNpyler](https://github.com/BuildACell/bioCRNpyler)  
**Stars:** 54 | **License:** MIT

### Recent Open Issues (July–August 2026)

| # | Title | Type | Date | Comments |
|---|-------|------|------|----------|
| #333 | Use consistent naming conventions for classes | Internal consistency | Jul 30, 2026 | 3 |
| #341 | Include bioscrape in CI tests? | Test infrastructure | Aug 21, 2026 | 0 |
| #339 | Decide how to handle examples | Documentation | Aug 21, 2026 | 0 |
| #337 | Bug: ODEint fails with EnergyTXTL | Bug — simulation stability | Aug 14, 2026 | 2 |
| #338 | Allow lists of multiple substrates for Membrane Components | Feature — transport | Aug 14, 2026 | Assigned |
| #328 | Implement TMSE circuits as a "companion module" | Feature — RNA devices | Jul 9, 2026 | 1 (assigned) |

**Takeaway:** The project is actively expanding toward **RNA-based devices** (TMSE module, #328) and **cell-free expression** (EnergyTXTL, #338). The ODEint convergence bug (#337) is particularly concerning for users relying on TXTL simulations — it's a simulation stability issue that could produce misleading results.

---

## 8. poly — Release-Blocking Dependency Chain

**Repository:** [bebop/poly](https://github.com/bebop/poly)  
**Stars:** 737 | **License:** MIT  
**The most-starred open-source pure synthbio software tool on GitHub.**

### Critical Issue Chain Blocking v1.0

| # | Title | Priority | Status |
|---|-------|----------|--------|
| **#359** | **Implement Gibson Assembly** | 🔴 **High** | **Blocked by #367** |
| **#367** | **Refactor `clone` package** | 🔴 **High** | **Blocks #359** |
| #383 | Genbank parser doesn't handle colliding feature names | 🔴 High | Stale |
| #434 | Genbank parser needs heavy refactor or rewrite | Medium | 10 comments, stale |
| #448 | Remove lunny/log dependency from genbank.go | Low | Stale |
| #442 | Turn on `revive` linter in golangci config | Low | Stale |

**Takeaway:** The v1.0 release cannot ship until the clone package is refactored (#367), which is a classic case of **technical debt blocking feature delivery**. Gibson Assembly (#359) is the one feature that would make poly truly useful for modular DNA construction, but it's gated by a prerequisite refactor. The stale issues (#383, #434) about Genbank parser bugs suggest quality concerns that also need attention.

---

## 9. Coral — The Maintenance Benchmark

**Repository:** [klavinslab/coral](https://github.com/klavinslab/coral)  
**Stars:** 32 | **License:** MIT

**Open Issues:** Only **1** ([#37](https://github.com/klavinslab/coral/issues/37) — Ubuntu 22.04 Python 3 compatibility). Actively maintained, recent updates (June 2026).

**Takeaway:** Coral is the **health benchmark** of the ecosystem. A well-maintained, open-source Python library with only 1 open issue. It demonstrates that sustainable open-source maintenance is possible in academia — the key is having a dedicated lab with ongoing student turnover keeping the project alive.

---

## Cross-Cutting Themes

### Theme 1: The SynBioHub Swagger API Is the Linchpin

The single most impactful action the community could take is completing the Swagger API (#1106). This would:
- Fix iBioSim's broken upload (affecting every researcher who uses iBioSim)
- Enable third-party clients (imagine a GENtle2 plugin for SynBioHub v3)
- Serve as the migration bridge from v1 to v3
- Unlock reliable data exchange across the entire tool ecosystem

### Theme 2: Data Integrity Is the New Urgency

Across SynBioHub v1, the issues are no longer about "nice to have" features — they're about whether the data can be trusted:
- SubCollections not reporting members (#1756)
- Recursive downloads breaking (#1755)
- OMEX exports missing files (#1753)
- Legacy data cluttering the database (#1754)

When the iGEM Registry and *B. subtilis* data are at stake, these aren't cosmetic bugs.

### Theme 3: The Desktop Tool Bottleneck

iBioSim (305+ issues) and GENtle2 (75+ issues) both struggle with the same fundamental problem: desktop applications are hard to maintain. Java dependency hell, OS-specific behavior, and aging UI codebases make them brittle. The future is web-native (GENtle2's rewrite, SynBioHub v3's React stack) or containerized (Coral's clean Python, Syn-Zeug's Rust+WASM).

### Theme 4: The Missing Open-Source ML Stack

ART (private code) and 20n/act (internally maintained) demonstrate that ML-augmented biological design is happening — but it's closed. The open-source community needs a tool that combines:
- DnaChisel's sequence optimization (open, Python)
- ART's ML-driven strain recommendations (closed, Jupyter)
- Syn-Zeug's modern architecture (open, Rust)

### Theme 5: Standards Are Maturing, but Pipelines Aren't

SBOL and SBML are well-defined standards. SBOL Explorer exists. OMEX bundles are specified. But the *pipelines* that move data between tools are broken:
- OMEX exports miss SBML files (SynBioHub #1753)
- Incremental sync fails (SynBioHub #1746)
- iBioSim can't upload to SynBioHub (iBioSim #639)

The standards exist. The plumbing doesn't.

### Theme 6: Ancient UI Code Is a National Disaster

GENtle2's issues date to 2014. That's 12 years of unfixed UX bugs in a tool used by synthetic biologists worldwide. The maintainer is trying a refactor, but the community can't sustain it. The lesson: **if you build a scientific tool, you must either maintain it or formally hand it off.**

---

## Recommended Episode Topics Based on These Findings

| Episode | Title | Core Question |
|---------|-------|----------------|
| EP001 | The Swagger That Could Fix Everything | Can a single API issue unlock the entire synbio ecosystem? |
| EP002 | The OMEX Export Mystery | Why can't we reliably download synthetic biology designs? |
| EP003 | Java, Mac, Windows: Why Can't Our Tools Just Run? | The cross-platform bottleneck in desktop synbio CAD |
| EP004 | The 12-Year Bug | What happens when academic open-source software stops being maintained? |
| EP005 | Rust for Biology | Is Syn-Zeug the template for the next generation of bioinformatics tools? |
| EP006 | From Hand Engineering to Computational Design | How ART and 20n/act are changing the game |
| EP007 | The Migration | SynBioHub v1 to v3 — what does it take to move an ecosystem? |
| EP008 | Chemistry-Aware DNA Design | When DnaChisel users want to explore the fitness landscape |
| EP009 | The Missing Open-Source ML Stack | Why the most exciting synbio design tools are closed-source |
| EP010 | Coral's secret to sustainable maintenance | How one lab keeps a 32-star library shipshape |

---

*Research compiled from live GitHub API data on September 18, 2026. All issue references, comment threads, and commit histories are verified against current repository state.*