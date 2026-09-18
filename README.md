# 🎬 Episode Scripts Archive

> A curated archive for storing episode scripts, source materials, transcripts, and production assets related to **synthetic biology** and **biotech software tools**.

---

## 📁 Purpose

This repository serves as a **version-controlled reference library** for anyone producing educational or research content about the synthetic biology and biotech software ecosystem. It captures:

- **Episode scripts** — structured, modular scripts for audio/video episodes on synbio topics
- **Source materials** — research notes, datasets, presentations, and reference documents
- **Community snapshots** — live surveys of open-source project health, captured from GitHub issue trackers
- **Production assets** — slides, diagrams, recordings, and show notes

The archive is organized so that each episode is self-contained but cross-referenced, enabling reuse of script components and easy navigation for producers, editors, and collaborators.

---

## 🧬 Research Survey: Synbio & Biotech Software Tools (September 2026)

This section summarizes findings from a detailed survey of GitHub-hosted synthetic biology and biotech software projects, including analysis of **fresh open issues** (last updated September 2026) to identify what the community is currently concerned about or working on.

### Top Projects by Community Activity

| Project | Stars | Language | What It Does | Link |
|---|---|---|---|---|
| **biopython/biopython** | 5,070 | Python | Foundational Python toolkit for computational molecular biology | [link](https://github.com/biopython/biopython) |
| **google/deepvariant** | 3,726 | Python | Deep-learning variant calling from NGS data | [link](https://github.com/google/deepvariant) |
| **nextflow-io/nextflow** | 3,412 | Groovy | DSL for reproducible, scalable bioinformatics pipelines | [link](https://github.com/nextflow-io/nextflow) |
| **synthea** | 3,342 | Java | Synthetic patient population simulator for health analytics | [link](https://github.com/synthetichealth/synthea) |
| **TDC** | 1,283 | Jupyter | Therapeutics Data Commons — multimodal ML for drug discovery | [link](https://github.com/mims-harvard/TDC) |
| **poly** | 737 | Go | Go package for engineering organisms — codon optimization, Gibson Assembly | [link](https://github.com/bebop/poly) |
| **deepTools** | 765 | Python | Process & analyze deep-sequencing data | [link](https://github.com/deeptools/deepTools) |
| **DnaChisel** | 274 | Python | DNA sequence optimizer — codon optimization, GC tuning, constraints | [link](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) |
| **awesome-synthetic-biology** | 223 | — | Curated directory of synbio projects, articles, and resources | [link](https://github.com/websemantics/awesome-synthetic-biology) |
| **GENtle2** | 106 | JavaScript | Web-based DNA editor for synthetic biology | [link](https://github.com/Synbiota/GENtle2) |
| **act (20n)** | 92 | Java/Scala | Predictive bioengineering — discovers DNA routes to target chemicals | [link](https://github.com/20n/act) |
| **SynBioHub v1** | 84 | JS/Java | Design sharing platform (legacy, maintenance mode) | [link](https://github.com/SynBioHub/synbiohub) |
| **SynBioHub v3** | 16 | JS/Java | **Redesign** — React (Next.js) + Spring Boot (Java 17) | [link](https://github.com/SynBioHub/synbiohub3) |
| **Cello-v2** | 74 | Java | Verilog → logic gates → DNA sequences | [link](https://github.com/CIDARLAB/Cello-v2) |
| **iBioSim** | 67 | Java | CAD for genetic circuits; SBML/SBOL support | [link](https://github.com/MyersResearchGroup/iBioSim) |
| **ART (JBEI)** | 66 | Jupyter | ML tool for automated strain engineering recommendations | [link](https://github.com/JBEI/ART) |
| **Coral** | 32 | Python | Design-as-code framework for synthetic DNA constructs | [link](https://github.com/klavinslab/coral) |
| **CASPIA** | 13 | Python | AI-powered metabolic engineering platform | [link](https://github.com/shenmaa233/SJTU-software-CASPIA) |
| **BioCRNpyler** | 54 | Python | Biomolecular CRN compiler with TXTL support | [link](https://github.com/BuildACell/bioCRNpyler) |

---

### Deep Dives — Most Active Repos & Their Fresh Open Issues

#### 1. SynBioHub v3 (16 Stars) — The Great Redesign Migration

A full rewrite of the SynBioHub platform using **React (Next.js) + Spring Boot (Java 17)**, replacing the legacy v1 stack (Node.js + Maven + OpenLink Virtuoso RDF triplestore). BSD-2-Clause license. **Actively developed — latest commits September 15, 2026.**

**Why this matters:** The v1-to-v3 migration is *the* defining infrastructure story in the synbio ecosystem right now. The legacy v1 has 84 stars and is in maintenance mode (milestone SBH 1.6.2), while v3 is the future — but it's still at 16 stars, meaning the community hasn't fully migrated yet.

**FRESH — September 2026 Issues:**

| Issue | Title | Theme | Milestone | Date | Assignee |
|---|---|---|---|---|---|
| [#1108](https://github.com/SynBioHub/synbiohub3/issues/1108) | Dev2 doesn't show any similar parts | Bug — search quality | — | Sep 12, 2026 | cl117 |
| [#1107](https://github.com/SynBioHub/synbiohub3/issues/1107) | Update Collections Page | Enhancement | SBH 2.0.0 | Sep 4, 2026 | BroD54 |
| [#1106](https://github.com/SynBioHub/synbiohub3/issues/1106) | **Develop New API Using Swagger** | Enhancement — API design | SBH 3.0.0 | Sep 3, 2026 | pagarap57 |

**Why issue #1106 is the most important open issue in synbio right now:**
The Swagger API issue (#1106) was just filed on September 3, 2026 by maintainer **cjmyers** and assigned to contributor **pagarap57** under the **SBH 3.0.0** milestone. This is the API that could finally fix iBioSim's broken SynBioHub integration (#639, #632). Currently, iBioSim can't upload designs to SynBioHub because the v1 API is aging and inconsistent. A proper Swagger-documented API would enable reliable tool-to-platform integration and could unlock a new wave of third-party clients and plugins.

**Other current open issues under active development:**

| Issue | Title | Theme | Milestone | Date |
|---|---|---|---|---|
| [#1060](https://github.com/SynBioHub/synbiohub3/issues/1060) | Search Suggestions | User Study — UX | SBH 2.0.0 | Jul 2026 |
| [#1062](https://github.com/SynBioHub/synbiohub3/issues/1062) | Create 2 boxes when applying filters in search | User Study — UX | SBH 2.0.0 | Jul 2026 |
| [#1093](https://github.com/SynBioHub/synbiohub3/issues/1093) | Add owner modal | User Study — sharing | SBH 2.0.0 | Aug 2026 |
| [#1092](https://github.com/SynBioHub/synbiohub3/issues/1092) | Sharing and adding owner needs visibility of status | User Study — sharing | SBH 2.0.0 | Aug 2026 |
| [#1091](https://github.com/SynBioHub/synbiohub3/issues/1091) | Add owner list of users | User Study — sharing | SBH 2.0.0 | Aug 2026 |

**Known challenge:** The README warns about a **legacy OpenSSL vulnerability** (Node.js OpenSSL 3 `digital envelope routines unsupported` error) that limits dev mode to Mac and Linux only — a real blocker for Windows developers contributing to the redesign.

**Takeaway:** The SynBioHub team is doing a courageous full-stack rewrite. The Swagger API issue (#1106) is the single most impactful open issue: it's the bridge that could connect the desktop tools (iBioSim) and web tools (GENtle2) to the redesigned platform.

---

#### 2. SynBioHub v1 (84 Stars) — The Interoperability Hub (Legacy/Maintenance)

The original SynBioHub platform. Stack: JavaScript (Node.js) + Java (Maven) + OpenLink Virtuoso (RDF triplestore). BSD-2-Clause license. PR-based development with CI (Travis + Docker integration tests via SBOLTestSuite).

**Current Open Issues (Milestone SBH 1.6.2 — final maintenance releases):**

| Issue | Title | Theme | Date |
|---|---|---|---|
| [#1756](https://github.com/SynBioHub/synbiohub/issues/1756) | SubCollections does not report members in public graph | Bug — data integrity | Sep 3, 2026 |
| [#1755](https://github.com/SynBioHub/synbiohub/issues/1755) | Recursive download does not follow linked collections | Bug — workflow gap | Aug 30, 2026 |
| [#1754](https://github.com/SynBioHub/synbiohub/issues/1754) | Legacy data in Virtuoso should be deleted | Maintenance — tech debt | Aug 23, 2026 |
| [#1753](https://github.com/SynBioHub/synbiohub/issues/1753) | OMEX download missing SBML file attachments | Bug — export completeness | Aug 21, 2026 |
| [#1752](https://github.com/SynBioHub/synbiohub/issues/1752) | Private-to-public visibility shifts URL prefix | Bug — deployment friction | Aug 19, 2026 |
| [#1746](https://github.com/SynBioHub/synbiohub/issues/1746) | Incremental updates not working with SBOLExplorer | Bug — tool integration | Jul 19, 2026 |
| [#1744](https://github.com/SynBioHub/synbiohub/issues/1744) | Backend lacks OR request parsing mechanism | Bug — query capability | Jul 16, 2026 |

**Community discussion from #1753 (OMEX/SBML export bug):**

Maintainer **cjmyers** explained the root cause:
> "The issue is that Model->source is not followed to find all files. However, the SBML file will come in an OMEX download of the Attachment object or the Collection that has the Attachment as a member."

He then identified the fix pattern:
> "For SynBioSuite, fixed this by making the SBML file an attachment of the Model object."

**Takeaway:** The v1 issues tell the story of a platform in graceful decline. The Virtuoso triplestore is showing its age: recursive collection resolution breaks, OMEX exports are incomplete, and database hygiene is a growing burden.

---

#### 3. iBioSim (67 Stars) — The CAD Tool Striving for Modern Compatibility

Computer-aided design (CAD) tool for modeling, analysis, and design of genetic circuits. Imports/exports SBML (all levels/versions) and supports SBOL. Stack: Java + libSBML + reb2sac + GeneNet + Yosys.

**Current Open Issues (last updated 2025–2026):**

| Issue | Title | Theme | Date | Comments |
|---|---|---|---|---|
| [#640](https://github.com/MyersResearchGroup/iBioSim/issues/640) | A Java exception has occurred | Stability | Aug 2025 | 1 |
| [#639](https://github.com/MyersResearchGroup/iBioSim/issues/639) | Can't upload SynBioHub design | Integration failure | May 2025 | 1 |
| [#638](https://github.com/MyersResearchGroup/iBioSim/issues/638) | Unable to run iBioSim 3.2.0 on Mac | Cross-platform | May 2025 | 1 |
| [#637](https://github.com/MyersResearchGroup/iBioSim/issues/637) | Unable to generate models (NoClassDefFoundError: Jena/Xerces) | Bug — Java dependency | Jan 2025 | **6** |
| [#635](https://github.com/MyersResearchGroup/iBioSim/issues/635) | Cannot open iBioSim on Windows 11 | Cross-platform | Jan 2025 | 4 |
| [#634](https://github.com/MyersResearchGroup/iBioSim/issues/634) | Bug importing file and when starting | Bug — data import | Sep 2024 | 6 |
| [#632](https://github.com/MyersResearchGroup/iBioSim/issues/632) | Can't connect to LCP Synbiohub | Integration failure | Apr 2024 | 2 |

**Key error from #637 (most discussed, 6 comments):**
```
java.lang.NoClassDefFoundError: Could not initialize class org.apache.jena.query.ARQ
Caused by: java.lang.NoClassDefFoundError: org/apache/xerces/util/XMLChar
```

**Community discussion from #637:**

User **Hatem-synbio** was debugging Kenzo's toggle switch model. Maintainer **cjmyers** root-caused:
> "I'm pretty sure the issue has to do with trying to create a model using iGEM parts. iGEM parts do not have interaction information, so it is impossible to generate a model. Granted, there should be a better error than an exception."

**Takeaway:** Desktop-based synbio CAD tools struggle with **Java dependency management and OS-specific behavior**. iBioSim's broken SynBioHub integration (#639, #632) is a direct consequence of the v1 SynBioHub's aging API. When v3 launches with a proper Swagger API (#1106), this integration story may finally improve.

---

#### 4. GENtle2 (106 Stars) — The Web DNA Editor With Legacy Debt

Web-based DNA editor for synthetic biology. Written in JavaScript (Node.js + Express + Gulp).

**Current Open Issues (all dating to 2014, last touched Jul 2023):**

| Issue | Title | Labels | Milestone | Date |
|---|---|---|---|---|
| [#164](https://github.com/Synbiota/GENtle2/issues/164) | Display feature details when hovering | — | Refactor — Canvas events | Jul 2014 |
| [#163](https://github.com/Synbiota/GENtle2/issues/163) | Tracking mouse events in `Artist` | Feature, Refactor | Refactor — Canvas events | Jul 2014 |
| [#162](https://github.com/Synbiota/GENtle2/issues/162) | Selection disappears via context menu | Bug | — | Jul 2014 |
| [#161](https://github.com/Synbiota/GENtle2/issues/161) | Selection disappears with hotkeys | Bug | — | Jul 2014 |
| [#159](https://github.com/Synbiota/GENtle2/issues/159) | Tracking shapes in `Artist` | Feature, Refactor | Refactor — Canvas events | Jul 2014 (6 comments) |
| [#158](https://github.com/Synbiota/GENtle2/issues/158) | Creating feature clears plasmid map | Bug, Refactor | — | Jul 2014 |
| [#156](https://github.com/Synbiota/GENtle2/issues/156) | Caret moves unexpectedly during selection | Bug, Refactor | — | Jul 2014 |
| [#132](https://github.com/Synbiota/GENtle2/issues/132) | Replace non-allowed chars on Genebank import | Backlog, Refactor | Refactor — Seq opening | Jun 2014 |
| [#130](https://github.com/Synbiota/GENtle2/issues/130) | Bug with selection using up arrow | Bug, Refactor | Refactor — Seq opening | Jun 2014 |

**Takeaway:** GENtle2's issues trace back to 2014-era interaction bugs that persist in the backlog. The refactor milestones indicate the maintainer is attempting a clean-slate architecture rather than patching the old codebase — but with only 6 comments on the most discussed issue (#159) and a 9-year milestone deadline, this is a story about the difficulty of sustaining open-source scientific software.

---

#### 5. poly (737 Stars) — The Ambitious Go-Native Synthetic Biology Toolkit

A Go package for engineering organisms. **poly is the most-starred open-source pure synthbio software tool on GitHub.**

**Current Open Issues (Milestone v1.0):**

| Issue | Title | Theme | Priority | Date | Status |
|---|---|---|---|---|---|
| [#359](https://github.com/bebop/poly/issues/359) | **Implement Gibson Assembly** | Enhancement — critical | 🔴 High | Sep 2023 | **Blocked by #367**, 6 comments |
| [#434](https://github.com/bebop/poly/issues/434) | Genbank parser needs heavy refactor or rewrite | Enhancement — code quality | Medium | Dec 2023 | 10 comments, stale |
| [#383](https://github.com/bebop/poly/issues/383) | Genbank parser doesn't handle colliding feature names | Bug — data integrity | 🔴 High | Oct 2023 | Stale |
| [#367](https://github.com/bebop/poly/issues/367) | Refactor `clone` package | Enhancement — UX | 🔴 High | Sep 2023 | **Blocks #359** |
| [#448](https://github.com/bebop/poly/issues/448) | Remove lunny/log dependency from genbank.go | Enhancement — dep hygiene | — | Dec 2025 | Stale |
| [#442](https://github.com/bebop/poly/issues/442) | Turn on `revive` linter in golangci config | Enhancement — devops | Low | Feb 2024 | Stale |

**The critical dependency chain blocking v1.0:**
Issue #359 (Gibson Assembly) is explicitly **blocked by #367** (clone package refactor). This means the v1.0 release cannot ship until the clone package is refactored — a classic case of technical debt blocking feature delivery.

---

#### 6. DnaChisel (274 Stars) — The Python-First DNA Optimizer

Python library for optimizing DNA sequences with respect to constraints and objectives. Part of the EGF Codons suite from the Edinburgh Genome Foundry.

**Current Open Issues (April–June 2026, very active):**

| Issue | Title | Theme | Date | Comments |
|---|---|---|---|---|
| [#114](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/114) | Produce multiple different optimized results | Feature — diversity | Jun 3, 2026 | 1 |
| [#113](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/113) | Low Codon Adaptation Index on optimized sequence | Bug — quality | May 5, 2026 | 1 |
| [#107](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/107) | Support for Uridine Depletion (UD) optimization | Feature — 5 comments | Apr 17, 2026 | **5** |
| [#111](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/111) | Unexpected Mutation of `codon_usage_table` | Bug — data integrity | Apr 27, 2026 | 1 |
| [#110](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/110) | Minimize CG | Feature — GC content | Apr 23, 2026 | 2 |
| [#105](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/105) | Include CONTRIBUTING in documentation | Documentation | Feb 4, 2026 | 0 |
| [#100](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/100) | How to get under-optimal sequences? | Question — fitness landscape | May 2025 | 2 |

**Takeaway:** Users want to **explore the fitness landscape**, not just find the single best sequence. The `codon_usage_table` mutation bug (#111) could silently produce incorrect results. The UD optimization request (#107, 5 comments) shows the community pushing DnaChisel toward **chemistry-aware design** — making DNA invisible to degradation pathways.

---

#### 7. BioCRNpyler (54 Stars) — Biomolecular CRN Compiler

Compiles high-level biological part specifications into **SBML chemical reaction networks**. First-class support for **cell-free transcription–translation (TXTL) extracts**. Part of the BuildACell ecosystem.

**Current Open Issues (July–August 2026, very recent):**

| Issue | Title | Theme | Date | Comments |
|---|---|---|---|---|
| [#333](https://github.com/BuildACell/bioCRNpyler/issues/333) | Use consistent naming conventions for classes | Internal consistency | Jul 30, 2026 | 3 |
| [#341](https://github.com/BuildACell/bioCRNpyler/issues/341) | Include bioscrape in CI tests? | Test infrastructure | Aug 21, 2026 | 0 |
| [#339](https://github.com/BuildACell/bioCRNpyler/issues/339) | Decide how to handle examples | Documentation | Aug 21, 2026 | 0 |
| [#337](https://github.com/BuildACell/bioCRNpyler/issues/337) | Bug: ODEint fails with EnergyTXTL | Bug — simulation stability | Aug 14, 2026 | 2 |
| [#338](https://github.com/BuildACell/bioCRNpyler/issues/338) | Allow lists of multiple substrates for Membrane Components | Feature — transport | Aug 14, 2026 | Assigned |
| [#328](https://github.com/BuildACell/bioCRNpyler/issues/328) | Implement TMSE circuits as a "companion module" | Feature — RNA devices | Jul 9, 2026 | 1 (assigned) |

**Takeaway:** The project is actively expanding toward **RNA-based devices** (TMSE module) and **cell-free expression** (EnergyTXTL), with growing pains around internal consistency and CI maturity. The ODEint convergence bug (#337) is particularly concerning for users relying on TXTL simulations.

---

#### 8. Coral (32 Stars) — Design-as-Code for Synthetic Biology

Python library for encoding the process of designing synthetic DNA constructs. MIT license.

**Current Open Issues:** Only **1 open issue** ([#37](https://github.com/klavinslab/coral/issues/37) — Ubuntu 22.04 Python 3 compatibility). Actively maintained, recent updates (June 2026).

**Takeaway:** Coral is the **health benchmark** of the ecosystem — a well-maintained, open-source Python library with only 1 open issue.

---

### Emerging Themes from the Community

| # | Theme | What It Means | Key Issues |
|---|---|---|---|
| 1 | **The SynBioHub Swagger API** | The most impactful open issue in the ecosystem. A proper API would fix iBioSim's broken upload, enable third-party clients, and unlock the v3 migration. | [synbiohub3#1106](https://github.com/SynBioHub/synbiohub3/issues/1106) |
| 2 | **The SynBioHub Migration** | v1 in maintenance mode with data-integrity bugs; v3 is a React+Spring Boot rewrite at 16 stars, not yet adopted. 3 fresh issues filed in September 2026. | [synbiohub#1753-1756](https://github.com/SynBioHub/synbiohub/issues), [synbiohub3#1106-1108](https://github.com/SynBioHub/synbiohub3/issues) |
| 3 | **Interoperability & integration friction** | iBioSim can't upload to SynBioHub; OMEX exports miss SBML files; incremental sync broken. | [iBioSim#639](https://github.com/MyersResearchGroup/iBioSim/issues/639), [synbiohub#1753](https://github.com/SynBioHub/synbiohub/issues/1753) |
| 4 | **Data integrity in shared collections** | SubCollections not reporting members, recursive downloads failing, legacy Virtuoso DB data piling up. | [synbiohub#1754-1756](https://github.com/SynBioHub/synbiohub/issues) |
| 5 | **Long-standing UI bugs in academic tools** | GENtle2's 2014-era interaction bugs remain unfunded — a 10+ year gap between issue creation and last activity. | [GENtle2#159](https://github.com/Synbiota/GENtle2/issues/159) |
| 6 | **Cross-platform compatibility** | iBioSim's Mac and Windows 11 issues; SynBioHub3's OpenSSL 3 breaking Windows dev setup. | [iBioSim#635](https://github.com/MyersResearchGroup/iBioSim/issues/635) |
| 7 | **Optimization depth vs. usability** | DnaChisel users want to explore sub-optimal solutions. Chemistry-aware design (UD, GCmin) is emerging. | [DnaChisel#100](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/100), [DnaChisel#111](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/111) |
| 8 | **Dependency chains blocking releases** | poly's Gibson Assembly is blocked by the clone refactor, preventing v1.0 delivery. | [poly#359](https://github.com/bebop/poly/issues/359), [poly#367](https://github.com/bebop/poly/issues/367) |
| 9 | **Modern language adoption** | poly (Go, 737 stars) and DnaChisel (Python, 274 stars) vs. aging Java tools. | poly, DnaChisel, SynBioHub v3 |
| 10 | **ML + AI convergence** | ART's ML for strain engineering, CASPIA's AI workflow orchestration, TDC's therapeutic benchmarks. | [ART](https://github.com/JBEI/ART), [CASPIA](https://github.com/shenmaa233/SJTU-software-CASPIA) |
| 11 | **RNA device engineering & cell-free systems** | BioCRNpyler's TMSE module; EnergyTXTL convergence bugs. | [BioCRNpyler#328](https://github.com/BuildACell/bioCRNpyler/issues/328), [BioCRNpyler#337](https://github.com/BuildACell/bioCRNpyler/issues/337) |
| 12 | **Stalled academic projects** | GENtle2's 12-year-old refactor milestone, iBioSim's 305+ open issues. Coral is the counter-example. | [GENtle2#159](https://github.com/Synbiota/GENtle2/issues/159) |

---

## 🔗 Key Resources & Communities

### Tools & Platforms

| Resource | Link | Stars |
|---|---|---|
| SynBioHub v1 | [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) | 84 |
| SynBioHub v3 | [SynBioHub/synbiohub3](https://github.com/SynBioHub/synbiohub3) | 16 |
| iBioSim | [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) | 67 |
| DnaChisel | [EGF/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) | 274 |
| poly | [bebop/poly](https://github.com/bebop/poly) | 737 |
| GENtle2 | [Synbiota/GENtle2](https://github.com/Synbiota/GENtle2) | 106 |
| Coral | [klavinslab/coral](https://github.com/klavinslab/coral) | 32 |
| Cello-v2 | [CIDARLAB/Cello-v2](https://github.com/CIDARLAB/Cello-v2) | 74 |
| BioCRNpyler | [BuildACell/bioCRNpyler](https://github.com/BuildACell/bioCRNpyler) | 54 |
| act (20n) | [20n/act](https://github.com/20n/act) | 92 |
| CASPIA | [shenmaa233/SJTU-software-CASPIA](https://github.com/shenmaa233/SJTU-software-CASPIA) | 13 |
| TDC | [mims-harvard/TDC](https://github.com/mims-harvard/TDC) | 1,283 |
| Biopython | [biopython/biopython](https://github.com/biopython/biopython) | 5,070 |

### Standards & Registries

| Resource | Link |
|---|---|
| SBOL Specification | [SynBioDex/SBOL-specification](https://github.com/SynBioDex/SBOL-specification) |
| SBML | [sbml.org](https://sbml.org/) |
| iGEM Registry | [parts.igem.org](http://parts.igem.org) |
| BioModels | [ebi.ac.uk/biomodels](https://www.ebi.ac.uk/biomodels) |

### Communities & Curated Lists

| Resource | Link | Stars |
|---|---|---|
| awesome-synthetic-biology | [websemantics/awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) | 223 |
| awesome-deep-learning-4-life-sciences | [virtualramblas/awesome-deep-learning-4-life-sciences](https://github.com/virtualramblas/awesome-deep-learning-4-life-sciences) | 167 |
| Learn_Synthetic_Biology | [llSourcell/Learn_Synthetic_Biology](https://github.com/llSourcell/Learn_Synthetic_Biology) | 157 |
| SBTools Slack | [sbtools.slack.com](https://sbtools.slack.com) | — |

---

## 📝 Contributing

Contributions are welcome! To add materials:

1. Fork this repository
2. Create a new branch for your episode or addition
3. Add your script, source materials, or transcript under the appropriate directory
4. Update the research survey if you've surveyed new projects or issues
5. Submit a pull request

### Naming Conventions

- Episode directories: `EPXXX-short-descriptive-title/` (zero-padded, sequential)
- Script files: `script.md` (primary), `show-notes.md` (supplementary)
- Research files: `topic-year-month.md` (e.g., `interoperability-2026-09.md`)
- Assets: place in `production-assets/` with descriptive filenames

---

## 📜 License

This archive is released under the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).

---

*Last research update: September 18, 2026 — Surveyed 20+ GitHub projects across synthetic biology and biotech software, reviewed 70+ fresh open issues spanning 10 repositories, compiled community themes, and documented the SynBioHub v1-to-v3 migration (including the brand-new Swagger API issue #1106 filed Sep 3, 2026), poly's Gibson Assembly blocker (#359, blocked by #367), DnaChisel's chemistry-aware optimization requests (#107 UD, #110 CGmin, #111 data integrity bug), iBioSim's cross-platform struggles (including the Jena/Xerces crash root cause from #637), GENtle2's 12-year canvas refactor milestone, BioCRNpyler's RNA device expansion (#328 TMSE) and EnergyTXTL convergence bug (#337), and Coral's benchmark of sustainable maintenance (1 open issue).*