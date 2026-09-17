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
| **DeepVariant** | 3,807 | Python | Deep learning variant caller for NGS data (BAM/CRAM → VCF/gVCF) | [google/deepvariant](https://github.com/google/deepvariant) |
| **Sourmash** | 557 | Python+Rust | K-mer analysis multitool for genomic & metagenomic comparison | [sourmash-bio/sourmash](https://github.com/sourmash-bio/sourmash) |
| **MEGAHIT** | 727 | C++ | Ultra-fast, memory-efficient metagenome assembler | [voutcn/megahit](https://github.com/voutcn/megahit) |
| **poly** | 737 | Go | Go package for engineering organisms — codon optimization, primer design, Gibson Assembly, Golden Gate | [bebop/poly](https://github.com/bebop/poly) |
| **Kaiju** | 307 | C | Fast taxonomic classification of metagenomic reads using protein DB | [bioinformatics-centre/kaiju](https://github.com/bioinformatics-centre/kaiju) |
| **KrakenUniq** | 253 | C++ | Metagenomics classifier with unique k-mer counting | [fbreitwieser/krakenuniq](https://github.com/fbreitwieser/krakenuniq) |
| **SemiBin** | 175 | Python | Metagenomics binning with self-supervised deep learning | [BigDataBiology/SemiBin](https://github.com/BigDataBiology/SemiBin) |
| **MetaEuk** | 211 | C | Sensitive gene discovery & annotation for eukaryotic metagenomics | [soedinglab/metaeuk](https://github.com/soedinglab/metaeuk) |
| **DnaChisel** | 281 | Python | Versatile DNA sequence optimizer — codon optimization, GC tuning, constraint satisfaction | [Edinburgh-Genome-Foundry/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) |
| **awesome-synthetic-biology** | 223 | — | Curated directory of synbio projects, articles, and resources | [websemantics/awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) |
| **GENtle2** | 106 | JavaScript | Web-based DNA editor for synthetic biology | [Synbiota/GENtle2](https://github.com/Synbiota/GENtle2) |
| **act (20n)** | 92 | Java/Scala | Predictive bioengineering — discovers DNA routes to make target chemicals | [20n/act](https://github.com/20n/act) |
| **SynBioHub v1** | 84 | JavaScript/Java | Web platform for browsing, uploading & sharing synthetic biology designs (legacy) | [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) |
| **SynBioHub v3** | 16 | JavaScript/Java | **Redesign** of SynBioHub using React (Next.js) + Spring Boot (Java 17) | [SynBioHub/synbiohub3](https://github.com/SynBioHub/synbiohub3) |
| **iBioSim** | 67 | Java | CAD for genetic circuits; SBML/SBOL support | [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) |
| **ART (JBEI)** | 66 | Jupyter Notebook | ML tool for automated strain engineering recommendations | [JBEI/ART](https://github.com/JBEI/ART) |
| **SyMBac** | 23 | Python | Synthetic micrographs of bacteria for ML segmentation training data | [georgeoshardo/SyMBac](https://github.com/georgeoshardo/SyMBac) |
| **Coral** | 32 | Python | Library & framework for specifying synthetic biology design processes | [klavinslab/coral](https://github.com/klavinslab/coral) |
| **CASPIA** | 13 | Python | AI-powered platform for automatable, knowledge-retrieval-driven metabolic engineering | [shenmaa233/SJTU-software-CASPIA](https://github.com/shenmaa233/SJTU-software-CASPIA) |
| **ClothoBiofabEdition** | 9 | Java | Synthetic Biology Computer-Aided Design tool | [BIOFAB/ClothoBiofabEdition](https://github.com/BIOFAB/ClothoBiofabEdition) |

---

### 🔬 Deep Dives — Most Active Repos & Their Open Issues

#### 1. DeepVariant (3,807 ⭐) — The Gold Standard for Variant Calling

**Scope:** DeepVariant is a deep learning-based variant caller that takes aligned reads (BAM or CRAM), produces pileup image tensors, classifies each tensor using a convolutional neural network, and reports results in VCF/gVCF format. Supports germline variant-calling in diploid organisms across Illumina, PacBio HiFi, Oxford Nanopore, and hybrid data types. BSD-3-Clause license. Actively maintained by Google's Genomics team.

**Why this matters:** DeepVariant won the 2020 PrecisionFDA Truth Challenge V2 for all categories. It's the most widely used open-source variant caller in clinical and research genomics. Its Docker-based deployment model and support for multiple sequencing technologies make it a cornerstone of modern bioinformatics pipelines.

**Current status:** No open issues found in the primary issue tracker — the project appears to be in a stable, well-maintained phase with regular releases (latest: v1.10.0). The community communicates via a Google Group announcements forum rather than GitHub issues.

**Takeaway:** DeepVariant's stability is itself a story — it represents the maturation of deep learning in genomics. The open questions are shifting from "does it work?" to "how do we extend it to non-human organisms, pangenome-aware calling, and somatic variant detection?" The sibling project [DeepSomatic](https://github.com/google/deepsomatic) addresses somatic calling, and [DeepTrio](https://github.com/google/deepvariant) extends to trio-based variant calling.

---

#### 2. MEGAHIT (727 ⭐) — The Metagenome Assembler Workhorse

**Scope:** Ultra-fast and memory-efficient NGS assembler optimized for metagenomes. Uses succinct de Bruijn graphs to assemble large, complex metagenomic datasets on a single node. Also works well on generic single-genome and single-cell assembly. GPL-3.0 license.

**Current Open Issues (9 open):**

| Issue | Title | Theme | Date |
|---|---|---|---|
| [#390](https://github.com/voutcn/megahit/issues/390) | Assemble Terabase-scale metagenomic reads | Scale & performance | Jan 2026 |
| [#391](https://github.com/voutcn/megahit/issues/391) | Interpretation of log output "Memory used" | Usability / docs | Aug 2026 |
| [#389](https://github.com/voutcn/megahit/issues/389) | How to generate FASTG/GFA with IDs matching final.contigs.fa? | Feature request | Jan 2026 |
| [#388](https://github.com/voutcn/megahit/issues/388) | Circular contigs | Feature — known issue | Dec 2025 |
| [#385](https://github.com/voutcn/megahit/issues/385) | Fails if `--num-cpu-threads` > 1 on macOS | Cross-platform bug | Sep 2025 |
| [#384](https://github.com/voutcn/megahit/issues/384) | Project status and missing decode | Maintenance concern | Jun 2025 |
| [#383](https://github.com/voutcn/megahit/issues/383) | `megahit --test` aborts and dumps core | Crash on test | May 2025 |
| [#379](https://github.com/voutcn/megahit/issues/379) | Assembly failed — error -9 | OOM / resource | Mar 2025 |
| [#378](https://github.com/voutcn/megahit/issues/378) | Not running — `[Errno 2]` | Installation/OS bug | Sep 2024 |

**Takeaway:** MEGAHIT's issues reveal a tool at the edge of its design envelope — users are pushing it toward terabase-scale assemblies (#390) that stress its memory model, while basic functionality like multi-threaded execution on macOS (#385) and core dump on `--test` (#383) suggest declining maintenance attention. Issue #384 ("Project status and missing decode") is particularly concerning — it may signal dormancy. The community needs a maintained fork or a successor assembler for ultra-large metagenomes.

---

#### 3. Sourmash (557 ⭐) — The K-mer Multitool

**Scope:** Quickly search, compare, and analyze genomic and metagenomic data sets. Key features include `FracMinHash` sketching for accurate comparisons between data sets of different sizes, and `sourmash gather` for combinatorial k-mer metagenomic profiling. Published on JOSS (Journal of Open Source Software).BSD-3-Clause license. Python + Rust core.

**Current Open Issues (3 open):**

| Issue | Title | Theme | Date |
|---|---|---|---|
| [#3983](https://github.com/sourmash-bio/sourmash/issues/3983) | Updating prepared databases | Data maintenance | Aug 2026 |
| [#3980](https://github.com/sourmash-bio/sourmash/issues/3980) | Tax lineage file for legacy pre-sketched Mar2018 RefSeq dbs | Data compatibility | Aug 2026 |
| [#3979](https://github.com/sourmash-bio/sourmash/issues/3979) | Good comparison of sourmash and sylph | Feature — benchmarking | Aug 2026 |

**Takeaway:** Sourmash has very few open issues (3!), which is remarkable for a tool with 557 stars. This suggests either excellent maintenance or a community that has moved on. Issue #3979 — comparing Sourmash against [Sylph](https://github.com/sourmash-bio/sourmash) — is interesting because it's an internal comparison, suggesting the maintainers are actively benchmarking their own tool against newer alternatives. The database update issues (#3983, #3980) point to the ongoing challenge of keeping reference databases current with rapidly growing genomic data.

---

#### 4. 🆕 poly (737 ⭐) — The Ambitious Go-Native Synthetic Biology Toolkit

**Scope:** A Go package for engineering organisms. Goal: "the most complete, open, and well used collection of computational synthetic biology tools ever assembled." Covers codon optimization, primer design, sequence hashing, Gibson Assembly, Golden Gate, and more. MIT license. Active Discord community.

**Why this matters:** With 737 stars and 74 forks, **poly is the most-starred open-source pure synthbio software tool on GitHub** — surpassing even established tools like iBioSim and GENtle2. Its modern Go codebase, comprehensive module coverage, and active development (latest updates September 2026) make it the clearest signal that the synbio software community is shifting toward modern, fast, deployable languages.

**Current Open Issues (Milestone v1.0 — Let's get poly to a releasable state!):**

| Issue | Title | Theme | Priority | Date |
|---|---|---|---|---|
| [#359](https://github.com/bebop/poly/issues/359) | Implement Gibson Assembly | Enhancement — critical feature | High | Sep 2023 |
| [#434](https://github.com/bebop/poly/issues/434) | Genbank parser needs heavy refactor or rewrite | Enhancement — code quality | Medium | Dec 2023 |
| [#383](https://github.com/bebop/poly/issues/383) | Genbank parser doesn't handle colliding feature names | Bug — data integrity | High | Oct 2023 |
| [#367](https://github.com/bebop/poly/issues/367) | Refactor `clone` package | Enhancement — UX | High | Sep 2023 |
| [#448](https://github.com/bebop/poly/issues/448) | Remove lunny/log dependency from genbank.go | Enhancement — dep hygiene | — | Dec 2025 |
| [#442](https://github.com/bebop/poly/issues/442) | Turn on `revive` linter in golangci config | Enhancement — devops | Low | Feb 2024 |
| [#399](https://github.com/bebop/poly/issues/399) | Tutorial and tests for refactored golden gate | Enhancement — docs | — | Nov 2023 |
| [#422](https://github.com/bebop/poly/issues/422) | Proposal: Create a biological reviewers group | Proposal — governance | — | Dec 2023 |

**Takeaway:** poly's v1.0 milestone has 12 open issues — a mix of critical features (Gibson Assembly), code quality debt (genbank parser), and governance proposals (biological reviewers). The Gibson Assembly issue (#359) is blocked by the clone refactor (#367), creating a dependency chain that illustrates the challenge of building a comprehensive toolkit from scratch. The proposal for a "biological reviewers group" (#422) is particularly notable — it signals that the community is thinking about how to ensure biological accuracy of computationally designed constructs, a question that becomes urgent as design tools scale.

---

#### 5. 🆕 CASPIA (13 ⭐) — AI-Powered Automatable Metabolic Engineering

**Scope:** CASPIA (Cell-Automated Synthetic Pathway Intelligent Architecture) is an integrated AI-native software platform developed by Team SJTU-Software for the iGEM 2025 competition. Unifies automated genome-scale modeling, high-precision parameter prediction, intelligent agent orchestration, and vision-enhanced literature retrieval.

**Key Modules:**
- **GEMFactory:** Transforms raw genomes into parameter-enriched genome-scale metabolic models (ecGEMs/etcGEMs), incorporating kinetic and thermodynamic parameters (*kcat*, *Topt*)
- **CASPred:** Multimodal predictive engine integrating protein sequence (ESMC-300M) and structural features (GVP) for missing kinetic parameters with uncertainty quantification
- **CASPIAgent:** Natural-language-driven AI agent that plans and executes complex toolchains for gene annotation, model construction, parameter completion, and strain design optimization
- **CASPIA-RAG:** Vision-augmented Retrieval-Augmented Generation system for analyzing text and figures from scientific literature
- **Tasks Monitor:** Real-time monitoring of CASPIA computational workflows

**Stack:** Python 3.10, PyTorch (CUDA 12.8), Gradio web UI, Hugging Face models, ChromaDB vector database, GeneMarkS, Diamond, CarveMe. GPU with 16GB+ VRAM required.

**Why this matters:** CASPIA represents the emerging wave of **AI-native metabolic engineering platforms** — tools that don't just optimize sequences but orchestrate entire research workflows, retrieve relevant knowledge from literature, and suggest experimental next steps. It sits at the intersection of LLM-powered research assistance and traditional bioengineering pipelines. The vision-enhanced RAG component (analyzing figures and tables in papers) is particularly innovative — most RAG systems only process text.

**Current status:** No open issues found. The project is at v1.0.0-beta status with active development. Roadmap includes Docker containerization, cloud deployment, multi-language UI, and dynamic modeling (ODE/DAE integration with GEMs).

**Takeaway:** While still small (13 stars), CASPIA signals where metabolic engineering is heading: from manual, hypothesis-driven experimentation toward AI-coordinated, automated design-build-test-learn cycles. Its knowledge-retrieval layer could be the glue that connects disparate synbio tools into an intelligent workflow. The requirement for a 16GB+ GPU is a significant accessibility barrier —cloud-deployed versions could democratize access.

---

#### 6. 🆕 SyMBac (23 ⭐) — Synthetic Micrographs for ML Training Data

**Scope:** SyMBac generates synthetic phase contrast or fluorescence images of bacteria using a segment-chain physics model, 3D cell geometry, and optical models (point spread function). Provides unlimited, free training data for machine learning image segmentation algorithms. Published in *BMC Molecular and Cell Biology* (DOI: 10.1186/s12915-022-01453-6). GPL-2.0 license.

**Why this matters:** Training data scarcity is a major bottleneck in biological image analysis. SyMBac solves this by generating physically accurate synthetic images that can be used to train U-Net and other segmentation networks. It supports multiple microscope objectives (20x air to 100x oil) and imaging modalities (phase contrast/fluorescence). Speed comparison: SyMBac is ~40x faster than manual annotation.

**Current Open Issues (1 open):**

| Issue | Title | Theme | Date |
|---|---|---|---|
| [#69](https://github.com/georgeoshardo/SyMBac/issues/69) | Design Chromatix brightfield module | Feature — new imaging mode | Jul 2026 |

**Takeaway:** SyMBac has essentially one open issue — a feature request for a new imaging modality (brightfield via Chromatix). This is remarkably clean for an active research tool. It demonstrates that tools with a narrow, well-defined scope (generating synthetic images) can maintain high quality with minimal maintenance burden. The Colab notebook version also lowers the barrier to entry.

---

#### 7. SynBioHub v3 (16 ⭐) — The Great Redesign Migration

**Scope:** A full rewrite of the SynBioHub platform using **React (Next.js) + Spring Boot (Java 17)**, replacing the legacy v1 stack (Node.js + Maven + OpenLink Virtuoso RDF triplestore). BSD-2-Clause license. Actively developed — latest commits September 15, 2026.

**Why this matters:** The v1→v3 migration is *the* defining infrastructure story in the synbio ecosystem right now. The legacy v1 has 84 stars and is in maintenance mode (milestone SBH 1.6.2), while v3 is the future — but it's still at 16 stars, meaning the community hasn't fully migrated yet.

**Current Open Issues (Milestones SBH 2.0.0 & SBH 3.0.0):**

| Issue | Title | Theme | Milestone | Date |
|---|---|---|---|---|
| [#1108](https://github.com/SynBioHub/synbiohub3/issues/1108) | Dev2 doesn't show any similar parts | Bug — search quality | — | Sep 2026 |
| [#1107](https://github.com/SynBioHub/synbiohub3/issues/1107) | Update Collections Page | Enhancement | SBH 2.0.0 | Sep 2026 |
| [#1106](https://github.com/SynBioHub/synbiohub3/issues/1106) | Develop New API Using Swagger | Enhancement — API design | SBH 3.0.0 | Sep 2026 |
| [#1060](https://github.com/SynBioHub/synbiohub3/issues/1060) | Search Suggestions | User Study — UX | SBH 2.0.0 | Jul 2026 |
| [#1062](https://github.com/SynBioHub/synbiohub3/issues/1062) | Create 2 boxes when applying filters in search | User Study — UX | SBH 2.0.0 | Jul 2026 |
| [#1093](https://github.com/SynBioHub/synbiohub3/issues/1093) | Add owner modal | User Study — sharing | SBH 2.0.0 | Aug 2026 |
| [#1092](https://github.com/SynBioHub/synbiohub3/issues/1092) | Sharing and adding owner needs visibility of status | User Study — sharing | SBH 2.0.0 | Aug 2026 |
| [#1091](https://github.com/SynBioHub/synbiohub3/issues/1091) | Add owner list of users | User Study — sharing | SBH 2.0.0 | Aug 2026 |

**Takeaway:** The SynBioHub team is doing a courageous full-stack rewrite. They're shifting from a triplestore-based architecture to a modern React + Spring Boot stack, but the community hasn't caught up yet (16 vs. 84 stars). The migration story — from Virtuoso to relational DB, from server-rendered pages to React SPA, from opaque APIs to Swagger-documented ones — is a rich narrative about the cost and necessity of modernizing scientific infrastructure.

---

#### 8. SynBioHub v1 (84 ⭐) — The Interoperability Hub (Legacy/Maintenance)

**Scope:** The original SynBioHub platform. Web application enabling users and software to browse, upload, and share synthetic biology designs. Hosts the iGEM Registry of Standard Biological Parts. Stack: JavaScript (Node.js) + Java (Maven) + OpenLink Virtuoso (RDF triplestore).

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

**Takeaway:** The v1 issues tell the story of a platform in graceful decline — the team is doing maintenance releases but the real innovation is in v3. The Virtuoso triplestore, once cutting-edge for RDF-based design sharing, is now showing its age: recursive collection resolution breaks, OMEX exports are incomplete, and database hygiene is a growing burden. These are classic symptoms of a legacy graph database struggling at scale.

---

#### 9. iBioSim (67 ⭐) — The CAD Tool Striving for Modern Compatibility

**Scope:** Computer-aided design (CAD) tool for modeling, analysis, and design of genetic circuits. Imports/exports SBML (all levels/versions) and supports SBOL. Includes multi-cellular and spatial modeling support. Active developers: Lukas Buecherl, Pedro Fontanarrosa, Chris Myers. Apache-2.0 license.

**Current Open Issues:**

| Issue | Title | Theme | Date |
|---|---|---|---|
| [#640](https://github.com/MyersResearchGroup/iBioSim/issues/640) | A Java exception has occurred | Stability / runtime | Aug 2025 |
| [#639](https://github.com/MyersResearchGroup/iBioSim/issues/639) | Can't upload SynBioHub design | Integration failure | May 2025 |
| [#638](https://github.com/MyersResearchGroup/iBioSim/issues/638) | Unable to run iBioSim 3.2.0 on Mac | Cross-platform | May 2025 |
| [#637](https://github.com/MyersResearchGroup/iBioSim/issues/637) | Unable to generate models (NoClassDefFoundError: Apache Jena/Xerces) | Bug — Java dependency | Jan 2025 |
| [#635](https://github.com/MyersResearchGroup/iBioSim/issues/635) | Cannot open iBioSim on Windows 11 | Cross-platform | Jan 2025 |
| [#632](https://github.com/MyersResearchGroup/iBioSim/issues/632) | Can't connect to LCP Synbiohub | Integration failure | Apr 2024 |

**Key error from #637 (most discussed):**
```
java.lang.NoClassDefFoundError: Could not initialize class org.apache.jena.query.ARQ
Caused by: java.lang.NoClassDefFoundError: org/apache/xerces/util/XMLChar
```
A transitive dependency conflict — Apache Jena can't initialize because Xerces is missing or conflicting.

**Takeaway:** Desktop-based synbio CAD tools struggle with **Java dependency management and OS-specific behavior**. iBioSim's 305+ open issues and its broken SynBioHub integration (#639, #632) are a direct consequence of the v1 SynBioHub's aging API. When v3 launches with a proper Swagger API (#1106), this integration story may finally improve. This signals a strong opportunity for containerized or web-based alternatives.

---

#### 10. DnaChisel (281 ⭐) — The Python-First DNA Optimizer

**Scope:** Python library for optimizing DNA sequences with respect to constraints and objectives. 15+ classes of sequence specifications: codon-optimization, GC-content tuning, restriction site avoidance, homology removal, and more. Part of the EGF Codons suite from the Edinburgh Genome Foundry.

**Current Open Issues:**

| Issue | Title | Theme | Date |
|---|---|---|---|
| [#114](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/114) | Produce multiple different optimized results | Feature — diversity in output | Jun 2026 |
| [#113](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/113) | Low Codon Adaptation Index on optimized sequence | Bug — optimization quality | May 2026 |
| [#111](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/111) | Unexpected Mutation of `codon_usage_table` During Optimization | Bug — data integrity | Apr 2026 |
| [#110](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/110) | Minimize CG | Feature — GC content optimization | Apr 2026 |
| [#107](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/107) | Support for Uridine Depletion (UD) optimization objectives | Feature — new target (5 comments) | Apr 2026 |
| [#102](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/102) | Feature: PDF report generation optional during optimize_with_report | Enhancement | Jul 2025 |
| [#100](https://github.com/Edinburgh-Genome-Foundry/DnaChisel/issues/100) | How to get under-optimal sequences during optimization? | Question — fitness landscape | May 2025 |

**Takeaway:** Users want to **explore the fitness landscape**, not just find the single best sequence. The `codon_usage_table` mutation bug (#111) is concerning because it could silently produce incorrect optimization results. The UD optimization request (#107, 5 comments) and GC minimization (#110) show that the community is pushing DnaChisel toward chemistry-aware targets (making DNA invisible to degradation pathways). The missing CONTRIBUTING docs (#105) hint that the maintainer is a solo academic struggling to absorb community contributions.

---

#### 11. Coral (32 ⭐) — Design-as-Code for Synthetic Biology

**Scope:** Python library for encoding the process of designing synthetic DNA constructs. Mirrors traditional GUI-based design steps (ApE, j5, Benchling) as operations on data structures. Enables iterative design through analysis modules. MIT license. Stack: Python (works with PyPy + numpy), Biopython.

**Current Open Issues:** Only 1 open issue ([#37](https://github.com/klavinslab/coral/issues/37) — Ubuntu 22.04 Python 3 compatibility). Actively maintained, recent updates (June 2026).

**Takeaway:** Coral is a rare example of a **well-maintained, open-source Python library** for synbio design automation. It's a great reference for how to structure design-as-code workflows.

---

### 📊 Metagenomics & Bioinformatics Pipeline Tools

Beyond synthetic biology-specific tools, the broader biotech software ecosystem includes a robust set of metagenomics and bioinformatics pipelines essential for anyone working with sequencing data:

| Tool | ⭐ Stars | Language | Category | Link |
|---|---|---|---|---|
| **MEGAHIT** | 727 | C++ | Metagenome assembly | [voutcn/megahit](https://github.com/voutcn/megahit) |
| **Sourmash** | 557 | Python+Rust | K-mer comparison & metagenomic profiling | [sourmash-bio/sourmash](https://github.com/sourmash-bio/sourmash) |
| **DeepVariant** | 3,807 | Python | Variant calling (CNN-based) | [google/deepvariant](https://github.com/google/deepvariant) |
| **Kaiju** | 307 | C | Taxonomic classification (protein DB) | [bioinformatics-centre/kaiju](https://github.com/bioinformatics-centre/kaiju) |
| **KrakenUniq** | 253 | C++ | Metagenomics classifier (unique k-mer) | [fbreitwieser/krakenuniq](https://github.com/fbreitwieser/krakenuniq) |
| **MetaEuk** | 211 | C | Gene discovery & annotation (eukaryotic) | [soedinglab/metaeuk](https://github.com/soedinglab/metaeuk) |
| **SemiBin** | 175 | Python | Metagenome binning (self-supervised DL) | [BigDataBiology/SemiBin](https://github.com/BigDataBiology/SemiBin) |
| **Decontam** | 176 | R | Contaminant removal in marker-gene data | [benjjneb/decontam](https://github.com/benjjneb/decontam) |
| **SingleM** | 195 | Python | Novelty-inclusive community profiling | [wwood/singlem](https://github.com/wwood/singlem) |

**Key issues across metagenomics tools:**

- **MEGAHIT:** Terabase-scale assembly requests (#390), macOS threading bug (#385), possible project dormancy (#384)
- **KrakenUniq:** Database build failures (#197, #195 — "2 days and going"), compiler compatibility with GCC 13 (#193), missing `uint32_t` include in newer GCC (#190)
- **SemiBin:** NaN errors in coverage computation (#211, #201, #204), v2.1.0 producing fewer bins than v2.0.2 (#212), long runtimes (#200)
- **Sourmash:** Database currency concerns (#3983), legacy RefSeq lineage mapping (#3980)

> **Takeaway:** The metagenomics pipeline community faces two parallel challenges: (1) scaling to ever-larger datasets (terabase assemblies, database builds taking days), and (2) maintaining compatibility across evolving compiler ecosystems and reference databases. NaN-related issues in SemiBin suggest that deep learning approaches in metagenomics still have numerical stability problems that need attention.

---

### 📊 Emerging Themes from the Community

Based on open-issue triage across all surveyed projects, these are the themes dominating community attention right now:

| # | Theme | What It Means |
|---|---|---|
| 1 | **The SynBioHub Migration** | v1 is in maintenance mode with data-integrity bugs (OMEX exports broken, recursive downloads failing); v3 is a React+Spring Boot rewrite at 16 stars, not yet adopted by the community. The migration story is the central narrative of 2026 in synbio infrastructure. |
| 2 | **Interoperability & integration friction** | iBioSim can't upload to SynBioHub; OMEX exports miss SBML files; collection prefixes shift when changing visibility. The connected synbio toolchain is still hampered by format/URL/API mismatches. |
| 3 | **Data integrity in shared collections** | SubCollections not reporting members, recursive downloads not following links, legacy Virtuoso DB data piling up. Growing-pains for platforms hosting community-wide design registries. |
| 4 | **Long-standing UI bugs in academic tools** | GENtle2's 2014-era interaction bugs remain unfunded; a common pattern in academic tools that lose active maintainers. |
| 5 | **Cross-platform compatibility** | iBioSim's Mac and Windows 11 issues; SynBioHub3's OpenSSL 3 breaking Windows dev setup. Java "write once, run anywhere" remains aspirational. |
| 6 | **Optimization depth vs. usability** | DnaChisel users want to explore sub-optimal solutions (fitness landscapes), not just get the single best answer. New requests for UD optimization and GC minimization show the community pushing toward chemistry-aware design. A fundamental UX challenge in computational biology. |
| 7 | **Modern language adoption** | The success of **poly** (Go, 737⭐) and **DnaChisel** (Python, 281⭐) vs. aging Java tools (iBioSim, GENtle2) suggests the community is gravitating toward modern, fast, easy-to-deploy languages. Even SynBioHub is rewriting from Node.js+Virtuoso to React+Spring Boot. |
| 8 | **ML + sequence design convergence** | ART's ML for strain engineering, CASPIA's AI workflow orchestration, iBioSim's circuit design, DeepVariant's CNN-based variant calling, and the broader ecosystem point to an accelerating intersection of ML and biological design automation. |
| 9 | **Metagenomics scaling challenges** | MEGAHIT users pushing toward terabase-scale assemblies; KrakenUniq database builds taking days; SemiBin NaN errors suggesting numerical stability issues in deep learning approaches. The pipeline is maturing but hitting scalability walls. |
| 10 | **Stalled academic projects** | BiArkit, BIOFAB Studio, and SynBioCAD/biocad all show signs of dormancy. The "publish and abandon" pattern is prevalent in university synbio software. |
| 11 | **Tool governance & biological review** | poly's proposal for a "biological reviewers group" (#422) signals that the community is grappling with how to ensure biological accuracy of computationally designed constructs — a question that becomes urgent as design tools scale. |

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
│   ├── EP009-metagenomics-pipeline-scale/ # MEGAHIT, KrakenUniq, SemiBin scaling challenges
│   ├── EP010-deepvariant-variant-calling/ # Deep learning in clinical genomics
│   └── ...
├── research/
│   ├── synbio-tools-survey-2026-09.md     # Full survey data
│   ├── community-issues-snapshot-2026-09.md # Curated issue list
│   ├── synbiohub-migration-analysis.md    # v1→v3 rewrite deep dive
│   ├── poly-tool-analysis.md             # Go-native toolkit analysis
│   ├── metagenomics-pipeline-analysis.md  # MEGAHIT, KrakenUniq, SemiBin
│   ├── deepvariant-analysis.md            # DeepVariant & variant calling
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

### Synthetic Biology Tools & Platforms

| Resource | Link | Stars |
|---|---|---|
| [SynBioHub v1](https://synbiohub.org) | [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) | 84 |
| [SynBioHub v3](https://github.com/SynBioHub/synbiohub3) | [SynBioHub/synbiohub3](https://github.com/SynBioHub/synbiohub3) | 16 |
| [poly](https://github.com/bebop/poly) | [bebop/poly](https://github.com/bebop/poly) | 737 |
| [iBioSim](http://www.ibiosim.org/) | [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) | 67 |
| [DnaChisel](https://edinburgh-genome-foundry.github.io/DnaChisel/) | [EGF/DnaChisel](https://github.com/Edinburgh-Genome-Foundry/DnaChisel) | 281 |
| [GENtle2](https://synbiota.com) | [Synbiota/GENtle2](https://github.com/Synbiota/GENtle2) | 106 |
| [Coral](https://github.com/klavinslab/coral) | [klavinslab/coral](https://github.com/klavinslab/coral) | 32 |
| [act](https://github.com/20n/act) | [20n/act](https://github.com/20n/act) | 92 |
| [CASPIA](https://github.com/shenmaa233/SJTU-software-CASPIA) | [shenmaa233/SJTU-software-CASPIA](https://github.com/shenmaa233/SJTU-software-CASPIA) | 13 |
| [SyMBac](https://github.com/georgeoshardo/SyMBac) | [georgeoshardo/SyMBac](https://github.com/georgeoshardo/SyMBac) | 23 |
| [ART](https://github.com/JBEI/ART) | [JBEI/ART](https://github.com/JBEI/ART) | 66 |
| [ClothoBiofabEdition](https://github.com/BIOFAB/ClothoBiofabEdition) | [BIOFAB/ClothoBiofabEdition](https://github.com/BIOFAB/ClothoBiofabEdition) | 9 |
| [ToeholdSwitchDesign](https://github.com/SASTRA-iGEM2019/ToeholdSwitchDesign) | [SASTRA-iGEM2019/ToeholdSwitchDesign](https://github.com/SASTRA-iGEM2019/ToeholdSwitchDesign) | — |

### Metagenomics & Bioinformatics Pipelines

| Resource | Link | Stars |
|---|---|---|
| [DeepVariant](https://github.com/google/deepvariant) | [google/deepvariant](https://github.com/google/deepvariant) | 3,807 |
| [MEGAHIT](https://github.com/voutcn/megahit) | [voutcn/megahit](https://github.com/voutcn/megahit) | 727 |
| [Sourmash](https://github.com/sourmash-bio/sourmash) | [sourmash-bio/sourmash](https://github.com/sourmash-bio/sourmash) | 557 |
| [Kaiju](https://github.com/bioinformatics-centre/kaiju) | [bioinformatics-centre/kaiju](https://github.com/bioinformatics-centre/kaiju) | 307 |
| [KrakenUniq](https://github.com/fbreitwieser/krakenuniq) | [fbreitwieser/krakenuniq](https://github.com/fbreitwieser/krakenuniq) | 253 |
| [MetaEuk](https://github.com/soedinglab/metaeuk) | [soedinglab/metaeuk](https://github.com/soedinglab/metaeuk) | 211 |
| [SemiBin](https://github.com/BigDataBiology/SemiBin) | [BigDataBiology/SemiBin](https://github.com/BigDataBiology/SemiBin) | 175 |

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
| [CASPIA Wiki (iGEM 2025)](https://2025.igem.wiki/sjtu-software/) | Team SJTU-Software project wiki | — |

### Organizations to Follow

- **SynBioHub** — Primary design-sharing platform & SBOL standards (v1 maintenance, v3 rewrite)
- **SynBioDex** — SBOL specification & related tools
- **Edinburgh Genome Foundry** — DnaChisel & EGF Codons suite
- **Myers Research Group** — iBioSim (academic CAD tool)
- **JBEI** — ART for strain engineering
- **20n** — Commercial bioengineering (act platform)
- **klavinslab** — Coral design framework
- **BIOFAB** — Early web-based synbio CAD tools
- **Google Genomics** — DeepVariant & DeepTrio
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

*Last research update: September 2026 — Surveyed 25+ GitHub projects across synthetic biology, metagenomics, and bioinformatics; reviewed 50+ open issues spanning 15 repositories; compiled community themes across 11 categories; documented the SynBioHub v1→v3 migration, poly (Go toolkit), DnaChisel optimization landscape, CASPIA's AI-native platform, SyMBac's synthetic image generation, and the metagenomics pipeline scaling challenges. Research sources: GitHub issue trackers, repository READMEs, commit histories, and community documentation.*