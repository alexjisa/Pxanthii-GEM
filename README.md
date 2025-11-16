## PxCm-GEM: Genome-scale metabolic models for pathogen–plant interaction

#### Description

PxCm-GEM is a repository that hosts a set of genome-scale metabolic models describing the biotrophic interaction between the powdery mildew fungus *Podosphaera xanthii* and the cucurbit plant *Cucumis melo*.  

The repository currently includes three complementary models:

- **Px-GEM**: genome-scale metabolic model of *Podosphaera xanthii*, an obligate biotrophic fungal pathogen causing powdery mildew in cucurbits.  
- **Cm-GEM**: genome-scale metabolic model of the host plant *Cucumis melo*.  
- **PxCm-GEM**: integrated host–pathogen interaction model between *P. xanthii* and *C. melo*.

The models are reconstructed and curated using genomic annotations, transcriptomics and metabolomics data, and they follow the [standard-GEM](https://github.com/MetabolicAtlas/standard-GEM) structure to ensure transparency, version control and compatibility with the COBRA community ecosystem.

---

#### Citation

> If you use any of the models (Px-GEM, Cm-GEM or PxCm-GEM), or the associated omics datasets in your research, please cite:

---

#### Model Keywords

**Utilisation:** experimental data reconstruction; multi-omics integrative analysis; host–pathogen interaction modelling; target identification; _in silico_ perturbation analysis  
**Field:** metabolic-network reconstruction; systems biology; plant pathology  
**Type of model:** reconstruction; curated; host–pathogen interaction  
**Omic source:** Genomics; Transcriptomics; Metabolomics  
**Taxon:** [identifiers.org/taxonomy:181420](https://identifiers.org/taxonomy:181420) (_Podosphaera xanthii_); [identifiers.org/taxonomy:3656](https://identifiers.org/taxonomy:3656) (_Cucumis melo_)  
**Isolate (fungus):** 2086  
**GenBank Assembly (fungus):** GCA_014884795.1  
**Metabolic system:** general metabolism; plant–fungal biotrophic interaction

#### Model statistics

|                          | *Podosphaera xanthii* 2086           | *Cucumis melo* DHL92           |
|--------------------------|--------------------------------------|--------------------------------|
| **Model (name)**         | Px-GEM                               | Cm-GEM                         |
| **Reactions (number)**   | 1,560                                | 2,602                          |
| **Metabolites (number)** | 1,749                                | 2,703                          |
| **Genes (number)**       | 828                                  | 3,319                          |

---

#### Model Overview

This repository adheres to the [standard-GEM](https://github.com/MetabolicAtlas/standard-GEM) layout. In brief:

- `model/`
  - `Px-GEM/`  
    Genome-scale model of *Podosphaera xanthii* in multiple formats (e.g. SBML, JSON, YAML, MAT).
  - `Cm-GEM/`  
    Genome-scale model of *Cucumis melo*.
  - `PxCm-GEM/`  
    Integrated host–pathogen model including:
    - Separate compartments for host, pathogen and interface (e.g. apoplast, haustorium).  
    - Exchange reactions capturing nutrient acquisition, redox coupling and metabolite flows during infection.  

- `data/`  
  Omics and annotation data used for reconstruction and curation, including:
  - Genome annotations for *P. xanthii* isolate 2086 (GCA_014884795.1).  
  - Transcriptomics and metabolomics datasets from infected and control plant tissues.  

- `code/`  
  Scripts for:
  - Model reconstruction and processing  
  - Integration of omics data  
  - Simulation and analysis (_e.g._ FBA, FVA, gene/reaction knockouts, condition-specific models)

More details on the exact file formats and reconstruction pipeline are provided in the `docs/` folder.

---

### Installation

This repository can be used with common constraint-based modelling toolboxes such as:

- **Python**: [COBRApy](https://github.com/opencobra/cobrapy)  
- **MATLAB**: [COBRA Toolbox](https://opencobra.github.io/cobratoolbox/stable/)  
- Other compatible tools that support SBML L3 and related formats.

To obtain the models:

```bash
git clone https://github.com/{{organization or username}}/PxCm-GEM.git
cd PxCm-GEM
