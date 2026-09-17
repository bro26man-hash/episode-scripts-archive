# 🎬 Episode Scripts Archive

A curated archive for storing episode scripts, source materials, research notes, and community findings related to **synthetic biology** and **biotech software tools**. This repository serves as a reference library for anyone producing educational or research content about the synbio/biotech ecosystem — capturing the tools, standards, communities, and open questions that define the field.

> **Research compiled:** September 2026 | **Sources:** GitHub issue triage, repository analysis, and community documentation across 15+ active synbio/biotech open-source projects.

---

## 📁 Purpose

This archive exists to:

- **Document** the synthetic biology and biotech software landscape as it evolves
- **Preserve** episode scripts and source materials tied to specific tools, standards, and research projects
- **Connect** content creators with the active open-source communities and their current concerns
- **Serve as a starting point** for anyone wanting to understand what the synbio community is building and struggling with
- **Anchor research** — every episode note ties back to real, live open-source projects and the concerns bubbling up in their issue trackers

---

## 🔬 Key Synbio & Biotech Tools & Communities

Below are the most active open-source projects identified during research, along with the issues the community is currently focused on.

### 🏆 Landscape Overview

| Project | Stars | Language | What it does | Link |
|---|---|---|---|---|
| **synthetichealth/synthea** | 3,342 | Java | Synthetic patient population simulator for EHR modeling & health analytics | [link](https://github.com/synthetichealth/synthea) |
| **mims-harvard/TDC** | 1,283 | Jupyter | Therapeutics Data Commons — multimodal ML foundation for drug discovery | [link](https://github.com/mims-harvard/TDC) |
| **websemantics/awesome-synthetic-biology** | 223 | — | Curated directory of synbio projects, articles, resources & standards | [link](https://github.com/websemantics/awesome-synthetic-biology) |
| **virtualramblas/awesome-deep-learning-4-life-sciences** | 167 | — | Curated list of deep-learning resources for biotech & pharma | [link](https://github.com/virtualramblas/awesome-deep-learning-4-life-sciences) |
| **GENtle2** | 105 | JavaScript | Web-based DNA editor for synthetic biology | [Synbiota/GENtle2](https://github.com/Synbiota/GENtle2) |
| **20n/act** | 92 | Java/Scala | Predictive bioengineering — discovers DNA routes to make target chemicals | [link](https://github.com/20n/act) |
| **SynBioHub** | 84 | JavaScript/Java | Web platform for browsing, uploading & sharing synthetic biology designs | [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) |
| **dportik/Biotech-Job-Search-Engine** | 81 | Python | Open-source job-discovery for biotech, genomics & bioinformatics roles | [link](https://github.com/dportik/Biotech-Job-Search-Engine) |
| **JBEI/ART** | 66 | Jupyter | ML tool to improve strain engineering effectiveness | [link](https://github.com/JBEI/ART) |
| **MyersResearchGroup/iBioSim** | 67 | Java | CAD for genetic circuits; SBML/SBOL support | [link](https://github.com/MyersResearchGroup/iBioSim) |
| **chaibio/chaipcr** | 96 | C++ | Software behind Chai's open-source Real-Time PCR instrument | [link](https://github.com/chaibio/chaipcr) |
| **Autodesk/bionano-wetLabAccelerator** | 32 | JavaScript | Designs robotic wet-lab protocols via visual UI (no coding) | [link](https://github.com/Autodesk/bionano-wetLabAccelerator) |
| **klavinslab/coral** | 32 | Python | Library & framework for specifying synbio design processes | [link](https://github.com/klavinslab/coral) |
| **SynBioDex/libSBOLj** | 43 | Java | Java library for the Synthetic Biology Open Language (SBOL) | [link](https://github.com/SynBioDex/libSBOLj) |
| **Sheffield-iGEM/syn-zeug** | 7 | Rust | A modern toolbox for synthetic biology (sequence operations, ORF finding, etc.) | [link](https://github.com/Sheffield-iGEM/syn-zeug) |
| **SynBioDex/sboljs3** | 7 | TypeScript | SBOL library for TypeScript/JavaScript applications (browser & Node.js) | [link](https://github.com/SynBioDex/sboljs3) |
| **SynBioCAD/biocad** | 16 | JavaScript | Web-based CAD tool for synthetic biology built on SBOL standard | [link](https://github.com/SynBioCAD/biocad) |

---

### 🧬 In-Depth: Most Active Repos & Current Community Concerns

#### 1. synthetichealth/synthea — Synthetic Patient Population Simulator (3,342 ⭐)

The largest project in this survey. Synthea generates synthetic patient populations and corresponding electronic health records (EHRs) for research, benchmarking, and software testing. It models demographics, comorbidities, medications, labs, and clinical encounters using a modular, parameterized architecture.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #1700 | Proposal: stable de-identified export manifest for downstream benchmarks | Feature — standardization for benchmarking |
| #1703 | CSV SYSTEM column depends on whether FHIR export is enabled | Bug — data consistency across export formats |
| #1702 | FHIR R4 allergy export loses reaction severity by mutating a HashMap key | Bug — data corruption in FHIR export |
| #1365 | US Core 3.1 | Feature — compliance with latest US Core FHIR spec |

> **Takeaway:** The community is focused on **data consistency across export formats** (CSV vs FHIR), **standardization for benchmarking** (stable export manifests), and **regulatory compliance** (US Core 3.1). The HashMap key mutation bug (#1702) silently corrupts allergy reaction severity data in FHIR R4 exports — a serious data-integrity concern.

#### 2. mims-harvard/TDC — Therapeutics Data Commons (1,283 ⭐)

The largest AI-for-drug-discovery project. TDC provides ready-to-use datasets, data functions, leaderboards, and benchmarks for ML-driven drug discovery across therapeutic modalities.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #399 | Leaderboard submission for Catalyst-V4-Turbo (ADMET Group 22/22) | Benchmark — active community participation |
| #394 | Score discrepancy and data contamination in Bioavailability_Ma leaderboard | Bug — data integrity in benchmarks |
| #392 | `convert_y_unit` applies p-to-nM conversion twice; nM-to-p is incorrect | Bug — unit-conversion logic |
| #390 | Buchwald-Hartwig dataset size mismatch | Bug — dataset curation |
| #389 | Dataset download failed | Infra — Dataverse availability |
| #387 | Question about mixing Hepatocyte clearance datasets (rat vs human) | Data — cross-species consistency |
| #386 | Pip install fails: "Compiler cl cannot compile programs" | DevOps — Windows build environment |

> **Takeaway:** TDC has a vibrant, active community. Issues range from data curation bugs and unit-conversion errors to cross-species dataset mixing questions. The reliance on Harvard Dataverse for dataset hosting introduces a single point of failure.

#### 3. SynBioHub — Design Sharing Platform (84 ⭐)

The community's primary web-based repository for sharing synthetic biology designs, supporting SBOL import/export. It hosts the complete iGEM Registry of Standard Biological Parts via a public instance at synbiohub.org. Stack: JavaScript (Node.js) + Java (Maven) + OpenLink Virtuoso (RDF triplestore).

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #1756 | SubCollections does not report members in public graph | Bug — data integrity in shared collections |
| #1755 | Recursive download does not follow linked collections | Bug — user workflow gap |
| #1754 | Legacy data in Virtuoso should be deleted | Maintenance — technical debt from DB migrations |
| #1753 | OMEX download missing SBML file (only downloads SBOL) | Bug — export completeness |
| #1752 | Changing private collection to public shifts prefix from `localhost:3333` to `synbiohub.org` | Bug — deployment/shareability friction |

> **Takeaway:** The community is focused on **data integrity** (collections, exports), **technical-debt cleanup** (legacy DB data), and **deployment friction** (prefix/URL issues when sharing local designs publicly). These are classic growing-pains for a platform bridging academic research and real-world deployment.

#### 4. 20n/act — Predictive Bioengineering (92 ⭐)

A platform for **computational synthetic biology** that predicts DNA insertions into cells that modify the cell to produce a target molecule via fermentation. It famously predicted the first bio-route to Acetaminophen. The stack includes: predictive modeling (reaction-operator inference, SAR, reachables computation, cascade enumeration, DNA design), analytics (LCMS untargeted metabolomics via deep learning), and unit-economics modeling for bioproduction.

**Recent open issues:** No open issues — suggesting the project is in a stable, production-ready state with the core predictive pipeline considered finished. Contact is required for enterprise licensing.

> **Takeaway:** The sheer scope of the platform (10+ modules from NLP to patent search to cost modeling) makes it one of the most ambitious open-source bioengineering projects, but it also means the community is small and enterprise-oriented rather than broadly contributor-friendly.

#### 5. iBioSim — CAD for Genetic Circuits (67 ⭐)

A CAD tool for modeling, analysis, and design of genetic circuits, with full SBML (all levels/versions) and SBOL support. Includes multi-cellular and spatial modeling support. Developed by the Myers Research Group at the University of Utah. Stack: Java + libSBML + reb2sac + GeneNet + Yosys.

**Recent open issues (most recent, sorted by update date):**

| Issue | Summary | Theme |
|---|---|---|
| #640 | A Java exception has occurred | Stability / runtime |
| #639 | Can't upload SynBioHub design | Integration with design-sharing platforms |
| #638 | Unable to run iBioSim 3.2.0 on Mac | Cross-platform compatibility |
| #637 | Unable to generate models automatically (NoClassDefFoundError: Apache Jena/Xerces) | Java dependency conflict |
| #635 | I cannot open iBioSim on Windows 11 | Cross-platform compatibility |
| #634 | Bug importing file and when starting iBioSim | Import/startup crash |
| #632 | Can't connect to LCP Synbiohub | SynBioHub connection handshake failure |
| #631 | Problem with External Components | External component integration |
| #629 | sbml2prism conversion bug | Conversion tool bug (assigned to dev) |

**Key error from #637 (most discussed):**
```
java.lang.NoClassDefFoundError: Could not initialize class org.apache.jena.query.ARQ
Caused by: java.lang.NoClassDefFoundError: org/apache/xerces/util/XMLChar
```
This is a transitive dependency conflict — Apache Jena can't initialize because Xerces is missing or conflicting. Users hit this when trying to generate models from SBOL designs via SynBioHub integration.

> **Takeaway:** Issues center on **cross-platform compatibility** (Mac, Windows 11), **runtime stability** (Java exceptions), **interoperability with SynBioHub** (upload failures, connection handshakes), and **Java dependency management** (Apache Jena/Xerces conflict). This reinforces a key theme: synbio CAD tools struggle with smooth integration across the networked ecosystem.

#### 6. GENtle2 — Web DNA Editor (105 ⭐)

A re-thought-for-the-web version of the classic GENtle desktop DNA editor. Core features are being extracted into modules. Stack: JavaScript (Node.js + Express + Gulp).

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #253 | Jumping annotations | UI bug (open since 2015) |
| #252 | Anchor and Cap selections won't change | UI bug (open since 2015) |
| #251 | Spacing button doesn't work | UI bug (open since 2015) |
| #250 | BLAST show button doesn't do anything | UI / integration bug (open since 2015) |
| #247 | sequenceModel should validate stickyEnds | Improvement (open since 2015) |

> **Takeaway:** These issues are very old (created 2015) and point to long-standing UI interaction bugs that haven't been addressed — a common pattern in academic tools that lose active maintainers. The project is still listed as "in development" with recent updates, but the open issues suggest a gap between roadmap and bug triage.

#### 7. libSBOLj — SBOL Java Library (43 ⭐)

The reference Java implementation for the Synthetic Biology Open Language (SBOL). Provides core interfaces and implementation for SBOL objects, read/write SBOL documents as XML/RDF, and a validator for checking the correctness of SBOL models. Underpins many other tools in the ecosystem.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #623 | Opaque failure while reading GenBank | Bug — unclear error messages when parsing malformed GenBank files |
| #621 | Invalid reporting of error sbol-11003 | Bug — validation error reporting is incorrect/misleading |
| #620 | displayID truncation in LOCUS field of GenBank conversions | Bug — data loss during format conversion |

> **Takeaway:** All three open issues center on **GenBank format handling** — parsing failures with poor error messages, validation error codes that don't accurately describe the problem, and data truncation during conversion. Since libSBOLj is the reference implementation for SBOL, bugs here ripple across the entire ecosystem.

#### 8. SynBioDex/sboljs3 — SBOL TypeScript Library (7 ⭐)

A library for the Synthetic Biology Open Language (SBOL) written in TypeScript, for JavaScript/TypeScript applications in the browser or Node.js. Built on [rdfoo](https://github.com/udp/rdfoo), a library for creating object-oriented RDF abstractions in TypeScript.

**Implemented:** Reading/writing SBOL1, SBOL2, SBOL3; converting between SBOL versions; reading FASTA and GenBank.
**Not implemented:** Writing FASTA and GenBank; validation.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #22 | Publish a new version with the latest commit | Release management |
| #21 | Node package | Packaging/distribution |
| #20 | SBOL 3->2: access is not set on ComponentInstance objects | Conversion bug |
| #17 | sbolgraph cannot handle CombinatorialDerivation objects | Conversion bug (10 comments — active discussion) |
| #16 | SBOL 3->2 needs to remap sequence encodings and component types | Conversion bug |
| #14 | SBOL 2->3 conversion errors | Conversion bug |
| #15 | SBOL 3->2 conversion loses Activities | Conversion bug |

> **Takeaway:** The community is actively working on **SBOL version conversion** — the bugs in 3->2 and 2->3 conversion are numerous and well-discussed. This signals that while the SBOL standard exists, the tooling for reliable bidirectional conversion between versions is still maturing.

#### 9. Sheffield-iGEM/syn-zeug — Modern Rust Toolbox for Synbio (7 ⭐)

A modern toolbox for synthetic biology, written in Rust with a Svelte web UI. Includes sequence validation, reverse complement, GC content, ORF finding, DNA→RNA→Protein conversion, Hamming/Levenshtein distance, and more. Also provides a WASM interface via `biobox`.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #47 | Find ORFs In Proteins | Feature request |
| #46 | Upstream `rust-bio` changes | Dependency tracking |
| #42 | Miscellaneous Tools | Feature request |
| #39 | Add information about selected regions of sequence (like Benchling) | UX feature |
| #38 | Pause a tool in the pipeline | UX feature |
| #37 | Add nice looking tooltips! | UX improvement |
| #36 | Add dragging for building up a pipeline | UX feature |
| #25 | Look Into WebAssembly Features for Improving Performance | Performance |
| #26 | Implement New Tool: "Percent Composition" | Feature request |

> **Takeaway:** A vibrant, actively-developed modern tool with clear issue labels (enhancement, tool, basic, performance). The community is focused on **building out the toolset**, **improving UX**, and **performance optimization via WASM**. This is one of the few synbio projects with a clear roadmap and active contribution workflow.

---

### 📚 Learning & Resource Hubs

| Project | Stars | Description | Link |
|---|---|---|---|
| **websemantics/awesome-synthetic-biology** | 223 | Curated list of synbio projects, articles, resources & standards | [link](https://github.com/websemantics/awesome-synthetic-biology) |
| **virtualramblas/awesome-deep-learning-4-life-sciences** | 167 | Deep learning resources for life sciences (biotech & pharma focus) | [link](https://github.com/virtualramblas/awesome-deep-learning-4-life-sciences) |
| **llSourcell/Learn_Synthetic_Biology** | 157 | Educational resources for getting started in synbio | [link](https://github.com/llSourcell/Learn_Synthetic_Biology) |
| **PackTPublishing/Machine-Learning-in-Biotechnology** | 106 | ML in biotechnology using Python | [link](https://github.com/PackTPublishing/Machine-Learning-in-Biotechnology-and-Life-Sciences) |
| **robertosolari/BioTech-Resources** | 16 | Resources for learning biotech, biology, synbio, genomics & bioinformatics | [link](https://github.com/robertosolari/BioTech-Resources) |
| **xielab2017/Bioinformatics_SUAT_2026_FALL** | 16 | Bioinformatics course from the Faculty of Synthetic Biology at Shenzhen University | [link](https://github.com/xielab2017/Bioinformatics_SUAT_2026_FALL) |

---

## 🌐 What the Community Is Currently Working On & Concerned About

Based on recent open issues across the top projects, here are the themes dominating community attention:

### 1. Interoperability & Integration Friction

The **#1 issue** across the ecosystem. iBioSim can't upload to SynBioHub (#639), OMEX exports miss SBML files (#1753), collection prefixes shift when changing visibility (#1752), and SBOL version conversion has numerous bugs (sboljs3 issues #14–#20). The dream of a connected synbio toolchain is still hampered by format/URL/API mismatches.

### 2. Data Integrity in Shared Collections

SynBioHub's open issues (#1756, #1755, #1754) reveal a platform dealing with **growing pains**: sub-collections not reporting members, recursive downloads not following links, and legacy database data piling up. As the community's design registry scales, these data-integrity issues become critical.

### 3. Cross-Platform Compatibility

iBioSim's Mac issue (#638) and Windows 11 issue (#635) are not isolated. The **"Java write once, run anywhere"** ideal is aspirational, not guaranteed. Desktop-based synbio CAD tools struggle with OS-specific behavior, signaling a strong opportunity for containerized or web-native alternatives.

### 4. Long-standing UI Bugs in Academic Tools

GENtle2's 2015-era interaction bugs remain unfixed; SynBioCAD/biocad's 2019-era UI issues persist. A common pattern in academic tools that lose active maintainers. The community is waiting for modernized, web-native replacements.

### 5. SBOL Standards Maturation

Both libSBOLj (Java) and sboljs3 (TypeScript) have open issues centered on **format conversion bugs**, **GenBank parsing failures**, and **validation error reporting**. The SBOL standard itself is well-defined, but the tooling for reliable format conversion and validation is still maturing.

### 6. ML + Biological Design Convergence

- **ART** (JBEI): Provides probabilistic strain recommendations using MCMC sampling and Bayesian optimization — a paradigm shift from trial-and-error to computational-directed metabolic engineering
- **20n/act**: Demonstrates end-to-end DNA design automation, having predicted the first bio-route to acetaminophen
- **TDC** (mims-harvard): Provides ML benchmarks for drug discovery across therapeutic modalities
- **Synthea**: Generates synthetic patient populations for health analytics

> **Takeaway:** The field is moving from manual, intuition-driven engineering toward computational, ML-augmented design pipelines. However, ART's code is private, 20n/act is internally maintained, and TDC is benchmark-focused — there's a gap for open-source, community-friendly ML design tools.

### 7. Deployment & DevOps Gaps

SynBioHub requires Virtuoso (RDF triplestore), Maven, Node, and Docker — a complex deployment stack. iBioSim requires libSBML, reb2sac, GeneNet, and Yosys as separate binaries. These barriers push away potential contributors and users who just want to run the tool.

### 8. Stalled Academic Projects

BiArkit, BIOFAB Studio, and SynBioCAD/biocad all show signs of dormancy with zero open issues but no active maintenance. The **"publish and abandon"** pattern is prevalent in university synbio software — projects ship a proof-of-concept, get published, and then lose community engagement.

### 9. Open Hardware vs. Open Software Divide

Chai Bio released qPCR software as open source (chaipcr, 96 stars) but keeps hardware schematics closed (issue #44 still open). This reveals a gap in the open-science philosophy when commercial interests are involved.

### 10. Information Overload & Literature Tracking

The explosion of daily ArXiv/bioRxiv preprints in ML-for-biology has created demand for automated paper digests, filtering tools, and prioritized reading lists. Multiple community-maintained daily-paper repos indicate this is a real pain point.

---

## 🏛️ Key Organizations & Communities

| Organization | What they do | Key projects |
|---|---|---|
| **SynBioHub** | Maintains the primary design-sharing platform and SBOL Java library | SynBioHub, libSBOLj |
| **SynBioDex** | Publishes the SBOL specification and related tools | sboljs3, libSBOLj, SBOL-specification |
| **Myers Research Group** | Academic lab behind iBioSim; university synbio CAD efforts | iBioSim, reb2sac, GeneNet |
| **JBEI** (Joint BioEnergy Institute) | DOE-funded lab; produces ART for strain engineering | ART |
| **20n** | Startup that produced act; bridges academic research and commercial bioengineering | act |
| **Autodesk Bio/Nano/Protospace** | Big-design-interest in synbio protocol automation | bionano-wetLabAccelerator |
| **klavinslab** (UW) | Contributes Coral framework for synbio design processes | Coral |
| **MIMS/Harvard** (Marinka Zitnik's lab) | Produces TDC; largest community in therapeutics ML | TDC |
| **synthetichealth** | Produces Synthea; largest synbio-adjacent project by stars | Synthea |
| **Chai Bio** | Produces chaipcr; open-hardware science instrumentation (with limitations) | chaipcr |
| **websemantics** | Curates the awesome-synthetic-biology list; community front door | awesome-synthetic-biology |
| **BIOFAB** | Early contributor to web-based synbio CAD tools | BIOFAB/Studio |
| **Sheffield-iGEM** | Student team producing modern Rust-based synbio tools | syn-zeug |

---

## 📂 Repository Structure

```
episode-scripts-archive/
├── episodes/
│   ├── EPXXX-title/
│   │   ├── script.md
│   │   ├── sources.md
│   │   └── assets/
│   └── ...
├── research/
│   ├── synbio-tools-survey-2026-09.md
│   ├── community-issues-snapshot-2026-09.md
│   └── ...
├── source-materials/
│   ├── presentations/
│   ├── datasets/
│   └── references/
├── templates/
│   ├── episode-script-template.md
│   └── sources-template.md
└── README.md
```

---

## 🔗 Quick Reference Links

| Resource | URL |
|---|---|
| SynBioHub (hosted platform) | https://synbiohub.org |
| SynBioHub Wiki | https://wiki.synbiohub.org |
| 20n/act Wiki | https://github.com/20n/act/wiki |
| Therapeutics Data Commons | https://tdcommons.ai |
| Synthea | https://synthetichealth.github.io/synthea/ |
| iBioSim | http://www.ibiosim.org/ |
| SBOL Specification | https://sbolstandard.org/ |
| GENtle2 | https://synbiota.com |
| Autodesk Wet Lab Accelerator | https://wla.bionano.autodesk.com |

---

## 📜 Related Communities & Links

- [SynBioHub](https://synbiohub.org) — Design repository & sharing platform
- [Addgene](https://www.addgene.org) — Nonprofit plasmid repository
- [iGEM Registry](http://parts.igem.org) — Standard Biological Parts
- [SBOL Standard](https://sbolstandard.org) — Synthetic Biology Open Language
- [SBML](https://sbml.org) — Systems Biology Markup Language
- [BioModels](https://www.ebi.ac.uk/biomodels) — Database of mathematical models
- [3DuF](https://3duf.org) — Open-source microfluidics design tool
- [BioHackAcademy](https://biohackacademy.github.io) — Community hardware/course platform
- [SynBioBeta](https://www.synbiobeta.com) — Synthetic biology community & conference
- [awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) — Curated list of all things synbio

---

## 🤝 Contributing

Contributions are welcome! To add materials:

1. Fork this repository
2. Create a new branch for your episode or addition (`git checkout -b episode-01-genome-editing`)
3. Add your scripts, source materials, or transcripts under the appropriate directory
4. Submit a pull request with a clear description of the content and its sources

When adding research findings:
- Reference the specific GitHub issues and PRs you consulted
- Note the date of your research snapshot
- Include links to all relevant repositories and discussions

---

## 📄 License

This archive is released under the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/), same as the awesome-synthetic-biology list. Individual episode scripts may carry their own licenses — check each episode directory for details.

---

*This archive was compiled from active GitHub research on the synthetic biology and biotech software ecosystem, capturing the tools, standards, and community concerns as of September 2026. Research methodology: repository search, star-ranked analysis, open-issue triage across 15+ projects, and detailed issue inspection of 30+ high-priority bugs across SynBioHub, iBioSim, GENtle2, libSBOLj, sboljs3, synthea, TDC, and more.*