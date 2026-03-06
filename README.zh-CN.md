# LabClaw Library

<div align="center">

**为 OpenClaw 提供 206 个面向生物医学自主研究的生产级技能**

[![Skills](https://img.shields.io/badge/skills-206-blue?style=flat-square)](skills/)
[![Biology](https://img.shields.io/badge/🧬_biology-66-brightgreen?style=flat-square)](skills/bio/)
[![LabOS](https://img.shields.io/badge/🤖_labos-7-cyan?style=flat-square)](skills/labos/)
[![Pharmacy](https://img.shields.io/badge/💊_pharmacy-36-blueviolet?style=flat-square)](skills/pharma/)
[![Medicine](https://img.shields.io/badge/🏥_medicine-20-red?style=flat-square)](skills/med/)
[![General](https://img.shields.io/badge/⚙️_general-48-orange?style=flat-square)](skills/general/)
[![Literature](https://img.shields.io/badge/📚_literature-29-purple?style=flat-square)](skills/literature/)
[![License](https://img.shields.io/badge/license-MIT-lightgrey?style=flat-square)](LICENSE)

[English](README.md) · **简体中文**

</div>

> [!NOTE]
> LabClaw 是一个技能库，而不是单体软件包。你可以整体使用，也可以只挑选与你的研究流程相关的技能文件夹。

---

## 项目简介

LabClaw 将 **206 个生产级 `SKILL.md` 文件** 按照生物学、药物发现、医学、数据科学与文献检索等方向进行组织，供 OpenClaw 兼容代理在生物医学研究中直接调用。每个技能都会告诉代理：**何时使用**、**如何调用**、以及**应该产出什么结果**。

这个仓库适合希望为代理提供可复用、可组合、面向研究任务的技能层的用户，而不是仅靠通用提示词完成复杂科研流程的场景。你可以把它当作完整的起始技能库，也可以只选用与你的实验室、项目或团队相关的部分。

## 一览

| 领域 | 技能数 | 重点方向 |
|------|------:|----------|
| [🧬 Biology & Life Sciences](skills/bio/) | **66** | 生物信息学、单细胞、基因组学、蛋白质组学、多组学、数据库 |
| [🤖 LabOS & Automation](skills/labos/) | **7** | 实验室机器人、LIMS/ELN、云平台、协议管理 |
| [💊 Pharmacy & Drug Discovery](skills/pharma/) | **36** | 化学信息学、分子机器学习、对接、靶点研究、药理学、药物数据库 |
| [🏥 Medical & Clinical](skills/med/) | **20** | 临床试验、精准医疗、肿瘤学、传染病、医学影像 |
| [⚙️ General & Data Science](skills/general/) | **48** | 统计分析、机器学习、数据管理、可视化、科学写作 |
| [📚 Literature & Search](skills/literature/) | **29** | 学术检索、生物医学数据库、多源发现、专利、基金、引文 |

## 代表性工作流

| 工作流 | 示例技能 |
|--------|----------|
| 单细胞与空间组学 | [`anndata`](skills/bio/anndata/SKILL.md), [`scanpy`](skills/bio/scanpy/SKILL.md), [`tooluniverse-spatial-transcriptomics`](skills/bio/tooluniverse-spatial-transcriptomics/SKILL.md) |
| 药物发现与分子设计 | [`rdkit`](skills/pharma/rdkit/SKILL.md), [`diffdock`](skills/pharma/diffdock/SKILL.md), [`tooluniverse-drug-repurposing`](skills/pharma/tooluniverse-drug-repurposing/SKILL.md) |
| 临床与精准医疗 | [`clinical`](skills/med/clinical/SKILL.md), [`tooluniverse-precision-oncology`](skills/med/tooluniverse-precision-oncology/SKILL.md), [`clinicaltrials-database`](skills/literature/clinicaltrials-database/SKILL.md) |
| 统计分析、机器学习与图形生成 | [`statistics`](skills/general/statistics/SKILL.md), [`scikit-learn`](skills/general/scikit-learn/SKILL.md), [`scientific-visualization`](skills/general/scientific-visualization/SKILL.md) |
| 文献综述与科研写作 | [`pubmed-search`](skills/literature/pubmed-search/SKILL.md), [`citation-management`](skills/literature/citation-management/SKILL.md), [`scientific-writing`](skills/general/scientific-writing/SKILL.md) |

## 3秒快速开始

复制下面的消息给OpenClaw:
```bash
install https://github.com/wu-yc/LabClaw
```
<p align="center"> <img src="./install_demo.gif" alt="Install Demo" width="30%"> </p>


## 仓库结构

```text
LabClaw/
├── README.md
├── README.zh-CN.md
└── skills/
    ├── bio/         # 66 个技能：基因组学、蛋白质组学、单细胞、系统生物学
    ├── labos/       # 7 个技能：实验室机器人、LIMS/ELN、云平台、协议
    ├── pharma/      # 36 个技能：化学信息学、分子对接、靶点发现、药理学
    ├── med/         # 20 个技能：临床研究、精准医疗、肿瘤学、影像
    ├── general/     # 48 个技能：统计、机器学习、可视化、写作、可复现性
    └── literature/  # 29 个技能：检索、数据库、基金、专利、引文
```

## 相关仓库

如果你希望把 LabClaw 放到更大的生物医学代理生态中理解，下面这些仓库最值得一起阅读：

| 仓库 | 关联原因 |
|------|----------|
| [`openclaw/openclaw`](https://github.com/openclaw/openclaw) | 这是承载技能运行的主平台。LabClaw 的目录结构与使用方式就是围绕 OpenClaw 的 skills platform、onboarding 流程与 agent workspace 模型设计的。 |
| [`mims-harvard/ToolUniverse`](https://github.com/mims-harvard/ToolUniverse) | 一个面向 AI scientist 的大型工具生态。LabClaw 在组学、药物研究、临床和文献工作流中包含了大量 `tooluniverse-*` 技能。 |
| [`snap-stanford/Biomni`](https://github.com/snap-stanford/Biomni) | 一个互补的生物医学 AI 代理项目。LabClaw 已经提供 `biomni` 技能，因此 Biomni 是理解相关能力边界和生态定位时非常自然的参考仓库。 |

## 技能目录

> [!TIP]
> 为了与目录路径、技能文件名以及上游工具名称保持一致，下方的技能标识符保持英文；大部分具体描述也保留原始英文，便于直接对应到各个 `SKILL.md` 文件。

---

<details>
<summary><strong>🧬 Biology & Life Sciences（生命科学与生物学） — 66 个技能</strong></summary>

> 面向基因组学、转录组学、蛋白质组学、单细胞分析、结构生物学、系统生物学与实验自动化的工具。

**66 个技能** &nbsp;·&nbsp; [`skills/bio/`](skills/bio/)

#### 生物信息学基础

| 技能 | 说明 |
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

#### 单细胞与空间转录组

| 技能 | 说明 |
|-------|-------------|
| [`anndata`](skills/bio/anndata/SKILL.md) | Data structure for annotated matrices in single-cell analysis. Use when working with .h5ad files or integrating with the... |
| [`cellxgene-census`](skills/bio/cellxgene-census/SKILL.md) | Query the CELLxGENE Census (61M+ cells) programmatically. Use when you need expression data across tissues, diseases, or... |
| [`scanpy`](skills/bio/scanpy/SKILL.md) | Standard single-cell RNA-seq analysis pipeline. Use for QC, normalization, dimensionality reduction (PCA/UMAP/t-SNE), cl... |
| [`scvi-tools`](skills/bio/scvi-tools/SKILL.md) | Deep generative models for single-cell omics. Use when you need probabilistic batch correction (scVI), transfer learning... |
| [`tooluniverse-single-cell`](skills/bio/tooluniverse-single-cell/SKILL.md) | Production-ready single-cell and expression matrix analysis using scanpy, anndata, and scipy. Performs scRNA-seq QC, nor... |
| [`tooluniverse-spatial-omics-analysis`](skills/bio/tooluniverse-spatial-omics-analysis/SKILL.md) | Computational analysis framework for spatial multi-omics data integration. Given spatially variable genes (SVGs), spatia... |
| [`tooluniverse-spatial-transcriptomics`](skills/bio/tooluniverse-spatial-transcriptomics/SKILL.md) | Analyze spatial transcriptomics data to map gene expression in tissue architecture. Supports 10x Visium, MERFISH, seqFIS... |
| [`umap-learn`](skills/bio/umap-learn/SKILL.md) | UMAP dimensionality reduction. Fast nonlinear manifold learning for 2D/3D visualization, clustering preprocessing (HDBSCAN), supervised/parametric UMAP, for high-dimensional data. |

#### 基因组学、NGS 与变异分析

| 技能 | 说明 |
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

#### 蛋白质组学与结构生物学

| 技能 | 说明 |
|-------|-------------|
| [`alphafold-database`](skills/bio/alphafold-database/SKILL.md) | Access AlphaFold 200M+ AI-predicted protein structures. Retrieve structures by UniProt ID, download PDB/mmCIF files, ana... |
| [`esm`](skills/bio/esm/SKILL.md) | Comprehensive toolkit for protein language models including ESM3 (generative multimodal protein design across sequence, ... |
| [`pyopenms`](skills/bio/pyopenms/SKILL.md) | Complete mass spectrometry analysis platform. Use for proteomics workflows feature detection, peptide identification, pr... |
| [`tooluniverse-protein-interactions`](skills/bio/tooluniverse-protein-interactions/SKILL.md) | Analyze protein-protein interaction networks using STRING, BioGRID, and SASBDB databases. Maps protein identifiers, retr... |
| [`tooluniverse-protein-structure-retrieval`](skills/bio/tooluniverse-protein-structure-retrieval/SKILL.md) | Retrieves protein structure data from RCSB PDB, PDBe, and AlphaFold with protein disambiguation, quality assessment, and... |
| [`tooluniverse-proteomics-analysis`](skills/bio/tooluniverse-proteomics-analysis/SKILL.md) | Analyze mass spectrometry proteomics data including protein quantification, differential expression, post-translational ... |
| [`uniprot-database`](skills/bio/uniprot-database/SKILL.md) | Direct REST API access to UniProt. Protein searches, FASTA retrieval, ID mapping, Swiss-Prot/TrEMBL. For Python workflow... |

#### 多组学与系统生物学

| 技能 | 说明 |
|-------|-------------|
| [`matchms`](skills/bio/matchms/SKILL.md) | Spectral similarity and compound identification for metabolomics. Use for comparing mass spectra, computing similarity s... |
| [`tooluniverse-metabolomics`](skills/bio/tooluniverse-metabolomics/SKILL.md) | Comprehensive metabolomics research skill for identifying metabolites, analyzing studies, and searching metabolomics dat... |
| [`tooluniverse-metabolomics-analysis`](skills/bio/tooluniverse-metabolomics-analysis/SKILL.md) | Analyze metabolomics data including metabolite identification, quantification, pathway analysis, and metabolic flux. Pro... |
| [`tooluniverse-multi-omics-integration`](skills/bio/tooluniverse-multi-omics-integration/SKILL.md) | Integrate and analyze multiple omics datasets (transcriptomics, proteomics, epigenomics, genomics, metabolomics) for sys... |
| [`tooluniverse-multiomic-disease-characterization`](skills/bio/tooluniverse-multiomic-disease-characterization/SKILL.md) | Comprehensive multi-omics disease characterization integrating genomics, transcriptomics, proteomics, pathway, and thera... |
| [`tooluniverse-phylogenetics`](skills/bio/tooluniverse-phylogenetics/SKILL.md) | Production-ready phylogenetics and sequence analysis skill for alignment processing, tree analysis, and evolutionary met... |
| [`tooluniverse-systems-biology`](skills/bio/tooluniverse-systems-biology/SKILL.md) | Comprehensive systems biology and pathway analysis using multiple pathway databases (Reactome, KEGG, WikiPathways, Pathw... |

#### 生物数据库

| 技能 | 说明 |
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

#### 实验平台与成像

| 技能 | 说明 |
|-------|-------------|
| [`flowio`](skills/bio/flowio/SKILL.md) | Parse FCS (Flow Cytometry Standard) files v2.0-3.1. Extract events as NumPy arrays, read metadata/channels, convert to C... |
| [`histolab`](skills/bio/histolab/SKILL.md) | Lightweight WSI tile extraction and preprocessing. Use for basic slide processing tissue detection, tile extraction, sta... |
| [`lamindb`](skills/bio/lamindb/SKILL.md) | This skill should be used when working with LaminDB, an open-source data framework for biology that makes data queryable... |
| [`omero-integration`](skills/bio/omero-integration/SKILL.md) | Microscopy data management platform. Access images via Python, retrieve datasets, analyze pixels, manage ROIs/annotation... |
| [`pathml`](skills/bio/pathml/SKILL.md) | Full-featured computational pathology toolkit. Use for advanced WSI analysis including multiplexed immunofluorescence (C... |

</details>

<details>
<summary><strong>🤖 LabOS & Laboratory Automation（实验室自动化） — 7 个技能</strong></summary>

> 面向实验室机器人、LIMS/ELN系统、云平台与科学协议管理的工具。优化用于 Stanford LabOS 工作流与自动化实验室研究。

**7 个技能** &nbsp;·&nbsp; [`skills/labos/`](skills/labos/)

#### 实验室机器人与自动化

| 技能 | 说明 |
|-------|-------------|
| [`pylabrobot`](skills/bio/pylabrobot/SKILL.md) | Vendor-agnostic lab automation framework. Use when controlling multiple equipment types (Hamilton, Tecan, Opentrons, plate readers, pumps) or needing unified programming across different vendors. Best for complex workflows, multi-vendor setups, simulation. |
| [`opentrons-integration`](skills/bio/opentrons-integration/SKILL.md) | Official Opentrons Protocol API for OT-2 and Flex robots. Use when writing protocols specifically for Opentrons hardware with full access to Protocol API v2 features. Best for production Opentrons protocols, official API compatibility. |

#### LIMS/ELN 系统

| 技能 | 说明 |
|-------|-------------|
| [`benchling-integration`](skills/bio/benchling-integration/SKILL.md) | Benchling R&D platform integration. Access registry (DNA, proteins), inventory, ELN entries, workflows via API, build Benchling Apps, query Data Warehouse, for lab data management automation. |
| [`labarchive-integration`](skills/bio/labarchive-integration/SKILL.md) | Electronic lab notebook API integration. Access notebooks, manage entries/attachments, backup notebooks, integrate with laboratory workflows, for ELN automation. |

#### 实验室云平台

| 技能 | 说明 |
|-------|-------------|
| [`latchbio-integration`](skills/bio/latchbio-integration/SKILL.md) | Latch platform for bioinformatics workflows. Build pipelines with Latch SDK, @workflow/@task decorators, deploy serverless bioinformatics apps, for cloud bioinformatics. |
| [`dnanexus-integration`](skills/bio/dnanexus-integration/SKILL.md) | DNAnexus cloud genomics platform. Build apps/applets, manage data (upload/download), dxpy Python SDK, run workflows, FASTQ/BAM/CRAM processing, for cloud genomic analysis. |

#### 协议管理

| 技能 | 说明 |
|-------|-------------|
| [`protocolsio-integration`](skills/bio/protocolsio-integration/SKILL.md) | Integration with protocols.io API for managing scientific protocols. This skill should be used when working with protoco... |

</details>

<details>
<summary><strong>💊 Pharmacy & Drug Discovery（药学与药物发现） — 36 个技能</strong></summary>

> 面向化学信息学、分子对接、药物设计、药理学、药物警戒与药物数据库的工具。

**36 个技能** &nbsp;·&nbsp; [`skills/pharma/`](skills/pharma/)

#### 化学信息学与分子设计

| 技能 | 说明 |
|-------|-------------|
| [`chemistry`](skills/pharma/chemistry/SKILL.md) | Computational chemistry, cheminformatics, and drug discovery workflows. |
| [`datamol`](skills/pharma/datamol/SKILL.md) | Pythonic wrapper around RDKit with simplified interface and sensible defaults. Preferred for standard drug discovery inc... |
| [`deepchem`](skills/pharma/deepchem/SKILL.md) | Molecular ML with diverse featurizers and pre-built datasets. Use for property prediction (ADMET, toxicity) with traditi... |
| [`medchem`](skills/pharma/medchem/SKILL.md) | Medicinal chemistry filters. Apply drug-likeness rules (Lipinski, Veber), PAINS filters, structural alerts, complexity m... |
| [`molfeat`](skills/pharma/molfeat/SKILL.md) | Molecular featurization for ML (100+ featurizers). ECFP, MACCS, descriptors, pretrained models (ChemBERTa), convert SMIL... |
| [`rdkit`](skills/pharma/rdkit/SKILL.md) | Cheminformatics toolkit for fine-grained molecular control. SMILES/SDF parsing, descriptors (MW, LogP, TPSA), fingerprin... |
| [`rowan`](skills/pharma/rowan/SKILL.md) | Cloud-based quantum chemistry platform with Python API. Preferred for computational chemistry workflows including pKa pr... |

#### 分子机器学习

| 技能 | 说明 |
|-------|-------------|
| [`pytdc`](skills/pharma/pytdc/SKILL.md) | Therapeutics Data Commons. AI-ready drug discovery datasets (ADME, toxicity, DTI), benchmarks, scaffold splits, molecula... |
| [`torch_geometric`](skills/pharma/torch_geometric/SKILL.md) | Graph Neural Networks (PyG). Node/graph classification, link prediction, GCN, GAT, GraphSAGE, heterogeneous graphs, mole... |
| [`torchdrug`](skills/pharma/torchdrug/SKILL.md) | PyTorch-native graph neural networks for molecules and proteins. Use when building custom GNN architectures for drug dis... |

#### 分子对接与蛋白治疗

| 技能 | 说明 |
|-------|-------------|
| [`adaptyv`](skills/pharma/adaptyv/SKILL.md) | Cloud laboratory platform for automated protein testing and validation. Use when designing proteins and needing experime... |
| [`diffdock`](skills/pharma/diffdock/SKILL.md) | Diffusion-based molecular docking. Predict protein-ligand binding poses from PDB/SMILES, confidence scores, virtual scre... |
| [`tooluniverse-antibody-engineering`](skills/pharma/tooluniverse-antibody-engineering/SKILL.md) | Comprehensive antibody engineering and optimization for therapeutic development. Covers humanization, affinity maturatio... |
| [`tooluniverse-binder-discovery`](skills/pharma/tooluniverse-binder-discovery/SKILL.md) | Discover novel small molecule binders for protein targets using structure-based and ligand-based approaches. Creates act... |
| [`tooluniverse-protein-therapeutic-design`](skills/pharma/tooluniverse-protein-therapeutic-design/SKILL.md) | Design novel protein therapeutics (binders, enzymes, scaffolds) using AI-guided de novo design. Uses RFdiffusion for bac... |

#### 药物研究与靶点发现

| 技能 | 说明 |
|-------|-------------|
| [`tooluniverse-drug-repurposing`](skills/pharma/tooluniverse-drug-repurposing/SKILL.md) | Identify drug repurposing candidates using ToolUniverse for target-based, compound-based, and disease-driven strategies.... |
| [`tooluniverse-drug-research`](skills/pharma/tooluniverse-drug-research/SKILL.md) | Generates comprehensive drug research reports with compound disambiguation, evidence grading, and mandatory completeness... |
| [`tooluniverse-drug-target-validation`](skills/pharma/tooluniverse-drug-target-validation/SKILL.md) | Comprehensive computational validation of drug targets for early-stage drug discovery. Evaluates targets across 10 dimen... |
| [`tooluniverse-target-research`](skills/pharma/tooluniverse-target-research/SKILL.md) | Gather comprehensive biological target intelligence from 9 parallel research paths covering protein info, structure, int... |

#### 药理学与安全性

| 技能 | 说明 |
|-------|-------------|
| [`tooluniverse-adverse-event-detection`](skills/pharma/tooluniverse-adverse-event-detection/SKILL.md) | Detect and analyze adverse drug event signals using FDA FAERS data, drug labels, disproportionality analysis (PRR, ROR, ... |
| [`tooluniverse-chemical-safety`](skills/pharma/tooluniverse-chemical-safety/SKILL.md) | Comprehensive chemical safety and toxicology assessment integrating ADMET-AI predictions, CTD toxicogenomics, FDA label ... |
| [`tooluniverse-drug-drug-interaction`](skills/pharma/tooluniverse-drug-drug-interaction/SKILL.md) | Comprehensive drug-drug interaction (DDI) prediction and risk assessment. Analyzes interaction mechanisms (CYP450, trans... |
| [`tooluniverse-network-pharmacology`](skills/pharma/tooluniverse-network-pharmacology/SKILL.md) | Construct and analyze compound-target-disease networks for drug repurposing, polypharmacology discovery, and systems pha... |
| [`tooluniverse-pharmacovigilance`](skills/pharma/tooluniverse-pharmacovigilance/SKILL.md) | Analyze drug safety signals from FDA adverse event reports, label warnings, and pharmacogenomic data. Calculates disprop... |

#### 化学与药物数据库

| 技能 | 说明 |
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
<summary><strong>🏥 Medical & Clinical（医学与临床） — 20 个技能</strong></summary>

> 面向临床研究、精准医疗、肿瘤学、传染病与医学影像的工具。

**20 个技能** &nbsp;·&nbsp; [`skills/med/`](skills/med/)

#### 临床研究与试验

| 技能 | 说明 |
|-------|-------------|
| [`clinical`](skills/med/clinical/SKILL.md) | Clinical study design, statistical analysis, and regulatory compliance for medical research. |
| [`clinical-decision-support`](skills/med/clinical-decision-support/SKILL.md) | Generate professional clinical decision support (CDS) documents for pharmaceutical and clinical research settings, inclu... |
| [`clinical-reports`](skills/med/clinical-reports/SKILL.md) | Write comprehensive clinical reports including case reports (CARE guidelines), diagnostic reports (radiology/pathology/l... |
| [`tooluniverse-clinical-guidelines`](skills/med/tooluniverse-clinical-guidelines/SKILL.md) | Search and retrieve clinical practice guidelines across 12+ authoritative sources including NICE, WHO, ADA, AHA/ACC, NCC... |
| [`tooluniverse-clinical-trial-design`](skills/med/tooluniverse-clinical-trial-design/SKILL.md) | Strategic clinical trial design feasibility assessment using ToolUniverse. Evaluates patient population sizing, biomarke... |
| [`tooluniverse-clinical-trial-matching`](skills/med/tooluniverse-clinical-trial-matching/SKILL.md) | AI-driven patient-to-trial matching for precision medicine and oncology. Given a patient profile (disease, molecular alt... |
| [`treatment-plans`](skills/med/treatment-plans/SKILL.md) | Generate concise (3-4 page), focused medical treatment plans in LaTeX/PDF format for all clinical specialties. Supports ... |

#### 精准医疗与肿瘤学

| 技能 | 说明 |
|-------|-------------|
| [`tooluniverse-cancer-variant-interpretation`](skills/med/tooluniverse-cancer-variant-interpretation/SKILL.md) | Provide comprehensive clinical interpretation of somatic mutations in cancer. Given a gene symbol + variant (e.g., EGFR ... |
| [`tooluniverse-disease-research`](skills/med/tooluniverse-disease-research/SKILL.md) | Generate comprehensive disease research reports using 100+ ToolUniverse tools. Creates a detailed markdown report file a... |
| [`tooluniverse-immunotherapy-response-prediction`](skills/med/tooluniverse-immunotherapy-response-prediction/SKILL.md) | Predict patient response to immune checkpoint inhibitors (ICIs) using multi-biomarker integration. Given a cancer type, ... |
| [`tooluniverse-infectious-disease`](skills/med/tooluniverse-infectious-disease/SKILL.md) | Rapid pathogen characterization and drug repurposing analysis for infectious disease outbreaks. Identifies pathogen taxo... |
| [`tooluniverse-precision-medicine-stratification`](skills/med/tooluniverse-precision-medicine-stratification/SKILL.md) | Comprehensive patient stratification for precision medicine by integrating genomic, clinical, and therapeutic data. Give... |
| [`tooluniverse-precision-oncology`](skills/med/tooluniverse-precision-oncology/SKILL.md) | Provide actionable treatment recommendations for cancer patients based on molecular profile. Interprets tumor mutations,... |
| [`tooluniverse-rare-disease-diagnosis`](skills/med/tooluniverse-rare-disease-diagnosis/SKILL.md) | Provide differential diagnosis for patients with suspected rare diseases based on phenotype and genetic data. Matches sy... |

#### 医学影像、器械与监管

| 技能 | 说明 |
|-------|-------------|
| [`iso-13485-certification`](skills/med/iso-13485-certification/SKILL.md) | Comprehensive toolkit for preparing ISO 13485 certification documentation for medical device Quality Management Systems.... |
| [`neurokit2`](skills/med/neurokit2/SKILL.md) | Comprehensive biosignal processing toolkit for analyzing physiological data including ECG, EEG, EDA, RSP, PPG, EMG, and ... |
| [`neuropixels-analysis`](skills/med/neuropixels-analysis/SKILL.md) | Neuropixels neural recording analysis. Load SpikeGLX/OpenEphys data, preprocess, motion correction, Kilosort4 spike sort... |
| [`pydicom`](skills/med/pydicom/SKILL.md) | Python library for working with DICOM (Digital Imaging and Communications in Medicine) files. Use this skill when readin... |
| [`pyhealth`](skills/med/pyhealth/SKILL.md) | Comprehensive healthcare AI toolkit for developing, testing, and deploying machine learning models with clinical data. T... |
| [`tooluniverse-image-analysis`](skills/med/tooluniverse-image-analysis/SKILL.md) | Production-ready microscopy image analysis and quantitative imaging data skill for colony morphometry, cell counting, fl... |

</details>

<details>
<summary><strong>⚙️ General & Data Science（通用与数据科学） — 48 个技能</strong></summary>

> 面向统计分析、机器学习、数据管理、可视化与科学写作的通用工具。

**48 个技能** &nbsp;·&nbsp; [`skills/general/`](skills/general/)

#### 统计学与数学建模

| 技能 | 说明 |
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

#### 机器学习与 AI

| 技能 | 说明 |
|-------|-------------|
| [`aeon`](skills/general/aeon/SKILL.md) | This skill should be used for time series machine learning tasks including classification, regression, clustering, forec... |
| [`pytorch-lightning`](skills/general/pytorch-lightning/SKILL.md) | Deep learning framework (PyTorch Lightning). Organize PyTorch code into LightningModules, configure Trainers for multi-G... |
| [`scikit-learn`](skills/general/scikit-learn/SKILL.md) | Machine learning in Python with scikit-learn. Use when working with supervised learning (classification, regression), un... |
| [`shap`](skills/general/shap/SKILL.md) | Model interpretability and explainability using SHAP (SHapley Additive exPlanations). Use this skill when explaining mac... |
| [`transformers`](skills/general/transformers/SKILL.md) | This skill should be used when working with pre-trained transformer models for natural language processing, computer vis... |

#### 数据管理与计算

| 技能 | 说明 |
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

#### 可视化

| 技能 | 说明 |
|-------|-------------|
| [`matplotlib`](skills/general/matplotlib/SKILL.md) | Low-level plotting library for full customization. Use when you need fine-grained control over every plot element, creat... |
| [`plotly`](skills/general/plotly/SKILL.md) | Interactive visualization library. Use when you need hover info, zoom, pan, or web-embeddable charts. Best for dashboard... |
| [`scientific-diagram-generation`](skills/general/scientific-diagram-generation/SKILL.md) | AI-powered scientific illustration generation using Gemini Image models. Creates publication-quality mechanism diagrams,... |
| [`scientific-visualization`](skills/general/scientific-visualization/SKILL.md) | Meta-skill for publication-ready figures. Use when creating journal submission figures requiring multi-panel layouts, si... |
| [`seaborn`](skills/general/seaborn/SKILL.md) | Statistical visualization with pandas integration. Use for quick exploration of distributions, relationships, and catego... |
| [`visualization`](skills/general/visualization/SKILL.md) | Publication-quality scientific figure generation. GENERAL: language-agnostic (R, Python, Julia, or any tool). |

#### 科学写作与展示

| 技能 | 说明 |
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

#### 知识产权、监管与报告

| 技能 | 说明 |
|-------|-------------|
| [`patent-drafting`](skills/general/patent-drafting/SKILL.md) | Draft patent applications for scientific inventions, covering claims, specification, and prior art analysis. |
| [`regulatory-submission`](skills/general/regulatory-submission/SKILL.md) | Prepare regulatory submissions for drugs, biologics, devices, and diagnostics. |

</details>

<details>
<summary><strong>📚 Literature & Search（文献与检索） — 29 个技能</strong></summary>

> 面向学术检索、数据库查询、引文管理与综述写作的工具。

**29 个技能** &nbsp;·&nbsp; [`skills/literature/`](skills/literature/)

#### 生物医学文献检索

| 技能 | 说明 |
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

#### 基因组与临床数据库

| 技能 | 说明 |
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

#### 多源检索与发现

| 技能 | 说明 |
|-------|-------------|
| [`arxiv-search`](skills/literature/arxiv-search/SKILL.md) | Search arXiv physics, math, and computer science preprints using natural language queries. Powered by Valyu semantic sea... |
| [`bioservices`](skills/literature/bioservices/SKILL.md) | Unified Python interface to 40+ bioinformatics services. Use when querying multiple databases (UniProt, KEGG, ChEMBL, Re... |
| [`perplexity-search`](skills/literature/perplexity-search/SKILL.md) | Perform AI-powered web searches with real-time information using Perplexity models via LiteLLM and OpenRouter. This skil... |
| [`research-lookup`](skills/literature/research-lookup/SKILL.md) | Look up current research information using Perplexity Sonar Pro Search or Sonar Reasoning Pro models through OpenRouter.... |

#### 专利、基金与引文管理

| 技能 | 说明 |
|-------|-------------|
| [`citation-management`](skills/literature/citation-management/SKILL.md) | Comprehensive citation management for academic research. Search Google Scholar and PubMed for papers, extract accurate m... |
| [`patents-search`](skills/literature/patents-search/SKILL.md) | Search global patents with natural language queries. Prior art, patent landscapes, and innovation tracking via Valyu. |
| [`research-grants`](skills/literature/research-grants/SKILL.md) | Write competitive research proposals for NSF, NIH, DOE, DARPA, and Taiwan NSTC. Agency-specific formatting, review crite... |
| [`review-writing`](skills/literature/review-writing/SKILL.md) | Use this skill when the user asks to write a literature review, review article, or 综述 based on an outline. Trigger keywo... |
| [`uspto-database`](skills/literature/uspto-database/SKILL.md) | Access USPTO APIs for patent/trademark searches, examination history (PEDS), assignments, citations, office actions, TSD... |

</details>

---

## `SKILL.md` 结构

每个 `SKILL.md` 基本遵循统一结构：

```markdown
# Skill Name
## Overview        — 这个技能解决什么问题
## When to Use     — 触发条件与适用场景
## Key Capabilities — 关键能力、工具、API 与参数
## Usage Examples  — 典型用法与工作流示例
```

## 致谢

Skills curated by Yingcheng (Charles) Wu at Le Cong Lab of Stanford & Mengdi Wang Lab at Princeton.

## License

[MIT License](LICENSE)
