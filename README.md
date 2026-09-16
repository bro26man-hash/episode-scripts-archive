# 🎬 Episode Scripts Archive

A curated archive for storing episode scripts, source materials, research notes, and community discussions — with a dedicated focus on **synthetic biology (synbio)**, **biotech software tools**, and the open-source communities building them.

---

## 📁 Repository Purpose

This archive serves as a centralized, version-controlled home for:

- **Episode scripts** — full write-ups and outlines for episodes covering science, technology, and open-source topics
- **Source materials** — research notes, citations, GitHub issue threads, and community discussions consulted during episode prep
- **Reference links** — curated pointers to key projects, papers, and communities
- **Background research** — snapshots of the open-source landscape at the time of each episode's production

---

## 🔬 Synthetic Biology & Biotech Software Tools Landscape (September 2026)

The following open-source projects represent the active frontier of computational synthetic biology and bioinformatics tooling on GitHub. Each project's open issues were surveyed to understand what the community is currently concerned about or working on.

---

### 🏆 Top-Tier Synbio Tools

#### 1. [PyLabRobot — PyLabRobot/pylabrobot](https://github.com/PyLabRobot/pylabrobot) ⭐ 533 | `Python` | `MIT`
**Hardware-agnostic SDK for lab automation.** PyLabRobot provides a universal Python interface for liquid handling robots (Hamilton STAR, Opentrons OT-2, Tecan Freedom EVO), plate readers, centrifuges, pumps, scales, heater shakers, and thermocyclers. Developed at the MIT Media Lab's Sculpting Evolution Group.

