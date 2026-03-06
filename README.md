# LabClaw Skills Library

> **231 curated AI agent skills** for scientific research — organized from [ScienceClaw](https://github.com/Zaoqu-Liu/ScienceClaw) into five focused domains.

[![Skills](https://img.shields.io/badge/skills-231-blue?style=flat-square)](skills/)
[![Biology](https://img.shields.io/badge/biology-87-brightgreen?style=flat-square)](skills/bio/)
[![Medicine](https://img.shields.io/badge/medicine-32-red?style=flat-square)](skills/med/)
[![General](https://img.shields.io/badge/general-61-orange?style=flat-square)](skills/general/)
[![Literature](https://img.shields.io/badge/literature-38-purple?style=flat-square)](skills/literature/)
[![License](https://img.shields.io/badge/license-MIT-yellow?style=flat-square)](LICENSE)

---

## Overview

Each skill is a `SKILL.md` file that tells an AI agent (Claude, GPT-4, Gemini, etc.) **when** and **how** to use a specific scientific tool, database, or methodology. Skills cover the full research lifecycle — from literature search and data analysis to visualization and manuscript writing.

**Skills are organized into five domains:**

| Domain | Skills | Description |
|--------|--------|-------------|
| [🧬 Biology](skills/bio/) | 87 | Genomics, proteomics, single-cell, structural biology, cheminformatics |
| [🏥 Medicine](skills/med/) | 32 | Clinical research, drug discovery, precision medicine, pharmacology |
| [⚙️ General](skills/general/) | 61 | Statistics, machine learning, visualization, scientific writing |
| [📚 Literature](skills/literature/) | 38 | Academic search, databases, citation management, literature review |
| [🔬 Other](skills/other/) | 13 | Quantum computing, materials science, astronomy, physical sciences |

---

## Repository Structure

```
LabClaw-git/
├── README.md
└── skills/
    ├── bio/                    # 87 biology & life sciences skills
    │   ├── scanpy/SKILL.md
    │   ├── rdkit/SKILL.md
    │   └── ...
    ├── med/                    # 32 medical & clinical skills
    │   ├── clinical/SKILL.md
    │   └── ...
    ├── general/                # 61 general & data science skills
    │   ├── statistics/SKILL.md
    │   └── ...
    ├── literature/             # 38 literature & search skills
    │   ├── pubmed-search/SKILL.md
    │   └── ...
    └── other/                  # 13 specialized science skills
        ├── astropy/SKILL.md
        └── ...
```

---

## Table of Contents

- [🧬 Biology & Life Sciences](#biologylifesciences) — **87 skills**
- [🏥 Medical & Clinical](#medicalclinical) — **32 skills**
- [⚙️ General & Data Science](#generaldatascience) — **61 skills**
- [📚 Literature & Search](#literaturesearch) — **38 skills**
- [🔬 Other Sciences](#othersciences) — **13 skills**

---

## How to Use

### With an AI Agent (Claude / GPT-4 / Gemini)

Prepend any `SKILL.md` as a system prompt before your request:

```python
import openai, pathlib

skill = pathlib.Path("skills/bio/scanpy/SKILL.md").read_text()
client = openai.OpenAI()
response = client.chat.completions.create(
    model="gpt-4o",
    messages=[
        {"role": "system", "content": skill},
        {"role": "user", "content": "Analyze my scRNA-seq data in data.h5ad"}
    ]
)
```

### With ScienceClaw (Full Platform)

```bash
git clone https://github.com/Zaoqu-Liu/ScienceClaw.git
cd ScienceClaw && bash scripts/setup.sh
scienceclaw skills scanpy    # search skill library
scienceclaw tui              # open chat with Monica (orchestrator)
```

### With Cursor / Windsurf

Place any `SKILL.md` into `.cursor/skills/` for automatic skill loading in the IDE.

---

---

## 🧬 Biology & Life Sciences

> Tools for genomics, transcriptomics, proteomics, single-cell analysis, structural biology, cheminformatics, and computational biology.

**87 skills** · [`skills/bio/`](skills/bio/)

| Skill | Title | Description |
|-------|-------|-------------|
| [`adaptyv`](skills/bio/adaptyv/SKILL.md) | Adaptyv | Cloud laboratory platform for automated protein testing and validation. Use when designing proteins and needin... |
| [`alphafold-database`](skills/bio/alphafold-database/SKILL.md) | AlphaFold Database | Access AlphaFold 200M+ AI-predicted protein structures. Retrieve structures by UniProt ID, download PDB/mmCIF ... |
| [`anndata`](skills/bio/anndata/SKILL.md) | AnnData | Data structure for annotated matrices in single-cell analysis. Use when working with .h5ad files or integratin... |
| [`arboreto`](skills/bio/arboreto/SKILL.md) | Arboreto | Infer gene regulatory networks (GRNs) from gene expression data using scalable algorithms (GRNBoost2, GENIE3).... |
| [`benchling-integration`](skills/bio/benchling-integration/SKILL.md) | Benchling Integration | Benchling R&D platform integration. Access registry (DNA, proteins), inventory, ELN entries, workflows via API... |
| [`bioinformatics`](skills/bio/bioinformatics/SKILL.md) | Bioinformatics Analysis | Computational biology and genomics analysis pipelines. GENERAL: not locked to any specific tool — use Scanpy, ... |
| [`biomni`](skills/bio/biomni/SKILL.md) | Biomni | Autonomous biomedical AI agent framework for executing complex research tasks across genomics, drug discovery,... |
| [`biopython`](skills/bio/biopython/SKILL.md) | Biopython: Computational Molecular Biology in Python | Comprehensive molecular biology toolkit. Use for sequence manipulation, file parsing (FASTA/GenBank/PDB), phyl... |
| [`brenda-database`](skills/bio/brenda-database/SKILL.md) | BRENDA Database | Access BRENDA enzyme database via SOAP API. Retrieve kinetic parameters (Km, kcat), reaction equations, organi... |
| [`cellxgene-census`](skills/bio/cellxgene-census/SKILL.md) | CZ CELLxGENE Census | Query the CELLxGENE Census (61M+ cells) programmatically. Use when you need expression data across tissues, di... |
| [`chemistry`](skills/bio/chemistry/SKILL.md) | Chemistry & Drug Discovery | Computational chemistry, cheminformatics, and drug discovery workflows. |
| [`clinpgx-database`](skills/bio/clinpgx-database/SKILL.md) | ClinPGx Database | Access ClinPGx pharmacogenomics data (successor to PharmGKB). Query gene-drug interactions, CPIC guidelines, a... |
| [`cobrapy`](skills/bio/cobrapy/SKILL.md) | COBRApy - Constraint-Based Reconstruction and Analysis | Constraint-based metabolic modeling (COBRA). FBA, FVA, gene knockouts, flux sampling, SBML models, for systems... |
| [`cosmic-database`](skills/bio/cosmic-database/SKILL.md) | COSMIC Database | Access COSMIC cancer mutation database. Query somatic mutations, Cancer Gene Census, mutational signatures, ge... |
| [`datamol`](skills/bio/datamol/SKILL.md) | Datamol Cheminformatics Skill | Pythonic wrapper around RDKit with simplified interface and sensible defaults. Preferred for standard drug dis... |
| [`deepchem`](skills/bio/deepchem/SKILL.md) | DeepChem | Molecular ML with diverse featurizers and pre-built datasets. Use for property prediction (ADMET, toxicity) wi... |
| [`deeptools`](skills/bio/deeptools/SKILL.md) | deepTools: NGS Data Analysis Toolkit | NGS analysis toolkit. BAM to bigWig conversion, QC (correlation, PCA, fingerprints), heatmaps/profiles (TSS, p... |
| [`diffdock`](skills/bio/diffdock/SKILL.md) | DiffDock: Molecular Docking with Diffusion Models | Diffusion-based molecular docking. Predict protein-ligand binding poses from PDB/SMILES, confidence scores, vi... |
| [`dnanexus-integration`](skills/bio/dnanexus-integration/SKILL.md) | DNAnexus Integration | DNAnexus cloud genomics platform. Build apps/applets, manage data (upload/download), dxpy Python SDK, run work... |
| [`drugbank-database`](skills/bio/drugbank-database/SKILL.md) | DrugBank Database | Access and analyze comprehensive drug information from the DrugBank database including drug properties, intera... |
| [`ena-database`](skills/bio/ena-database/SKILL.md) | ENA Database | Access European Nucleotide Archive via API/FTP. Retrieve DNA/RNA sequences, raw reads (FASTQ), genome assembli... |
| [`ensembl-database`](skills/bio/ensembl-database/SKILL.md) | Ensembl Database | Query Ensembl genome database REST API for 250+ species. Gene lookups, sequence retrieval, variant analysis, c... |
| [`esm`](skills/bio/esm/SKILL.md) | ESM: Evolutionary Scale Modeling | Comprehensive toolkit for protein language models including ESM3 (generative multimodal protein design across ... |
| [`etetoolkit`](skills/bio/etetoolkit/SKILL.md) | ETE Toolkit Skill | Phylogenetic tree toolkit (ETE). Tree manipulation (Newick/NHX), evolutionary event detection, orthology/paral... |
| [`fda-database`](skills/bio/fda-database/SKILL.md) | FDA Database Access | Query openFDA API for drugs, devices, adverse events, recalls, regulatory submissions (510k, PMA), substance i... |
| [`flowio`](skills/bio/flowio/SKILL.md) | FlowIO: Flow Cytometry Standard File Handler | Parse FCS (Flow Cytometry Standard) files v2.0-3.1. Extract events as NumPy arrays, read metadata/channels, co... |
| [`geniml`](skills/bio/geniml/SKILL.md) | Geniml: Genomic Interval Machine Learning | This skill should be used when working with genomic interval data (BED files) for machine learning tasks. Use ... |
| [`gget`](skills/bio/gget/SKILL.md) | gget | Fast CLI/Python queries to 20+ bioinformatics databases. Use for quick lookups: gene info, BLAST searches, Alp... |
| [`gtars`](skills/bio/gtars/SKILL.md) | Gtars: Genomic Tools and Algorithms in Rust | High-performance toolkit for genomic interval analysis in Rust with Python bindings. Use when working with gen... |
| [`histolab`](skills/bio/histolab/SKILL.md) | Histolab | Lightweight WSI tile extraction and preprocessing. Use for basic slide processing tissue detection, tile extra... |
| [`hypogenic`](skills/bio/hypogenic/SKILL.md) | Hypogenic | Automated LLM-driven hypothesis generation and testing on tabular datasets. Use when you want to systematicall... |
| [`kegg-database`](skills/bio/kegg-database/SKILL.md) | KEGG Database | Direct REST API access to KEGG (academic use only). Pathway analysis, gene-pathway mapping, metabolic pathways... |
| [`labarchive-integration`](skills/bio/labarchive-integration/SKILL.md) | LabArchives Integration | Electronic lab notebook API integration. Access notebooks, manage entries/attachments, backup notebooks, integ... |
| [`lamindb`](skills/bio/lamindb/SKILL.md) | LaminDB | This skill should be used when working with LaminDB, an open-source data framework for biology that makes data... |
| [`latchbio-integration`](skills/bio/latchbio-integration/SKILL.md) | LatchBio Integration | Latch platform for bioinformatics workflows. Build pipelines with Latch SDK, @workflow/@task decorators, deplo... |
| [`matchms`](skills/bio/matchms/SKILL.md) | Matchms | Spectral similarity and compound identification for metabolomics. Use for comparing mass spectra, computing si... |
| [`medchem`](skills/bio/medchem/SKILL.md) | Medchem | Medicinal chemistry filters. Apply drug-likeness rules (Lipinski, Veber), PAINS filters, structural alerts, co... |
| [`metabolomics-workbench-database`](skills/bio/metabolomics-workbench-database/SKILL.md) | Metabolomics Workbench Database | Access NIH Metabolomics Workbench via REST API (4,200+ studies). Query metabolites, RefMet nomenclature, MS/NM... |
| [`molfeat`](skills/bio/molfeat/SKILL.md) | Molfeat - Molecular Featurization Hub | Molecular featurization for ML (100+ featurizers). ECFP, MACCS, descriptors, pretrained models (ChemBERTa), co... |
| [`omero-integration`](skills/bio/omero-integration/SKILL.md) | OMERO Integration | Microscopy data management platform. Access images via Python, retrieve datasets, analyze pixels, manage ROIs/... |
| [`opentargets-database`](skills/bio/opentargets-database/SKILL.md) | Open Targets Database | Query Open Targets Platform for target-disease associations, drug target discovery, tractability/safety data, ... |
| [`pathml`](skills/bio/pathml/SKILL.md) | PathML | Full-featured computational pathology toolkit. Use for advanced WSI analysis including multiplexed immunofluor... |
| [`pydeseq2`](skills/bio/pydeseq2/SKILL.md) | PyDESeq2 | Differential gene expression analysis (Python DESeq2). Identify DE genes from bulk RNA-seq counts, Wald tests,... |
| [`pylabrobot`](skills/bio/pylabrobot/SKILL.md) | PyLabRobot | Vendor-agnostic lab automation framework. Use when controlling multiple equipment types (Hamilton, Tecan, Open... |
| [`pyopenms`](skills/bio/pyopenms/SKILL.md) | PyOpenMS | Complete mass spectrometry analysis platform. Use for proteomics workflows feature detection, peptide identifi... |
| [`pysam`](skills/bio/pysam/SKILL.md) | Pysam | Genomic file toolkit. Read/write SAM/BAM/CRAM alignments, VCF/BCF variants, FASTA/FASTQ sequences, extract reg... |
| [`pytdc`](skills/bio/pytdc/SKILL.md) | PyTDC (Therapeutics Data Commons) | Therapeutics Data Commons. AI-ready drug discovery datasets (ADME, toxicity, DTI), benchmarks, scaffold splits... |
| [`rdkit`](skills/bio/rdkit/SKILL.md) | RDKit Cheminformatics Toolkit | Cheminformatics toolkit for fine-grained molecular control. SMILES/SDF parsing, descriptors (MW, LogP, TPSA), ... |
| [`reactome-database`](skills/bio/reactome-database/SKILL.md) | Reactome Database | Query Reactome REST API for pathway analysis, enrichment, gene-pathway mapping, disease pathways, molecular in... |
| [`rowan`](skills/bio/rowan/SKILL.md) | Rowan: Cloud-Based Quantum Chemistry Platform | Cloud-based quantum chemistry platform with Python API. Preferred for computational chemistry workflows includ... |
| [`scanpy`](skills/bio/scanpy/SKILL.md) | Scanpy: Single-Cell Analysis | Standard single-cell RNA-seq analysis pipeline. Use for QC, normalization, dimensionality reduction (PCA/UMAP/... |
| [`scikit-bio`](skills/bio/scikit-bio/SKILL.md) | scikit-bio | Biological data toolkit. Sequence analysis, alignments, phylogenetic trees, diversity metrics (alpha/beta, Uni... |
| [`scvi-tools`](skills/bio/scvi-tools/SKILL.md) | scvi-tools | Deep generative models for single-cell omics. Use when you need probabilistic batch correction (scVI), transfe... |
| [`string-database`](skills/bio/string-database/SKILL.md) | STRING Database | Query STRING API for protein-protein interactions (59M proteins, 20B interactions). Network analysis, GO/KEGG ... |
| [`tooluniverse`](skills/bio/tooluniverse/SKILL.md) | ToolUniverse Router | Router skill for ToolUniverse tasks. First checks if specialized tooluniverse skills (34+ skills covering dise... |
| [`tooluniverse-crispr-screen-analysis`](skills/bio/tooluniverse-crispr-screen-analysis/SKILL.md) | ToolUniverse CRISPR Screen Analysis | Comprehensive CRISPR screen analysis for functional genomics. Analyze pooled or arrayed CRISPR screens (knocko... |
| [`tooluniverse-epigenomics`](skills/bio/tooluniverse-epigenomics/SKILL.md) | Genomics and Epigenomics Data Processing | Production-ready genomics and epigenomics data processing for BixBench questions. Handles methylation array an... |
| [`tooluniverse-expression-data-retrieval`](skills/bio/tooluniverse-expression-data-retrieval/SKILL.md) | Gene Expression & Omics Data Retrieval | Retrieves gene expression and omics datasets from ArrayExpress and BioStudies with gene disambiguation, experi... |
| [`tooluniverse-gene-enrichment`](skills/bio/tooluniverse-gene-enrichment/SKILL.md) | Gene Enrichment and Pathway Analysis | Perform comprehensive gene enrichment and pathway analysis using gseapy (ORA and GSEA), PANTHER, STRING, React... |
| [`tooluniverse-gwas-drug-discovery`](skills/bio/tooluniverse-gwas-drug-discovery/SKILL.md) | GWAS-to-Drug Target Discovery | Transform GWAS signals into actionable drug targets and repurposing opportunities. Performs locus-to-gene mapp... |
| [`tooluniverse-gwas-finemapping`](skills/bio/tooluniverse-gwas-finemapping/SKILL.md) | GWAS Fine-Mapping & Causal Variant Prioritization | Identify and prioritize causal variants at GWAS loci using statistical fine-mapping and locus-to-gene predicti... |
| [`tooluniverse-gwas-snp-interpretation`](skills/bio/tooluniverse-gwas-snp-interpretation/SKILL.md) | GWAS SNP Interpretation Skill | Interpret genetic variants (SNPs) from GWAS studies by aggregating evidence from multiple databases (GWAS Cata... |
| [`tooluniverse-gwas-study-explorer`](skills/bio/tooluniverse-gwas-study-explorer/SKILL.md) | GWAS Study Deep Dive & Meta-Analysis | Compare GWAS studies, perform meta-analyses, and assess replication across cohorts. Integrates NHGRI-EBI GWAS ... |
| [`tooluniverse-gwas-trait-to-gene`](skills/bio/tooluniverse-gwas-trait-to-gene/SKILL.md) | GWAS Trait-to-Gene Discovery | Discover genes associated with diseases and traits using GWAS data from the GWAS Catalog (500,000+ association... |
| [`tooluniverse-immune-repertoire-analysis`](skills/bio/tooluniverse-immune-repertoire-analysis/SKILL.md) | ToolUniverse Immune Repertoire Analysis | Comprehensive immune repertoire analysis for T-cell and B-cell receptor sequencing data. Analyze TCR/BCR reper... |
| [`tooluniverse-metabolomics`](skills/bio/tooluniverse-metabolomics/SKILL.md) | Metabolomics Research | Comprehensive metabolomics research skill for identifying metabolites, analyzing studies, and searching metabo... |
| [`tooluniverse-metabolomics-analysis`](skills/bio/tooluniverse-metabolomics-analysis/SKILL.md) | Metabolomics Analysis | Analyze metabolomics data including metabolite identification, quantification, pathway analysis, and metabolic... |
| [`tooluniverse-multi-omics-integration`](skills/bio/tooluniverse-multi-omics-integration/SKILL.md) | Multi-Omics Integration | Integrate and analyze multiple omics datasets (transcriptomics, proteomics, epigenomics, genomics, metabolomic... |
| [`tooluniverse-multiomic-disease-characterization`](skills/bio/tooluniverse-multiomic-disease-characterization/SKILL.md) | Multi-Omics Disease Characterization Pipeline | Comprehensive multi-omics disease characterization integrating genomics, transcriptomics, proteomics, pathway,... |
| [`tooluniverse-phylogenetics`](skills/bio/tooluniverse-phylogenetics/SKILL.md) | Phylogenetics and Sequence Analysis | Production-ready phylogenetics and sequence analysis skill for alignment processing, tree analysis, and evolut... |
| [`tooluniverse-polygenic-risk-score`](skills/bio/tooluniverse-polygenic-risk-score/SKILL.md) | Polygenic Risk Score (PRS) Builder | Build and interpret polygenic risk scores (PRS) for complex diseases using GWAS summary statistics. Calculates... |
| [`tooluniverse-protein-interactions`](skills/bio/tooluniverse-protein-interactions/SKILL.md) | Protein Interaction Network Analysis | Analyze protein-protein interaction networks using STRING, BioGRID, and SASBDB databases. Maps protein identif... |
| [`tooluniverse-protein-structure-retrieval`](skills/bio/tooluniverse-protein-structure-retrieval/SKILL.md) | Protein Structure Data Retrieval | Retrieves protein structure data from RCSB PDB, PDBe, and AlphaFold with protein disambiguation, quality asses... |
| [`tooluniverse-proteomics-analysis`](skills/bio/tooluniverse-proteomics-analysis/SKILL.md) | Proteomics Analysis | Analyze mass spectrometry proteomics data including protein quantification, differential expression, post-tran... |
| [`tooluniverse-rnaseq-deseq2`](skills/bio/tooluniverse-rnaseq-deseq2/SKILL.md) | RNA-seq Differential Expression Analysis (DESeq2) | Production-ready RNA-seq differential expression analysis using PyDESeq2. Performs DESeq2 normalization, dispe... |
| [`tooluniverse-sequence-retrieval`](skills/bio/tooluniverse-sequence-retrieval/SKILL.md) | Biological Sequence Retrieval | Retrieves biological sequences (DNA, RNA, protein) from NCBI and ENA with gene disambiguation, accession type ... |
| [`tooluniverse-single-cell`](skills/bio/tooluniverse-single-cell/SKILL.md) | Single-Cell Genomics and Expression Matrix Analysis | Production-ready single-cell and expression matrix analysis using scanpy, anndata, and scipy. Performs scRNA-s... |
| [`tooluniverse-spatial-omics-analysis`](skills/bio/tooluniverse-spatial-omics-analysis/SKILL.md) | Spatial Multi-Omics Analysis Pipeline | Computational analysis framework for spatial multi-omics data integration. Given spatially variable genes (SVG... |
| [`tooluniverse-spatial-transcriptomics`](skills/bio/tooluniverse-spatial-transcriptomics/SKILL.md) | Spatial Transcriptomics Analysis | Analyze spatial transcriptomics data to map gene expression in tissue architecture. Supports 10x Visium, MERFI... |
| [`tooluniverse-structural-variant-analysis`](skills/bio/tooluniverse-structural-variant-analysis/SKILL.md) | Structural Variant Analysis Workflow | Comprehensive structural variant (SV) analysis skill for clinical genomics. Classifies SVs (deletions, duplica... |
| [`tooluniverse-systems-biology`](skills/bio/tooluniverse-systems-biology/SKILL.md) | Systems Biology & Pathway Analysis | Comprehensive systems biology and pathway analysis using multiple pathway databases (Reactome, KEGG, WikiPathw... |
| [`tooluniverse-variant-analysis`](skills/bio/tooluniverse-variant-analysis/SKILL.md) | Variant Analysis and Annotation | Production-ready VCF processing, variant annotation, mutation analysis, and structural variant (SV/CNV) interp... |
| [`tooluniverse-variant-interpretation`](skills/bio/tooluniverse-variant-interpretation/SKILL.md) | tooluniverse-variant-interpretation | Systematic clinical variant interpretation from raw variant calls to ACMG-classified recommendations with stru... |
| [`torch_geometric`](skills/bio/torch_geometric/SKILL.md) | PyTorch Geometric (PyG) | Graph Neural Networks (PyG). Node/graph classification, link prediction, GCN, GAT, GraphSAGE, heterogeneous gr... |
| [`torchdrug`](skills/bio/torchdrug/SKILL.md) | TorchDrug | PyTorch-native graph neural networks for molecules and proteins. Use when building custom GNN architectures fo... |
| [`umap-learn`](skills/bio/umap-learn/SKILL.md) | UMAP-Learn | UMAP dimensionality reduction. Fast nonlinear manifold learning for 2D/3D visualization, clustering preprocess... |
| [`uniprot-database`](skills/bio/uniprot-database/SKILL.md) | UniProt Database | Direct REST API access to UniProt. Protein searches, FASTA retrieval, ID mapping, Swiss-Prot/TrEMBL. For Pytho... |
---

## 🏥 Medical & Clinical

> Tools for clinical research, drug discovery, precision medicine, oncology, pharmacology, and medical imaging.

**32 skills** · [`skills/med/`](skills/med/)

| Skill | Title | Description |
|-------|-------|-------------|
| [`clinical`](skills/med/clinical/SKILL.md) | Clinical Research | Clinical study design, statistical analysis, and regulatory compliance for medical research. |
| [`clinical-decision-support`](skills/med/clinical-decision-support/SKILL.md) | Clinical Decision Support Documents | Generate professional clinical decision support (CDS) documents for pharmaceutical and clinical research setti... |
| [`clinical-reports`](skills/med/clinical-reports/SKILL.md) | Clinical Report Writing | Write comprehensive clinical reports including case reports (CARE guidelines), diagnostic reports (radiology/p... |
| [`neurokit2`](skills/med/neurokit2/SKILL.md) | NeuroKit2 | Comprehensive biosignal processing toolkit for analyzing physiological data including ECG, EEG, EDA, RSP, PPG,... |
| [`neuropixels-analysis`](skills/med/neuropixels-analysis/SKILL.md) | Neuropixels Data Analysis | Neuropixels neural recording analysis. Load SpikeGLX/OpenEphys data, preprocess, motion correction, Kilosort4 ... |
| [`pydicom`](skills/med/pydicom/SKILL.md) | Pydicom | Python library for working with DICOM (Digital Imaging and Communications in Medicine) files. Use this skill w... |
| [`pyhealth`](skills/med/pyhealth/SKILL.md) | PyHealth: Healthcare AI Toolkit | Comprehensive healthcare AI toolkit for developing, testing, and deploying machine learning models with clinic... |
| [`scientific-schematics`](skills/med/scientific-schematics/SKILL.md) | Scientific Schematics and Diagrams | Create publication-quality scientific diagrams using Nano Banana Pro AI with smart iterative refinement. Uses ... |
| [`tooluniverse-adverse-event-detection`](skills/med/tooluniverse-adverse-event-detection/SKILL.md) | Adverse Drug Event Signal Detection & Analysis | Detect and analyze adverse drug event signals using FDA FAERS data, drug labels, disproportionality analysis (... |
| [`tooluniverse-antibody-engineering`](skills/med/tooluniverse-antibody-engineering/SKILL.md) | Antibody Engineering & Optimization | Comprehensive antibody engineering and optimization for therapeutic development. Covers humanization, affinity... |
| [`tooluniverse-binder-discovery`](skills/med/tooluniverse-binder-discovery/SKILL.md) | Small Molecule Binder Discovery Strategy | Discover novel small molecule binders for protein targets using structure-based and ligand-based approaches. C... |
| [`tooluniverse-cancer-variant-interpretation`](skills/med/tooluniverse-cancer-variant-interpretation/SKILL.md) | Cancer Variant Interpretation for Precision Oncology | Provide comprehensive clinical interpretation of somatic mutations in cancer. Given a gene symbol + variant (e... |
| [`tooluniverse-chemical-safety`](skills/med/tooluniverse-chemical-safety/SKILL.md) | Chemical Safety & Toxicology Assessment | Comprehensive chemical safety and toxicology assessment integrating ADMET-AI predictions, CTD toxicogenomics, ... |
| [`tooluniverse-clinical-guidelines`](skills/med/tooluniverse-clinical-guidelines/SKILL.md) | Clinical Guidelines Search & Retrieval | Search and retrieve clinical practice guidelines across 12+ authoritative sources including NICE, WHO, ADA, AH... |
| [`tooluniverse-clinical-trial-design`](skills/med/tooluniverse-clinical-trial-design/SKILL.md) | Clinical Trial Design Feasibility Assessment | Strategic clinical trial design feasibility assessment using ToolUniverse. Evaluates patient population sizing... |
| [`tooluniverse-clinical-trial-matching`](skills/med/tooluniverse-clinical-trial-matching/SKILL.md) | Clinical Trial Matching for Precision Medicine | AI-driven patient-to-trial matching for precision medicine and oncology. Given a patient profile (disease, mol... |
| [`tooluniverse-disease-research`](skills/med/tooluniverse-disease-research/SKILL.md) | ToolUniverse Disease Research | Generate comprehensive disease research reports using 100+ ToolUniverse tools. Creates a detailed markdown rep... |
| [`tooluniverse-drug-drug-interaction`](skills/med/tooluniverse-drug-drug-interaction/SKILL.md) | Drug-Drug Interaction Prediction & Risk Assessment | Comprehensive drug-drug interaction (DDI) prediction and risk assessment. Analyzes interaction mechanisms (CYP... |
| [`tooluniverse-drug-repurposing`](skills/med/tooluniverse-drug-repurposing/SKILL.md) | Drug Repurposing with ToolUniverse | Identify drug repurposing candidates using ToolUniverse for target-based, compound-based, and disease-driven s... |
| [`tooluniverse-drug-research`](skills/med/tooluniverse-drug-research/SKILL.md) | Drug Research Strategy | Generates comprehensive drug research reports with compound disambiguation, evidence grading, and mandatory co... |
| [`tooluniverse-drug-target-validation`](skills/med/tooluniverse-drug-target-validation/SKILL.md) | Drug Target Validation Pipeline | Comprehensive computational validation of drug targets for early-stage drug discovery. Evaluates targets acros... |
| [`tooluniverse-image-analysis`](skills/med/tooluniverse-image-analysis/SKILL.md) | Microscopy Image Analysis and Quantitative Imaging Data | Production-ready microscopy image analysis and quantitative imaging data skill for colony morphometry, cell co... |
| [`tooluniverse-immunotherapy-response-prediction`](skills/med/tooluniverse-immunotherapy-response-prediction/SKILL.md) | Immunotherapy Response Prediction | Predict patient response to immune checkpoint inhibitors (ICIs) using multi-biomarker integration. Given a can... |
| [`tooluniverse-infectious-disease`](skills/med/tooluniverse-infectious-disease/SKILL.md) | Infectious Disease Outbreak Intelligence | Rapid pathogen characterization and drug repurposing analysis for infectious disease outbreaks. Identifies pat... |
| [`tooluniverse-network-pharmacology`](skills/med/tooluniverse-network-pharmacology/SKILL.md) | Network Pharmacology Pipeline | Construct and analyze compound-target-disease networks for drug repurposing, polypharmacology discovery, and s... |
| [`tooluniverse-pharmacovigilance`](skills/med/tooluniverse-pharmacovigilance/SKILL.md) | Pharmacovigilance Safety Analyzer | Analyze drug safety signals from FDA adverse event reports, label warnings, and pharmacogenomic data. Calculat... |
| [`tooluniverse-precision-medicine-stratification`](skills/med/tooluniverse-precision-medicine-stratification/SKILL.md) | Precision Medicine Patient Stratification | Comprehensive patient stratification for precision medicine by integrating genomic, clinical, and therapeutic ... |
| [`tooluniverse-precision-oncology`](skills/med/tooluniverse-precision-oncology/SKILL.md) | Precision Oncology Treatment Advisor | Provide actionable treatment recommendations for cancer patients based on molecular profile. Interprets tumor ... |
| [`tooluniverse-protein-therapeutic-design`](skills/med/tooluniverse-protein-therapeutic-design/SKILL.md) | Therapeutic Protein Designer | Design novel protein therapeutics (binders, enzymes, scaffolds) using AI-guided de novo design. Uses RFdiffusi... |
| [`tooluniverse-rare-disease-diagnosis`](skills/med/tooluniverse-rare-disease-diagnosis/SKILL.md) | Rare Disease Diagnosis Advisor | Provide differential diagnosis for patients with suspected rare diseases based on phenotype and genetic data. ... |
| [`tooluniverse-target-research`](skills/med/tooluniverse-target-research/SKILL.md) | Comprehensive Target Intelligence Gatherer | Gather comprehensive biological target intelligence from 9 parallel research paths covering protein info, stru... |
| [`treatment-plans`](skills/med/treatment-plans/SKILL.md) | Treatment Plan Writing | Generate concise (3-4 page), focused medical treatment plans in LaTeX/PDF format for all clinical specialties.... |
---

## ⚙️ General & Data Science

> General-purpose tools for statistics, machine learning, visualization, scientific writing, and data management.

**61 skills** · [`skills/general/`](skills/general/)

| Skill | Title | Description |
|-------|-------|-------------|
| [`aeon`](skills/general/aeon/SKILL.md) | Aeon Time Series Machine Learning | This skill should be used for time series machine learning tasks including classification, regression, cluster... |
| [`article-writing`](skills/general/article-writing/SKILL.md) | Article Writing | Write articles, guides, blog posts, tutorials, newsletter issues, and other long-form content in a distinctive... |
| [`dask`](skills/general/dask/SKILL.md) | Dask | Distributed computing for larger-than-RAM pandas/NumPy workflows. Use when you need to scale existing pandas/N... |
| [`datacommons-client`](skills/general/datacommons-client/SKILL.md) | Data Commons Client | Work with Data Commons, a platform providing programmatic access to public statistical data from global source... |
| [`exploratory-data-analysis`](skills/general/exploratory-data-analysis/SKILL.md) | Exploratory Data Analysis | Perform comprehensive exploratory data analysis on scientific data files across 200+ file formats. This skill ... |
| [`fair-data`](skills/general/fair-data/SKILL.md) | FAIR Data Principles — Findable, Accessible, Interoperable, Reusable | Guidelines for making scientific data FAIR: Findable, Accessible, Interoperable, and Reusable. |
| [`frontend-slides`](skills/general/frontend-slides/SKILL.md) | Frontend Slides | Create stunning, animation-rich HTML presentations from scratch or by converting PowerPoint files. Use when th... |
| [`generate-image`](skills/general/generate-image/SKILL.md) | Generate Image | Generate or edit images using AI models (FLUX, Gemini). Use for general-purpose image generation including pho... |
| [`geopandas`](skills/general/geopandas/SKILL.md) | GeoPandas | Python library for working with geospatial vector data including shapefiles, GeoJSON, and GeoPackage files. Us... |
| [`get-available-resources`](skills/general/get-available-resources/SKILL.md) | Get Available Resources | This skill should be used at the start of any computationally intensive scientific task to detect and report a... |
| [`hypothesis-generation`](skills/general/hypothesis-generation/SKILL.md) | Scientific Hypothesis Generation | Structured hypothesis formulation from observations. Use when you have experimental observations or data and n... |
| [`latex-posters`](skills/general/latex-posters/SKILL.md) | LaTeX Research Posters | Create professional research posters in LaTeX using beamerposter, tikzposter, or baposter. Support for confere... |
| [`market-research-reports`](skills/general/market-research-reports/SKILL.md) | Market Research Reports | Generate comprehensive market research reports (50+ pages) in the style of top consulting firms (McKinsey, BCG... |
| [`markitdown`](skills/general/markitdown/SKILL.md) | MarkItDown - File to Markdown Conversion | Convert files and office documents to Markdown. Supports PDF, DOCX, PPTX, XLSX, images (with OCR), audio (with... |
| [`matlab`](skills/general/matlab/SKILL.md) | MATLAB/Octave Scientific Computing | MATLAB and GNU Octave numerical computing for matrix operations, data analysis, visualization, and scientific ... |
| [`matplotlib`](skills/general/matplotlib/SKILL.md) | Matplotlib | Low-level plotting library for full customization. Use when you need fine-grained control over every plot elem... |
| [`modal`](skills/general/modal/SKILL.md) | Modal | Run Python code in the cloud with serverless containers, GPUs, and autoscaling. Use when deploying ML models, ... |
| [`networkx`](skills/general/networkx/SKILL.md) | NetworkX | Comprehensive toolkit for creating, analyzing, and visualizing complex networks and graphs in Python. Use when... |
| [`nutrient-document-processing`](skills/general/nutrient-document-processing/SKILL.md) | Nutrient Document Processing | Process, convert, OCR, extract, redact, sign, and fill documents using the Nutrient DWS API. Works with PDFs, ... |
| [`paper-2-web`](skills/general/paper-2-web/SKILL.md) | Paper2All: Academic Paper Transformation Pipeline | This skill should be used when converting academic papers into promotional and presentation formats including ... |
| [`patent-drafting`](skills/general/patent-drafting/SKILL.md) | Patent Drafting — Intellectual Property Protection for Research | Draft patent applications for scientific inventions, covering claims, specification, and prior art analysis. |
| [`peer-review`](skills/general/peer-review/SKILL.md) | Scientific Critical Evaluation and Peer Review | Structured manuscript/grant review with checklist-based evaluation. Use when writing formal peer reviews with ... |
| [`plotly`](skills/general/plotly/SKILL.md) | Plotly | Interactive visualization library. Use when you need hover info, zoom, pan, or web-embeddable charts. Best for... |
| [`polars`](skills/general/polars/SKILL.md) | Polars | Fast in-memory DataFrame library for datasets that fit in RAM. Use when pandas is too slow but data still fits... |
| [`pptx-generation`](skills/general/pptx-generation/SKILL.md) | Academic Presentation Generation | Create publication-quality academic presentations (.pptx) for group meetings, thesis defenses, conference talk... |
| [`pptx-posters`](skills/general/pptx-posters/SKILL.md) | PPTX Research Posters (HTML-Based) | Create research posters using HTML/CSS that can be exported to PDF or PPTX. Use this skill ONLY when the user ... |
| [`protocol-writing`](skills/general/protocol-writing/SKILL.md) | Protocol Writing — Reproducible Lab Protocols & SOPs | Write clear, reproducible experimental protocols and Standard Operating Procedures (SOPs) for any scientific d... |
| [`pumc-create-docx`](skills/general/pumc-create-docx/SKILL.md) | Markdown 转协和博士论文 DOCX | 将markdown论文稿转换为符合北京协和医学院2025版博士学位论文格式规范的docx文件。当用户提到转docx、生成docx、导出Word、md转Word、格式化论文、create docx时触发。所有字体字号行距边... |
| [`pumc-thesis-review`](skills/general/pumc-thesis-review/SKILL.md) | 协和论文审核与修改 | 审核并修改已写好的协和医学院博士论文内容，检查格式规范、AI写作痕迹、学术表达质量，然后直接修改原文。当用户提到审核论文、检查论文、review论文、查AI味、去AI味、降AI率、论文审稿、帮我看看、检查格式、帮我改改时... |
| [`pumc-thesis-writing`](skills/general/pumc-thesis-writing/SKILL.md) | 协和医学院博士论文写作规范 | 按照北京协和医学院（PUMC）博士学位论文的严格格式规范撰写论文内容。当用户提到协和论文、协和格式、写论文、写前言、写结果、写讨论、写结论、去AI味、降AI率、PUMC thesis、协和参考论文、部分制论文时触发。基于... |
| [`pymc`](skills/general/pymc/SKILL.md) | PyMC Bayesian Modeling | Bayesian modeling with PyMC. Build hierarchical models, MCMC (NUTS), variational inference, LOO/WAIC compariso... |
| [`pymoo`](skills/general/pymoo/SKILL.md) | Pymoo - Multi-Objective Optimization in Python | Multi-objective optimization framework. NSGA-II, NSGA-III, MOEA/D, Pareto fronts, constraint handling, benchma... |
| [`pytorch-lightning`](skills/general/pytorch-lightning/SKILL.md) | PyTorch Lightning | Deep learning framework (PyTorch Lightning). Organize PyTorch code into LightningModules, configure Trainers f... |
| [`regulatory-submission`](skills/general/regulatory-submission/SKILL.md) | Regulatory Submission — FDA/EMA Dossier Structure | Prepare regulatory submissions for drugs, biologics, devices, and diagnostics. |
| [`reproducibility-checklist`](skills/general/reproducibility-checklist/SKILL.md) | Reproducibility Checklist — Open Science Best Practices | Ensure research is reproducible, transparent, and meets open science standards. |
| [`scholar-evaluation`](skills/general/scholar-evaluation/SKILL.md) | Scholar Evaluation | Systematically evaluate scholarly work using the ScholarEval framework, providing structured assessment across... |
| [`science-communication`](skills/general/science-communication/SKILL.md) | Science Communication — Making Research Accessible | Translate complex scientific findings into engaging content for non-specialist audiences. |
| [`scienceclaw-aesthetics`](skills/general/scienceclaw-aesthetics/SKILL.md) | ScienceClaw Aesthetics — Publication-Quality Figure Standards | Rachel's aesthetic reference for all visualization work. Use this skill when generating any scientific figure. |
| [`scienceclaw-presentations`](skills/general/scienceclaw-presentations/SKILL.md) | ScienceClaw Presentations — Joey's PPT Templates | Joey's reference for all presentation work. Use this skill when creating academic presentations. |
| [`scientific-brainstorming`](skills/general/scientific-brainstorming/SKILL.md) | Scientific Brainstorming | Creative research ideation and exploration. Use for open-ended brainstorming sessions, exploring interdiscipli... |
| [`scientific-critical-thinking`](skills/general/scientific-critical-thinking/SKILL.md) | Scientific Critical Thinking | Evaluate scientific claims and evidence quality. Use for assessing experimental design validity, identifying b... |
| [`scientific-diagram-generation`](skills/general/scientific-diagram-generation/SKILL.md) | Scientific Diagram Generation | AI-powered scientific illustration generation using Gemini Image models. Creates publication-quality mechanism... |
| [`scientific-slides`](skills/general/scientific-slides/SKILL.md) | Scientific Slides | Build slide decks and presentations for research talks. Use this for making PowerPoint slides, conference pres... |
| [`scientific-visualization`](skills/general/scientific-visualization/SKILL.md) | Scientific Visualization | Meta-skill for publication-ready figures. Use when creating journal submission figures requiring multi-panel l... |
| [`scientific-writing`](skills/general/scientific-writing/SKILL.md) | Scientific Writing | Core skill for the deep research and writing tool. Write scientific manuscripts in full paragraphs (never bull... |
| [`scikit-learn`](skills/general/scikit-learn/SKILL.md) | Scikit-learn | Machine learning in Python with scikit-learn. Use when working with supervised learning (classification, regre... |
| [`scikit-survival`](skills/general/scikit-survival/SKILL.md) | scikit-survival: Survival Analysis in Python | Comprehensive toolkit for survival analysis and time-to-event modeling in Python using scikit-survival. Use th... |
| [`seaborn`](skills/general/seaborn/SKILL.md) | Seaborn Statistical Visualization | Statistical visualization with pandas integration. Use for quick exploration of distributions, relationships, ... |
| [`shap`](skills/general/shap/SKILL.md) | SHAP (SHapley Additive exPlanations) | Model interpretability and explainability using SHAP (SHapley Additive exPlanations). Use this skill when expl... |
| [`stable-baselines3`](skills/general/stable-baselines3/SKILL.md) | Stable Baselines3 | Production-ready reinforcement learning algorithms (PPO, SAC, DQN, TD3, DDPG, A2C) with scikit-learn-like API.... |
| [`statistical-analysis`](skills/general/statistical-analysis/SKILL.md) | Statistical Analysis | Guided statistical analysis with test selection and reporting. Use when you need help choosing appropriate tes... |
| [`statistics`](skills/general/statistics/SKILL.md) | Statistical Analysis & Quality Control | Comprehensive statistical methodology for scientific research. Covers test selection, assumption verification,... |
| [`statsmodels`](skills/general/statsmodels/SKILL.md) | Statsmodels: Statistical Modeling and Econometrics | Statistical models library for Python. Use when you need specific model classes (OLS, GLM, mixed models, ARIMA... |
| [`sympy`](skills/general/sympy/SKILL.md) | SymPy - Symbolic Mathematics in Python | Use this skill when working with symbolic mathematics in Python. This skill should be used for symbolic comput... |
| [`tooluniverse-statistical-modeling`](skills/general/tooluniverse-statistical-modeling/SKILL.md) | Statistical Modeling for Biomedical Data Analysis | Perform statistical modeling and regression analysis on biomedical datasets. Supports linear regression, logis... |
| [`transformers`](skills/general/transformers/SKILL.md) | Transformers | This skill should be used when working with pre-trained transformer models for natural language processing, co... |
| [`vaex`](skills/general/vaex/SKILL.md) | Vaex | Use this skill for processing and analyzing large tabular datasets (billions of rows) that exceed available RA... |
| [`venue-templates`](skills/general/venue-templates/SKILL.md) | Venue Templates | Access comprehensive LaTeX templates, formatting requirements, and submission guidelines for major scientific ... |
| [`visualization`](skills/general/visualization/SKILL.md) | Scientific Visualization | Publication-quality scientific figure generation. GENERAL: language-agnostic (R, Python, Julia, or any tool). |
| [`writing`](skills/general/writing/SKILL.md) | Academic Writing | Scientific manuscript writing across all formats, fields, and journals. |
| [`zarr-python`](skills/general/zarr-python/SKILL.md) | Zarr Python | Chunked N-D arrays for cloud storage. Compressed arrays, parallel I/O, S3/GCS integration, NumPy/Dask/Xarray c... |
---

## 📚 Literature & Search

> Tools for academic search, database queries, citation management, and literature review.

**38 skills** · [`skills/literature/`](skills/literature/)

| Skill | Title | Description |
|-------|-------|-------------|
| [`academic-literature-search`](skills/literature/academic-literature-search/SKILL.md) | Academic Literature Search — 学术文献检索与引用管理 | Use this skill when the user asks to search for academic papers, retrieve literature, generate citations, form... |
| [`arxiv-search`](skills/literature/arxiv-search/SKILL.md) | arxiv-search | Search arXiv physics, math, and computer science preprints using natural language queries. Powered by Valyu se... |
| [`biomedical-search`](skills/literature/biomedical-search/SKILL.md) | biomedical-search | Complete biomedical information search combining PubMed, preprints, clinical trials, and FDA drug labels. Powe... |
| [`biorxiv-database`](skills/literature/biorxiv-database/SKILL.md) | bioRxiv Database | Efficient database search tool for bioRxiv preprint server. Use this skill when searching for life sciences pr... |
| [`biorxiv-search`](skills/literature/biorxiv-search/SKILL.md) | biorxiv-search | Search bioRxiv biology preprints with natural language queries. Semantic search powered by Valyu. |
| [`bioservices`](skills/literature/bioservices/SKILL.md) | BioServices | Unified Python interface to 40+ bioinformatics services. Use when querying multiple databases (UniProt, KEGG, ... |
| [`chembl-database`](skills/literature/chembl-database/SKILL.md) | ChEMBL Database | Query ChEMBL bioactive molecules and drug discovery data. Search compounds by structure/properties, retrieve b... |
| [`chembl-search`](skills/literature/chembl-search/SKILL.md) | chembl-search | Search ChEMBL bioactive molecules database with natural language queries. Find compounds and assay data with V... |
| [`citation-management`](skills/literature/citation-management/SKILL.md) | Citation Management | Comprehensive citation management for academic research. Search Google Scholar and PubMed for papers, extract ... |
| [`clinical-trials-search`](skills/literature/clinical-trials-search/SKILL.md) | clinical-trials-search | Search ClinicalTrials.gov with natural language queries. Find clinical trials, enrollment, and outcomes using ... |
| [`clinicaltrials-database`](skills/literature/clinicaltrials-database/SKILL.md) | ClinicalTrials.gov Database | Query ClinicalTrials.gov via API v2. Search trials by condition, drug, location, status, or phase. Retrieve tr... |
| [`clinvar-database`](skills/literature/clinvar-database/SKILL.md) | ClinVar Database | Query NCBI ClinVar for variant clinical significance. Search by gene/position, interpret pathogenicity classif... |
| [`drug-discovery-search`](skills/literature/drug-discovery-search/SKILL.md) | drug-discovery-search | End-to-end drug discovery platform combining ChEMBL compounds, DrugBank, targets, and FDA labels. Natural lang... |
| [`drug-labels-search`](skills/literature/drug-labels-search/SKILL.md) | drug-labels-search | Search FDA drug labels with natural language queries. Official drug information, indications, and safety data ... |
| [`drugbank-search`](skills/literature/drugbank-search/SKILL.md) | drugbank-search | Search DrugBank comprehensive drug database with natural language queries. Drug mechanisms, interactions, and ... |
| [`gene-database`](skills/literature/gene-database/SKILL.md) | Gene Database | Query NCBI Gene via E-utilities/Datasets API. Search by symbol/ID, retrieve gene info (RefSeqs, GO, locations,... |
| [`geo-database`](skills/literature/geo-database/SKILL.md) | GEO Database | Access NCBI GEO for gene expression/genomics data. Search/download microarray and RNA-seq datasets (GSE, GSM, ... |
| [`gwas-database`](skills/literature/gwas-database/SKILL.md) | GWAS Catalog Database | Query NHGRI-EBI GWAS Catalog for SNP-trait associations. Search variants by rs ID, disease/trait, gene, retrie... |
| [`hmdb-database`](skills/literature/hmdb-database/SKILL.md) | HMDB Database | Access Human Metabolome Database (220K+ metabolites). Search by name/ID/structure, retrieve chemical propertie... |
| [`literature`](skills/literature/literature/SKILL.md) | Literature Search & Review | Comprehensive academic literature search and synthesis across 15+ sources. |
| [`literature-review`](skills/literature/literature-review/SKILL.md) | Literature Review | Conduct comprehensive, systematic literature reviews using multiple academic databases (PubMed, arXiv, bioRxiv... |
| [`literature-search`](skills/literature/literature-search/SKILL.md) | literature-search | Comprehensive scientific literature search across PubMed, arXiv, bioRxiv, medRxiv. Natural language queries po... |
| [`medrxiv-search`](skills/literature/medrxiv-search/SKILL.md) | medrxiv-search | Search medRxiv medical preprints with natural language queries. Powered by Valyu semantic search. |
| [`open-targets-search`](skills/literature/open-targets-search/SKILL.md) | open-targets-search | Search Open Targets drug-disease associations with natural language queries. Target validation powered by Valy... |
| [`openalex-database`](skills/literature/openalex-database/SKILL.md) | OpenAlex Database | Query and analyze scholarly literature using the OpenAlex database. This skill should be used when searching f... |
| [`patents-search`](skills/literature/patents-search/SKILL.md) | patents-search | Search global patents with natural language queries. Prior art, patent landscapes, and innovation tracking via... |
| [`pdb-database`](skills/literature/pdb-database/SKILL.md) | PDB Database | Access RCSB PDB for 3D protein/nucleic acid structures. Search by text/sequence/structure, download coordinate... |
| [`perplexity-search`](skills/literature/perplexity-search/SKILL.md) | Perplexity Search | Perform AI-powered web searches with real-time information using Perplexity models via LiteLLM and OpenRouter.... |
| [`pubchem-database`](skills/literature/pubchem-database/SKILL.md) | PubChem Database | Query PubChem via PUG-REST API/PubChemPy (110M+ compounds). Search by name/CID/SMILES, retrieve properties, si... |
| [`pubmed-database`](skills/literature/pubmed-database/SKILL.md) | PubMed Database | Direct REST API access to PubMed. Advanced Boolean/MeSH queries, E-utilities API, batch processing, citation m... |
| [`pubmed-search`](skills/literature/pubmed-search/SKILL.md) | pubmed-search | Search PubMed biomedical literature with natural language queries powered by Valyu semantic search. Full-text ... |
| [`research-grants`](skills/literature/research-grants/SKILL.md) | Research Grant Writing | Write competitive research proposals for NSF, NIH, DOE, DARPA, and Taiwan NSTC. Agency-specific formatting, re... |
| [`research-lookup`](skills/literature/research-lookup/SKILL.md) | Research Information Lookup | Look up current research information using Perplexity Sonar Pro Search or Sonar Reasoning Pro models through O... |
| [`review-writing`](skills/literature/review-writing/SKILL.md) | Review Writing — 学术综述逐节写作方法论 | Use this skill when the user asks to write a literature review, review article, or 综述 based on an outline. Tri... |
| [`tooluniverse-chemical-compound-retrieval`](skills/literature/tooluniverse-chemical-compound-retrieval/SKILL.md) | Chemical Compound Information Retrieval | Retrieves chemical compound information from PubChem and ChEMBL with disambiguation, cross-referencing, and qu... |
| [`tooluniverse-literature-deep-research`](skills/literature/tooluniverse-literature-deep-research/SKILL.md) | Literature Deep Research Strategy (Enhanced) | Conduct comprehensive literature research with target disambiguation, evidence grading, and structured theme e... |
| [`uspto-database`](skills/literature/uspto-database/SKILL.md) | USPTO Database | Access USPTO APIs for patent/trademark searches, examination history (PEDS), assignments, citations, office ac... |
| [`zinc-database`](skills/literature/zinc-database/SKILL.md) | ZINC Database | Access ZINC (230M+ purchasable compounds). Search by ZINC ID/SMILES, similarity searches, 3D-ready structures ... |
---

## 🔬 Other Sciences

> Specialized tools for quantum computing, materials science, astronomy, and other physical sciences.

**13 skills** · [`skills/other/`](skills/other/)

| Skill | Title | Description |
|-------|-------|-------------|
| [`astropy`](skills/other/astropy/SKILL.md) | Astropy | Comprehensive Python library for astronomy and astrophysics. This skill should be used when working with astro... |
| [`cirq`](skills/other/cirq/SKILL.md) | Cirq - Quantum Computing with Python | Google quantum computing framework. Use when targeting Google Quantum AI hardware, designing noise-aware circu... |
| [`fluidsim`](skills/other/fluidsim/SKILL.md) | FluidSim | Framework for computational fluid dynamics simulations using Python. Use when running fluid dynamics simulatio... |
| [`iso-13485-certification`](skills/other/iso-13485-certification/SKILL.md) | ISO 13485 Certification Documentation Assistant | Comprehensive toolkit for preparing ISO 13485 certification documentation for medical device Quality Managemen... |
| [`materials`](skills/other/materials/SKILL.md) | Materials Science | Computational materials science, simulation, and property prediction. |
| [`opentrons-integration`](skills/other/opentrons-integration/SKILL.md) | Opentrons Integration | Official Opentrons Protocol API for OT-2 and Flex robots. Use when writing protocols specifically for Opentron... |
| [`pennylane`](skills/other/pennylane/SKILL.md) | PennyLane | Hardware-agnostic quantum ML framework with automatic differentiation. Use when training quantum circuits via ... |
| [`protocolsio-integration`](skills/other/protocolsio-integration/SKILL.md) | Protocols.io Integration | Integration with protocols.io API for managing scientific protocols. This skill should be used when working wi... |
| [`pufferlib`](skills/other/pufferlib/SKILL.md) | PufferLib - High-Performance Reinforcement Learning | High-performance reinforcement learning framework optimized for speed and scale. Use when you need fast parall... |
| [`pymatgen`](skills/other/pymatgen/SKILL.md) | Pymatgen - Python Materials Genomics | Materials science toolkit. Crystal structures (CIF, POSCAR), phase diagrams, band structure, DOS, Materials Pr... |
| [`qiskit`](skills/other/qiskit/SKILL.md) | Qiskit | IBM quantum computing framework. Use when targeting IBM Quantum hardware, working with Qiskit Runtime for prod... |
| [`qutip`](skills/other/qutip/SKILL.md) | QuTiP: Quantum Toolbox in Python | Quantum physics simulation library for open quantum systems. Use when studying master equations, Lindblad dyna... |
| [`simpy`](skills/other/simpy/SKILL.md) | SimPy - Discrete-Event Simulation | Process-based discrete-event simulation framework in Python. Use this skill when building simulations of syste... |

---

## Skill Format

Every `SKILL.md` follows a consistent structure readable by any AI agent:

```markdown
# Skill Name

## Overview
What this skill enables.

## When to Use
Trigger conditions — when the AI agent should apply this skill.

## Key Capabilities / Tools
...

## Usage Examples
...

## Limitations / Notes
...
```

---

## Contributing

1. Fork this repository
2. Create a folder: `skills/<domain>/<skill-name>/`
3. Add a `SKILL.md` following the format above
4. Open a pull request

---

## Credits

Skills sourced from [ScienceClaw](https://github.com/Zaoqu-Liu/ScienceClaw) by [LIU Zaoqu](https://github.com/Zaoqu-Liu) (IAPM · pi-HuB).

---

## License

MIT License
