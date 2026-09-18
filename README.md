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

## 🔬 Deep Dives — The Most Active Repos

### 1. SynBioHub v3 (16 Stars) — The Great Redesign Migration

A full rewrite of the SynBioHub platform using **React (Next.js) + Spring Boot (Java 17)**, replacing the legacy v1 stack (Node.js + Maven + OpenLink Virtuoso RDF triplestore). BSD-2-Clause license. **Actively developed — latest commits September 15, 2026.**

**Why this matters:** The v1-to-v3 migration is *the* defining infrastructure story in the synbio ecosystem right now. The legacy v1 has 84 stars and is in maintenance mode (milestone SBH 1.6.2), while v3 is the future — but it's still at 16 stars, meaning the community hasn't fully migrated yet.

**Fresh — September 2026 Issues:**

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

#### Repository Details — SynBioHub v3
- **Stack:** React (Next.js) + Spring Boot (Java 17)
- **License:** BSD-2-Clause
- **Development model:** PR-based with CI; GitHub Actions auto-publish to Docker Hub on release
- **Active contributors:** cjmyers (lead), cl117, pagarap57, BroD54
- **Milestones:** SBH 2.0.0 (UX & sharing), SBH 3.0.0 (Swagger API)

---

### 2. SynBioHub v1 (84 Stars) — The Interoperability Hub (Legacy/Maintenance)

The original SynBioHub platform. Stack: JavaScript (Node.js) + Java (Maven) + OpenLink Virtuoso (RDF triplestore). BSD-2-Clause license. PR-based development with CI (Travis + Docker integration tests via SBOLTestSuite).

**Current Open Issues (Milestone SBH 1.6.2 — final maintenance releases):**

