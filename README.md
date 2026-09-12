# 🎬 Episode Scripts Archive

A curated archive for storing episode scripts and associated source materials (research notes, references, tooling context, and community discussions). This repository is organized for version-controlled collaboration on audiovisual and written episode content.

---

## 📁 Repository Purpose

- **Centralize** episode scripts, show notes, source materials, and production assets in a single, version-controlled location
- **Preserve** content history through Git's branching and commit tracking
- **Collaborate** by providing a clear workflow for writers, editors, producers, and guests
- **Enable reuse** — modular script components can be repurposed across episodes
- **Document provenance** — every edit and contributor is tracked
- **Anchor research** — each episode's notes tie back to real, live open-source projects and the concerns bubbling up in their issue trackers

---

## 🔬 Synthetic Biology & Biotech Software Tools (Research Survey)

This archive keeps a running snapshot of the GitHub-based **synthetic biology (synbio)** and **biotech software** ecosystem, with a live eye on each project's open issues. The projects below were surveyed as part of episode research, with several investigated in depth.

### 🏆 Synthesized Landscape (key synbio & biotech tools found on GitHub)

| Project | Stars | Language | What it does |
|---|---|---|---|
| [Synbiota/GENtle2](https://github.com/Synbiota/GENtle2) | 106 | JavaScript | Web-based DNA editor for synthetic biology |
| [20n/act](https://github.com/20n/act) | 92 | Java | Predictive bioengineering — discovers DNA routes to make target chemicals |
| [SynBioHub/synbiohub](https://github.com/SynBioHub/synbiohub) | 84 | JavaScript | Web platform for browsing, uploading & sharing synthetic biology designs |
| [JBEI/ART](https://github.com/JBEI/ART) | 66 | Jupyter Notebook | ML tool to improve strain engineering effectiveness |
| [MyersResearchGroup/iBioSim](https://github.com/MyersResearchGroup/iBioSim) | 67 | Java | CAD for genetic circuits; SBML/SBOL support |
| [SynBioDex/libSBOLj](https://github.com/SynBioDex/libSBOLj) | 43 | Java | Java library for the Synthetic Biology Open Language (SBOL) |
| [klavinslab/coral](https://github.com/klavinslab/coral) | 32 | Python | Library & framework for specifying synbio design processes |
| [Autodesk/bionano-wetLabAccelerator](https://github.com/Autodesk/bionano-wetLabAccelerator) | 32 | JavaScript | Designs robotic wet-lab protocols via visual UI (no coding) |
| [Gardner-BinfLab/TISIGNER-ReactJS](https://github.com/Gardner-BinfLab/TISIGNER-ReactJS) | 30 | JavaScript | TISIGNER: interactive synbio design tool |
| [SynBioDex/SBOL-specification](https://github.com/SynBioDex/SBOL-specification) | 23 | TeX | The Synthetic Biology Open Language specification |
| [virtualramblas/awesome-deep-learning-4-life-sciences](https://github.com/virtualramblas/awesome-deep-learning-4-life-sciences) | 167 | — | Curated resources for deep learning in life sciences (biotech/pharma focus) |
| [dportik/Biotech-Job-Search-Engine](https://github.com/dportik/Biotech-Job-Search-Engine) | 80 | Python | Open-source job-discovery system for biotech, genomics & bioinformatics roles |

### 🧬 In-Depth Investigation (active repos, open issues reviewed)

#### SynBioHub/synbiohub (design sharing platform — actively maintained)
SynBioHub is the community's primary web-based repository for sharing synthetic biology designs, supporting SBOL import/export and deployment via Docker. It hosts the complete iGEM Registry of Standard Biological Parts via a public instance at synbiohub.org.

**Recent open issues (as of September 2026):**

| Issue | Summary | Theme |
|---|---|---|
| #1756 | SubCollections does not report members in public graph | Bug — data integrity in shared collections |
| #1755 | Recursive download does not follow linked collections | Bug — user workflow gap |
| #1754 | Legacy data in Virtuoso should be deleted | Maintenance — technical debt from database migrations |
| #1753 | OMEX download is missing SBML file (only downloads SBOL) | Bug — export completeness |
| #1752 | Changing private collection to public shifts prefix from `localhost:3333` to `synbiohub.org` | Bug — deployment/shareability friction |

**Takeaway:** The community is focused on **data integrity** (collections, exports), **technical-debt cleanup** (legacy DB data), and **deployment friction** (prefix/URL issues when sharing local designs publicly). These are classic growing-pains for a platform bridging academic research and real-world deployment.

---

#### 20n/act (predictive bioengineering — actively maintained)
20n/act is a platform for **computational synthetic biology** that predicts DNA insertions into cells (e.g., *E. coli*, *S. cerevisiae*) that modify the cell to produce a target molecule via fermentation. It famously predicted the first bio-route to Acetaminophen. The stack includes: predictive modeling (reaction-operator inference, SAR, reachables computation, cascade enumeration, DNA design), analytics (LCMS untargeted metabolomics via deep learning), and unit-economics modeling for bioproduction.

**Recent open issues:** No open issues as of the last check — suggesting the project is in a stable, production-ready state, with the core predictive pipeline considered finished. Contact is required for enterprise licensing and pre-packaged databases.

**Takeaway:** The sheer scope of the platform (10+ modules from NLP to patent search to cost modeling) makes it one of the most ambitious open-source bioengineering projects, but it also means the community is small and enterprise-oriented rather than broadly contributor-friendly.

---

#### Synbiota/GENtle2 (web DNA editor)
GENtle2 is a re-thought-for-the-web version of the classic GENtle desktop DNA editor. Core features are being extracted into modules.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #253 | Jumping annotations | UI bug |
| #252 | Anchor and Cap selections won't change | UI bug |
| #251 | Spacing button doesn't work | UI bug |
| #250 | BLAST show button doesn't do anything | UI / integration bug |

**Takeaway:** These issues are quite old (created 2015) and point to long-standing UI interaction bugs that haven't been addressed — a common pattern in academic tools that lose active maintainers. The project is still listed as "in development" with recent updates, but the open issues suggest a gap between roadmap and bug triage.

---

#### MyersResearchGroup/iBioSim (CAD for genetic circuits)
iBioSim is a CAD tool for modeling, analysis, and design of genetic circuits, with SBML/SBOL support.

**Recent open issues:**

| Issue | Summary | Theme |
|---|---|---|
| #640 | A Java exception has occurred | Stability / runtime |
| #639 | Can't upload SynBioHub design | Integration with design-sharing platforms |
| #638 | Unable to run iBioSim 3.2.0 on Mac | Cross-platform compatibility |

**Takeaway:** Issues center on cross-platform compatibility (Mac), runtime stability (Java exceptions), and interoperability with SynBioHub — reinforcing a key theme that synbio tools struggle with smooth integration across the networked ecosystem.

---

### 📊 Community Themes (from issue surveys across all projects)

Across these projects, the synbio/biotech open-source community is currently focused on:

1. **Interoperability & integration friction** — iBioSim can't upload to SynBioHub; OMEX exports miss SBML files; collection prefixes shift when changing visibility. The dream of a connected synbio toolchain is still hampered by format/URL/API mismatches.
2. **Data integrity in shared collections** — SubCollections not reporting members, recursive downloads not following links, legacy DB data piling up — these are growing-pains for platforms that host community-wide design registries.
3. **Long-standing UI bugs in academic tools** — GENtle2's 2015-era interaction bugs remain unfixed, suggesting limited maintainer bandwidth for UI polish in favor of core algorithmic work.
4. **Cross-platform compatibility** — iBioSim's Mac issue persists, a reminder that Java "write once" is aspirational, not guaranteed.
5. **Stable enterprise-oriented platforms vs. community-friendly ones** — 20n/act has zero open issues but requires enterprise licensing for the full database; this creates a tension between open-source ideals and practical deployment.
6. **Deployment & DevOps gaps** — Virtuoso database migrations, Docker image complexity (SynBioHub requires Virtuoso, Maven, Node, etc.) — these barriers push away potential contributors and users who just want to run the tool.
7. **ML + sequence design convergence** — ART's ML for strain engineering, iBioSim's circuit design, and the broader ecosystem point to an accelerating intersection of machine learning and biological design automation.

---

### 🗺️ Community Resources & Curated Lists

| Resource | Stars | Description |
|---|---|---|
| [virtualramblas/awesome-deep-learning-4-life-sciences](https://github.com/virtualramblas/awesome-deep-learning-4-life-sciences) | 167 | Curated list of deep-learning resources for biotech & pharma |

---

## 🏛️ Key Organizations & Communities

- **SynBioHub (SynBioHub org)** — Maintains the primary design-sharing platform and the SBOL Java library (libSBOLj)
- **SynBioDex** — Publishes the SBOL specification and related tools; community-driven standards effort
- **Myers Research Group** — Academic lab behind iBioSim; representative of university synbio CAD efforts
- **JBEI (Joint BioEnergy Institute)** — DOE-funded lab; produces ART for strain engineering
- **20n** — Startup that produced act; bridges academic research and commercial bioengineering
- **Autodesk Bio/Nano/Protospace** — Surprising entry! Autodesk's wet-lab-accelerator tool shows big-design-interest in synbio protocol automation
- **klavinslab** — University of Washington lab; contributes Coral framework for synbio design processes

---

## 📂 Archive Structure (proposed)

```
episode-scripts-archive/
├── episodes/
│   └── EPXXX-title/
│       ├── script.md
│       ├── sources.md
│       └── assets/
├── research/
│   ├── synbio-tools-survey-2026-09.md
│   └── community-issues-snapshot.md
├── templates/
│   ├── episode-script-template.md
│   └── sources-template.md
└── README.md
```

---

## 🔗 Quick Reference Links

- [SynBioHub](https://synbiohub.org) — Hosted design-sharing platform (public instance)
- [SynBioHub Wiki](https://wiki.synbiohub.org) — Installation & API docs
- [20n/act Wiki](https://github.com/20n/act/wiki) — Predictive bioengineering docs
- [iBioSim](http://www.ibiosim.org/) — Genetic circuit CAD tool
- [SBOL Specification](https://sbolstandard.org/) — Synthetic Biology Open Language standard
- [TISIGNER](http://tignamer.com/) — Interactive synbio design

---

*Last research update: September 2026*
