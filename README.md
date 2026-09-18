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

*Research compiled: September 2026 | Methodology: repository search, star-ranked analysis, open-issue triage across 15+ projects, detailed issue inspection across 6 thematic categories, direct review of community discussion threads (SynBioHub #1753, iBioSim #637), and live commit-activity analysis of the two most actively maintained repos.*

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

## 🔍 Deep Dives: The Two Most Active Repos

### 🔬 SynBioHub (84 stars, BSD-2-Clause license)

- **What it does:** Web application enabling users and software to browse, upload, and share synthetic biology designs. Hosts the iGEM Registry of Standard Biological Parts and enriched *B. subtilis* and *E. coli* data.
- **Stack:** JavaScript (Node.js) + Java (Maven) + OpenLink Virtuoso (RDF triplestore)
- **Development model:** PR-based with CI (Travis + Docker integration tests via SBOLTestSuite); automatic Docker Hub publishing via GitHub Actions; releases auto-published to Docker Hub via GitHub Actions
- **Recent commit activity (as of Sep 6, 2026):** Very active — 5 commits in the last week, including fixes for public subcollection graph clauses and Explorer compatibility pinning. Maintainer `cjmyers` and contributor `Mike Arpaia` are co-leading the 1.6.2 milestone.
- **Current issue focus (8 open issues in milestone SBH 1.6.2):** Data portability, interoperability, and infrastructure maintenance

#### Open Issues (Sep 2026)

| Issue | Title | Labels | Date | Summary |
|-------|-------|--------|------|---------|
| [#1756](https://github.com/SynBioHub/synbiohub/issues/1756) | SubCollections does not report members in public graph | bug | Sep 3, 2026 | Fix already merged (`7c6c191` — "Fix public subcollection graph clauses") |
| [#1755](https://github.com/SynBioHub/synbiohub/issues/1755) | Recursive download does not follow linked collections | bug | Aug 30, 2026 | Downloads don't traverse linked collection references |
| [#1754](https://github.com/SynBioHub/synbiohub/issues/1754) | Legacy data in Virtuoso should be deleted | — | Aug 23, 2026 | Database cleanup needed for deprecated entries |
| [#1753](https://github.com/SynBioHub/synbiohub/issues/1753) | OMEX download missing SBML file attachments | bug | Aug 21, 2026 | OMEX export missing SBML attachments (2 comments, community affected) |
| [#1752](https://github.com/SynBioHub/synbiohub/issues/1752) | Private-to-public visibility change resets prefix | — | Aug 19, 2026 | Changing visibility from private to public resets the URI prefix |
| [#1746](https://github.com/SynBioHub/synbiohub/issues/1746) | Incremental updates not working with SBOLExplorer | bug | Jul 19, 2026 | SBOLExplorer can't pull incremental updates (assigned to cl117) |
| [#1745](https://github.com/SynBioHub/synbiohub/issues/1745) | Root collection filter should handle SBOLCanvas layout properly | change | Jul 16, 2026 | SBOLCanvas layout not respected in root collection filter |
| [#1744](https://github.com/SynBioHub/synbiohub/issues/1744) | Backend should have a mechanism to parse OR request | bug | Jul 16, 2026 | Backend lacks OR (or) query parsing support |

#### Community Discussion Highlights

**Issue #1753 — OMEX download missing SBML file attachments** (2 comments)

- **cjmyers (maintainer):** *"The issue is that Model->source is not followed to find all files. However, the SBML file will come in an OMEX download of the Attachment object or the Collection that has the Attachment as a member."*
- **cjmyers (follow-up):** *"For SynBioSuite, fixed this by making the SBML file an attachment of the Model object."* — suggesting the fix is to restructure how SBML files are referenced within OMEX bundles.

> **Takeaway:** The community is seriously focused on making design data more reliably portable and interoperable across tools. OMEX bundle integrity, recursive collection resolution, and database hygiene are the pain points. This signals the ecosystem is maturing — users need dependable data pipelines.

---

### 🔬 iBioSim (67 stars, Apache-2.0 license)

- **What it does:** Computer-aided design (CAD) tool for modeling, analysis, and design of genetic circuits. Imports/exports SBML (all levels/versions) and supports SBOL. Includes multi-cellular and spatial modeling support.
- **Stack:** Java + libSBML + reb2sac + GeneNet + Yosys
- **Active developers:** Lukas Buecherl, Pedro Fontanarrosa, Chris Myers
- **Recent commit activity (as of Apr 7, 2026):** Moderate but steady — 5 commits in recent months, including headless-mode stdout fixes, Java SDK gitignore updates, and build dependency fixes. Contributor `Travis Uhrig` is actively maintaining alongside `cjmyers`.
- **Current issue focus (305+ open issues):** Cross-platform compatibility, Java dependency management, and SynBioHub integration

#### Recent Open Issues (2024–2026)

| Issue | Title | Labels | Date | Summary |
|-------|-------|--------|------|---------|
| [#640](https://github.com/MyersResearchGroup/iBioSim/issues/640) | A Java exception has occurred | — | Aug 24, 2025 | Java runtime crash (1 comment) |
| [#639](https://github.com/MyersResearchGroup/iBioSim/issues/639) | Can't upload SynBioHub design | — | May 31, 2025 | SBOL upload integration failure (1 comment) |
| [#638](https://github.com/MyersResearchGroup/iBioSim/issues/638) | Unable to run iBioSim 3.2.0 in Mac | — | May 22, 2025 | macOS compatibility break (1 comment) |
| [#637](https://github.com/MyersResearchGroup/iBioSim/issues/637) | Unable to generate models automatically | — | Jan 20, 2025 | `NoClassDefFoundError: org.apache.xerces.util.XMLChar` — Apache Jena init failure. 6 comments, active discussion. |
| [#635](https://github.com/MyersResearchGroup/iBioSim/issues/635) | I cannot open iBioSim on Windows 11 | — | Jan 6, 2025 | Windows 11 launch failure (4 comments) |
| [#634](https://github.com/MyersResearchGroup/iBioSim/issues/634) | Bug importing file and when starting | — | Sep 2024 | Import/startup crash (6 comments) |
| [#632](https://github.com/MyersResearchGroup/iBioSim/issues/632) | Can't connect to LCP SynBioHub | — | Apr 2024 | SynBioHub connection handshake failure |

#### Community Discussion Highlights

**Issue #637 — Unable to generate models automatically** (6 comments, most discussed recent issue)

Error from the issue:
```
java.lang.NoClassDefFoundError: Could not initialize class org.apache.jena.query.ARQ
Caused by: java.lang.NoClassDefFoundError: org/apache/xerces/util/XMLChar
```

- **Hatem-synbio (reporter):** Was debugging Kenzo's toggle switch model and following the iBioSim tutorial on page 94 for automatic model generation. Shared screenshots and offered the COMBINE archive on Slack.
- **cjmyers (maintainer):** Identified the root cause — *"I'm pretty sure the issue has to do with trying to create a model using iGEM parts. iGEM parts do not have interaction information, so it is impossible to generate a model. Granted, there should be a better error than an exception. To actually test this better, should use the Cello library."*

> **Takeaway:** Desktop-based synbio CAD tools struggle with Java dependency management and OS-specific behavior. The #637 discussion reveals a deeper issue: iBioSim fails with a cryptic Jena/Xerles crash when the underlying data (iGEM parts) lacks the required interaction information — rather than giving a user-friendly error. This signals a strong opportunity for containerized or web-based alternatives with better error handling.

---

### 🔬 GENtle2 (106 stars, JavaScript)

- **What it does:** Web-based DNA editor for synthetic biology. A re-think of the original GENtle desktop application for the web. Written in JavaScript (Node.js + Express + Gulp).
- **Current issue focus (75+ open issues, many dating to 2014):** Persistent UI/UX bugs and feature gaps. The maintainer (`alexandremeunier`) has been working on a "Refactor" milestone targeting Canvas events, RES/annotation cards, and sequence opening/editing — but progress is slow.

Notable long-standing issues:

| Issue | Title | Labels | Date | Milestone |
|-------|-------|--------|------|-----------|
| [#164](https://github.com/Synbiota/GENtle2/issues/164) | Display feature details when hovering | — | Sep 2014 | Refactor — Canvas events |
| [#163](https://github.com/Synbiota/GENtle2/issues/163) | Tracking mouse events in `Artist` | Feature, Refactor | Sep 2014 | Refactor — Canvas events |
| [#162](https://github.com/Synbiota/GENtle2/issues/162) | Selection disappears via context menu | Bug | Sep 2014 | — |
| [#161](https://github.com/Synbiota/GENtle2/issues/161) | Selection disappears with hotkeys without shift | Bug | Sep 2014 | — |
| [#159](https://github.com/Synbiota/GENtle2/issues/159) | Tracking shapes in `Artist` | Feature, Refactor | Sep 2014 | Refactor — Canvas events |
| [#158](https://github.com/Synbiota/GENtle2/issues/158) | Creating a feature clears plasmid map without redraw | Bug, Refactor | Sep 2014 | — |
| [#156](https://github.com/Synbiota/GENtle2/issues/156) | Caret moves by one base unexpectedly during selection | Bug, Refactor | Sep 2014 | — |
| [#132](https://github.com/Synbiota/GENtle2/issues/132) | Replace non-allowed characters when importing Genebank | Backlog, Refactor | Jun 2014 | Refactor — Sequence opening |

> **Takeaway:** Even well-established tools have significant UI debt. The GENtle project's long-standing unaddressed issues suggest the community is waiting for a modernized, web-native replacement. GENtle2's rewrite is a step in this direction but still has its own open issues. The refactor milestones suggest awareness of the problems, but the 10+ year gap between issue creation and last update signals a community starved for contributors.

---

### 🔬 Syn-Zeug (7 stars, Rust — Emerging)

- **What it does:** A modern toolbox for synthetic biology, written in Rust with a Svelte SPA web interface and a WASM shim (biobox). Represents a new generation of Rust-based bioinformatics tools.
- **Stack:** Rust (core library) + Svelte (web UI) + WASM (biobox shim)
- **Currently implemented tools:**
  - **Web UI:** Sequence Validation, Sequence Length, Reverse Sequence, Count Sequence Elements, Reverse Complement, Convert Case (DNA↔RNA↔Protein), GC Content, Find Open Reading Frames
  - **Rust Library:** Extract Subsequences, Hamming Distance, Levenshtein Distance
- **Deployment:** Pre-built web UI at https://sheffield-igem.github.io/syn-zeug/; walkthrough video available on YouTube
- **Development model:** Open to contributions; high code standards in the Rust library with reviewer guidance for new contributors

#### Open Issues (2022–2023) — All Feature Requests, Zero Bug Reports

| Issue | Title | Labels | Date | Assignee |
|-------|-------|--------|------|----------|
| [#47](https://github.com/Sheffield-iGEM/syn-zeug/issues/47) | Find ORFs In Proteins | — | Oct 2022 | — |
| [#46](https://github.com/Sheffield-iGEM/syn-zeug/issues/46) | Upstream `rust-bio` changes | — | Oct 2022 | 1 comment |
| [#42](https://github.com/Sheffield-iGEM/syn-zeug/issues/42) | Miscellaneous Tools | — | Sep 2022 | 1 comment |
| [#39](https://github.com/Sheffield-iGEM/syn-zeug/issues/39) | Add region info to input field (like Benchling) | — | Aug 2022 | kesler20 |
| [#38](https://github.com/Sheffield-iGEM/syn-zeug/issues/38) | Pause a tool in the pipeline | — | Aug 2022 | kesler20 |
| [#37](https://github.com/Sheffield-iGEM/syn-zeug/issues/37) | Add nice looking tooltips! | — | Aug 2022 | kesler20 |
| [#36](https://github.com/Sheffield-iGEM/syn-zeug/issues/36) | Add dragging for building up a pipeline | — | Aug 2022 | kesler20 |
| [#26](https://github.com/Sheffield-iGEM/syn-zeug/issues/26) | Implement New Tool: "Percent Composition" | enhancement, tool | Apr 2022 | adam-spencer |
| [#17](https://github.com/Sheffield-iGEM/syn-zeug/issues/17) | Implement New Tool: "Shuffle Sequence" | enhancement, tool | Apr 2022 | adam-spencer |
| [#8](https://github.com/Sheffield-iGEM/syn-zeug/issues/8) | Implement New Tool: "Mutate Sequence" | enhancement, tool | Apr 2022 | adam-spencer |

> **Takeaway:** Syn-Zeug's all-feature-request issue list signals a stable core ready for community expansion. The Rust+Svelte+WASM architecture is a pattern worth watching — it may represent the future of web-native bioinformatics tooling.

---

## 📊 What the Community Is Currently Working On & Concerned About

Based on recent open issues and commit activity across the top projects, here are the themes dominating community attention as of September 2026:

### 1. SBOL Data Handling & Interoperability (SynBioHub)

SynBioHub is in its most active development sprint in months. The 1.6.2 milestone has 8 open issues, all focused on data portability and reliability. The maintainer (`cjmyers`) is actively merging fixes weekly.

**Key pattern:** 6 of 8 issues are about **data not moving correctly** between tools — OMEX bundles missing SBML files, recursive downloads breaking, incremental sync failing, query parsing missing. This is not about new features; it's about the **plumbing** of the ecosystem.

### 2. Cross-Platform Compatibility & Stability (iBioSim)

iBioSim users are hitting friction on multiple front — 305+ open issues suggest significant maintenance burden, but recent commits show the team is actively addressing build and headless-mode issues.

**Key pattern:** Users on Mac, Windows 11, and automated workflows are all hitting Java runtime crashes. The #637 discussion reveals the root cause is **data-level** (iGEM parts lack interaction information), not code-level — yet the error message is a cryptic `NoClassDefFoundError`. There's a strong opportunity for **better error handling and containerized deployment**.

### 3. UI/UX Debt in DNA Editors (GENtle2)

GENtle2's 75+ open issues (many dating to 2014) reveal persistent UX debt. The maintainer has created "Refactor" milestones targeting Canvas events, RES/annotation cards, and sequence opening/editing, but progress is slow.

**Key pattern:** The same categories of bugs (selection disappearing, features not redrawing, mouse tracking) have been open for **10+ years**. The community is waiting for a modernized, web-native replacement — and GENtle2 is trying to be that replacement, but it needs contributors.

### 4. Machine Learning & Automated Design (ART, 20n/act)

- **ART** provides **probabilistic strain recommendations** without requiring full mechanistic understanding — a paradigm shift from trial-and-error to computational-directed metabolic engineering. Uses MCMC sampling and Bayesian optimization. Source code is private (access via license).
- **20n/act** demonstrates **end-to-end DNA design automation**, having predicted the first bio-route to acetaminophen. Its 10-module pipeline covers data integration, reaction inference, reachability computation, cascade enumeration, DNA design, NLP, and cost modeling. No open issues — maintained internally by 20n Inc.

**Key pattern:** The field is moving from manual, intuition-driven engineering toward **computational, ML-augmented design pipelines**. However, ART's code is private and 20n/act is internally maintained — suggesting a **gap for open-source alternatives**.

### 5. Modern Stacks & Feature Expansion (Syn-Zeug)

Syn-Zeug's 10 open issues are all feature requests (no bug reports), including:
- Protein ORF finding (#47)
- Tooltips and UI polish (#37, #39)
- Pipeline UX: pause, drag-and-drop (#38, #36)
- New analysis tools: Percent Composition (#26), Shuffle Sequence (#17), Mutate Sequence (#8)
- Dependency updates for upstream rust-bio (#46)

**Key pattern:** The Rust+Svelte+WASM architecture is a **greenfield opportunity** for the community. Zero bug reports means the core is solid — this is the right time for contributors to add features.

### 6. Community Coordination & Resource Curation (awesome-synthetic-biology)

- The curated list (223 stars, 27 forks) remains the **central hub** for discovering tools, standards (SBOL, SBML), programming languages (Verilog/Cello, Eugene), and hardware (BioHackAcademy, 3DuF)
- No open issues — the project is well-maintained and community contributions flow smoothly
- Covers the full stack: software tools → standards → hardware → education → interviews

**Key pattern:** As the ecosystem fragments across dozens of specialized tools, curated indexes and standards become increasingly critical glue. Content creators should reference this list as the **canonical starting point**.

---

## 📖 Emerging Narratives — Stories the Community Is Telling

### 1. "The Interoperability Crisis"
SynBioHub's open issues are almost all about **data not moving correctly** between tools. The #1753 discussion reveals the root cause: `Model->source` references aren't traversed during export, so SBML attachments get orphaned. This is the *current* bottleneck in the synbio workflow. The maintainer's fix — restructuring SBML files as attachments of Model objects — is a **design-level solution**, not a patch.

### 2. "The Desktop Tool Bottleneck"
iBioSim's 305+ issues and GENtle2's 75+ issues both point to the same problem: **desktop-based CAD tools are struggling** with Java dependency hell, OS compatibility, and aging UI codebases. The #637 discussion shows even the maintainer acknowledges the error message is unhelpful — *"there should be a better error than an exception."* **Web-native and containerized tools are the future.**

### 3. "From Hand Engineering to Computational Design"
ART and 20n/act represent a fundamental shift: instead of designing one construct at a time, you **enumerate all possible designs computationally** and pick the best. This is the "DeepSeek moment" for synbio — the design space is too large for human intuition alone.

### 4. "The Missing Open-Source Stack"
ART's code is private, 20n/act is internally maintained, and GENtle2 has a fractured community. There's a **clear opportunity** for an open-source, web-native, ML-integrated design tool that the community can actually build and modify together. **Syn-Zeug (Rust) and sboljs3 (TypeScript)** are early indicators of this direction — modern tech stacks, open development, web-first deployment.

### 5. "Standards Are Maturing, but Pipelines Aren't"
SBOL and SBML are well-defined standards, but the **pipelines that move data between tools** (OMEX exports, recursive downloads, incremental sync) are broken. The standards exist; the plumbing doesn't. **sboljs3** bringing SBOL to the browser is a promising sign — the next step is making those standards reachable from web-native tools end-to-end.

---

## 🛠️ Supporting Tools & Frameworks

Beyond the headline projects, the synbio ecosystem includes a rich set of supporting tools:

| Tool | Category | Description | Link |
|------|----------|-------------|------|
| **Cello/CelloCad** | Genetic circuit design | Logic-gate-based genetic circuit design automation | [CIDARLAB/cello](https://github.com/CIDARLAB/cello) |
| **Eugene** | Design language | Human- and machine-readable language for specifying biological system designs | [eugenecad.org](http://eugenecad.org/) |
| **SBOL Canvas** | Visualization | Genetic circuit schematic building using SBOL standard | [sbolcanvas.org](https://sbolcanvas.org/) |
| **SnapGene** | Plasmid simulation | Visual plasmid construction + simulation (commercial) | [snapgene.com](https://www.snapgene.com/) |
| **DNA Chisel** | Codon optimization | Codon optimization and solving sequence constraints | [Edinburgh-Genome-Foundry/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) |
| **PySB** | Systems biology modeling | Systems biology modeling in Python | [pysb.org](https://pysb.org/) |
| **COPASI** | Metabolic modeling | Modeling biochemical reaction networks | [copasi.org](https://copasi.org/) |
| **COBRA** | Metabolic modeling | Whole-cell metabolic modeler (E. Coli, etc.) | [opencobra.github.io](https://opencobra.github.io/) |
| **BioNetGen** | Rule-based modeling | Structure-based modeling of biochemical reaction networks | [RuleWorld/bionetgen](https://github.com/RuleWorld/bionetgen) |
| **BioCRNpyler** | CRN compiler | Biomolecular chemical reaction network compiler | [BuildACell/bioCRNpyler](https://github.com/BuildACell/bioCRNpyler) |
| **KBase** | Analysis platform | "AWS for systems bio analysis," hosted by DOE | [kbase.us](https://kbase.us) |

---

## 📚 Learning & Resource Hubs

| Project | Stars | Description | Link |
|---------|-------|-------------|------|
| **awesome-synthetic-biology** | 223 | The canonical curated list of synbio projects, articles, resources & standards | [websemantics/awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) |
| **awesome-deep-learning-4-life-sciences** | 168 | Deep learning resources for life sciences (biotech & pharma focus) | [virtualramblas/awesome-deep-learning-4-life-sciences](https://github.com/virtualramblas/awesome-deep-learning-4-life-sciences) |
| **Machine-Learning-in-Biotechnology** | 106 | ML in biotechnology using Python (Packt Publishing companion) | [PacktPublishing/Machine-Learning-in-Biotechnology-and-Life-Sciences](https://github.com/PacktPublishing/Machine-Learning-in-Biotechnology-and-Life-Sciences) |
| **Learn_Synthetic_Biology** | 157 | Educational resources for getting started in synbio | [llSourcell/Learn_Synthetic_Biology](https://github.com/llSourcell/Learn_Synthetic_Biology) |
| **BioTech-Resources** | 16 | Resources for learning biotech, biology, synbio, genomics & bioinformatics | [robertosolari/BioTech-Resources](https://github.com/robertosolari/BioTech-Resources) |
| **synthetic-biology-reading-roadmap** | 13 | Curated list of seminal reviews and papers in synthetic biology | [crimsonigem/synthetic-biology-reading-roadmap](https://github.com/crimsonigem/synthetic-biology-reading-roadmap) |
| **Bioinformatics_SUAT** | 16 | Course materials: "Bioinformatics: From Multi-Omics Data to Discovery" — Shenzhen University Faculty of Synthetic Biology | [xielab2017/Bioinformatics_SUAT_2026_FALL](https://github.com/xielab2017/Bioinformatics_SUAT_2026_FALL) |

---

## 📐 Standards & Interoperability

| Standard | Description | Tools |
|----------|-------------|-------|
| **SBOL** (Synthetic Biology Open Language) | Standard interchange format for design information exchange | SynBioHub, iBioSim, sboljs3, libSBOLj |
| **SBML** (Systems Biology Markup Language) | Standards for mathematical models of biological systems | iBioSim (imports all levels/versions, exports Level 3 V1), COPASI, PySB |
| **iGEM Registry** | Registry of Standard Biological Parts | Hosted via SynBioHub |
| **OMEX** | Bundled download format (SBOL + SBML + other data) | SynBioHub export |
| **SBOL Canvas** | Visualization standard for genetic circuit schematics | SBOLCanvas, GENtle2 |

---

## 📁 Repository Structure

```
episode-scripts-archive/
├── README.md                  ← You are here
├── episodes/
│   ├── episode-01-genome-editing/
│   ├── episode-02-synbio-tools/
│   ├── episode-03-DNA-data-storage/
│   ├── episode-04-interoperability-crisis/
│   ├── episode-05-ml-designed-biology/
│   ├── episode-06-rust-bioinformatics/
│   ├── episode-07-sbol-web-standard/
│   └── ...
├── source-materials/
│   ├── presentations/
│   ├── datasets/
│   └── references/
└── transcripts/
```

---

## 🤝 Contributing

Contributions are welcome! To add materials:

1. Fork this repository
2. Create a new branch for your episode or addition
3. Add your scripts, source materials, or transcripts under the appropriate directory
4. Submit a pull request

Please follow consistent naming conventions:
- Episode directories: `episode-NN-short-title/`
- Script files: `script.md` within each episode directory
- Source materials: reference the originating repo/issue/standard

---

## 📜 License

This archive is released under the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/), same as the awesome-synthetic-biology list. Individual episode scripts may carry their own licenses — check each episode directory for details.

---

## 🔗 Related Communities & Links

### Core Platforms & Registries
- [SynBioHub](https://synbiohub.org) — Design repository & sharing platform
- [Addgene](https://www.addgene.org) — Nonprofit plasmid repository
- [iGEM Registry](http://parts.igem.org) — Standard Biological Parts
- [BioModels](https://www.ebi.ac.uk/biomodels) — Database of mathematical models

### Standards
- [SBOL Standard](https://sbolstandard.org) — Synthetic Biology Open Language
- [SBML](https://sbml.org) — Systems Biology Markup Language
- [SBOL Test Suite](https://github.com/SynBioDex/sboltestsuite) — Compliance testing for SBOL tools

### Tools & Software
- [GENtle2](https://github.com/Synbiota/GENtle2) — Web-based DNA editor
- [iBioSim](https://github.com/MyersResearchGroup/iBioSim) — CAD tool for genetic circuits
- [Coral](https://github.com/klavinslab/coral) — Python library for synthetic DNA design
- [Syn-Zeug](https://github.com/Sheffield-iGEM/syn-zeug) — Rust toolbox for synthetic biology
- [sboljs3](https://github.com/SynBioDex/sboljs3) — TypeScript SBOL library
- [Cello/CelloCad](http://www.cellocad.org/) — Genetic circuit design automation
- [3DuF](https://3duf.org) — Open-source microfluidics design tool
- [KBase](https://kbase.us) — DOE systems biology analysis platform

### Education & Curation
- [awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) — Curated list of all things synbio
- [BioTech-Resources](https://github.com/robertosolari/BioTech-Resources) — Learning resources for biotech & synbio
- [BioHackAcademy](https://biohackacademy.github.io) — Community hardware/course platform
- [COMPSynBio](https://compsynbio.org) — Boston University computational synbio course

---

*This archive was compiled from active GitHub research on the synthetic biology and biotech software ecosystem, capturing the tools, standards, and community concerns as of September 2026. Research methodology: repository search, star-ranked analysis, open-issue triage across 15+ projects, detailed issue inspection of 15+ high-priority bugs across 6 thematic categories, direct review of community discussion threads on the most-reported issues (SynBioHub #1753, iBioSim #637), and live commit-activity analysis of the two most actively maintained repos (SynBioHub: 5 commits/week; iBioSim: steady monthly fixes for headless mode and build deps).*