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

## 🧬 Research Survey: Synbio & Biotech Software Tools

This section summarizes findings from a detailed survey of GitHub-hosted synthetic biology and biotech software projects, including analysis of active open issues to identify what the community is currently concerned about or working on.

### 🏆 Top Projects by Community Activity

| Project | ⭐ Stars | Language | What It Does | Link |
|---|---|---|---|---|
| **biopython/biopython** | 5,070 | Python | Foundational Python toolkit for computational molecular biology | [biopython/biopython](https://github.com/biopython/biopython) |
| **google/deepvariant** | 3,726 | Python | Deep-learning variant calling from NGS data | [google/deepvariant](https://github.com/google/deepvariant) |
| **nextflow-io/nextflow** | 3,412 | Groovy | DSL for reproducible, scalable bioinformatics pipelines | [nextflow-io/nextflow](https://github.com/nextflow-io/nextflow) |
| **synthea** | 3,342 | Java | Synthetic patient population simulator for health analytics & EHR modeling | [synthetichealth/synthea](https://github.com/synthetichealth/synthea) |
| **TDC** | 1,283 | Jupyter | Therapeutics Data Commons — multimodal ML foundation for drug discovery | [mims-harvard/TDC](https://github.com/mims-harvard/TDC) |
| **DnaFeaturesViewer** | 690 | Python | Plot DNA sequence features from GenBank/GFF files | [EGF/DnaFeaturesViewer](https://github.com/Edinburgh-Genome-Foundry/DnaFeaturesViewer) |
| **poly** | 737 | Go | Go package for engineering organisms — codon optimization, primer design, synthesis fragments | [bebop/poly](https://github.com/bebop/poly) |
| **deepTools** | 765 | Python | Process & analyze deep-sequencing data (normalization, coverage, visualization) | [deeptools/deepTools](https://github.com/deeptools/deepTools) |
| **awesome-synthetic-biology** | 223 | — | Curated directory of synbio projects, articles, and resources | [websemantics/awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) |
| **DnaChisel** | 274 | Python | Versatile DNA sequence optimizer — codon optimization, GC tuning, constraint satisfaction | [EGF/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) |
| **GENtle2** | 106 | JavaScript | Web-based DNA editor for synthetic biology | [Synbiota/GENtle2](https://github.com/Synbiota/GENtle2) |
| **act (20n)** | 92 | Java/Scala | Predictive bioengineering — discovers DNA routes to make target chemicals | [20n/act](https://github.com/20n/act) |
| **SynBioHub v1** | 84 | JavaScript/Java | Web platform for browsing, uploading & sharing synthetic biology designs (legacy) | [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) |
| **SynBioHub v3** | 16 | JavaScript/Java | **Redesign** of SynBioHub using React (Next.js) + Spring Boot (Java 17) | [SynBioHub/synbiohub3](https://github.com/SynBioHub/synbiohub3) |
| **Cello-v2** | 74 | Java | Genetic circuit design automation — Verilog → logic gates → DNA sequences | [CIDARLAB/Cello-v2](https://github.com/CIDARLAB/Cello-v2) |
| **iBioSim** | 67 | Java | CAD for genetic circuits; SBML/SBOL support | [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) |
| **ART (JBEI)** | 66 | Jupyter Notebook | ML tool for automated strain engineering recommendations | [JBEI/ART](https://github.com/JBEI/ART) |
| **Coral** | 32 | Python | Library & framework for specifying synthetic biology design processes | [klavinslab/coral](https://github.com/klavinslab/coral) |
| **CASPIA** | 13 | Python | AI-powered platform for automatable, knowledge-retrieval-driven metabolic engineering | [shenmaa233/SJTU-software-CASPIA](https://github.com/shenmaa233/SJTU-software-CASPIA) |
| **BioCRNpyler** | 54 | Python | Modular compiler for biomolecular chemical reaction networks (SBML output) | [BuildACell/bioCRNpyler](https://github.com/BuildACell/bioCRNpyler) |

---

### 🔬 Deep Dives — Most Active Repos & Their Open Issues

#### 1. SynBioHub v3 (16 ⭐) — The Great Redesign Migration

**Scope:** A full rewrite of the SynBioHub platform using **React (Next.js) + Spring Boot (Java 17)**, replacing the legacy v1 stack (Node.js + Maven + OpenLink Virtuoso RDF triplestore). BSD-2-Clause license. Actively developed — latest commits September 15, 2026.

**Why this matters:** The v1→v3 migration is *the* defining infrastructure story in the synbio ecosystem right now. The legacy v1 has 84 stars and is in maintenance mode (milestone SBH 1.6.2), while v3 is the future — but it's still at 16 stars, meaning the community hasn't fully migrated yet.

**🌟 FRESH — September 2026 Issues (just filed!):**

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

**Recent commits (Sep 15, 2026):** Implemented `removeCollection` for the v3 backend, added tests for add/edit/remove field operations, aligned v3 response format with v1.

**Known challenge:** The README explicitly warns about a **legacy OpenSSL vulnerability** (Node.js OpenSSL 3 `digital envelope routines unsupported` error) that limits dev mode to Mac and Linux only — a real blocker for Windows developers contributing to the redesign.

**Takeaway:** The SynBioHub team is doing a courageous full-stack rewrite. They're shifting from a triplestore-based architecture to a modern React + Spring Boot stack, but the community hasn't caught up yet (16 vs. 84 stars). The migration story — from Virtuoso to relational DB, from server-rendered pages to React SPA, from opaque APIs to Swagger-documented ones — is a rich narrative about the cost and necessity of modernizing scientific infrastructure. The Swagger API issue (#1106) is the single most impactful open issue: it's the bridge that could connect the desktop tools (iBioSim) and web tools (GENtle2) to the redesigned platform.

---

#### 2. SynBioHub v1 (84 ⭐) — The Interoperability Hub (Legacy/Maintenance)

**Scope:** The original SynBioHub platform. Web application enabling users and software to browse, upload, and share synthetic biology designs. Hosts the iGEM Registry of Standard Biological Parts and enriched *B. subtilis* and *E. coli* data. Stack: JavaScript (Node.js) + Java (Maven) + OpenLink Virtuoso (RDF triplestore). BSD-2-Clause license. PR-based development with CI (Travis + Docker integration tests via SBOLTestSuite); automatic Docker Hub publishing via GitHub Actions.

**Current Open Issues (Milestone SBH 1.6.2 — final maintenance releases):**

| Issue | Title | Theme | Date |
|---|---|---|---|
| [#1756](https://github.com/SynBioHub/synbiohub/issues/1756) | SubCollections does not report members in public graph | Bug — data integrity | Sep 2026 |
| [#1755](https://github.com/SynBioHub/synbiohub/issues/1755) | Recursive download does not follow linked collections | Bug — workflow gap | Aug 2026 |
| [#1754](https://github.com/SynBioHub/synbiohub/issues/1754) | Legacy data in Virtuoso should be deleted | Maintenance — tech debt | Aug 2026 |
| [#1753](https://github.com/SynBioHub/synbiohub/issues/1753) | OMEX download missing SBML file attachments | Bug — export completeness | Aug 2026 |
| [#1752](https://github.com/SynBioHub/synbiohub/issues/1752) | Private→public visibility shifts URL prefix | Bug — deployment friction | Aug 2026 |
| [#1746](https://github.com/SynBioHub/synbiohub/issues/1746) | Incremental updates not working with SBOLExplorer | Bug — tool integration | Jul 2026 |
| [#1744](https://github.com/SynBioHub/synbiohub/issues/1744) | Backend lacks OR request parsing mechanism | Bug — query capability | Jul 2026 |

**Community discussion highlights from #1753 (OMEX/SBML export bug):**

Maintainer **cjmyers** explained the root cause:
> *"The issue is that Model->source is not followed to find all files. However, the SBML file will come in an OMEX download of the Attachment object or the Collection that has the Attachment as a member."*

He then identified the fix pattern used in the sibling project:
> *"For SynBioSuite, fixed this by making the SBML file an attachment of the Model object."*

**Takeaway:** The v1 issues tell the story of a platform in graceful decline — the team is doing maintenance releases but the real innovation is in v3. The Virtuoso triplestore, once cutting-edge for RDF-based design sharing, is now showing its age: recursive collection resolution breaks, OMEX exports are incomplete, and database hygiene is a growing burden. These are classic symptoms of a legacy graph database struggling at scale. The #1753 discussion reveals a specific structural problem: the OMEX export pipeline doesn't traverse `Model->source` references, so SBML attachments get orphaned in the download bundle. The fix — promoting SBML files to top-level Model attachments — is a schema-level change that will ripple across all downstream consumers.

---

#### 3. iBioSim (67 ⭐) — The CAD Tool Striving for Modern Compatibility

**Scope:** Computer-aided design (CAD) tool for modeling, analysis, and design of genetic circuits. Imports/exports SBML (all levels/versions) and supports SBOL. Includes multi-cellular and spatial modeling support. Active developers: Lukas Buecherl, Pedro Fontanarrosa, Chris Myers. Apache-2.0 license. Stack: Java + libSBML + reb2sac + GeneNet + Yosys.

**Current Open Issues (no new activity since Aug 2025):**

| Issue | Title | Theme | Date | Comments |
|---|---|---|---|---|
| [#640](https://github.com/MyersResearchGroup/iBioSim/issues/640) | A Java exception has occurred | Stability / runtime | Aug 2025 | 1 |
| [#639](https://github.com/MyersResearchGroup/iBioSim/issues/639) | Can't upload SynBioHub design | Integration failure | May 2025 | 1 |
| [#638](https://github.com/MyersResearchGroup/iBioSim/issues/638) | Unable to run iBioSim 3.2.0 on Mac | Cross-platform | May 2025 | 1 |
| [#637](https://github.com/MyersResearchGroup/iBioSim/issues/637) | Unable to generate models (NoClassDefFoundError: Apache Jena/Xerces) | Bug — Java dependency | Jan 2025 | 6 |
| [#635](https://github.com/MyersResearchGroup/iBioSim/issues/635) | Cannot open iBioSim on Windows 11 | Cross-platform | Jan 2025 | 4 |
| [#634](https://github.com/MyersResearchGroup/iBioSim/issues/634) | Bug importing file and when starting iBioSim | Bug — data import | Sep 2024 | 6 |
| [#632](https://github.com/MyersResearchGroup/iBioSim/issues/632) | Can't connect to LCP Synbiohub | Integration failure | Apr 2024 | 2 |
| [#631](https://github.com/MyersResearchGroup/iBioSim/issues/631) | Problem with External Components | Bug — component handling | Mar 2024 | — |

**Key error from #637 (most discussed, 6 comments):**
```
java.lang.NoClassDefFoundError: Could not initialize class org.apache.jena.query.ARQ
Caused by: java.lang.NoClassDefFoundError: org/apache/xerces/util/XMLChar
```
A transitive dependency conflict — Apache Jena can't initialize because Xerces is missing or conflicting. The stack trace shows the failure chain: `SBOLStackHandler.getInteractions` → `TripleStoreHandler.executeSparql` → `QueryEngineHTTP.<init>` → `ARQ.<clinit>` → `XMLChar` missing.

**Community discussion highlights from #637:**

User **Hatem-synbio** was debugging Kenzo's toggle switch model, following the iBioSim tutorial page 94 for automatic model generation. Offered to share the COMBINE archive on Slack.

Maintainer **cjmyers** root-caused the issue:
> *"I'm pretty sure the issue has to do with trying to create a model using iGEM parts. iGEM parts do not have interaction information, so it is impossible to generate a model. Granted, there should be a better error than an exception. To actually test this better, should use the Cello library."*

This reveals two layered problems:
1. **Immediate cause:** Apache Jena's Xerces dependency is missing or conflicting in the distribution
2. **Deeper cause:** iGEM Registry parts lack the SBOL interaction annotations that iBioSim requires for model generation — and instead of a graceful error, users get a cryptic Java stack trace

**Takeaway:** Desktop-based synbio CAD tools struggle with **Java dependency management and OS-specific behavior**. iBioSim's 305+ open issues and its broken SynBioHub integration (#639, #632) are a direct consequence of the v1 SynBioHub's aging API. When v3 launches with a proper Swagger API (#1106), this integration story may finally improve. The #637 discussion is particularly telling: the maintainer himself acknowledged the error message is unhelpful — *"there should be a better error than an exception."* This signals a strong opportunity for containerized or web-based alternatives with proper error handling and input validation.

---

#### 4. GENtle2 (106 ⭐) — The Web DNA Editor With Legacy Debt

**Scope:** Web-based DNA editor for synthetic biology. A re-think of the original GENtle desktop application for the web. Written in JavaScript (Node.js + Express + Gulp). The README notes: *"GENtle2 has been almost entirely rewritten over the past year, and remains very much in development. Core features will be extracted into their own modules in the coming months."*

**Current Open Issues (organized under "Refactor" milestones):**

**Milestone: Refactor — Canvas events & RES/annotation cards information** (3 open issues, due Aug 2014):

| Issue | Title | Labels | Comments |
|---|---|---|---|
| [#164](https://github.com/Synbiota/GENtle2/issues/164) | Display feature details when hovering | — | 0 |
| [#163](https://github.com/Synbiota/GENtle2/issues/163) | Tracking mouse events in `Artist` | Feature, Refactor | 0 |
| [#159](https://github.com/Synbiota/GENtle2/issues/159) | Tracking shapes in `Artist` | Feature, Refactor | 6 |

**Milestone: Refactor — Sequence opening/editing** (2 open issues):

| Issue | Title | Labels |
|---|---|---|
| [#132](https://github.com/Synbiota/GENtle2/issues/132) | Replace non-allowed characters by placeholder when importing Genebank | Backlog, Refactor, Optimization |
| [#130](https://github.com/Synbiota/GENtle2/issues/130) | Bug with selection using up arrow | Bug, Refactor |

**Community discussion from #159 (Tracking shapes in `Artist`):**

The maintainer **alexandremeunier** laid out a detailed technical plan:
> *"When drawing a shape, add as an option the ability to `track` the shape, i.e. store it in the `Artist#shapes` array. When clearing or scrolling via `Artist`, the list of shapes needs to be updated (invisible shapes should be removed, position of shapes still visible should be updated when scrolling). We'll need, for each `Shape` subclass: `moveVertically(yOffset)`, `isVisible`, `includesPoint(x, y)`."*

This is a fundamental canvas event system rethink — but the milestone was due August 2, 2014, and was last updated July 19, 2023. The 9-year gap between issue creation and last activity signals a community starved for contributors.

**Takeaway:** GENtle2's issues trace back to 2014-era interaction bugs that persist in the backlog. The refactor milestones indicate the maintainer is attempting a **clean-slate architecture** rather than patching the old codebase — but with only 6 comments on the most discussed issue and a 9-year milestone deadline, this is a story about the difficulty of sustaining open-source scientific software. The canvas event system rewrite (#159, #163, #164) is the key to unlocking hover tooltips, interactive annotation cards, and modern UX — but it remains incomplete.

---

#### 5. DnaChisel (274 ⭐) — The Python-First DNA Optimizer

**Scope:** Python library for optimizing DNA sequences with respect to constraints and objectives. 15+ classes of sequence specifications: codon-optimization, GC-content tuning, restriction site avoidance, homology removal, and more. Part of the EGF Codons suite from the Edinburgh Genome Foundry.

**Current Open Issues:**

| Issue | Title | Theme | Date |
|---|---|---|---|
| [#114](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/114) | Produce multiple different optimized results | Feature — diversity in output | Jun 2026 |
| [#113](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/113) | Low Codon Adaptation Index on optimized sequence | Bug — optimization quality | May 2026 |
| [#111](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/111) | Unexpected Mutation of `codon_usage_table` During Optimization | Bug — data integrity | Apr 2026 |
| [#110](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/110) | Minimize CG | Feature — GC content optimization | Apr 2026 |
| [#107](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/107) | Support for Uridine Depletion (UD) optimization objectives | Feature — new target (5 comments) | Apr 2026 |
| [#102](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/102) | PDF report generation optional during optimize_with_report | Enhancement | Jul 2025 |
| [#105](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/105) | Include / point to "CONTRIBUTING" in the documentation | Documentation | Feb 2026 |
| [#100](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/100) | How to get under-optimal sequences during optimization? | Question — fitness landscape | May 2025 |

**Takeaway:** Users want to **explore the fitness landscape**, not just find the single best sequence. The `codon_usage_table` mutation bug (#111) is concerning because it could silently produce incorrect optimization results. The UD optimization request (#107, 5 comments) and GC minimization (#110) show that the community is pushing DnaChisel toward chemistry-aware targets (making DNA invisible to degradation pathways). The missing CONTRIBUTING docs (#105) hint that the maintainer is a solo academic struggling to absorb community contributions.

---

#### 6. 🆕 poly (737 ⭐) — The Ambitious Go-Native Synthetic Biology Toolkit

**Scope:** A Go package for engineering organisms. Goal: "the most complete, open, and well used collection of computational synthetic biology tools ever assembled." Covers codon optimization, primer design, sequence hashing, Gibson Assembly, Golden Gate, and more. MIT license. Active Discord community (74 forks).

**Why this matters:** With 737 stars and 74 forks, **poly is the most-starred open-source pure synthbio software tool on GitHub** — surpassing even established tools like iBioSim and GENtle2. Its modern Go codebase, comprehensive module coverage, and active development make it the clearest signal that the synbio software community is shifting toward modern, fast, deployable languages.

**Current Open Issues (Milestone v1.0 — Let's get poly to a releasable state!):**

| Issue | Title | Theme | Priority | Date | Status |
|---|---|---|---|---|---|
| [#359](https://github.com/bebop/poly/issues/359) | **Implement Gibson Assembly** | Enhancement — critical feature | 🔴 High | Sep 2023 | **Blocked by #367**, 6 comments, assigned to carreter |
| [#434](https://github.com/bebop/poly/issues/434) | Genbank parser needs heavy refactor or rewrite | Enhancement — code quality | Medium | Dec 2023 | 10 comments, marked stale |
| [#383](https://github.com/bebop/poly/issues/383) | Genbank parser doesn't handle colliding feature names | Bug — data integrity | 🔴 High | Oct 2023 | Marked stale |
| [#367](https://github.com/bebop/poly/issues/367) | Refactor `clone` package | Enhancement — UX | 🔴 High | Sep 2023 | **Blocks #359** |
| [#448](https://github.com/bebop/poly/issues/448) | Remove lunny/log dependency from genbank.go | Enhancement — dep hygiene | — | Dec 2025 | Updated Feb 2026, marked stale |
| [#442](https://github.com/bebop/poly/issues/442) | Turn on `revive` linter in golangci config | Enhancement — devops | Low | Feb 2024 | Good first issue, marked stale |
| [#399](https://github.com/bebop/poly/issues/399) | Tutorial and tests for refactored golden gate | Enhancement — docs | — | Nov 2023 | Marked stale |
| [#422](https://github.com/bebop/poly/issues/422) | Proposal: Create a biological reviewers group | Proposal — governance | — | Dec 2023 | Community governance question |
| [#426](https://github.com/bebop/poly/issues/426) | Proposal — New external package (rebased) | Enhancement — modular design | Medium | Dec 2023 | Architecture discussion |
| [#413](https://github.com/bebop/poly/issues/413) | Each fragment in PCR amplification should have a circular tag | Proposal — PCR modeling | — | Dec 2023 | Feature modeling |

**The critical dependency chain blocking v1.0:**
Issue #359 (Gibson Assembly) is explicitly **blocked by #367** (clone package refactor). This means the v1.0 release cannot ship until the clone package is refactored — a classic case of technical debt blocking feature delivery. The Gibson Assembly issue has 6 comments and is marked "high priority" and "intermediate" difficulty, making it the most important missing piece for the v1.0 milestone.

**The governance question (#422):**
The proposal for a "biological reviewers group" is particularly notable — it signals that the community is thinking about how to ensure biological accuracy of computationally designed constructs. As poly grows and more people use it without wet-lab expertise, this question becomes urgent: who validates that the DNA sequences poly generates are biologically correct and safe?

**Takeaway:** poly's v1.0 milestone has 12 open issues — a mix of critical features (Gibson Assembly), code quality debt (genbank parser), and governance proposals (biological reviewers). The Gibson Assembly issue (#359) is blocked by the clone refactor (#367), creating a dependency chain that illustrates the challenge of building a comprehensive toolkit from scratch. The proposal for a "biological reviewers group" (#422) is particularly notable — it signals that the community is thinking about how to ensure biological accuracy of computationally designed constructs, a question that becomes urgent as design tools scale.

---

#### 7. 🆕 CASPIA (13 ⭐) — AI-Powered Automatable Metabolic Engineering

**Scope:** CASPIA (Computational Automation for Synthetic Biology and Metabolic Engineering) is an AI-powered platform designed to revolutionize synthetic biology research through intelligent automation, knowledge retrieval, and metabolic engineering workflow orchestration. Python-based. Actively maintained (last update May 2026).

**Why this matters:** CASPIA represents the emerging wave of **AI-native metabolic engineering platforms** — tools that don't just optimize sequences but orchestrate entire research workflows, retrieve relevant knowledge from literature, and suggest experimental next steps. It sits at the intersection of LLM-powered research assistance and traditional bioengineering pipelines.

**Takeaway:** While still small (13 stars), CASPIA signals where metabolic engineering is heading: from manual, hypothesis-driven experimentation toward AI-coordinated, automated design-build-test-learn cycles. It complements — rather than competes with — tools like ART (which focuses on strain recommendation) and 20n/act (which focuses on DNA route prediction). CASPIA's knowledge-retrieval layer could be the glue that connects disparate synbio tools into an intelligent workflow.

---

#### 8. Coral (32 ⭐) — Design-as-Code for Synthetic Biology

**Scope:** Python library for encoding the process of designing synthetic DNA constructs. Mirrors traditional GUI-based design steps (ApE, j5, Benchling) as operations on data structures. Enables iterative design through analysis modules. MIT license. Stack: Python (works with PyPy + numpy), Biopython.

**Current Open Issues:** Only **1 open issue** ([#37](https://github.com/klavinslab/coral/issues/37) — Ubuntu 22.04 Python 3 compatibility, filed Dec 2023, 1 comment). Actively maintained, recent updates (June 2026).

**Takeaway:** Coral is a rare example of a **well-maintained, open-source Python library** for synbio design automation. With only 1 open issue and consistent updates, it's the health benchmark of the ecosystem. It's a great reference for how to structure design-as-code workflows, and a contrast point to the struggling desktop tools (iBioSim, GENtle2) that are grappling with dependency and maintenance debt. If you want to see what "sustainable open-source synbio software" looks like, Coral is the model.

---

#### 9. Cello-v2 (74 ⭐) — Verilog-to-DNA Circuit Synthesis

**Scope:** CIDARLab's Cello-v2 lets users specify genetic circuits in **Verilog**, synthesizes them into logic gates, assigns experimentally characterized **TetR homologs** as NOR/NOT gates using Hill-function response curves, and then generates physical DNA sequences via the **Eugene language**. BSD-2-Clause license. Includes a Docker-based DNACompiler container for hosted use.

**Current Open Issues:**

| Issue | Theme | Date |
|---|---|---|
| #50 | Licensing question for DNACompiler container | Licensing — Docker |
| #49 / #48 | Login failures on cellocad.org using Gmail | Hosted service — DevOps |
| #47 | Sequential logic support | Feature — circuit design |
| #26 | GFF/APE/FASTA output formats | Enhancement — export |

**Takeaway:** Friction between the **open-source CLI** and the **hosted web service** — a common theme across academic synbio tooling. Users trust the community cloud but it lacks DevOps backing. The sequential logic request (#47) signals growing ambition beyond combinational circuits.

---

#### 10. BioCRNpyler (54 ⭐) — Biomolecular CRN Compiler

**Scope:** BioCRNpyler compiles high-level biological part specifications (promoters, RBSs, CDSs, terminators) into **SBML chemical reaction networks**. First-class support for **cell-free transcription–translation (TXTL) extracts** as simulation contexts. BSD-3-Clause license. Part of the BuildACell ecosystem.

**Current Open Issues:**

| Issue | Title | Theme | Date |
|---|---|---|---|
| #328 | TMSE companion module — toehold-mediated strand displacement | Feature — RNA devices | — |
| #337 | ODEint convergence failure with EnergyTXTL context | Bug — simulation stability | — |
| #338 | Multi-substrate membrane components for transport | Feature — transport modeling | — |
| #333 | Consistent naming conventions for classes | Task — internal consistency | — |
| #341 | Include bioscrape in CI tests | Task — test infrastructure | — |
| #339 | Decide how to handle examples | Task — documentation | — |

**Takeaway:** The project is actively expanding toward **RNA-based devices** (TMSE module bridges into the toehold-switch toolchain from SASTRA-iGEM) and **cell-free expression** (EnergyTXTL), with growing pains around internal consistency and CI maturity. The ODEint convergence bug (#337) is particularly concerning for users relying on TXTL simulations.

---

### 📊 Emerging Themes from the Community

Based on open-issue triage across all surveyed projects, these are the themes dominating community attention right now:

| # | Theme | What It Means | Key Issues |
|---|---|---|---|
| 1 | **🔴 The SynBioHub Swagger API** | The just-filed #1106 (Sep 3, 2026) is the most impactful open issue in the ecosystem. A proper API would fix iBioSim's broken upload (#639), enable third-party clients, and unlock the v3 migration. Without it, the toolchain remains disconnected. | [synbiohub3#1106](https://github.com/SynBioHub/synbiohub3/issues/1106), [iBioSim#639](https://github.com/MyersResearchGroup/iBioSim/issues/639) |
| 2 | **The SynBioHub Migration** | v1 is in maintenance mode with data-integrity bugs (OMEX exports broken, recursive downloads failing, SubCollections not reporting members); v3 is a React+Spring Boot rewrite at 16 stars, not yet adopted by the community. | [synbiohub#1753-1756](https://github.com/SynBioHub/synbiohub/issues), [synbiohub3#1106-1108](https://github.com/SynBioHub/synbiohub3/issues) |
| 3 | **Interoperability & integration friction** | iBioSim can't upload to SynBioHub; OMEX exports miss SBML files; collection prefixes shift when changing visibility; incremental sync broken with SBOLExplorer. The connected synbio toolchain is still hampered by format/URL/API mismatches. | [iBioSim#639](https://github.com/MyersResearchGroup/iBioSim/issues/639), [synbiohub#1753](https://github.com/SynBioHub/synbiohub/issues/1753), [synbiohub#1746](https://github.com/SynBioHub/synbiohub/issues/1746) |
| 4 | **Data integrity in shared collections** | SubCollections not reporting members (#1756), recursive downloads not following links (#1755), legacy Virtuoso DB data piling up (#1754). Growing-pains for platforms hosting community-wide design registries. | [synbiohub#1754-1756](https://github.com/SynBioHub/synbiohub/issues) |
| 5 | **Long-standing UI bugs in academic tools** | GENtle2's 2014-era interaction bugs remain unfunded; a common pattern in academic tools that lose active maintainers. The "Refactor — Canvas events" milestone has been open for 12 years. | [GENtle2#159](https://github.com/Synbiota/GENtle2/issues/159), [GENtle2#162](https://github.com/Synbiota/GENtle2/issues/162) |
| 6 | **Cross-platform compatibility** | iBioSim's Mac (#638) and Windows 11 (#635) issues; SynBioHub3's OpenSSL 3 breaking Windows dev setup. Java "write once, run everywhere" remains aspirational. | [iBioSim#635](https://github.com/MyersResearchGroup/iBioSim/issues/635), [iBioSim#638](https://github.com/MyersResearchGroup/iBioSim/issues/638) |
| 7 | **Optimization depth vs. usability** | DnaChisel users want to explore sub-optimal solutions (fitness landscapes, #100), not just get the single best answer. New requests for UD optimization (#107, 5 comments) and GC minimization (#110) show chemistry-aware design. The `codon_usage_table` mutation bug (#111) could silently produce incorrect results. | [DnaChisel#100](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/100), [DnaChisel#111](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/111) |
| 8 | **Dependency chains blocking releases** | poly's Gibson Assembly (#359) is blocked by the clone refactor (#367), preventing v1.0 delivery. Dependency hygiene issues (#448, #442) compound the problem. This is a pattern: academic tools ship incomplete because refactors block features. | [poly#359](https://github.com/bebop/poly/issues/359), [poly#367](https://github.com/bebop/poly/issues/367) |
| 9 | **Modern language adoption** | The success of **poly** (Go, 737⭐) and **DnaChisel** (Python, 274⭐) vs. aging Java tools (iBioSim, GENtle2) shows the community gravitating toward modern, fast, easy-to-deploy languages. Even SynBioHub is rewriting from Node.js+Virtuoso to React+Spring Boot. | poly, DnaChisel, SynBioHub v3 |
| 10 | **ML + AI convergence** | ART's ML for strain engineering, CASPIA's AI workflow orchestration, TDC's therapeutic benchmarks, DeepVariant point to an accelerating intersection of ML and biological design automation. | [ART](https://github.com/JBEI/ART), [CASPIA](https://github.com/shenmaa233/SJTU-software-CASPIA), [TDC](https://github.com/mims-harvard/TDC) |
| 11 | **RNA device engineering & cell-free systems** | BioCRNpyler's TMSE module (#328); EnergyTXTL convergence bugs (#337); toehold-switch design tools from SASTRA-iGEM — growing interest in programmable RNA devices and cell-free expression as alternatives to in-vivo circuit characterization. | [BioCRNpyler#328](https://github.com/BuildACell/bioCRNpyler/issues/328), [BioCRNpyler#337](https://github.com/BuildACell/bioCRNpyler/issues/337) |
| 12 | **Governance & biological review** | poly's proposal for a "biological reviewers group" (#422) signals that the community is grappling with how to ensure biological accuracy of computationally designed constructs — urgent as design tools scale and more people use them without wet-lab expertise. | [poly#422](https://github.com/bebop/poly/issues/422) |
| 13 | **Dependency management in desktop tools** | iBioSim's Jena/Xerces crash (#637), GENtle2's aging Node.js stack, poly's dependency hygiene issues (#448, #442) — all point to the challenge of managing transitive dependencies in scientific software that integrates many libraries. | [iBioSim#637](https://github.com/MyersResearchGroup/iBioSim/issues/637) |
| 14 | **Stalled academic projects** | GENtle2's 12-year-old refactor milestone, iBioSim's 305+ open issues with slow triage, and dormant projects — the "publish and abandon" pattern is prevalent in university synbio software. Coral (1 issue, consistently updated) is the counter-example. | [GENtle2#159](https://github.com/Synbiota/GENtle2/issues/159), [iBioSim#640](https://github.com/MyersResearchGroup/iBioSim/issues/640) |

---

## 🔥 Fresh Research Findings — September 2026

This section captures the most recent discoveries from the September 2026 research sweep, highlighting issues that are brand-new or have significant recent activity.

### 🆕 SynBioHub v3 — Swagger API (#1106) Just Landed

- **Filed:** September 3, 2026 by maintainer **cjmyers**
- **Assigned to:** Contributor **pagarap57**
- **Milestone:** SBH 3.0.0 (142 open issues, 65 closed)
- **Why it matters:** This is the **single most impactful open issue** in the entire synbio ecosystem. A Swagger-documented REST API would:
  - Fix iBioSim's broken SynBioHub upload integration (#639, open since May 2025)
  - Enable third-party clients and plugins (GENtle2, Desktop tools)
  - Provide a stable interface for the v3 migration, decoupling frontend from backend
  - Open the door for automated pipelines that programmatically upload and retrieve designs
- **Risk:** The SBH 3.0.0 milestone was due August 31, 2026 — it's already overdue. The Swagger API is critical path for the entire v3 vision.

### 🆕 SynBioHub v3 — Dev2 Search Bug (#1108)

- **Filed:** September 12, 2026 by **cl117** (likely the same contributor working on the v3 backend)
- **Label:** Bug
- **No comments yet** — may be a fresh report without community visibility
- **Context:** "dev2 doesn't show any similar parts" suggests the search/recommendation feature in the v3 development environment is broken. This is particularly concerning because search quality is fundamental to a design-sharing platform — if users can't find similar parts, the platform's utility drops significantly.

### 🆕 SynBioHub v3 — Collections Page Update (#1107)

- **Filed:** September 4, 2026 by **cjmyers**
- **Assigned to:** **BroD54** (new contributor?)
- **Milestone:** SBH 2.0.0
- **Context:** The collections page is a core navigation element. An enhancement here suggests the v3 team is refining the user experience for browsing and organizing design collections — a sign they're moving from "make it work" to "make it usable."

### 🆕 poly — Gibson Assembly Blocker (#359) Remains Unresolved

- **High priority, intermediate difficulty, 6 comments, assigned to carreter**
- **Blocked by #367** (clone package refactor) — this dependency chain means v1.0 cannot ship until the refactor is complete
- **Marked stale** but still assigned — the maintainer hasn't closed it, suggesting it's still on their radar
- **Impact:** Gibson Assembly is the most common molecular cloning method. Without it, poly can't compete with established tools like Benchling or ApE for standard cloning workflows

### 🆕 Coral — Nearly Complete Health

- **Only 1 open issue** (Ubuntu 22.04 Python 3 compatibility, filed Dec 2023)
- **Consistent maintenance** — recent updates through June 2026
- **This is the gold standard** for sustainable open-source synbio software in an ecosystem where many projects have 300+ open issues or 12-year-old milestones

---

## 📂 Archive Structure

```
episode-scripts-archive/
├── episodes/
│   ├── EP001-synbiohub-migration/     # The v1→v3 rewrite story
│   ├── EP002-interoperability-crisis/ # Data portability & OMEX bugs
│   ├── EP003-desktop-tool-bottleneck/ # iBioSim & GENtle2 cross-platform struggles
│   ├── EP004-from-hand-engineering-to-ml/ # ART, CASPIA, and computational design
│   ├── EP005-dna-optimization-deep-dive/ # DnaChisel, poly, and sequence design
│   ├── EP006-standards-maturation/    # SBOL, SBML, and the state of interoperability
│   ├── EP007-academic-tool-dormancy/  # The "publish and abandon" pattern
│   ├── EP008-poly-the-go-native-toolkit/ # Modern Go-based synbio engineering
│   ├── EP009-rna-devices-cell-free/   # BioCRNpyler, TMSE, EnergyTXTL
│   ├── EP010-cello-verilog-to-dna/    # Verilog-to-DNA circuit synthesis
│   ├── EP011-swagger-api-bridge/      # The SynBioHub v3 API story (Sep 2026)
│   └── ...
├── research/
│   ├── synbio-tools-survey-2026-09.md     # Full survey data
│   ├── community-issues-snapshot-2026-09.md # Curated issue list
│   ├── synbiohub-migration-analysis.md    # v1→v3 rewrite deep dive
│   ├── poly-tool-analysis.md             # Go-native toolkit analysis
│   ├── dnachisel-optimization-landscape.md # DNA design UX challenges
│   ├── ibiosim-cross-platform-struggles.md # iBioSim issue deep dive
│   ├── cello-verilog-synthesis.md        # Cello circuit design analysis
│   ├── swagger-api-impact-analysis.md    # The #1106 story
│   └── references/
├── source-materials/
│   ├── presentations/
│   ├── datasets/
│   └── tooling-context/
├── scripts/
│   ├── episode-template.md
│   └── show-notes-template.md
├── production-assets/
│   ├── slides/
│   ├── diagrams/
│   └── recordings/
└── README.md
```

---

## 🔗 Key Resources & Communities

### Tools & Platforms

| Resource | Link | Description |
|---|---|---|
| [SynBioHub v1](https://synbiohub.org) | [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) | Design repository & sharing platform (legacy, 84⭐) |
| [SynBioHub v3](https://github.com/SynBioHub/synbiohub3) | [SynBioHub/synbiohub3](https://github.com/SynBioHub/synbiohub3) | React + Spring Boot redesign (active, 16⭐) |
| [iBioSim](http://www.ibiosim.org/) | [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) | Genetic circuit CAD tool |
| [DnaChisel](https://edinburgh-genome-foundry.github.io/DnaChisel/) | [EGF/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) | Python DNA sequence optimizer |
| [poly](https://github.com/bebop/poly) | [bebop/poly](https://github.com/bebop/poly) | Go package for engineering organisms (737⭐) |
| [GENtle2](https://synbiota.com) | [Synbiota/GENtle2](https://github.com/Synbiota/GENtle2) | Web-based DNA editor |
| [Coral](https://github.com/klavinslab/coral) | [klavinslab/coral](https://github.com/klavinslab/coral) | Synbio design-as-code framework |
| [Cello-v2](https://github.com/CIDARLAB/Cello-v2) | [CIDARLAB/Cello-v2](https://github.com/CIDARLAB/Cello-v2) | Verilog-to-DNA genetic circuit synthesizer |
| [BioCRNpyler](https://github.com/BuildACell/bioCRNpyler) | [BuildACell/bioCRNpyler](https://github.com/BuildACell/bioCRNpyler) | Biomolecular CRN compiler |
| [act](https://github.com/20n/act) | [20n/act](https://github.com/20n/act) | Predictive bioengineering platform |
| [CASPIA](https://github.com/shenmaa233/SJTU-software-CASPIA) | [shenmaa233/SJTU-software-CASPIA](https://github.com/shenmaa233/SJTU-software-CASPIA) | AI-powered metabolic engineering platform |
| [TDC](https://tdcommons.ai) | [mims-harvard/TDC](https://github.com/mims-harvard/TDC) | Therapeutics Data Commons |
| [Synthea](https://synthetichealth.github.io/synthea/) | [synthetichealth/synthea](https://github.com/synthetichealth/synthea) | Synthetic patient simulator |
| [deepTools](https://deeptools.readthedocs.io/) | [deeptools/deepTools](https://github.com/deeptools/deepTools) | Deep-sequencing analysis toolkit |
| [Biopython](https://biopython.org/) | [biopython/biopython](https://github.com/biopython/biopython) | Foundational Python toolkit for molecular biology |

### Standards & Registries

| Resource | Link |
|---|---|
| [SBOL Specification](https://sbolstandard.org/) | [SynBioDex/SBOL-specification](https://github.com/SynBioDex/SBOL-specification) |
| [libSBOLj](https://github.com/SynBioDex/libSBOLj) | Java library for SBOL |
| [SBML](https://sbml.org/) | Systems Biology Markup Language |
| [iGEM Registry](http://parts.igem.org) | Standard Biological Parts |
| [BioModels](https://www.ebi.ac.uk/biomodels) | Database of mathematical models |

### Communities & Curated Lists

| Resource | Link | Stars |
|---|---|---|
| [awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) | Websemantic's curated list | 223 |
| [awesome-deep-learning-4-life-sciences](https://github.com/virtualramblas/awesome-deep-learning-4-life-sciences) | DL resources for biotech & pharma | 167 |
| [Learn_Synthetic_Biology](https://github.com/llSourcell/Learn_Synthetic_Biology) | Educational resources for synbio | 157 |
| [SBTools Google Group](https://groups.google.com/g/sbtools/) | Synbio tools community hub | — |
| [SBTools Slack](https://sbtools.slack.com) | Active Slack workspace for tool developers | — |

### Organizations to Follow

- **SynBioHub** — Primary design-sharing platform & SBOL standards (v1 maintenance, v3 rewrite)
- **SynBioDex** — SBOL specification & related tools
- **Edinburgh Genome Foundry** — DnaChisel & EGF Codons suite
- **Myers Research Group** — iBioSim (academic CAD tool)
- **JBEI** — ART for strain engineering
- **20n** — Commercial bioengineering (act platform)
- **Autodesk Bio/Nano/Protospace** — Wet-lab protocol automation
- **klavinslab** — Coral design framework
- **BIOFAB** — Early web-based synbio CAD tools
- **CIDARLab** — Cello genetic circuit synthesis (Verilog → DNA)
- **BuildACell** — BioCRNpyler & systems biology tools
- **SASTRA-iGEM** — Academic iGEM team producing ML tools for RNA device design

---

## 📝 Contributing

Contributions are welcome! To add materials:

1. Fork this repository
2. Create a new branch for your episode or addition (`git checkout -b ep-episode-XXX-topic`)
3. Add your script, source materials, or transcript under the appropriate directory
4. Update the research survey if you've surveyed new projects or issues
5. Submit a pull request with a clear description of your additions

### Naming Conventions

- Episode directories: `EPXXX-short-descriptive-title/` (zero-padded, sequential)
- Script files: `script.md` (primary), `show-notes.md` (supplementary)
- Research files: `topic-year-month.md` (e.g., `interoperability-2026-09.md`)
- Assets: place in `production-assets/` with descriptive filenames

---

## 📜 License

This archive is released under the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/), same as the awesome-synthetic-biology list. Individual episode scripts may carry their own licenses — check each episode directory for details.

---

*Last research update: September 18, 2026 — Surveyed 20+ GitHub projects across synthetic biology and biotech software, reviewed 90+ open issues spanning 15 repositories, compiled community themes, and documented the SynBioHub v1→v3 migration (including the brand-new Swagger API issue #1106 filed Sep 3, 2026), poly's Gibson Assembly blocker (#359, blocked by #367), DnaChisel optimization landscape, iBioSim cross-platform struggles (including the Jena/Xerces crash root cause from #637), Cello-v2 Verilog-to-DNA synthesis, BioCRNpyler's RNA device & cell-free systems expansion, GENtle2's 12-year canvas refactor milestone, and Coral's benchmark of sustainable maintenance (1 open issue). Research sources: GitHub issue trackers, repository READMEs, commit histories, community discussion threads (including maintainer commentary on issues #637, #1753, and the fresh Sep 2026 sweep of SynBioHub v3 issues #1106-1108), and organization pages.*