**Recent open issues / community focus:**
- **NanoDrop 1000 compatibility** — restoring macOS support, measuring both optical paths, averaging, crash-safe teardown (PR #1270)
- **New instrument support** — Biotek Multiflo, MultiFloFX, and 405TS (PR #1266); EL406 improvements
- **Hardware testing infrastructure** — new device testing page and reporting process (PR #1264)
- **Trash resource guide** — better documentation for waste handling in protocols (PR #1263)

> **Takeaway:** The community is rapidly expanding hardware support and hardening reliability — an active, well-maintained project with daily PR merges.

---

#### 2. [Synbiota/GENtle2](https://github.com/Synbiota/GENtle2) ⭐ 105 | `JavaScript`
**Web-based DNA editor for synthetic biology.** A complete rewrite of the classic GENtle desktop application, with core features being extracted into modular components.

**Recent open issues:**
- Long-standing UI bugs from 2015 still unfixed: jumping annotations, anchor/cap selection, spacing button, BLAST show button — suggesting limited maintainer bandwidth for UI polish.

> **Takeaway:** A promising web-native rewrite of a beloved tool, but plagued by decade-old interaction bugs that haven't been triaged — a common pattern in academic tools.

---

#### 3. [20n/act](https://github.com/20n/act) ⭐ 92 | `Java`
**Predictive bioengineering.** Predicts DNA insertions into *E. coli* and *S. cerevisiae* that modify cells to produce target molecules. Famously predicted the first bio-route to acetaminophen. The stack spans reaction-operator inference, SAR modeling, cascade enumeration, DNA design, LC-MS metabolomics via deep learning, and unit-economics modeling for bioproduction.

**Recent open issues:** None found — suggesting a stable, production-ready state. Enterprise licensing required for full database access.

> **Takeaway:** One of the most ambitious open-source bioengineering platforms, but its scope (10+ modules) means a small, enterprise-oriented contributor base rather than broad community engagement.

---

#### 4. [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) ⭐ 84 | `JavaScript`
**The community's primary design-sharing platform.** Enables users and software to browse, upload, and share synthetic biology designs with SBOL import/export. Hosts the complete iGEM Registry of Standard Biological Parts at synbiohub.org.

**Recent open issues (actively created in Sept 2026):**

| Issue | Summary | Theme |
|---|---|---|
| [#1756](https://github.com/SynBioHub/synbiohub/issues/1756) | SubCollections does not report members in public graph | Data integrity bug |
| [#1755](https://github.com/SynBioHub/synbiohub/issues/1755) | Recursive download does not follow linked collections | Workflow bug |
| [#1754](https://github.com/SynBioHub/synbiohub/issues/1754) | Legacy data in Virtuoso should be deleted | Technical debt from DB migrations |
| [#1753](https://github.com/SynBioHub/synbiohub/issues/1753) | OMEX download missing SBML file (downloads SBOL only) | Export completeness bug |
| [#1752](https://github.com/SynBioHub/synbiohub/issues/1752) | Visibility change shifts prefix from localhost:3333 to synbiohub.org | Deployment/friction bug |

> **Takeaway:** The community is grinding through **data integrity**, **export completeness**, and **deployment friction** — classic growing pains for a platform bridging academic research and real-world deployment.

---

#### 5. [JBEI/ART](https://github.com/JBEI/ART) ⭐ 66 | `Jupyter Notebook`
**ML tool for strain engineering.** Leverages machine learning and probabilistic modeling to guide metabolic engineering without full mechanistic understanding, using sampling-based optimization (MCMC). From the Joint BioEnergy Institute.

> **Takeaway:** Research-grade tool gated by academic licensing (non-commercial only, patent-pending). Limited open-source contributor accessibility.

---

#### 6. [chaibio/chaipcr](https://github.com/chaibio/chaipcr) ⭐ 96 | `C++`
**Open-source Real-Time PCR instrument software.** Powers Chai's line of qPCR thermocyclers (Open qPCR). Apache 2.0 licensed.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| [#105](https://github.com/chaibio/chaipcr/issues/105) | Website is down (origin unreachable) | Hosting/DevOps |
| [#104](https://github.com/chaibio/chaipcr/issues/104) | No screen after factory reset (device stuck) | Hardware/firmware bug |
| [#102](https://github.com/chaibio/chaipcr/issues/102) | Can't set up account after factory reset | User workflow |
| [#101](https://github.com/chaibio/chaipcr/issues/101) | PuTTY SSH access questions | DevOps/access |

> **Takeaway:** A passion project for open-source hardware, but maintenance seems thin — a website outage and a factory-reset bricking issue show the gap between open-source ideals and production-grade reliability.

---

### 🧬 Supporting Tools & Libraries

| Project | Stars | Language | Description | Community Concern |
|---|---|---|---|---|
| [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) | 67 | Java | CAD for genetic circuits; SBML/SBOL support | Java stability (exceptions), Mac compatibility, SynBioHub upload integration |
| [SynBioDex/libSBOLj](https://github.com/SynBioDex/libSBOLj) | 43 | Java | Java library for the Synthetic Biology Open Language | Maintaining compatibility with evolving SBOL spec |
| [Autodesk/bionano-wetLabAccelerator](https://github.com/Autodesk/bionano-wetLabAccelerator) | 32 | JavaScript | Visual designer for robotic wet-lab protocols | Bridging visual/no-code design with actual robot execution |
| [klavinslab/coral](https://github.com/klavinslab/coral) | 32 | Python | Framework for specifying synbio design processes | Academic maintenance, limited contributor base |
| [Gardner-BinfLab/TISIGNER-ReactJS](https://github.com/Gardner-BinfLab/TISIGNER-ReactJS) | 30 | JavaScript | Interactive synbio design tool | Niche tool with limited active development |
| [MyersResearchGroup/PartQualifier](https://github.com/MyersResearchGroup/PartQualifier) | — | Java | Sequence/file format conversion | Supporting multiple standards (SBOL, GenBank) |

---

### 🔬 Bioinformatics Infrastructure

| Project | Stars | Language | Description | Community Concern |
|---|---|---|---|---|
| [Biopython — biopython/biopython](https://github.com/biopython/biopython) | 5,070 | Python | Foundational Python toolkit for molecular biology | C++ acceleration for mmCIF parsing; SAM TLEN calculation bug |
| [Nextflow — nextflow-io/nextflow](https://github.com/nextflow-io/nextflow) | 3,412 | Groovy | DSL for data-driven computational pipelines | Lineage tracking bug (`TaskRun` omits cache inputs) — reproducibility concern |
| [Opentrons — Opentrons/opentrons](https://github.com/Opentrons/opentrons) | 503 | Python | Software for Opentrons OT-2/Flex robots | API evolution, hardware support expansion |
| [DeepVariant — google/deepvariant](https://github.com/google/deepvariant) | 3,726 | Python | Deep learning variant calling from NGS data | Ongoing model accuracy improvements |
| [nf-core/tools](https://github.com/nf-core/tools) | 320 | Python | Helper package for nf-core community | Pipeline maintenance across hundreds of community pipelines |
| [DnaFeaturesViewer](https://github.com/Edinburgh-Genome-Foundry/DnaFeaturesViewer) | 690 | Python | Plotting DNA sequence features from GenBank/GFF | GFF3 parser breakage (BCBio deprecated); multi-seq alignment viz requests |

---

### 🎓 Community Curated Lists & Resources

| Resource | Stars | Description |
|---|---|---|
| [websemantics/awesome-synthetic-biology](https://github.com/websemantics/awesome-synthetic-biology) | 223 | Curated list of synbio projects, articles, and resources |
| [danielecook/Awesome-Bioinformatics](https://github.com/danielecook/Awesome-Bioinformatics) | 4,098 | Comprehensive bioinformatics software list |
| [seandavi/awesome-single-cell](https://github.com/seandavi/awesome-single-cell) | 3,748 | Software & data resources for single-cell omics |
| [virtualramblas/awesome-deep-learning-4-life-sciences](https://github.com/virtualramblas/awesome-deep-learning-4-life-sciences) | 167 | Deep learning resources for biotech & pharma |
| [PacktPublishing/Machine-Learning-in-Biotechnology-and-Life-Sciences](https://github.com/PacktPublishing/Machine-Learning-in-Biotechnology-and-Life-Sciences) | 106 | ML in biotech course materials (Packt) |
| [dportik/Biotech-Job-Search-Engine](https://github.com/dportik/Biotech-Job-Search-Engine) | 80 | Open-source job discovery for biotech/genomics roles |

---

## 🌐 Key Themes Emerging from Community Issue Surveys

Based on the open issues surveyed across the projects above, the synbio/biotech open-source community is currently focused on:

1. **Interoperability & integration friction** — iBioSim can't upload to SynBioHub; OMEX exports miss SBML files; collection prefixes shift when changing visibility. The dream of a connected synbio toolchain is still hampered by format/URL/API mismatches.

2. **Data integrity in shared collections** — SubCollections not reporting members, recursive downloads not following links, legacy DB data piling up — these are growing pains for platforms that host community-wide design registries.

3. **Long-standing UI bugs in academic tools** — GENtle2's 2015-era interaction bugs remain unfixed, suggesting limited maintainer bandwidth for UI polish in favor of core algorithmic work.

4. **Parser reliability** — Both iBioSim's GenBank handling and DnaFeaturesViewer's GFF3 parser are dealing with fragile code as upstream dependencies shift or deprecate (e.g., BCBio ending active development).

5. **Production-grade DevOps gaps** — Chai PCR's website outage, SynBioHub's Virtuoso migration debris, and GENtle2's unfixed UI bugs all point to a pattern where academic tools are poorly maintained once the initial publication cycle ends.

6. **ML + sequence design convergence** — ART's ML for strain engineering, iBioSim's circuit design, and the broader bioinformatics toolchain (Biopython, DeepVariant, Nextflow) point to an accelerating intersection of machine learning and biological design automation.

7. **Reproducibility at scale** — Nextflow's lineage tracking bug highlights how critical cache and provenance tracking has become as pipelines grow more complex and outputs more data-intensive (AlphaFold2-scale structural datasets).

---

## 🏛️ Key Organizations & Communities

- **SynBioHub** — Maintains the primary design-sharing platform and the SBOL Java library (libSBOLj); hosts the iGEM Registry
- **SynBioDex** — Publishes the SBOL specification; community-driven standards effort
- **JBEI (Joint BioEnergy Institute)** — DOE-funded lab producing ART for strain engineering
- **20n** — Startup behind act; bridges academic research and commercial bioengineering
- **Autodesk Bio/Nano/Protospace** — Big-tech entry into synbio protocol automation
- **klavinslab (UW)** — Contributes Coral framework for synbio design processes
- **Edinburgh Genome Foundry** — Produces DnaFeaturesViewer, DnaChisel, and other widely-used Python tools for DNA design
- **Chai** — Open-source qPCR hardware company driving open-source instrumentation
- **Opentrons** — Leading open-source lab automation company
- **MIT Sculpting Evolution Group** — Behind PyLabRobot, pushing hardware-agnostic lab automation

---

## 📂 Archive Structure (Proposed)

```
episode-scripts-archive/
├── episodes/
│   └── EPXXX-title/
│       ├── script.md
│       ├── sources.md
│       └── assets/
├── research/
│   ├── synbio-tools-survey.md
│   └── community-issues-snapshot.md
├── templates/
│   ├── episode-script-template.md
│   └── sources-template.md
└── README.md
```

---

## 🔗 Quick Reference Links

- [SynBioHub](https://synbiohub.org) — Hosted design-sharing platform
- [SBOL Specification](https://sbolstandard.org/) — Synthetic Biology Open Language standard
- [Cello CAD](http://www.cellocad.org/) — Genetic circuit design automation
- [Biopython Docs](https://biopython.org/docs/latest/) — Full tutorial and API reference
- [Opentrons Protocol Library](https://protocols.opentrons.com/) — Community-shared lab automation protocols
- [nf-core](https://nf-co.re/) — Curated Nextflow pipelines for bioinformatics
- [PyLabRobot Docs](https://docs.pylabrobot.org) — Hardware-agnostic automation SDK
- [Edinburgh Genome Foundry](https://edinburgh-genome-foundry.github.io/) — Python tools for DNA design

---

*Last research update: September 2026*
