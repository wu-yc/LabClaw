# LabClaw – Skill Operating Layer for Stanford LabOS & Next-Gen AI Co-Scientists

<div align="center">

<p align="center">
  <img src="Weixin Image_20260308180016_466_6307.png" alt="LabClaw Logo" width="100">
</p>

**Powering dry-lab reasoning, protocol composition, and agentic workflows to close the loop with LabOS XR/wet-lab execution.**

[![Skills](https://img.shields.io/badge/skills-211-blue?style=flat-square)](skills/)
[![Biology](https://img.shields.io/badge/🧬_biology-66-brightgreen?style=flat-square)](skills/bio/)
[![LabOS](https://img.shields.io/badge/🤖_labos-7-cyan?style=flat-square)](skills/labos/)
[![Vision](https://img.shields.io/badge/👁️_vision-5-yellow?style=flat-square)](skills/vision/)
[![Pharmacy](https://img.shields.io/badge/💊_pharmacy-36-blueviolet?style=flat-square)](skills/pharma/)
[![Medicine](https://img.shields.io/badge/🏥_medicine-20-red?style=flat-square)](skills/med/)
[![General](https://img.shields.io/badge/⚙️_general-48-orange?style=flat-square)](skills/general/)
[![Literature](https://img.shields.io/badge/📚_literature-29-purple?style=flat-square)](skills/literature/)
[![License](https://img.shields.io/badge/license-MIT-lightgrey?style=flat-square)](LICENSE)

**English** · [简体中文](README.zh-CN.md)  · [Project](https://labclaw-ai.github.io/)

<br>

**☕ Support our research (Base):** `0x41060E28a182C2CA5ff66C6D3de70D90a9d83a98`
**☕ Support our research (Solana):** 6MKtYQYvn7k6PiTEE3N22wu6LoB36XVC2SoRqdL3bFom

</div>

</div>

LabClaw is a skill library, not a monolithic software package. You can install the full collection or copy only the skill folders that match your research workflows.

---

## Overview

LabClaw packages **211 production-ready `SKILL.md` files** for biomedical AI workflows across biology, lab automation, vision/XR, drug discovery, medicine, data science, and literature research. Each skill teaches an OpenClaw-compatible agent **when** to use a tool, **how** to call it, and **what kind of output** to produce.

The collection is designed for researchers who want a practical, modular skill layer instead of a generic prompt bundle. You can use it as a broad starter library, or cherry-pick only the subfolders relevant to your lab, team, or project.

## At a Glance

| Domain | Skills | Focus |
|--------|-------:|-------|
| [🧬 Biology & Life Sciences](skills/bio/) | **66** | Bioinformatics, single-cell, genomics, proteomics, multi-omics, databases |
| [🤖 LabOS & Automation](skills/labos/) | **7** | Lab robots, LIMS/ELN, cloud platforms, protocol management |
| [👁️ Vision & XR](skills/vision/) | **5** | Hand tracking, 3D pose estimation, segmentation, egocentric vision |
| [💊 Pharmacy & Drug Discovery](skills/pharma/) | **36** | Cheminformatics, molecular ML, docking, target research, pharmacology, drug databases |
| [🏥 Medical & Clinical](skills/med/) | **20** | Clinical trials, precision medicine, oncology, infectious disease, medical imaging |
| [⚙️ General & Data Science](skills/general/) | **48** | Statistics, machine learning, data management, visualization, scientific writing |
| [📚 Literature & Search](skills/literature/) | **29** | Academic search, biomedical databases, multi-source discovery, patents, grants, citations |

## Representative Workflows

| Workflow | Example skills |
|----------|----------------|
| Single-cell and spatial omics | [`anndata`](skills/bio/anndata/SKILL.md), [`scanpy`](skills/bio/scanpy/SKILL.md), [`tooluniverse-spatial-transcriptomics`](skills/bio/tooluniverse-spatial-transcriptomics/SKILL.md) |
| Drug discovery and molecular design | [`rdkit`](skills/pharma/rdkit/SKILL.md), [`diffdock`](skills/pharma/diffdock/SKILL.md), [`tooluniverse-drug-repurposing`](skills/pharma/tooluniverse-drug-repurposing/SKILL.md) |
| Clinical and precision medicine | [`clinical`](skills/med/clinical/SKILL.md), [`tooluniverse-precision-oncology`](skills/med/tooluniverse-precision-oncology/SKILL.md), [`clinicaltrials-database`](skills/literature/clinicaltrials-database/SKILL.md) |
| Statistics, ML, and figure generation | [`statistics`](skills/general/statistics/SKILL.md), [`scikit-learn`](skills/general/scikit-learn/SKILL.md), [`scientific-visualization`](skills/general/scientific-visualization/SKILL.md) |
| Literature review and reporting | [`pubmed-search`](skills/literature/pubmed-search/SKILL.md), [`citation-management`](skills/literature/citation-management/SKILL.md), [`scientific-writing`](skills/general/scientific-writing/SKILL.md) |

## 3-Second Quick Start

Just send the message to OpenClaw:
```bash
install https://github.com/wu-yc/LabClaw
```
<p align="center"> <img src="./install_demo.gif" alt="Install Demo" width="30%"> </p>



## Use Cases

In Lab (with XR):
<p align="center"> <img src="./inlab.gif" alt="Install Demo" width="30%"> </p>



## Repository Layout

```text
LabClaw/
├── README.md
├── README.zh-CN.md
└── skills/
    ├── bio/         # 66 skills: genomics, proteomics, single-cell, systems biology
    ├── labos/       # 7 skills: lab robots, LIMS/ELN, cloud platforms, protocols
    ├── vision/      # 5 skills: hand tracking, 3D pose, segmentation, egocentric
    ├── pharma/      # 36 skills: cheminformatics, docking, target discovery, pharmacology
    ├── med/         # 20 skills: clinical research, precision medicine, oncology, imaging
    ├── general/     # 48 skills: statistics, ML, visualization, writing, reproducibility
    └── literature/  # 29 skills: search, databases, grants, patents, citations
```

## Related Repositories

These projects are especially relevant if you want to place LabClaw in the broader biomedical-agent ecosystem:

| Repository | Why it matters |
|------------|----------------|
| [`openclaw/openclaw`](https://github.com/openclaw/openclaw) | The main runtime that loads workspace skills and provides the skills platform, onboarding flow, and agent workspace model that LabClaw is designed to fit into. |
| [`mims-harvard/ToolUniverse`](https://github.com/mims-harvard/ToolUniverse) | A large AI-scientist tool ecosystem. LabClaw includes many `tooluniverse-*` skills across omics, drug discovery, clinical workflows, and literature research. |
| [`snap-stanford/Biomni`](https://github.com/snap-stanford/Biomni) | A complementary biomedical AI agent project. LabClaw already includes a `biomni` skill, making Biomni a natural reference point for users exploring autonomous biomedical research agents. |

## Full Skill Catalog

The original catalog is preserved below, but grouped into collapsible sections to make browsing easier on GitHub.

---

<details>
<summary><strong>🧬 Biology & Life Sciences — 66 skills</strong></summary>

> Tools for genomics, transcriptomics, proteomics, single-cell analysis, structural biology, systems biology, and lab automation.

**66 skills** &nbsp;·&nbsp; [`skills/bio/`](skills/bio/)

#### Bioinformatics Core

| Skill | Description |
|-------|-------------|
| [`arboreto`](skills/bio/arboreto/SKILL.md) | Infer gene regulatory networks (GRNs) from gene expression data using scalable algorithms (GRNBoost2, GENIE3). Use when ... |
| [`bioinformatics`](skills/bio/bioinformatics/SKILL.md) | Computational biology and genomics analysis pipelines. GENERAL: not locked to any specific tool — use Scanpy, Seurat, DE... |
| [`biomni`](skills/bio/biomni/SKILL.md) | Autonomous biomedical AI agent framework for executing complex research tasks across genomics, drug discovery, molecular... |
| [`biopython`](skills/bio/biopython/SKILL.md) | Comprehensive molecular biology toolkit. Use for sequence manipulation, file parsing (FASTA/GenBank/PDB), phylogenetics,... |
| [`cobrapy`](skills/bio/cobrapy/SKILL.md) | Constraint-based metabolic modeling (COBRA). FBA, FVA, gene knockouts, flux sampling, SBML models, for systems biology a... |
| [`etetoolkit`](skills/bio/etetoolkit/SKILL.md) | Phylogenetic tree toolkit (ETE). Tree manipulation (Newick/NHX), evolutionary event detection, orthology/paralogy, NCBI ... |
| [`geniml`](skills/bio/geniml/SKILL.md) | This skill should be used when working with genomic interval data (BED files) for machine learning tasks. Use for traini... |
| [`gget`](skills/bio/gget/SKILL.md) | Fast CLI/Python queries to 20+ bioinformatics databases. Use for quick lookups: gene info, BLAST searches, AlphaFold str... |
| [`gtars`](skills/bio/gtars/SKILL.md) | High-performance toolkit for genomic interval analysis in Rust with Python bindings. Use when working with genomic regio... |
| [`hypogenic`](skills/bio/hypogenic/SKILL.md) | Automated LLM-driven hypothesis generation and testing on tabular datasets. Use when you want to systematically explore ... |
| [`scikit-bio`](skills/bio/scikit-bio/SKILL.md) | Biological data toolkit. Sequence analysis, alignments, phylogenetic trees, diversity metrics (alpha/beta, UniFrac), ord... |

#### Single-cell & Spatial Transcriptomics

| Skill | Description |
|-------|-------------|
| [`anndata`](skills/bio/anndata/SKILL.md) | Data structure for annotated matrices in single-cell analysis. Use when working with .h5ad files or integrating with the... |
| [`cellxgene-census`](skills/bio/cellxgene-census/SKILL.md) | Query the CELLxGENE Census (61M+ cells) programmatically. Use when you need expression data across tissues, diseases, or... |
| [`scanpy`](skills/bio/scanpy/SKILL.md) | Standard single-cell RNA-seq analysis pipeline. Use for QC, normalization, dimensionality reduction (PCA/UMAP/t-SNE), cl... |
| [`scvi-tools`](skills/bio/scvi-tools/SKILL.md) | Deep generative models for single-cell omics. Use when you need probabilistic batch correction (scVI), transfer learning... |
| [`tooluniverse-single-cell`](skills/bio/tooluniverse-single-cell/SKILL.md) | Production-ready single-cell and expression matrix analysis using scanpy, anndata, and scipy. Performs scRNA-seq QC, nor... |
| [`tooluniverse-spatial-omics-analysis`](skills/bio/tooluniverse-spatial-omics-analysis/SKILL.md) | Computational analysis framework for spatial multi-omics data integration. Given spatially variable genes (SVGs), spatia... |
| [`tooluniverse-spatial-transcriptomics`](skills/bio/tooluniverse-spatial-transcriptomics/SKILL.md) | Analyze spatial transcriptomics data to map gene expression in tissue architecture. Supports 10x Visium, MERFISH, seqFIS... |
| [`umap-learn`](skills/bio/umap-learn/SKILL.md) | UMAP dimensionality reduction. Fast nonlinear manifold learning for 2D/3D visualization, clustering preprocessing (HDBSCAN), supervised/parametric UMAP, for high-dimensional data. |

#### Genomics, NGS & Variant Analysis

| Skill | Description |
|-------|-------------|
| [`deeptools`](skills/bio/deeptools/SKILL.md) | NGS analysis toolkit. BAM to bigWig conversion, QC (correlation, PCA, fingerprints), heatmaps/profiles (TSS, peaks), for... |
| [`pydeseq2`](skills/bio/pydeseq2/SKILL.md) | Differential gene expression analysis (Python DESeq2). Identify DE genes from bulk RNA-seq counts, Wald tests, FDR corre... |
| [`pysam`](skills/bio/pysam/SKILL.md) | Genomic file toolkit. Read/write SAM/BAM/CRAM alignments, VCF/BCF variants, FASTA/FASTQ sequences, extract regions, calc... |
| [`tooluniverse-crispr-screen-analysis`](skills/bio/tooluniverse-crispr-screen-analysis/SKILL.md) | Comprehensive CRISPR screen analysis for functional genomics. Analyze pooled or arrayed CRISPR screens (knockout, activa... |
| [`tooluniverse-epigenomics`](skills/bio/tooluniverse-epigenomics/SKILL.md) | Production-ready genomics and epigenomics data processing for BixBench questions. Handles methylation array analysis (Cp... |
| [`tooluniverse-expression-data-retrieval`](skills/bio/tooluniverse-expression-data-retrieval/SKILL.md) | Retrieves gene expression and omics datasets from ArrayExpress and BioStudies with gene disambiguation, experiment quality assessment, and structured reports. Creates comprehensive dataset profiles with metadata, sample information, and download links. Use when users need expression data, omics datasets, or mention ArrayExpress (E-MTAB, E-GEOD) or BioStudies (S-BSST) accessions. |
| [`tooluniverse-gene-enrichment`](skills/bio/tooluniverse-gene-enrichment/SKILL.md) | Perform comprehensive gene enrichment and pathway analysis using gseapy (ORA and GSEA), PANTHER, STRING, Reactome, and 4... |
| [`tooluniverse-gwas-drug-discovery`](skills/bio/tooluniverse-gwas-drug-discovery/SKILL.md) | Transform GWAS signals into actionable drug targets and repurposing opportunities. Performs locus-to-gene mapping, targe... |
| [`tooluniverse-gwas-finemapping`](skills/bio/tooluniverse-gwas-finemapping/SKILL.md) | Identify and prioritize causal variants at GWAS loci using statistical fine-mapping and locus-to-gene predictions. Compu... |
| [`tooluniverse-gwas-snp-interpretation`](skills/bio/tooluniverse-gwas-snp-interpretation/SKILL.md) | Interpret genetic variants (SNPs) from GWAS studies by aggregating evidence from multiple databases (GWAS Catalog, Open ... |
| [`tooluniverse-gwas-study-explorer`](skills/bio/tooluniverse-gwas-study-explorer/SKILL.md) | Compare GWAS studies, perform meta-analyses, and assess replication across cohorts. Integrates NHGRI-EBI GWAS Catalog an... |
| [`tooluniverse-gwas-trait-to-gene`](skills/bio/tooluniverse-gwas-trait-to-gene/SKILL.md) | Discover genes associated with diseases and traits using GWAS data from the GWAS Catalog (500,000+ associations) and Ope... |
| [`tooluniverse-immune-repertoire-analysis`](skills/bio/tooluniverse-immune-repertoire-analysis/SKILL.md) | Comprehensive immune repertoire analysis for T-cell and B-cell receptor sequencing data. Analyze TCR/BCR repertoires to ... |
| [`tooluniverse-polygenic-risk-score`](skills/bio/tooluniverse-polygenic-risk-score/SKILL.md) | Build and interpret polygenic risk scores (PRS) for complex diseases using GWAS summary statistics. Calculates genetic r... |
| [`tooluniverse-rnaseq-deseq2`](skills/bio/tooluniverse-rnaseq-deseq2/SKILL.md) | Production-ready RNA-seq differential expression analysis using PyDESeq2. Performs DESeq2 normalization, dispersion esti... |
| [`tooluniverse-sequence-retrieval`](skills/bio/tooluniverse-sequence-retrieval/SKILL.md) | Retrieves biological sequences (DNA, RNA, protein) from NCBI and ENA with gene disambiguation, accession type handling, ... |
| [`tooluniverse-structural-variant-analysis`](skills/bio/tooluniverse-structural-variant-analysis/SKILL.md) | Comprehensive structural variant (SV) analysis skill for clinical genomics. Classifies SVs (deletions, duplications, inv... |
| [`tooluniverse-variant-analysis`](skills/bio/tooluniverse-variant-analysis/SKILL.md) | Production-ready VCF processing, variant annotation, mutation analysis, and structural variant (SV/CNV) interpretation f... |
| [`tooluniverse-variant-interpretation`](skills/bio/tooluniverse-variant-interpretation/SKILL.md) | Systematic clinical variant interpretation from raw variant calls to ACMG-classified recommendations with structural imp... |

#### Proteomics & Structural Biology

| Skill | Description |
|-------|-------------|
| [`alphafold-database`](skills/bio/alphafold-database/SKILL.md) | Access AlphaFold 200M+ AI-predicted protein structures. Retrieve structures by UniProt ID, download PDB/mmCIF files, ana... |
| [`esm`](skills/bio/esm/SKILL.md) | Comprehensive toolkit for protein language models including ESM3 (generative multimodal protein design across sequence, ... |
| [`pyopenms`](skills/bio/pyopenms/SKILL.md) | Complete mass spectrometry analysis platform. Use for proteomics workflows feature detection, peptide identification, pr... |
| [`tooluniverse-protein-interactions`](skills/bio/tooluniverse-protein-interactions/SKILL.md) | Analyze protein-protein interaction networks using STRING, BioGRID, and SASBDB databases. Maps protein identifiers, retr... |
| [`tooluniverse-protein-structure-retrieval`](skills/bio/tooluniverse-protein-structure-retrieval/SKILL.md) | Retrieves protein structure data from RCSB PDB, PDBe, and AlphaFold with protein disambiguation, quality assessment, and... |
| [`tooluniverse-proteomics-analysis`](skills/bio/tooluniverse-proteomics-analysis/SKILL.md) | Analyze mass spectrometry proteomics data including protein quantification, differential expression, post-translational ... |
| [`uniprot-database`](skills/bio/uniprot-database/SKILL.md) | Direct REST API access to UniProt. Protein searches, FASTA retrieval, ID mapping, Swiss-Prot/TrEMBL. For Python workflow... |

#### Multi-Omics & Systems Biology

| Skill | Description |
|-------|-------------|
| [`matchms`](skills/bio/matchms/SKILL.md) | Spectral similarity and compound identification for metabolomics. Use for comparing mass spectra, computing similarity s... |
| [`tooluniverse-metabolomics`](skills/bio/tooluniverse-metabolomics/SKILL.md) | Comprehensive metabolomics research skill for identifying metabolites, analyzing studies, and searching metabolomics dat... |
| [`tooluniverse-metabolomics-analysis`](skills/bio/tooluniverse-metabolomics-analysis/SKILL.md) | Analyze metabolomics data including metabolite identification, quantification, pathway analysis, and metabolic flux. Pro... |
| [`tooluniverse-multi-omics-integration`](skills/bio/tooluniverse-multi-omics-integration/SKILL.md) | Integrate and analyze multiple omics datasets (transcriptomics, proteomics, epigenomics, genomics, metabolomics) for sys... |
| [`tooluniverse-multiomic-disease-characterization`](skills/bio/tooluniverse-multiomic-disease-characterization/SKILL.md) | Comprehensive multi-omics disease characterization integrating genomics, transcriptomics, proteomics, pathway, and thera... |
| [`tooluniverse-phylogenetics`](skills/bio/tooluniverse-phylogenetics/SKILL.md) | Production-ready phylogenetics and sequence analysis skill for alignment processing, tree analysis, and evolutionary met... |
| [`tooluniverse-systems-biology`](skills/bio/tooluniverse-systems-biology/SKILL.md) | Comprehensive systems biology and pathway analysis using multiple pathway databases (Reactome, KEGG, WikiPathways, Pathw... |

#### Biological Databases

| Skill | Description |
|-------|-------------|
| [`brenda-database`](skills/bio/brenda-database/SKILL.md) | Access BRENDA enzyme database via SOAP API. Retrieve kinetic parameters (Km, kcat), reaction equations, organism data, a... |
| [`clinpgx-database`](skills/bio/clinpgx-database/SKILL.md) | Access ClinPGx pharmacogenomics data (successor to PharmGKB). Query gene-drug interactions, CPIC guidelines, allele func... |
| [`cosmic-database`](skills/bio/cosmic-database/SKILL.md) | Access COSMIC cancer mutation database. Query somatic mutations, Cancer Gene Census, mutational signatures, gene fusions... |
| [`ena-database`](skills/bio/ena-database/SKILL.md) | Access European Nucleotide Archive via API/FTP. Retrieve DNA/RNA sequences, raw reads (FASTQ), genome assemblies by acce... |
| [`ensembl-database`](skills/bio/ensembl-database/SKILL.md) | Query Ensembl genome database REST API for 250+ species. Gene lookups, sequence retrieval, variant analysis, comparative... |
| [`kegg-database`](skills/bio/kegg-database/SKILL.md) | Direct REST API access to KEGG (academic use only). Pathway analysis, gene-pathway mapping, metabolic pathways, drug int... |
| [`metabolomics-workbench-database`](skills/bio/metabolomics-workbench-database/SKILL.md) | Access NIH Metabolomics Workbench via REST API (4,200+ studies). Query metabolites, RefMet nomenclature, MS/NMR data, m/... |
| [`reactome-database`](skills/bio/reactome-database/SKILL.md) | Query Reactome REST API for pathway analysis, enrichment, gene-pathway mapping, disease pathways, molecular interactions... |
| [`string-database`](skills/bio/string-database/SKILL.md) | Query STRING API for protein-protein interactions (59M proteins, 20B interactions). Network analysis, GO/KEGG enrichment... |

#### Lab Platforms & Imaging

| Skill | Description |
|-------|-------------|
| [`flowio`](skills/bio/flowio/SKILL.md) | Parse FCS (Flow Cytometry Standard) files v2.0-3.1. Extract events as NumPy arrays, read metadata/channels, convert to C... |
| [`histolab`](skills/bio/histolab/SKILL.md) | Lightweight WSI tile extraction and preprocessing. Use for basic slide processing tissue detection, tile extraction, sta... |
| [`lamindb`](skills/bio/lamindb/SKILL.md) | This skill should be used when working with LaminDB, an open-source data framework for biology that makes data queryable... |
| [`omero-integration`](skills/bio/omero-integration/SKILL.md) | Microscopy data management platform. Access images via Python, retrieve datasets, analyze pixels, manage ROIs/annotation... |
| [`pathml`](skills/bio/pathml/SKILL.md) | Full-featured computational pathology toolkit. Use for advanced WSI analysis including multiplexed immunofluorescence (C... |

</details>

<details>
<summary><strong>🤖 LabOS & Laboratory Automation — 7 skills</strong></summary>

> Tools for lab robotics, LIMS/ELN systems, cloud platforms, and scientific protocol management. Optimized for Stanford LabOS workflows and automated laboratory research.

**7 skills** &nbsp;·&nbsp; [`skills/labos/`](skills/labos/)

#### Lab Robotics & Automation

| Skill | Description |
|-------|-------------|
| [`pylabrobot`](skills/bio/pylabrobot/SKILL.md) | Vendor-agnostic lab automation framework. Use when controlling multiple equipment types (Hamilton, Tecan, Opentrons, plate readers, pumps) or needing unified programming across different vendors. Best for complex workflows, multi-vendor setups, simulation. |
| [`opentrons-integration`](skills/bio/opentrons-integration/SKILL.md) | Official Opentrons Protocol API for OT-2 and Flex robots. Use when writing protocols specifically for Opentrons hardware with full access to Protocol API v2 features. Best for production Opentrons protocols, official API compatibility. |

#### LIMS/ELN Systems

| Skill | Description |
|-------|-------------|
| [`benchling-integration`](skills/bio/benchling-integration/SKILL.md) | Benchling R&D platform integration. Access registry (DNA, proteins), inventory, ELN entries, workflows via API, build Benchling Apps, query Data Warehouse, for lab data management automation. |
| [`labarchive-integration`](skills/bio/labarchive-integration/SKILL.md) | Electronic lab notebook API integration. Access notebooks, manage entries/attachments, backup notebooks, integrate with laboratory workflows, for ELN automation. |

#### Lab Cloud Platforms

| Skill | Description |
|-------|-------------|
| [`latchbio-integration`](skills/bio/latchbio-integration/SKILL.md) | Latch platform for bioinformatics workflows. Build pipelines with Latch SDK, @workflow/@task decorators, deploy serverless bioinformatics apps, for cloud bioinformatics. |
| [`dnanexus-integration`](skills/bio/dnanexus-integration/SKILL.md) | DNAnexus cloud genomics platform. Build apps/applets, manage data (upload/download), dxpy Python SDK, run workflows, FASTQ/BAM/CRAM processing, for cloud genomic analysis. |

#### Protocol Management

| Skill | Description |
|-------|-------------|
| [`protocolsio-integration`](skills/bio/protocolsio-integration/SKILL.md) | Integration with protocols.io API for managing scientific protocols. This skill should be used when working with protoco... |

</details>

<details>
<summary><strong>👁️ Vision & XR — 5 skills</strong></summary>

> Tools for hand tracking, 3D pose estimation, hand-object segmentation, and egocentric vision. Optimized for XR/AR applications, smart glasses interfaces, and computer vision research.

**5 skills** &nbsp;·&nbsp; [`skills/vision/`](skills/vision/)

#### Hand Detection & Tracking

| Skill | Description |
|-------|-------------|
| [`handtracking`](skills/vision/handtracking/SKILL.md) | Real-time hand detection in egocentric videos using victordibia/handtracking. Outputs bounding boxes for hands, specifically trained on EgoHands dataset. Lightweight and fast for egocentric view applications. |
| [`hands-3d-pose`](skills/vision/hands-3d-pose/SKILL.md) | High-quality 3D hand pose estimation for egocentric videos (ECCV 2024). Provides 3D joint keypoints and skeleton visualization projected to 2D. Optimized for daily egocentric activities with state-of-the-art accuracy. |

#### Segmentation & Analysis

| Skill | Description |
|-------|-------------|
| [`egohos-segmentation`](skills/vision/egohos-segmentation/SKILL.md) | Egocentric hand-object segmentation (EgoHOS) - pixel-level hand and object masks in egocentric videos. Specialized for hand-object interaction scenarios with pixel-accurate masks for detailed interaction analysis. |

#### Multi-View 3D Tracking

| Skill | Description |
|-------|-------------|
| [`hot3d`](skills/vision/hot3d/SKILL.md) | HOT3D (Hand-Object 3D Dataset) by Meta Facebook - multi-view egocentric hand and object 3D tracking for Aria/Quest smart glasses. State-of-the-art multi-view 3D hand pose, object pose, and hand-object interaction tracking with millimeter accuracy. |
| [`hand-tracking-toolkit`](skills/vision/hand-tracking-toolkit/SKILL.md) | Facebook Research hand tracking evaluation and visualization toolkit. Supports loading HOT3D data, computing metrics (PA-MPJPE, AUC), visualizing 3D pose projections, and generating tracking evaluation reports. |

</details>

<details>
<summary><strong>💊 Pharmacy & Drug Discovery — 36 skills</strong></summary>

> Tools for cheminformatics, molecular docking, drug design, pharmacology, pharmacovigilance, and drug databases.

**36 skills** &nbsp;·&nbsp; [`skills/pharma/`](skills/pharma/)

#### Cheminformatics & Molecular Design

| Skill | Description |
|-------|-------------|
| [`chemistry`](skills/pharma/chemistry/SKILL.md) | Computational chemistry, cheminformatics, and drug discovery workflows. |
| [`datamol`](skills/pharma/datamol/SKILL.md) | Pythonic wrapper around RDKit with simplified interface and sensible defaults. Preferred for standard drug discovery inc... |
| [`deepchem`](skills/pharma/deepchem/SKILL.md) | Molecular ML with diverse featurizers and pre-built datasets. Use for property prediction (ADMET, toxicity) with traditi... |
| [`medchem`](skills/pharma/medchem/SKILL.md) | Medicinal chemistry filters. Apply drug-likeness rules (Lipinski, Veber), PAINS filters, structural alerts, complexity m... |
| [`molfeat`](skills/pharma/molfeat/SKILL.md) | Molecular featurization for ML (100+ featurizers). ECFP, MACCS, descriptors, pretrained models (ChemBERTa), convert SMIL... |
| [`rdkit`](skills/pharma/rdkit/SKILL.md) | Cheminformatics toolkit for fine-grained molecular control. SMILES/SDF parsing, descriptors (MW, LogP, TPSA), fingerprin... |
| [`rowan`](skills/pharma/rowan/SKILL.md) | Cloud-based quantum chemistry platform with Python API. Preferred for computational chemistry workflows including pKa pr... |

#### Molecular Machine Learning

| Skill | Description |
|-------|-------------|
| [`pytdc`](skills/pharma/pytdc/SKILL.md) | Therapeutics Data Commons. AI-ready drug discovery datasets (ADME, toxicity, DTI), benchmarks, scaffold splits, molecula... |
| [`torch_geometric`](skills/pharma/torch_geometric/SKILL.md) | Graph Neural Networks (PyG). Node/graph classification, link prediction, GCN, GAT, GraphSAGE, heterogeneous graphs, mole... |
| [`torchdrug`](skills/pharma/torchdrug/SKILL.md) | PyTorch-native graph neural networks for molecules and proteins. Use when building custom GNN architectures for drug dis... |

#### Molecular Docking & Protein Therapeutics

| Skill | Description |
|-------|-------------|
| [`adaptyv`](skills/pharma/adaptyv/SKILL.md) | Cloud laboratory platform for automated protein testing and validation. Use when designing proteins and needing experime... |
| [`diffdock`](skills/pharma/diffdock/SKILL.md) | Diffusion-based molecular docking. Predict protein-ligand binding poses from PDB/SMILES, confidence scores, virtual scre... |
| [`tooluniverse-antibody-engineering`](skills/pharma/tooluniverse-antibody-engineering/SKILL.md) | Comprehensive antibody engineering and optimization for therapeutic development. Covers humanization, affinity maturatio... |
| [`tooluniverse-binder-discovery`](skills/pharma/tooluniverse-binder-discovery/SKILL.md) | Discover novel small molecule binders for protein targets using structure-based and ligand-based approaches. Creates act... |
| [`tooluniverse-protein-therapeutic-design`](skills/pharma/tooluniverse-protein-therapeutic-design/SKILL.md) | Design novel protein therapeutics (binders, enzymes, scaffolds) using AI-guided de novo design. Uses RFdiffusion for bac... |

#### Drug Research & Target Discovery

| Skill | Description |
|-------|-------------|
| [`tooluniverse-drug-repurposing`](skills/pharma/tooluniverse-drug-repurposing/SKILL.md) | Identify drug repurposing candidates using ToolUniverse for target-based, compound-based, and disease-driven strategies.... |
| [`tooluniverse-drug-research`](skills/pharma/tooluniverse-drug-research/SKILL.md) | Generates comprehensive drug research reports with compound disambiguation, evidence grading, and mandatory completeness... |
| [`tooluniverse-drug-target-validation`](skills/pharma/tooluniverse-drug-target-validation/SKILL.md) | Comprehensive computational validation of drug targets for early-stage drug discovery. Evaluates targets across 10 dimen... |
| [`tooluniverse-target-research`](skills/pharma/tooluniverse-target-research/SKILL.md) | Gather comprehensive biological target intelligence from 9 parallel research paths covering protein info, structure, int... |

#### Pharmacology & Safety

| Skill | Description |
|-------|-------------|
| [`tooluniverse-adverse-event-detection`](skills/pharma/tooluniverse-adverse-event-detection/SKILL.md) | Detect and analyze adverse drug event signals using FDA FAERS data, drug labels, disproportionality analysis (PRR, ROR, ... |
| [`tooluniverse-chemical-safety`](skills/pharma/tooluniverse-chemical-safety/SKILL.md) | Comprehensive chemical safety and toxicology assessment integrating ADMET-AI predictions, CTD toxicogenomics, FDA label ... |
| [`tooluniverse-drug-drug-interaction`](skills/pharma/tooluniverse-drug-drug-interaction/SKILL.md) | Comprehensive drug-drug interaction (DDI) prediction and risk assessment. Analyzes interaction mechanisms (CYP450, trans... |
| [`tooluniverse-network-pharmacology`](skills/pharma/tooluniverse-network-pharmacology/SKILL.md) | Construct and analyze compound-target-disease networks for drug repurposing, polypharmacology discovery, and systems pha... |
| [`tooluniverse-pharmacovigilance`](skills/pharma/tooluniverse-pharmacovigilance/SKILL.md) | Analyze drug safety signals from FDA adverse event reports, label warnings, and pharmacogenomic data. Calculates disprop... |

#### Chemical & Drug Databases

| Skill | Description |
|-------|-------------|
| [`chembl-database`](skills/pharma/chembl-database/SKILL.md) | Query ChEMBL bioactive molecules and drug discovery data. Search compounds by structure/properties, retrieve bioactivity... |
| [`chembl-search`](skills/pharma/chembl-search/SKILL.md) | Search ChEMBL bioactive molecules database with natural language queries. Find compounds and assay data with Valyu seman... |
| [`drug-discovery-search`](skills/pharma/drug-discovery-search/SKILL.md) | End-to-end drug discovery platform combining ChEMBL compounds, DrugBank, targets, and FDA labels. Natural language power... |
| [`drug-labels-search`](skills/pharma/drug-labels-search/SKILL.md) | Search FDA drug labels with natural language queries. Official drug information, indications, and safety data via Valyu. |
| [`drugbank-database`](skills/pharma/drugbank-database/SKILL.md) | Access and analyze comprehensive drug information from the DrugBank database including drug properties, interactions, ta... |
| [`drugbank-search`](skills/pharma/drugbank-search/SKILL.md) | Search DrugBank comprehensive drug database with natural language queries. Drug mechanisms, interactions, and safety dat... |
| [`fda-database`](skills/pharma/fda-database/SKILL.md) | Query openFDA API for drugs, devices, adverse events, recalls, regulatory submissions (510k, PMA), substance identificat... |
| [`open-targets-search`](skills/pharma/open-targets-search/SKILL.md) | Search Open Targets drug-disease associations with natural language queries. Target validation powered by Valyu semantic... |
| [`opentargets-database`](skills/pharma/opentargets-database/SKILL.md) | Query Open Targets Platform for target-disease associations, drug target discovery, tractability/safety data, genetics/o... |
| [`pubchem-database`](skills/pharma/pubchem-database/SKILL.md) | Query PubChem via PUG-REST API/PubChemPy (110M+ compounds). Search by name/CID/SMILES, retrieve properties, similarity/s... |
| [`tooluniverse-chemical-compound-retrieval`](skills/pharma/tooluniverse-chemical-compound-retrieval/SKILL.md) | Retrieves chemical compound information from PubChem and ChEMBL with disambiguation, cross-referencing, and quality asse... |
| [`zinc-database`](skills/pharma/zinc-database/SKILL.md) | Access ZINC (230M+ purchasable compounds). Search by ZINC ID/SMILES, similarity searches, 3D-ready structures for dockin... |

</details>

<details>
<summary><strong>🏥 Medical & Clinical — 20 skills</strong></summary>

> Tools for clinical research, precision medicine, oncology, infectious disease, and medical imaging.

**20 skills** &nbsp;·&nbsp; [`skills/med/`](skills/med/)

#### Clinical Research & Trials

| Skill | Description |
|-------|-------------|
| [`clinical`](skills/med/clinical/SKILL.md) | Clinical study design, statistical analysis, and regulatory compliance for medical research. |
| [`clinical-decision-support`](skills/med/clinical-decision-support/SKILL.md) | Generate professional clinical decision support (CDS) documents for pharmaceutical and clinical research settings, inclu... |
| [`clinical-reports`](skills/med/clinical-reports/SKILL.md) | Write comprehensive clinical reports including case reports (CARE guidelines), diagnostic reports (radiology/pathology/l... |
| [`tooluniverse-clinical-guidelines`](skills/med/tooluniverse-clinical-guidelines/SKILL.md) | Search and retrieve clinical practice guidelines across 12+ authoritative sources including NICE, WHO, ADA, AHA/ACC, NCC... |
| [`tooluniverse-clinical-trial-design`](skills/med/tooluniverse-clinical-trial-design/SKILL.md) | Strategic clinical trial design feasibility assessment using ToolUniverse. Evaluates patient population sizing, biomarke... |
| [`tooluniverse-clinical-trial-matching`](skills/med/tooluniverse-clinical-trial-matching/SKILL.md) | AI-driven patient-to-trial matching for precision medicine and oncology. Given a patient profile (disease, molecular alt... |
| [`treatment-plans`](skills/med/treatment-plans/SKILL.md) | Generate concise (3-4 page), focused medical treatment plans in LaTeX/PDF format for all clinical specialties. Supports ... |

#### Precision Medicine & Oncology

| Skill | Description |
|-------|-------------|
| [`tooluniverse-cancer-variant-interpretation`](skills/med/tooluniverse-cancer-variant-interpretation/SKILL.md) | Provide comprehensive clinical interpretation of somatic mutations in cancer. Given a gene symbol + variant (e.g., EGFR ... |
| [`tooluniverse-disease-research`](skills/med/tooluniverse-disease-research/SKILL.md) | Generate comprehensive disease research reports using 100+ ToolUniverse tools. Creates a detailed markdown report file a... |
| [`tooluniverse-immunotherapy-response-prediction`](skills/med/tooluniverse-immunotherapy-response-prediction/SKILL.md) | Predict patient response to immune checkpoint inhibitors (ICIs) using multi-biomarker integration. Given a cancer type, ... |
| [`tooluniverse-infectious-disease`](skills/med/tooluniverse-infectious-disease/SKILL.md) | Rapid pathogen characterization and drug repurposing analysis for infectious disease outbreaks. Identifies pathogen taxo... |
| [`tooluniverse-precision-medicine-stratification`](skills/med/tooluniverse-precision-medicine-stratification/SKILL.md) | Comprehensive patient stratification for precision medicine by integrating genomic, clinical, and therapeutic data. Give... |
| [`tooluniverse-precision-oncology`](skills/med/tooluniverse-precision-oncology/SKILL.md) | Provide actionable treatment recommendations for cancer patients based on molecular profile. Interprets tumor mutations,... |
| [`tooluniverse-rare-disease-diagnosis`](skills/med/tooluniverse-rare-disease-diagnosis/SKILL.md) | Provide differential diagnosis for patients with suspected rare diseases based on phenotype and genetic data. Matches sy... |

#### Medical Imaging, Devices & Regulatory

| Skill | Description |
|-------|-------------|
| [`iso-13485-certification`](skills/med/iso-13485-certification/SKILL.md) | Comprehensive toolkit for preparing ISO 13485 certification documentation for medical device Quality Management Systems.... |
| [`neurokit2`](skills/med/neurokit2/SKILL.md) | Comprehensive biosignal processing toolkit for analyzing physiological data including ECG, EEG, EDA, RSP, PPG, EMG, and ... |
| [`neuropixels-analysis`](skills/med/neuropixels-analysis/SKILL.md) | Neuropixels neural recording analysis. Load SpikeGLX/OpenEphys data, preprocess, motion correction, Kilosort4 spike sort... |
| [`pydicom`](skills/med/pydicom/SKILL.md) | Python library for working with DICOM (Digital Imaging and Communications in Medicine) files. Use this skill when readin... |
| [`pyhealth`](skills/med/pyhealth/SKILL.md) | Comprehensive healthcare AI toolkit for developing, testing, and deploying machine learning models with clinical data. T... |
| [`tooluniverse-image-analysis`](skills/med/tooluniverse-image-analysis/SKILL.md) | Production-ready microscopy image analysis and quantitative imaging data skill for colony morphometry, cell counting, fl... |

</details>

<details>
<summary><strong>⚙️ General & Data Science — 48 skills</strong></summary>

> General-purpose tools for statistics, machine learning, data management, visualization, and scientific writing.

**48 skills** &nbsp;·&nbsp; [`skills/general/`](skills/general/)

#### Statistics & Mathematical Modeling

| Skill | Description |
|-------|-------------|
| [`matlab`](skills/general/matlab/SKILL.md) | MATLAB and GNU Octave numerical computing for matrix operations, data analysis, visualization, and scientific computing. Use when writing MATLAB/Octave scripts for linear algebra, signal processing, image processing, differential equations, optimization, statistics, or creating scientific visualizations. Also use when the user needs help with MATLAB syntax, functions, or wants to convert between MATLAB and Python code. Scripts can be executed with MATLAB or the open-source GNU Octave interpreter. |
| [`pymc`](skills/general/pymc/SKILL.md) | Bayesian modeling with PyMC. Build hierarchical models, MCMC (NUTS), variational inference, LOO/WAIC comparison, posteri... |
| [`pymoo`](skills/general/pymoo/SKILL.md) | Multi-objective optimization framework. NSGA-II, NSGA-III, MOEA/D, Pareto fronts, constraint handling, benchmarks (ZDT, ... |
| [`scikit-survival`](skills/general/scikit-survival/SKILL.md) | Comprehensive toolkit for survival analysis and time-to-event modeling in Python using scikit-survival. Use this skill w... |
| [`statistical-analysis`](skills/general/statistical-analysis/SKILL.md) | Guided statistical analysis with test selection and reporting. Use when you need help choosing appropriate tests for you... |
| [`statistics`](skills/general/statistics/SKILL.md) | Comprehensive statistical methodology for scientific research. Covers test selection, assumption verification, power ana... |
| [`statsmodels`](skills/general/statsmodels/SKILL.md) | Statistical models library for Python. Use when you need specific model classes (OLS, GLM, mixed models, ARIMA) with det... |
| [`sympy`](skills/general/sympy/SKILL.md) | Use this skill when working with symbolic mathematics in Python. This skill should be used for symbolic computation task... |
| [`tooluniverse-statistical-modeling`](skills/general/tooluniverse-statistical-modeling/SKILL.md) | Perform statistical modeling and regression analysis on biomedical datasets. Supports linear regression, logistic regres... |

#### Machine Learning & AI

| Skill | Description |
|-------|-------------|
| [`aeon`](skills/general/aeon/SKILL.md) | This skill should be used for time series machine learning tasks including classification, regression, clustering, forec... |
| [`pytorch-lightning`](skills/general/pytorch-lightning/SKILL.md) | Deep learning framework (PyTorch Lightning). Organize PyTorch code into LightningModules, configure Trainers for multi-G... |
| [`scikit-learn`](skills/general/scikit-learn/SKILL.md) | Machine learning in Python with scikit-learn. Use when working with supervised learning (classification, regression), un... |
| [`shap`](skills/general/shap/SKILL.md) | Model interpretability and explainability using SHAP (SHapley Additive exPlanations). Use this skill when explaining mac... |
| [`transformers`](skills/general/transformers/SKILL.md) | This skill should be used when working with pre-trained transformer models for natural language processing, computer vis... |

#### Data Management & Computing

| Skill | Description |
|-------|-------------|
| [`dask`](skills/general/dask/SKILL.md) | Distributed computing for larger-than-RAM pandas/NumPy workflows. Use when you need to scale existing pandas/NumPy code ... |
| [`exploratory-data-analysis`](skills/general/exploratory-data-analysis/SKILL.md) | Perform comprehensive exploratory data analysis on scientific data files across 200+ file formats. This skill should be ... |
| [`fair-data`](skills/general/fair-data/SKILL.md) | Guidelines for making scientific data FAIR: Findable, Accessible, Interoperable, and Reusable. |
| [`geopandas`](skills/general/geopandas/SKILL.md) | Python library for working with geospatial vector data including shapefiles, GeoJSON, and GeoPackage files. Use when wor... |
| [`get-available-resources`](skills/general/get-available-resources/SKILL.md) | This skill should be used at the start of any computationally intensive scientific task to detect and report available s... |
| [`markitdown`](skills/general/markitdown/SKILL.md) | Convert files and office documents to Markdown. Supports PDF, DOCX, PPTX, XLSX, images (with OCR), audio (with transcrip... |
| [`networkx`](skills/general/networkx/SKILL.md) | Comprehensive toolkit for creating, analyzing, and visualizing complex networks and graphs in Python. Use when working w... |
| [`polars`](skills/general/polars/SKILL.md) | Fast in-memory DataFrame library for datasets that fit in RAM. Use when pandas is too slow but data still fits in memory... |
| [`reproducibility-checklist`](skills/general/reproducibility-checklist/SKILL.md) | Ensure research is reproducible, transparent, and meets open science standards. |
| [`vaex`](skills/general/vaex/SKILL.md) | Use this skill for processing and analyzing large tabular datasets (billions of rows) that exceed available RAM. Vaex ex... |
| [`zarr-python`](skills/general/zarr-python/SKILL.md) | Chunked N-D arrays for cloud storage. Compressed arrays, parallel I/O, S3/GCS integration, NumPy/Dask/Xarray compatible,... |

#### Visualization

| Skill | Description |
|-------|-------------|
| [`matplotlib`](skills/general/matplotlib/SKILL.md) | Low-level plotting library for full customization. Use when you need fine-grained control over every plot element, creat... |
| [`plotly`](skills/general/plotly/SKILL.md) | Interactive visualization library. Use when you need hover info, zoom, pan, or web-embeddable charts. Best for dashboard... |
| [`scientific-diagram-generation`](skills/general/scientific-diagram-generation/SKILL.md) | AI-powered scientific illustration generation using Gemini Image models. Creates publication-quality mechanism diagrams,... |
| [`scientific-visualization`](skills/general/scientific-visualization/SKILL.md) | Meta-skill for publication-ready figures. Use when creating journal submission figures requiring multi-panel layouts, si... |
| [`seaborn`](skills/general/seaborn/SKILL.md) | Statistical visualization with pandas integration. Use for quick exploration of distributions, relationships, and catego... |
| [`visualization`](skills/general/visualization/SKILL.md) | Publication-quality scientific figure generation. GENERAL: language-agnostic (R, Python, Julia, or any tool). |

#### Scientific Writing & Presentation

| Skill | Description |
|-------|-------------|
| [`article-writing`](skills/general/article-writing/SKILL.md) | Write articles, guides, blog posts, tutorials, newsletter issues, and other long-form content in a distinctive voice der... |
| [`hypothesis-generation`](skills/general/hypothesis-generation/SKILL.md) | Structured hypothesis formulation from observations. Use when you have experimental observations or data and need to for... |
| [`latex-posters`](skills/general/latex-posters/SKILL.md) | Create professional research posters in LaTeX using beamerposter, tikzposter, or baposter. Support for conference presen... |
| [`peer-review`](skills/general/peer-review/SKILL.md) | Structured manuscript/grant review with checklist-based evaluation. Use when writing formal peer reviews with specific c... |
| [`pptx-generation`](skills/general/pptx-generation/SKILL.md) | Create publication-quality academic presentations (.pptx) for group meetings, thesis defenses, conference talks, and pos... |
| [`pptx-posters`](skills/general/pptx-posters/SKILL.md) | Create research posters using HTML/CSS that can be exported to PDF or PPTX. Use this skill ONLY when the user explicitly... |
| [`protocol-writing`](skills/general/protocol-writing/SKILL.md) | Write clear, reproducible experimental protocols and Standard Operating Procedures (SOPs) for any scientific discipline. |
| [`scholar-evaluation`](skills/general/scholar-evaluation/SKILL.md) | Systematically evaluate scholarly work using the ScholarEval framework, providing structured assessment across research ... |
| [`science-communication`](skills/general/science-communication/SKILL.md) | Translate complex scientific findings into engaging content for non-specialist audiences. |
| [`scientific-brainstorming`](skills/general/scientific-brainstorming/SKILL.md) | Creative research ideation and exploration. Use for open-ended brainstorming sessions, exploring interdisciplinary conne... |
| [`scientific-critical-thinking`](skills/general/scientific-critical-thinking/SKILL.md) | Evaluate scientific claims and evidence quality. Use for assessing experimental design validity, identifying biases and ... |
| [`scientific-slides`](skills/general/scientific-slides/SKILL.md) | Build slide decks and presentations for research talks. Use this for making PowerPoint slides, conference presentations,... |
| [`scientific-writing`](skills/general/scientific-writing/SKILL.md) | Core skill for the deep research and writing tool. Write scientific manuscripts in full paragraphs (never bullet points)... |
| [`venue-templates`](skills/general/venue-templates/SKILL.md) | Access comprehensive LaTeX templates, formatting requirements, and submission guidelines for major scientific publicatio... |
| [`writing`](skills/general/writing/SKILL.md) | Scientific manuscript writing across all formats, fields, and journals. |

#### IP, Regulatory & Reporting

| Skill | Description |
|-------|-------------|
| [`patent-drafting`](skills/general/patent-drafting/SKILL.md) | Draft patent applications for scientific inventions, covering claims, specification, and prior art analysis. |
| [`regulatory-submission`](skills/general/regulatory-submission/SKILL.md) | Prepare regulatory submissions for drugs, biologics, devices, and diagnostics. |

</details>

<details>
<summary><strong>📚 Literature & Search — 29 skills</strong></summary>

> Tools for academic search, database queries, citation management, and literature review.

**29 skills** &nbsp;·&nbsp; [`skills/literature/`](skills/literature/)

#### Biomedical Literature Search

| Skill | Description |
|-------|-------------|
| [`academic-literature-search`](skills/literature/academic-literature-search/SKILL.md) | Use this skill when the user asks to search for academic papers, retrieve literature, generate citations, format referen... |
| [`biomedical-search`](skills/literature/biomedical-search/SKILL.md) | Complete biomedical information search combining PubMed, preprints, clinical trials, and FDA drug labels. Powered by Val... |
| [`biorxiv-database`](skills/literature/biorxiv-database/SKILL.md) | Efficient database search tool for bioRxiv preprint server. Use this skill when searching for life sciences preprints by... |
| [`biorxiv-search`](skills/literature/biorxiv-search/SKILL.md) | Search bioRxiv biology preprints with natural language queries. Semantic search powered by Valyu. |
| [`literature`](skills/literature/literature/SKILL.md) | Comprehensive academic literature search and synthesis across 15+ sources. |
| [`literature-review`](skills/literature/literature-review/SKILL.md) | Conduct comprehensive, systematic literature reviews using multiple academic databases (PubMed, arXiv, bioRxiv, Semantic... |
| [`literature-search`](skills/literature/literature-search/SKILL.md) | Comprehensive scientific literature search across PubMed, arXiv, bioRxiv, medRxiv. Natural language queries powered by V... |
| [`medrxiv-search`](skills/literature/medrxiv-search/SKILL.md) | Search medRxiv medical preprints with natural language queries. Powered by Valyu semantic search. |
| [`pubmed-database`](skills/literature/pubmed-database/SKILL.md) | Direct REST API access to PubMed. Advanced Boolean/MeSH queries, E-utilities API, batch processing, citation management.... |
| [`pubmed-search`](skills/literature/pubmed-search/SKILL.md) | Search PubMed biomedical literature with natural language queries powered by Valyu semantic search. Full-text access, in... |
| [`tooluniverse-literature-deep-research`](skills/literature/tooluniverse-literature-deep-research/SKILL.md) | Conduct comprehensive literature research with target disambiguation, evidence grading, and structured theme extraction.... |

#### Genomic & Clinical Databases

| Skill | Description |
|-------|-------------|
| [`clinical-trials-search`](skills/literature/clinical-trials-search/SKILL.md) | Search ClinicalTrials.gov with natural language queries. Find clinical trials, enrollment, and outcomes using Valyu sema... |
| [`clinicaltrials-database`](skills/literature/clinicaltrials-database/SKILL.md) | Query ClinicalTrials.gov via API v2. Search trials by condition, drug, location, status, or phase. Retrieve trial detail... |
| [`clinvar-database`](skills/literature/clinvar-database/SKILL.md) | Query NCBI ClinVar for variant clinical significance. Search by gene/position, interpret pathogenicity classifications, ... |
| [`gene-database`](skills/literature/gene-database/SKILL.md) | Query NCBI Gene via E-utilities/Datasets API. Search by symbol/ID, retrieve gene info (RefSeqs, GO, locations, phenotype... |
| [`geo-database`](skills/literature/geo-database/SKILL.md) | Access NCBI GEO for gene expression/genomics data. Search/download microarray and RNA-seq datasets (GSE, GSM, GPL), retr... |
| [`gwas-database`](skills/literature/gwas-database/SKILL.md) | Query NHGRI-EBI GWAS Catalog for SNP-trait associations. Search variants by rs ID, disease/trait, gene, retrieve p-value... |
| [`hmdb-database`](skills/literature/hmdb-database/SKILL.md) | Access Human Metabolome Database (220K+ metabolites). Search by name/ID/structure, retrieve chemical properties, biomark... |
| [`openalex-database`](skills/literature/openalex-database/SKILL.md) | Query and analyze scholarly literature using the OpenAlex database. This skill should be used when searching for academi... |
| [`pdb-database`](skills/literature/pdb-database/SKILL.md) | Access RCSB PDB for 3D protein/nucleic acid structures. Search by text/sequence/structure, download coordinates (PDB/mmC... |

#### Multi-Source Search & Discovery

| Skill | Description |
|-------|-------------|
| [`arxiv-search`](skills/literature/arxiv-search/SKILL.md) | Search arXiv physics, math, and computer science preprints using natural language queries. Powered by Valyu semantic sea... |
| [`bioservices`](skills/literature/bioservices/SKILL.md) | Unified Python interface to 40+ bioinformatics services. Use when querying multiple databases (UniProt, KEGG, ChEMBL, Re... |
| [`perplexity-search`](skills/literature/perplexity-search/SKILL.md) | Perform AI-powered web searches with real-time information using Perplexity models via LiteLLM and OpenRouter. This skil... |
| [`research-lookup`](skills/literature/research-lookup/SKILL.md) | Look up current research information using Perplexity Sonar Pro Search or Sonar Reasoning Pro models through OpenRouter.... |

#### Patents, Grants & Citation Management

| Skill | Description |
|-------|-------------|
| [`citation-management`](skills/literature/citation-management/SKILL.md) | Comprehensive citation management for academic research. Search Google Scholar and PubMed for papers, extract accurate m... |
| [`patents-search`](skills/literature/patents-search/SKILL.md) | Search global patents with natural language queries. Prior art, patent landscapes, and innovation tracking via Valyu. |
| [`research-grants`](skills/literature/research-grants/SKILL.md) | Write competitive research proposals for NSF, NIH, DOE, DARPA, and Taiwan NSTC. Agency-specific formatting, review crite... |
| [`review-writing`](skills/literature/review-writing/SKILL.md) | Use this skill when the user asks to write a literature review, review article, or 综述 based on an outline. Trigger keywo... |
| [`uspto-database`](skills/literature/uspto-database/SKILL.md) | Access USPTO APIs for patent/trademark searches, examination history (PEDS), assignments, citations, office actions, TSD... |

</details>

---

## Skill Format

Every `SKILL.md` follows a consistent structure:

```markdown
# Skill Name
## Overview        — what this skill enables
## When to Use     — trigger conditions for the AI agent
## Key Capabilities — specific tools, APIs, parameters
## Usage Examples  — concrete code or workflow examples
```

## Credits

Skills curated by Yingcheng (Charles) Wu, Jinglin Jian, Zhe Zhao at Le Cong Lab of Stanford & Mengdi Wang Lab at Princeton.

## License

[MIT License](LICENSE)


## Star History

[![Star History Chart](https://api.star-history.com/image?repos=wu-yc/LabClaw&type=date&legend=top-left)](https://www.star-history.com/?repos=wu-yc%2FLabClaw&type=date&legend=top-left)