| Issue | Title | Theme | Date | Comments |
|---|---|---|---|---|
| [#1756](https://github.com/SynBioHub/synbiohub/issues/1756) | SubCollections does not report members in public graph | Bug — data integrity | Sep 3, 2026 | 0 |
| [#1755](https://github.com/SynBioHub/synbiohub/issues/1755) | Recursive download does not follow linked collections | Bug — workflow gap | Aug 30, 2026 | 0 |
| [#1754](https://github.com/SynBioHub/synbiohub/issues/1754) | Legacy data in Virtuoso should be deleted | Maintenance — tech debt | Aug 23, 2026 | 0 |
| [#1753](https://github.com/SynBioHub/synbiohub/issues/1753) | OMEX download missing SBML file attachments | Bug — export completeness | Aug 21, 2026 | **2** |
| [#1752](https://github.com/SynBioHub/synbiohub/issues/1752) | Private-to-public visibility shifts URL prefix | Bug — deployment friction | Aug 19, 2026 | 0 |
| [#1746](https://github.com/SynBioHub/synbiohub/issues/1746) | Incremental updates not working with SBOLExplorer | Bug — tool integration | Jul 19, 2026 | 0 |
| [#1745](https://github.com/SynBioHub/synbiohub/issues/1745) | Root collection filter should handle SBOLCanvas layout | Change — visualization | Jul 16, 2026 | 0 |
| [#1744](https://github.com/SynBioHub/synbiohub/issues/1744) | Backend lacks OR request parsing mechanism | Bug — query capability | Jul 16, 2026 | 0 |

**Community discussion from #1753 (OMEX/SBML export bug):**

Maintainer **cjmyers** explained the root cause:
> "The issue is that Model->source is not followed to find all files. However, the SBML file will come in an OMEX download of the Attachment object or the Collection that has the Attachment as a member."

He then identified the fix pattern from SynBioSuite:
> "For SynBioSuite, fixed this by making the SBML file an attachment of the Model object."

**Takeaway:** The v1 issues tell the story of a platform in graceful decline. The Virtuoso triplestore is showing its age: recursive collection resolution breaks, OMEX exports are incomplete, and database hygiene is a growing burden. All 8 open issues are in the final maintenance milestone (SBH 1.6.2), signaling this is the last hurrah before the community fully migrates to v3.

#### Repository Details — SynBioHub v1
- **Stack:** JavaScript (Node.js) + Java (Maven) + OpenLink Virtuoso (RDF triplestore)
- **License:** BSD-2-Clause
- **Forks:** 30
- **Current milestone:** SBH 1.6.2 (maintenance)
- **Key features:** Hosts iGEM Registry of Standard Biological Parts, enriched *B. subtilis* and *E. coli* data
- **Deployment:** Docker image (auto-published via GitHub Actions); dev instance at dev.synbiohub.org

---

### 3. iBioSim (67 Stars) — The CAD Tool Striving for Modern Compatibility

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

Hatem-synbio shared screenshots and offered the COMBINE archive on Slack. cjmyers requested it for deeper testing and suggested using the **Cello library** instead of iGEM parts for proper model generation testing.

**Recent commits (2026):**
- `74ac459` — Merge PR #645: headless stdout fix (Apr 2026)
- `e2d8b7a` — Filter unread progress stdout noise in headless mode (Mar 2026)
- `17c876e` — Update .gitignore for Java SDKMAN (Mar 2026)
- `9df4464` — Add missing full local build deps (Mar 2026)

**Takeaway:** Desktop-based synbio CAD tools struggle with **Java dependency management and OS-specific behavior**. iBioSim's broken SynBioHub integration (#639, #632) is a direct consequence of the v1 SynBioHub's aging API. When v3 launches with a proper Swagger API (#1106), this integration story may finally improve.

#### Repository Details — iBioSim
- **Stack:** Java + libSBML + reb2sac + GeneNet + Yosys
- **License:** Apache-2.0
- **Forks:** 24
- **Active developers:** Lukas Buecherl, Pedro Fontanarrosa, Chris Myers (cjmyers)
- **Capabilities:** SBML import (all levels/versions), SBML export (Level 3 V1), SBOL support, multi-cellular & spatial modeling
- **Website:** http://www.async.ece.utah.edu/ibiosim

---

### 4. GENtle2 (106 Stars) — The Web DNA Editor With Legacy Debt

Web-based DNA editor for synthetic biology. Written in JavaScript (Node.js + Express + Gulp). A re-think of the original GENtle desktop application for the web.

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
| [#154](https://github.com/Synbiota/GENtle2/issues/154) | Plasmid map title overflows for long names | Refactor, Optimization | — | Jul 2014 |
| [#132](https://github.com/Synbiota/GENtle2/issues/132) | Replace non-allowed chars on Genebank import | Backlog, Refactor | Refactor — Seq opening | Jun 2014 |
| [#130](https://github.com/Synbiota/GENtle2/issues/130) | Bug with selection using up arrow | Bug, Refactor | Refactor — Seq opening | Jun 2014 |

**Takeaway:** GENtle2's issues trace back to 2014-era interaction bugs that persist in the backlog. The refactor milestones indicate the maintainer is attempting a clean-slate architecture rather than patching the old codebase — but with only 6 comments on the most discussed issue (#159) and a 9-year milestone deadline, this is a story about the difficulty of sustaining open-source scientific software. The community is starved for contributors.

---

### 5. Syn-Zeug (7 Stars) — The Modern Rust Toolbox

A modern toolbox for synthetic biology, written in **Rust** with a **Svelte SPA** web interface and a **WASM** shim (biobox). Represents a new generation of Rust-based bioinformatics tools.

**Current Open Issues (all feature requests — no bugs!):**

| Issue | Title | Theme | Date | Assignee |
|---|---|---|---|---|
| [#47](https://github.com/Sheffield-iGEM/syn-zeug/issues/47) | Find ORFs In Proteins | New tool — protein analysis | Oct 2022 | — |
| [#46](https://github.com/Sheffield-iGEM/syn-zeug/issues/46) | Upstream `rust-bio` changes | Dependency update | Oct 2022 | 1 comment |
| [#42](https://github.com/Sheffield-iGEM/syn-zeug/issues/42) | Miscellaneous Tools | General feature tracking | Sep 2022 | 1 comment |
| [#39](https://github.com/Sheffield-iGEM/syn-zeug/issues/39) | Add region info to input (like Benchling) | UX improvement | Aug 2022 | — |
| [#38](https://github.com/Sheffield-iGEM/syn-zeug/issues/38) | Pause a tool in the pipeline | Pipeline UX | Aug 2022 | — |
| [#37](https://github.com/Sheffield-iGEM/syn-zeug/issues/37) | Add nice looking tooltips! | UI enhancement | Aug 2022 | kesler20 |
| [#36](https://github.com/Sheffield-iGEM/syn-zeug/issues/36) | Add dragging for building up a pipeline | Pipeline UX | Aug 2022 | — |
| [#26](https://github.com/Sheffield-iGEM/syn-zeug/issues/26) | Implement New Tool: "Percent Composition" | New analysis tool | Aug 2022 | adam-spencer |
| [#17](https://github.com/Sheffield-iGEM/syn-zeug/issues/17) | Implement New Tool: "Shuffle Sequence" | New analysis tool | Apr 2022 | — |
| [#8](https://github.com/Sheffield-iGEM/syn-zeug/issues/8) | Implement New Tool: "Mutate Sequence" | New analysis tool | Apr 2022 | 1 comment |

**Currently implemented tools:**
- **Web UI:** Sequence Validation, Sequence Length, Reverse Sequence, Count Sequence Elements, Reverse Complement, Convert Case (DNA↔RNA↔Protein), GC Content, Find Open Reading Frames
- **Rust Library:** Extract Subsequences, Hamming Distance, Levenshtein Distance

**Takeaway:** Syn-Zeug's all-feature-request issue list signals a stable core ready for community expansion. The Rust+Svelte+WASM architecture is a modern alternative to the Java-based tools.

---

## 📊 What the Community Is Currently Working On & Concerned About

Based on fresh open issues and commit activity across the top projects (as of September 2026), here are the themes dominating community attention:

### 1. The SynBioHub Swagger API (Highest Impact)
The brand-new issue [#1106](https://github.com/SynBioHub/synbiohub3/issues/1106) — "Develop New API Using Swagger" — filed September 3, 2026 under the SBH 3.0.0 milestone, is the single most consequential open issue in the ecosystem. A proper Swagger-documented API would:
- Fix iBioSim's broken SynBioHub upload integration (#639, #632)
- Enable third-party clients and plugins
- Unlock reliable tool-to-platform data exchange
- Serve as the migration bridge from v1 to v3

### 2. SBOL Data Handling & Interoperability (SynBioHub v1)
SynBioHub v1's 8 open issues in milestone SBH 1.6.2 are all about **data portability and reliability**:

| Issue | Title | Theme |
|---|---|---|
| [#1756](https://github.com/SynBioHub/synbiohub/issues/1756) | SubCollections does not report members in public graph | Data integrity |
| [#1755](https://github.com/SynBioHub/synbiohub/issues/1755) | Recursive download does not follow linked collections | Workflow gap |
| [#1754](https://github.com/SynBioHub/synbiohub/issues/1754) | Legacy data in Virtuoso should be deleted | Tech debt |
| [#1753](https://github.com/SynBioHub/synbiohub/issues/1753) | OMEX download missing SBML file attachments | Export completeness |
| [#1752](https://github.com/SynBioHub/synbiohub/issues/1752) | Private-to-public visibility shifts URL prefix | Deployment friction |
| [#1746](https://github.com/SynBioHub/synbiohub/issues/1746) | Incremental updates not working with SBOLExplorer | Tool integration |
| [#1744](https://github.com/SynBioHub/synbiohub/issues/1744) | Backend lacks OR request parsing mechanism | Query capability |

The #1753 discussion reveals the root cause: `Model->source` references aren't traversed during export, so SBML attachments get orphaned. The fix — restructuring SBML files as attachments of Model objects — is a design-level solution, not a patch. **This is the current bottleneck in the synbio workflow.**

### 3. Cross-Platform Compatibility & Stability (iBioSim)
iBioSim users are hitting friction on multiple fronts:
- **Mac compatibility** (#638) — binary/launch failures
- **Windows 11** (#635) — launch failures
- **Java runtime crashes** (#640, #637) — dependency hell
- **SynBioHub integration** (#639, #632) — API incompatibility

The #637 discussion is particularly revealing: even the maintainer (cjmyers) acknowledges the error message is unhelpful — *"there should be a better error than an exception."* The root cause is that iGEM parts lack interaction information needed for model generation, but the tool crashes with a cryptic Jena/Xerces `NoClassDefFoundError` instead of a user-friendly message.

### 4. UI/UX Debt in DNA Editors (GENtle2)
GENtle2's 75+ open issues (many dating to 2014) reveal persistent UX debt. The maintainer has created "Refactor" milestones targeting Canvas events, RES/annotation cards, and sequence opening/editing, but progress is slow. The 10+ year gap between issue creation and last activity signals a community starved for contributors.

### 5. Modern Stacks & Feature Expansion (Syn-Zeug)
Syn-Zeug's 10 open issues are **all feature requests**, not bug reports:
- Protein ORF finding (#47)
- Tooltips and UI polish (#37, #39)
- Pipeline UX: pause, drag-and-drop (#38, #36)
- New analysis tools: Percent Composition (#26), Shuffle Sequence (#17), Mutate Sequence (#8)

This all-feature-request pattern signals a **stable core ready for community expansion**. The Rust+Svelte+WASM architecture is a modern alternative to the Java-based tools.

### 6. Community Coordination & Resource Curation
The [awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) list (223 stars) remains the **central hub** for discovering tools, standards (SBOL, SBML), programming languages (Verilog/Cello, Eugene), and hardware (BioHackAcademy, 3DuF). No open issues — well-maintained with smooth community contributions.

---

## 📋 Emerging Themes & Opportunities for Content

| # | Theme | Story Angle | Key Issues |
|---|---|---|---|
| 1 | **The Interoperability Crisis** | SynBioHub's issues are almost all about data not moving correctly. The #1753 discussion reveals the root cause: `Model->source` references aren't traversed. This is *the* current bottleneck. | [synbiohub#1753](https://github.com/SynBioHub/synbiohub/issues/1753) |
| 2 | **The Swagger API as Linchpin** | Issue #1106 could fix everything — iBioSim's broken upload, third-party clients, the v1→v3 migration. It's the most impactful open issue in the ecosystem. | [synbiohub3#1106](https://github.com/SynBioHub/synbiohub3/issues/1106) |
| 3 | **The Desktop Tool Bottleneck** | iBioSim's 305+ issues and GENtle2's 75+ issues both point to the same problem: desktop CAD tools struggle with Java dependency hell, OS compatibility, and aging UI codebases. | [iBioSim#637](https://github.com/MyersResearchGroup/iBioSim/issues/637), [GENtle2#159](https://github.com/Synbiota/GENtle2/issues/159) |
| 4 | **From Hand Engineering to Computational Design** | ART and 20n/act represent a fundamental shift: enumerate all possible designs computationally and pick the best. This is the "DeepSeek moment" for synbio. | [ART](https://github.com/JBEI/ART), [20n/act](https://github.com/20n/act) |
| 5 | **The Missing Open-Source Stack** | ART's code is private, 20n/act is internally maintained, and GENtle2 has a fractured community. There's a clear opportunity for an open-source, web-native, ML-integrated design tool. Syn-Zeug (Rust) and sboljs3 (TypeScript) are early indicators. | [Syn-Zeug](https://github.com/Sheffield-iGEM/syn-zeug) |
| 6 | **Standards Are Maturing, but Pipelines Aren't** | SBOL and SBML are well-defined, but the *pipelines* that move data between tools are broken. The standards exist; the plumbing doesn't. | [synbiohub#1753-1756](https://github.com/SynBioHub/synbiohub/issues) |
| 7 | **Modern Language Adoption** | poly (Go, 737 stars) and DnaChisel (Python, 274 stars) are outpacing traditional Java tools. The SynBioHub v3 rewrite to Spring Boot signals the old guard is adapting. | [poly](https://github.com/bebop/poly), [SynBioHub v3](https://github.com/SynBioHub/synbiohub3) |
| 8 | **Stalled Academic Projects** | GENtle2's 12-year-old refactor milestone and iBioSim's 305+ open issues contrast sharply with Coral (1 open issue) and Syn-Zeug (all features, no bugs). Sustainable maintenance is a choice, not an accident. | [GENtle2#159](https://github.com/Synbiota/GENtle2/issues/159), [Coral#37](https://github.com/klavinslab/coral/issues/37) |

---

## 🔗 Key Resources & Communities

### Core Tools & Platforms

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
| Syn-Zeug | [Sheffield-iGEM/syn-zeug](https://github.com/Sheffield-iGEM/syn-zeug) | 7 |
| sboljs3 | [SynBioDex/sboljs3](https://github.com/SynBioDex/sboljs3) | 7 |
| TDC | [mims-harvard/TDC](https://github.com/mims-harvard/TDC) | 1,283 |
| Biopython | [biopython/biopython](https://github.com/biopython/biopython) | 5,070 |

### Standards & Registries

| Resource | Link |
|---|---|
| SBOL Specification | [SynBioDex/SBOL-specification](https://github.com/SynBioDex/SBOL-specification) |
| SBOL Java Library | [SynBioDex/libSBOLj](https://github.com/SynBioDex/libSBOLj) |
| SBML | [sbml.org](https://sbml.org/) |
| iGEM Registry | [parts.igem.org](http://parts.igem.org) |
| BioModels | [ebi.ac.uk/biomodels](https://www.ebi.ac.uk/biomodels) |
| SBOL Test Suite | [SynBioDex/sboltestsuite](https://github.com/SynBioDex/sboltestsuite) |

### Communities & Curated Lists

| Resource | Link | Stars |
|---|---|---|
| awesome-synthetic-biology | [websemantics/awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) | 223 |
| awesome-deep-learning-4-life-sciences | [virtualramblas/awesome-deep-learning-4-life-sciences](https://github.com/virtualramblas/awesome-deep-learning-4-life-sciences) | 167 |
| Learn_Synthetic_Biology | [llSourcell/Learn_Synthetic_Biology](https://github.com/llSourcell/Learn_Synthetic_Biology) | 157 |
| BioTech-Resources | [robertosolari/BioTech-Resources](https://github.com/robertosolari/BioTech-Resources) | 16 |
| SBTools Slack | [sbtools.slack.com](https://sbtools.slack.com) | — |

---

## 📁 Repository Structure

```
episode-scripts-archive/
├── README.md                  ← You are here
├── RESEARCH.md                ← Detailed research notes & issue analysis
├── episodes/
│   ├── EP001-synbiohub-migration/
│   ├── EP002-the-swagger-api/
│   ├── EP003-interoperability-crisis/
│   ├── EP004-desktop-tool-bottleneck/
│   ├── EP005-ml-designed-biology/
│   ├── EP006-rust-bioinformatics/
│   ├── EP007-sbol-web-standard/
│   └── ...
├── source-materials/
│   ├── presentations/
│   ├── datasets/
│   └── references/
├── scripts/
│   ├── EP001-synbiohub-migration.md
│   ├── EP002-the-swagger-api.md
│   └── ...
├── transcripts/
│   └── EP001-synbiohub-migration-transcript.md
└── community-findings/
    ├── synbiohub-issues-sep-2026.md
    ├── ibiosim-issues-2025-2026.md
    ├── gen-tle2-legacy-analysis.md
    └── syn-zeug-feature-roadmap.md
```

---

## 📝 Contributing

Contributions are welcome! To add materials:

1. Fork this repository
2. Create a new branch for your episode or addition (`git checkout -b ep009-feature`)
3. Add your script, source materials, or transcript under the appropriate directory
4. Update the research survey if you've surveyed new projects or issues
5. Submit a pull request

### Naming Conventions

- Episode directories: `EPXXX-short-descriptive-title/` (zero-padded, sequential)
- Script files: `script.md` (primary), `show-notes.md` (supplementary)
- Research files: `topic-year-month.md` (e.g., `interoperability-2026-09.md`)
- Community findings: `project-name-issues-period.md` (e.g., `synbiohub-issues-sep-2026.md`)
- Assets: place in `production-assets/` with descriptive filenames

---

## 📜 License

This archive is released under the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).

---

*Last research update: September 18, 2026 — Surveyed 20+ GitHub projects across synthetic biology and biotech software, reviewed 70+ fresh open issues spanning 10 repositories, compiled community themes, and documented the SynBioHub v1-to-v3 migration (including the brand-new Swagger API issue #1106 filed Sep 3, 2026), poly's Gibson Assembly blocker, DnaChisel's chemistry-aware optimization requests, iBioSim's cross-platform struggles (including the Jena/Xerces crash root cause from #637), GENtle2's 12-year canvas refactor milestone, Syn-Zeug's all-feature-expansion roadmap, and Coral's benchmark of sustainable maintenance.*