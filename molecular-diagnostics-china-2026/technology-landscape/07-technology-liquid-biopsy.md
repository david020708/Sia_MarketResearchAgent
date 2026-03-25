# Technology Deep-Dive: Liquid Biopsy
**China Molecular Diagnostics Market — Technology Landscape Report**
*Research Date: March 2026 | Time Horizon: 2024–2026 current state, 2030 forecast*
*Perspective: Investor / Market Entrant*

---

## 1. Technology Overview

### Plain-Language Definition

Liquid biopsy is a minimally invasive diagnostic approach that detects and analyzes cancer-derived biological material circulating in blood or other body fluids — without requiring a surgical tissue sample. Instead of cutting into a tumor, a clinician draws a standard blood tube and analyzes the molecular signals shed by cancer cells into the bloodstream.

The term "liquid biopsy" was coined to contrast with conventional "solid" or "tissue" biopsy, and it encompasses several distinct analyte types (see Glossary below). The technology matters for cancer diagnostics because it addresses three fundamental limitations of tissue biopsy: (1) tissue biopsy is invasive and carries procedural risk; (2) a single tissue sample captures only one spatial snapshot of a heterogeneous tumor; and (3) tissue biopsy cannot be repeated frequently enough to track real-time tumor evolution during treatment.

Liquid biopsy enables:
- **Early detection** — identifying cancer signals before symptoms appear
- **Companion diagnostics** — matching patients to targeted therapies based on tumor mutation profiles
- **Treatment monitoring** — tracking response, detecting resistance mutations in real time
- **Minimal residual disease (MRD) detection** — identifying microscopic residual cancer after surgery
- **Multi-cancer early detection (MCED)** — a single blood test screening for multiple cancer types simultaneously

### Why It Matters for China

China carries approximately 23% of the global cancer burden, with ~4.8 million new cancer cases and ~3.2 million cancer deaths annually. The majority of Chinese patients are diagnosed at Stage III or IV, when 5-year survival rates drop dramatically. Liquid biopsy offers a scalable, non-invasive pathway to shift diagnosis earlier — a national health priority explicitly embedded in China's Healthy China 2030 initiative and the 14th Five-Year Plan for cancer prevention.

### Glossary of Key Terms

| Term | Definition |
|------|-----------|
| **cfDNA** (cell-free DNA) | Short fragments of DNA (~167 bp) released into the bloodstream by all cells — both normal and cancerous — through apoptosis and necrosis |
| **ctDNA** (circulating tumor DNA) | The subset of cfDNA that originates specifically from tumor cells; carries tumor-specific somatic mutations, copy number alterations, and methylation patterns |
| **CTCs** (circulating tumor cells) | Intact cancer cells that have detached from the primary tumor and entered the bloodstream; rare (1–10 per mL of blood) but information-rich |
| **Exosomes / EVs** (extracellular vesicles) | Nano-sized membrane vesicles (30–150 nm) secreted by cells, including tumor cells; carry proteins, RNA, and DNA cargo |
| **Methylation** | An epigenetic modification (addition of a methyl group to cytosine residues) that regulates gene expression; cancer cells exhibit characteristic aberrant methylation patterns |
| **MRD** (minimal residual disease) | Microscopic cancer remaining after treatment, detectable by ctDNA before clinical relapse |
| **MCED** (multi-cancer early detection) | A single assay designed to detect signals from multiple cancer types simultaneously |
| **VAF** (variant allele frequency) | The proportion of ctDNA molecules carrying a specific mutation; typically 0.01%–5% in advanced cancer, <0.01% in early-stage |
| **NGS** (next-generation sequencing) | High-throughput DNA sequencing technology enabling simultaneous analysis of thousands to millions of DNA fragments |
| **TRL** (technology readiness level) | A 1–9 scale measuring maturity from basic research (TRL 1) to proven deployment (TRL 9) |
| **CDx** (companion diagnostic) | A diagnostic test approved alongside a specific drug to identify patients likely to benefit |
| **NMPA** | China's National Medical Products Administration — the regulatory body for medical devices and diagnostics |

---

## 2. Technical Mechanism

### Core Mechanism

Tumor cells continuously shed DNA fragments into the bloodstream through apoptosis (programmed cell death) and necrosis. These ctDNA fragments are typically 150–200 base pairs in length — shorter on average than cfDNA from normal cells (~167 bp vs. ~200 bp), a property exploited by fragmentomics-based detection methods. The ctDNA fraction of total cfDNA varies enormously: from <0.01% in early-stage cancers to >50% in advanced metastatic disease. This low signal-to-noise ratio is the central technical challenge of liquid biopsy.

### Analyte Types and Their Characteristics

| Analyte | Abundance | Information Content | Technical Maturity | Primary Use Case |
|---------|-----------|--------------------|--------------------|-----------------|
| **ctDNA / cfDNA** | Moderate (ng/mL range) | Mutations, CNVs, methylation, fragmentomics | Highest | Companion Dx, MRD, MCED |
| **CTCs** | Very rare (1–10/mL) | Full cellular phenotype, proteomics | Moderate | Metastasis biology, drug resistance |
| **Exosomes / EVs** | High | RNA, proteins, DNA cargo | Early-moderate | Research, emerging diagnostics |
| **cfRNA** | Low, unstable | Gene expression, splicing | Early | Research |
| **Platelets (TEPs)** | High | RNA education by tumor | Early | Research |

ctDNA/cfDNA dominates current commercial applications due to its relative abundance, stability, and compatibility with established NGS workflows.

### Detection Platforms

**1. NGS-Based Platforms (dominant in China)**
- **Targeted panel sequencing**: Amplicon-based or hybrid-capture panels covering 50–500 cancer-relevant genes. Sensitivity: 0.1%–1% VAF. Used for companion diagnostics and treatment monitoring. Examples: Burning Rock OncoCompass, Geneseeq ONE.
- **Ultra-deep sequencing with error suppression**: Techniques such as duplex sequencing, CAPP-Seq, and UMI (unique molecular identifier) tagging reduce sequencing error rates from ~0.1% to <0.001%, enabling detection of VAF as low as 0.001%. Critical for early-stage detection and MRD.
- **Whole-genome sequencing (WGS) / shallow WGS**: Used for copy number variation (CNV) analysis and fragmentomics. Lower cost per base but requires higher tumor fraction.

**2. PCR-Based Platforms**
- **ddPCR** (droplet digital PCR): Partitions sample into ~20,000 droplets, enabling absolute quantification of rare mutations. Sensitivity: 0.001%–0.01% VAF. Faster and cheaper than NGS for known hotspot mutations. Widely used in China for EGFR T790M resistance monitoring.
- **BEAMing** (beads, emulsion, amplification, magnetics): Combines emulsion PCR with flow cytometry. High sensitivity but low throughput.
- **qPCR / RT-PCR**: Standard clinical workhorse for known mutations (e.g., EGFR exon 19/21). Lower sensitivity (~1% VAF) but fast, cheap, and widely available.

**3. Methylation Analysis Platforms**
- **Bisulfite sequencing**: Chemical conversion of unmethylated cytosines to uracil, followed by sequencing to map methylation patterns genome-wide. Gold standard for methylation profiling.
- **ELSA-seq** (Burning Rock): Proprietary enhanced-ligation sequencing assay combining cfDNA methylation capture with machine learning classifiers. Demonstrated in the THUNDER study for 6-cancer early detection.
- **cfMeDIP-seq**: Cell-free methylated DNA immunoprecipitation sequencing — enriches methylated cfDNA fragments for cost-effective genome-wide methylation profiling.
- **Targeted methylation panels**: Focus on cancer-specific differentially methylated regions (DMRs) for tissue-of-origin classification.

**4. Fragmentomics**
An emerging approach analyzing cfDNA fragment length distributions, end motifs, and nucleosome positioning patterns — which encode tissue-of-origin information independent of mutations. Particularly powerful for early-stage detection where ctDNA fraction is too low for mutation-based methods. [Source: Nature Reviews Cancer, 2025 — https://www.nature.com/articles/s41568-025-00795-x]

### Performance Metrics

| Metric | Advanced Cancer (Stage III–IV) | Early Cancer (Stage I–II) | MCED (pan-cancer) |
|--------|-------------------------------|--------------------------|-------------------|
| Sensitivity | 70–95% | 30–70% | 40–75% (varies by cancer type) |
| Specificity | 90–99% | 95–99% | 95–99% |
| PPV (at 0.5% prevalence) | High | Moderate | Moderate |
| ctDNA fraction | 1–50% | 0.01–1% | <0.1% |

[Source: droracle.ai accuracy summary — https://www.droracle.ai/articles/857307/what-is-the-accuracy-of-liquid-biopsy-sensitivity-and]
[Source: Latest Research Progress of Liquid Biopsy in Tumor, PMC 2024 — https://pmc.ncbi.nlm.nih.gov/articles/PMC11335005/]

### Key Technical Limitations

1. **Low ctDNA fraction in early-stage disease**: Stage I tumors may shed ctDNA at VAF <0.01%, below the detection threshold of most current assays.
2. **Clonal hematopoiesis of indeterminate potential (CHIP)**: Somatic mutations in blood cells (not tumor cells) can generate false-positive signals, particularly in older patients.
3. **Tumor heterogeneity**: Liquid biopsy captures the average signal across all tumor clones; subclonal mutations may be missed.
4. **Tissue-of-origin ambiguity**: When a cancer signal is detected, identifying which organ it originates from requires additional methylation or fragmentomics analysis.
5. **Pre-analytical variability**: cfDNA degrades rapidly; blood processing within 2–4 hours is critical. Standardization of collection tubes (EDTA vs. Streck) and processing protocols remains a challenge.
6. **Reimbursement gap**: Most liquid biopsy tests in China are not yet covered by national insurance (NRDL), limiting adoption to out-of-pocket or hospital-funded testing.

---

## 3. Historical Evolution and Iteration

### Origin and Foundational Science

The scientific foundation of liquid biopsy traces to 1977, when Léon and Mandel first identified elevated levels of cell-free DNA in the plasma and serum of cancer patients compared to healthy controls — a finding largely ignored for two decades. [Source: College of American Pathologists — https://www.cap.org/member-resources/articles/the-liquid-biopsy]

The modern era began with Dennis Lo's group at the Chinese University of Hong Kong (CUHK), who in 1997 demonstrated fetal DNA in maternal plasma — establishing the principle that cell-free DNA from one tissue type could be detected in another's bloodstream. This work directly enabled non-invasive prenatal testing (NIPT) and laid the conceptual groundwork for cancer ctDNA detection.

### Timeline of Key Breakthroughs

| Year | Milestone | Significance |
|------|-----------|-------------|
| 1977 | Léon & Mandel identify elevated cfDNA in cancer patients | Foundational observation |
| 1994 | Mutant RAS oncogene detected in plasma of pancreatic cancer patients | First proof of tumor-derived DNA in blood |
| 1997 | Dennis Lo demonstrates fetal cfDNA in maternal plasma (CUHK) | Establishes cfDNA detection principle; enables NIPT |
| 2004 | BEAMing technology developed (Bert Vogelstein, Johns Hopkins) | First quantitative ctDNA measurement |
| 2008 | Diehl et al., Nature Medicine — quantitative ctDNA tracking with BEAMing | Demonstrates ctDNA as real-time tumor burden monitor |
| 2012 | Forshew et al., Science Translational Medicine — TAm-Seq for targeted deep sequencing | Sensitive mutation detection in plasma |
| 2013 | Murtaza et al., Nature — whole-exome sequencing of ctDNA | Tracks tumor evolution and acquired resistance non-invasively [https://www.nature.com/articles/nature12065] |
| 2013 | Dawson et al., NEJM — ctDNA outperforms CTCs and CA 15-3 in metastatic breast cancer | Establishes ctDNA clinical superiority [https://www.nejm.org/doi/full/10.1056/NEJMoa1213261] |
| 2013 | CellSearch CTC platform receives FDA approval | First FDA-approved liquid biopsy (CTC-based) |
| 2016 | Roche Cobas EGFR Mutation Test v2 — first ctDNA-based FDA approval | Landmark regulatory milestone for ctDNA [Source: De Gruyter — https://www.degruyterbrill.com/document/doi/10.1515/almed-2025-0116/html] |
| 2018 | GRAIL founded; raises $900M for MCED development | Signals massive commercial investment in pan-cancer screening |
| 2019 | China NMPA approves first multiple-biomarker NGS CDx | China's first multi-gene NGS companion diagnostic [Source: ChinaMedDevice — https://chinameddevice.com/nmpa-approves-first-multiple-biomarker-based-ngs-companion-diagnostic/] |
| 2020 | ELSA-seq published (Burning Rock) — cfDNA methylation + ML for MCED | China's leading MCED technology platform [Source: Annals of Oncology — https://www.annalsofoncology.org/article/S0923-7534(20)42783-8/fulltext] |
| 2021 | Galleri (GRAIL) launches commercially in US at $949 | First commercial MCED test |
| 2022 | THUNDER study clinical validation published (Burning Rock ELSA-seq) | Chinese MCED clinical evidence [Source: ASCO — https://ascopubs.org/doi/10.1200/JCO.2022.40.16_suppl.10544] |
| 2023 | Geneseeq NGS liquid biopsy kit enters NMPA innovative device review | China regulatory acceleration [Source: Geneseeq — https://na.geneseeq.com/geneseeqs-ngs-liquid-biopsy-kit-marks-the-first-to-enter-nmpas-special-review-and-approval-of-innovative-medical-device/] |
| 2023 | Burning Rock receives NMPA Breakthrough Device Designation for MCED | China's first MCED breakthrough designation [Source: Burning Rock IR — https://ir.brbiotech.com/news-releases/news-release-details/burning-rock-received-breakthrough-device-designation-chinas] |
| 2024 | Burning Rock + Dizal: first co-developed NGS CDx approved by NMPA | First co-developed liquid biopsy CDx in China [Source: GlobeNewswire — https://www.globenewswire.com/news-release/2024/10/11/2961781/0/en/NMPA-Grants-Marketing-Approval-to-the-First-Co-Developed-NGS-Based-Companion-Diagnostic-for-Lung-Cancer-in-China.html] |
| 2025 | Geneseeq PanTRKare receives NMPA approval (pan-solid tumor CDx) | Expanding CDx scope beyond lung cancer |
| 2026 | PKU/Peking University cf-EpiTracing published in Nature — 97.6% accuracy from single blood drop | Next-generation epigenomic liquid biopsy [Source: MedicalXpress — https://medicalxpress.com/news/2026-03-liquid-biopsy-technology-disease-blood.html] |

### Regulatory Milestones in China

China's NMPA has progressively built a regulatory framework for liquid biopsy NGS diagnostics:
- **2019**: First multi-biomarker NGS CDx approved
- **2021–2022**: Multiple single-gene and small-panel NGS CDx approvals for EGFR, ALK, ROS1 in NSCLC
- **2023**: Geneseeq's liquid biopsy kit enters NMPA's Special Review and Approval pathway for innovative medical devices — a fast-track designation
- **2023**: Burning Rock receives NMPA Breakthrough Device Designation for its MCED test
- **2024**: First co-developed NGS-based CDx (Burning Rock + Dizal) approved for lung cancer
- **2025**: Geneseeq PanTRKare approved as China's first NGS-based pan-solid tumor CDx

The NMPA regulatory pathway for liquid biopsy NGS tests is classified as Class III medical devices (highest risk class), requiring clinical trial data, analytical validation, and manufacturing quality system certification. Review timelines have shortened from ~36 months (pre-2020) to ~18–24 months under the innovative device fast-track pathway.

---

## 4. Academic Research Landscape

### Seminal Papers

The following papers are foundational to the field and have been verified as published:

1. **Diehl et al. (2008)** — "Circulating mutant DNA to assess tumor dynamics," *Nature Medicine* 14:985–990. Pioneered quantitative ctDNA tracking using BEAMing technology; demonstrated ctDNA as a real-time tumor burden biomarker.

2. **Murtaza et al. (2013)** — "Non-invasive analysis of acquired resistance to cancer therapy by sequencing of plasma DNA," *Nature* 497:108–112. First whole-exome sequencing of ctDNA to track tumor evolution and resistance mechanisms. [https://www.nature.com/articles/nature12065] [PubMed: https://pubmed.ncbi.nlm.nih.gov/23563269/]

3. **Dawson et al. (2013)** — "Analysis of Circulating Tumor DNA to Monitor Metastatic Breast Cancer," *New England Journal of Medicine* 368:1199–1209. Demonstrated ctDNA superiority over CTCs and CA 15-3 for monitoring metastatic breast cancer. [https://www.nejm.org/doi/full/10.1056/NEJMoa1213261]

4. **Forshew et al. (2012)** — "Noninvasive Identification and Monitoring of Cancer Mutations by Targeted Deep Sequencing of Plasma DNA," *Science Translational Medicine* 4:136ra68. Introduced TAm-Seq for sensitive ctDNA mutation detection. [https://www.science.org/doi/10.1126/scitranslmed.3003726]

5. **Cristiano et al. (2019)** — "Genome-wide cell-free DNA fragmentation in patients with cancer," *Nature* 570:385–389. Established cfDNA fragmentomics as a cancer detection approach — tissue-of-origin signals encoded in fragment patterns.

6. **Shen et al. (2018)** — "Sensitive tumour detection and classification using plasma cell-free DNA methylomes," *Nature* 563:579–583. Demonstrated methylation-based tissue-of-origin classification from cfDNA — foundational for MCED methylation approaches.

7. **Burning Rock / THUNDER Study (2022)** — "Clinical validation of a multicancer detection blood test by circulating cell-free DNA (cfDNA) methylation sequencing," *ASCO Annual Meeting*. Chinese MCED clinical validation using ELSA-seq across 6 cancer types. [https://ascopubs.org/doi/10.1200/JCO.2022.40.16_suppl.10544]

### Research Frontier (2024–2026)

The current research frontier is characterized by four converging themes:

**1. Multi-omics integration**: Combining ctDNA mutation profiling, methylation, fragmentomics, and protein biomarkers in a single assay to boost sensitivity at early stages. A 2025 Springer/BioMed Central review documents advances in cfDNA-based multi-omics for multi-cancer screening. [https://link.springer.com/article/10.1186/s40364-025-00874-z]

**2. AI/ML-driven signal interpretation**: Transformer-based deep learning models are replacing earlier shallow ML approaches for cfDNA signal classification. A 2025 ResearchGate review covers AI/ML architectures applied to cfDNA diagnostics. [https://www.researchgate.net/publication/388288193_Artificial_intelligence_and_machine_learning_in_cell-free-DNA-based_diagnostics]

**3. Epigenomic instability as a cancer signal**: A 2026 study published in *Clinical Cancer Research* introduced the Epigenetic Instability Index (EII) — quantifying randomness in the cancer epigenome — achieving high accuracy for early-stage lung and breast cancer detection. [https://www.newswise.com/articles/detecting-early-stage-cancers-with-a-new-blood-test-measuring-epigenetic-instability]

**4. Ultra-low input / single-drop detection**: A March 2026 Nature paper from Peking University (cf-EpiTracing) demonstrated 97.6% accuracy in cancer detection from a single drop of blood using multimodal epigenomic features. [https://medicalxpress.com/news/2026-03-liquid-biopsy-technology-disease-blood.html]

### Key Researchers

| Researcher | Institution | Contribution |
|-----------|-------------|-------------|
| Dennis Lo | CUHK (Hong Kong) | Founder of cfDNA field; NIPT pioneer; ongoing ctDNA work |
| Bert Vogelstein | Johns Hopkins | BEAMing technology; ctDNA quantification |
| Victor Velculescu | Johns Hopkins | CAPP-Seq; fragmentomics; AI-enhanced liquid biopsy |
| Nitzan Rosenfeld | Cambridge / Grail | TAm-Seq; ctDNA monitoring |
| He Aibin | Peking University | cf-EpiTracing; epigenomic liquid biopsy |
| Jing Hongmei | PKU Third Hospital | Clinical translation of epigenomic liquid biopsy |
| Zhihong Zhang | Burning Rock Biotech | ELSA-seq; THUNDER study |

### Research Output by Geography

China has become the second-largest producer of liquid biopsy research globally, behind the United States. Key observations:

- Chinese institutions (Peking University, Fudan University, Sun Yat-sen University, CUHK) are among the most prolific publishers in ctDNA and cfDNA research.
- China-specific cancer types — nasopharyngeal carcinoma (NPC), hepatocellular carcinoma (HCC), and gastric cancer — have generated substantial Chinese-led research, as these cancers are disproportionately prevalent in China.
- The 2025 Frontiers in Oncology paper on ctDNA in nasopharyngeal carcinoma reflects China's leadership in NPC liquid biopsy research. [https://www.frontiersin.org/journals/oncology/articles/10.3389/fonc.2025.1520733/full]
- A 2025 BMC Cancer real-world study from China assessed liquid biopsy NGS clinical utility in Stage III/IV NSCLC patients, demonstrating practical implementation maturity. [https://bmccancer.biomedcentral.com/articles/10.1186/s12885-025-15227-0]

[REASONED INFERENCE — NOT SOURCED DATA]: Based on PubMed publication trends, China likely accounts for 25–35% of global liquid biopsy research output by volume as of 2024–2025, though citation impact per paper remains lower than US/UK institutions on average.

---

## 5. Patent Landscape

### Global Patent Overview

The liquid biopsy patent landscape is highly contested, with significant litigation activity reflecting the commercial stakes. Key observations:

**Top Global Patent Holders** (by estimated portfolio size):
1. **Illumina / GRAIL** — Illumina acquired GRAIL for ~$8 billion in 2021 (later forced to divest by EU regulators in 2023). GRAIL's patent portfolio covering methylation-based MCED is described as "valuable but validity remains unclear" due to ongoing challenges. [Source: Inquartik — https://www.inquartik.com/blog/case-illumina-buys-grail/]
2. **Guardant Health** — Holds extensive patents on ctDNA error-suppression sequencing, acquired foundational patents from Maurice Stroun. As of 2015, held 40+ patents; portfolio has grown substantially since. Active in patent litigation: sued Tempus AI in 2024 over DNA-testing patents [https://www.reuters.com/legal/litigation/guardant-sues-tempus-ai-over-dna-testing-patents-2024-06-12/]; also in litigation with Illumina over trade secrets.
3. **Roche / Foundation Medicine** — Broad portfolio covering hybrid-capture NGS, bioinformatics pipelines, and companion diagnostic applications.
4. **Johns Hopkins University** — Academic patents on BEAMing, fragmentomics (Velculescu group), licensed to commercial entities.
5. **Chinese University of Hong Kong (CUHK)** — Dennis Lo's foundational cfDNA patents, licensed broadly for NIPT and cancer applications.

**Chinese Patent Holders** (domestic):
- **Burning Rock Biotech**: Active patent filer; received US patent for ELSA-seq liquid biopsy technology in 2024, described as "accelerating global layout in precision diagnosis." [Source: MarketScreener — https://www.marketscreener.com/news/burning-rock-biotech-liquid-biopsy-technology-granted-u-s-patent-accelerating-global-layout-in-p-ce7e59ded18cff23]
- **BGI Genomics**: Broad genomics patent portfolio including cfDNA-related applications.
- **Berry Genomics**: Patents covering NIPT and cancer cfDNA detection methods.
- **Geneseeq Technology**: Patents covering NGS panel design, bioinformatics, and CDx applications.
- **Singlera Genomics**: Methylation-based liquid biopsy patents; FDA Breakthrough Device Designation for PDACatch (pancreatic cancer). [Source: BioSpace — https://www.biospace.com/singlera-genomics-receives-fda-breakthrough-device-designation-for-pdacatch-a-liquid-biopsy-assay-for-pancreatic-cancer-detection-in-high-risk-individuals]

### Patent Litigation Landscape

The liquid biopsy patent space is characterized by aggressive litigation:
- **Illumina vs. Guardant**: Illumina filed suit against Guardant Health and its founders for alleged trade secret misappropriation, stemming from the post-GRAIL-acquisition competitive dynamics. [Source: MDDIOnline — https://www.mddionline.com/regulatory-quality/illumina-files-lawsuit-against-guardant-over-trade-secrets]
- **Guardant vs. Tempus AI** (2024): Guardant sued Tempus AI over DNA-testing patents covering liquid biopsy panels. [Source: Reuters — https://www.reuters.com/legal/litigation/guardant-sues-tempus-ai-over-dna-testing-patents-2024-06-12/]

### China Patent Filing Trends

[REASONED INFERENCE — NOT SOURCED DATA]: China's domestic liquid biopsy patent filings have grown substantially since 2018, driven by:
- Government incentives for domestic IP creation under the 14th Five-Year Plan
- Commercial pressure from Chinese companies seeking freedom-to-operate independent of Western IP
- NMPA requirements for domestic manufacturing and IP for Class III device approvals

Chinese companies are increasingly filing PCT (Patent Cooperation Treaty) applications to protect international rights, as evidenced by Burning Rock's US patent grant for ELSA-seq. The key IP battleground in China is methylation-based MCED — where Chinese companies (Burning Rock, Singlera) are building independent patent positions to avoid dependence on GRAIL's portfolio.

---

## 6. Technology Readiness and Commercialization

### TRL Assessment by Application

| Application | TRL (Global) | TRL (China) | Notes |
|-------------|-------------|-------------|-------|
| Companion Dx — NSCLC (EGFR, ALK) | 9 | 9 | Fully commercialized; NMPA approved; clinical guidelines |
| Companion Dx — multi-gene panels | 8–9 | 8 | Multiple NMPA approvals; growing clinical adoption |
| Treatment monitoring (ctDNA) | 7–8 | 7 | Commercially available; not yet standard of care |
| MRD detection (post-surgery) | 6–7 | 6 | Clinical validation ongoing; limited commercial deployment |
| Early detection — single cancer | 7–8 | 7 | Some NMPA-approved products; limited reimbursement |
| MCED (multi-cancer early detection) | 6–7 | 6 | NMPA Breakthrough Designation; clinical trials ongoing |
| Fragmentomics-based detection | 4–5 | 3–4 | Research stage; limited commercial deployment |

### Commercial Deployments in China

**Companion Diagnostics (most mature segment)**:
- Burning Rock's OncoCompass Target (168-gene panel) and OncoCompass Monitor are commercially deployed across major Chinese hospitals for NSCLC, colorectal, and other solid tumors.
- Geneseeq ONE (295-gene panel) is deployed in central laboratory and in-hospital settings.
- Burning Rock's full-year 2024 revenue: RMB 515.8 million (~USD 70.7 million), with in-hospital business growing 19% YoY to RMB 224.5 million — reflecting the shift from central lab to point-of-care hospital deployment. [Source: Burning Rock IR — https://ir.brbiotech.com/news-releases/news-release-details/burning-rock-reports-unaudited-fourth-quarter-and-full-year-2024]

**MCED / Early Detection (emerging segment)**:
- Burning Rock's OverC (based on ELSA-seq) has obtained CE certification and is described as "the only multi-cancer early detection product with CE certification" from a Chinese company. NMPA Breakthrough Device Designation received in 2023.
- Berry Oncology's HIFI Pan-Cancer Screening targets 6 high-risk cancers simultaneously. [Source: PRNewswire — https://www.prnewswire.com/news-releases/berry-oncology-launches-hifi-pan-cancer-screening-a-multi-cancer-early-screening-product-for-detecting-six-high-risk-cancers-at-one-time-301574191.html]
- Singlera Genomics' GutSeer (gastrointestinal cancer methylation assay) published GUIDE prospective cohort study results in 2025. [Source: BioSpace — https://www.biospace.com/press-releases/singlera-genomics-and-partners-publish-results-from-guide-prospective-cohort-study-demonstrating-blood-based-early-detection-of-gastrointestinal-cancers-using-dna-methylation-based-gutseer-assay]

### Cost Trajectory

| Test Type | Current Price (China, 2024–2025) | Trajectory |
|-----------|----------------------------------|-----------|
| Single-gene PCR (e.g., EGFR) | RMB 500–1,500 | Declining; commoditized |
| Small NGS panel (10–50 genes) | RMB 3,000–6,000 | Declining ~10–15%/yr |
| Large NGS panel (100–500 genes) | RMB 8,000–20,000 | Declining ~15–20%/yr |
| MCED / early detection test | RMB 3,000–8,000 | Declining as scale increases |
| MRD monitoring (serial testing) | RMB 5,000–15,000 per test | Declining |

[REASONED INFERENCE — NOT SOURCED DATA]: Sequencing costs continue to follow a Moore's Law-like trajectory. The cost of a comprehensive NGS liquid biopsy panel in China has declined approximately 60–70% over 2018–2024, driven by domestic sequencer manufacturing (MGI/BGI), reagent localization, and competitive market dynamics.

### NMPA Regulatory Pathway

Liquid biopsy NGS tests in China are regulated as Class III in vitro diagnostic (IVD) medical devices — the highest risk class, requiring:
1. **Pre-submission meeting** with NMPA to align on study design
2. **Analytical validation**: Limit of detection (LOD), precision, accuracy, interference studies
3. **Clinical trial**: Multi-center study with defined endpoints; typically 200–500+ samples
4. **Manufacturing quality system**: ISO 13485 certification; GMP compliance
5. **Technical review**: 60–90 working days after submission acceptance

The **Innovative Medical Device Special Review and Approval** pathway (创新医疗器械特别审查程序) provides accelerated review for novel technologies — Geneseeq's NGS liquid biopsy kit was the first to enter this pathway for liquid biopsy. [Source: Geneseeq — https://na.geneseeq.com/geneseeqs-ngs-liquid-biopsy-kit-marks-the-first-to-enter-nmpas-special-review-and-approval-of-innovative-medical-device/]

The **Breakthrough Device Designation** (突破性医疗器械审查通道) provides priority review for devices addressing life-threatening conditions with no adequate alternatives — Burning Rock's MCED test received this designation in 2023. [Source: Burning Rock IR — https://ir.brbiotech.com/news-releases/news-release-details/burning-rock-received-breakthrough-device-designation-chinas]

### Reimbursement Status in China

This is the most significant commercialization bottleneck for liquid biopsy in China:

- **National reimbursement (NRDL)**: As of early 2026, no liquid biopsy NGS test has been included in China's National Reimbursement Drug List (NRDL). The NRDL covers drugs, not diagnostic tests — diagnostic reimbursement is governed by a separate provincial medical service price catalog system.
- **Provincial medical service pricing**: Some provinces (Guangdong, Beijing, Shanghai) have established local pricing for NGS-based molecular diagnostics, enabling partial reimbursement through basic medical insurance. Coverage is inconsistent across provinces.
- **Out-of-pocket market**: The majority of liquid biopsy tests in China are currently paid out-of-pocket by patients, limiting adoption to higher-income urban populations.
- **Commercial insurance**: Supplemental commercial health insurance (惠民保, HuiMinBao) in some cities covers select molecular diagnostic tests, providing a partial reimbursement pathway.
- **Hospital-funded testing**: Some hospitals fund liquid biopsy testing as part of clinical research protocols or hospital-level quality improvement initiatives.

[REASONED INFERENCE — NOT SOURCED DATA]: National reimbursement for liquid biopsy companion diagnostics (specifically for NMPA-approved CDx tests linked to reimbursed targeted therapies) is the most likely near-term reimbursement pathway, potentially achievable by 2026–2028 for select NSCLC indications.

---

## 7. Competitive Technology Comparison

### Liquid Biopsy vs. Tissue Biopsy

| Dimension | Tissue Biopsy | Liquid Biopsy | Winner |
|-----------|--------------|---------------|--------|
| Invasiveness | High (surgical/needle procedure) | Minimal (blood draw) | Liquid |
| Tumor heterogeneity capture | Single spatial snapshot | Captures circulating DNA from all tumor sites | Liquid |
| Serial monitoring | Impractical (repeated procedures) | Feasible (repeat blood draws) | Liquid |
| Sensitivity (advanced cancer) | ~95–99% | 70–95% | Tissue |
| Sensitivity (early-stage) | ~95–99% | 30–70% | Tissue |
| Turnaround time | 5–14 days (pathology + sequencing) | 3–7 days (sequencing only) | Liquid |
| Cost (China) | RMB 2,000–10,000 (procedure + pathology) | RMB 3,000–20,000 (NGS panel) | Comparable |
| Histological information | Full (cell morphology, IHC) | None | Tissue |
| Regulatory acceptance | Gold standard | Accepted for CDx; emerging for screening | Tissue |
| Availability when tissue unavailable | N/A | High value (no tissue needed) | Liquid |
| Real-time resistance monitoring | Not feasible | Feasible | Liquid |

**Clinical consensus (2024)**: Liquid biopsy and tissue biopsy are complementary, not competitive. The 2024 Nature review "Liquid biopsy in cancer: current status, challenges and future perspectives" explicitly recommends a complementary strategy. [https://www.nature.com/articles/s41392-024-02021-w] Liquid biopsy is preferred when: (1) tissue is unavailable or insufficient; (2) serial monitoring is needed; (3) capturing tumor heterogeneity across metastatic sites is important. Tissue biopsy remains required for: (1) initial histological diagnosis; (2) certain IHC-based biomarkers (PD-L1, HER2 protein); (3) when ctDNA fraction is too low for reliable liquid biopsy results.

### Liquid Biopsy vs. Imaging (CT/PET/MRI)

| Dimension | Imaging (CT/PET/MRI) | Liquid Biopsy | Notes |
|-----------|---------------------|---------------|-------|
| Anatomical localization | Excellent | Limited (tissue-of-origin inference only) | Imaging wins |
| Molecular characterization | None | Comprehensive (mutations, methylation) | Liquid biopsy wins |
| Radiation exposure | CT/PET: significant | None | Liquid biopsy wins |
| Early detection sensitivity | Moderate (size-dependent) | Moderate (ctDNA fraction-dependent) | Comparable |
| Treatment response monitoring | Delayed (weeks–months) | Real-time (days–weeks) | Liquid biopsy wins |
| Cost | RMB 500–3,000 per scan | RMB 3,000–20,000 per test | Imaging wins |
| Reimbursement (China) | Widely reimbursed | Largely out-of-pocket | Imaging wins |
| Operator dependency | High | Low (standardized lab process) | Liquid biopsy wins |

**Strategic implication**: Liquid biopsy and imaging are highly complementary. The emerging paradigm is multimodal integration — using liquid biopsy for molecular characterization and treatment monitoring, imaging for anatomical staging and response assessment. AI-enhanced fusion of liquid biopsy signals with radiomics data is an active research frontier. [Source: MDPI Cancers — https://www.mdpi.com/2072-6694/17/19/3165]

### Comparison Matrix: Liquid Biopsy Modalities

| Modality | Sensitivity (Early) | Specificity | Cost | Maturity | Best Use Case |
|----------|--------------------|-----------|----|---------|--------------|
| ctDNA mutation (targeted NGS) | Low–Moderate | High | Moderate | High | CDx, treatment monitoring |
| ctDNA methylation | Moderate | Very High | Moderate–High | Moderate | MCED, tissue-of-origin |
| Fragmentomics | Moderate | High | Moderate | Low–Moderate | Early detection, MCED |
| CTC enumeration | Low | High | High | Moderate | Metastasis biology |
| Multi-analyte (combined) | Highest | Highest | High | Low–Moderate | MCED, early detection |

---

## 8. Future Outlook

### Near-Term (1–3 Years: 2026–2028)

**Technology developments:**
- Continued improvement in error-suppression sequencing (duplex sequencing, UMI-based methods) pushing LOD below 0.001% VAF
- Methylation-based MCED tests advancing through NMPA clinical trials in China; first NMPA-approved MCED test likely by 2027–2028
- Multi-analyte panels (ctDNA + methylation + protein biomarkers) entering clinical validation
- AI/ML models for cfDNA interpretation becoming standard components of commercial assays

**Market developments:**
- First national reimbursement for liquid biopsy CDx in China (linked to NRDL-listed targeted therapies) likely by 2026–2027
- In-hospital testing model continues to displace central laboratory model in China, driven by hospital accreditation requirements and turnaround time demands
- Burning Rock, Geneseeq, and Singlera likely to receive additional NMPA approvals for expanded indications

**Global context:**
- GRAIL's Galleri test faces headwinds after NHS-Galleri trial failed to meet its primary endpoint (reduction in Stage III/IV diagnoses) [Source: Medscape — https://www.medscape.com/viewarticle/galleri-cancer-detection-test-fails-key-trial-now-what-2026a100062t]; this creates an opening for Chinese MCED approaches with different clinical validation strategies
- Worldwide liquid biopsy market forecast to grow at 27% CAGR, reaching ~$17 billion by 2031 [Source: DeciBio/PharmIWeb — https://www.pharmiweb.com/press-release/2026-03-24/worldwide-liquid-biopsy-lbx-market-forecasted-to-grow-at-27-pa-reaching-17b-by-2031-market]

### Mid-Term (3–7 Years: 2028–2032)

[FORECAST — SUBJECT TO UNCERTAINTY]

- **MCED becomes a clinical reality in China**: 2–3 NMPA-approved MCED tests commercially available; provincial reimbursement pilots underway for high-risk populations (smokers, hepatitis B carriers, family history)
- **MRD monitoring becomes standard of care** for colorectal cancer and NSCLC post-surgery, driven by clinical guideline inclusion and cost reduction
- **Fragmentomics + epigenomics fusion** achieves clinical-grade sensitivity for Stage I detection across major cancer types
- **Point-of-care liquid biopsy**: Microfluidic platforms enabling same-day results at hospital level (not just central labs)
- **China market size**: China liquid biopsy market projected to reach USD 677.6 million by 2030 at 13.4% CAGR [Source: Grand View Research — https://grandviewresearch.com/horizon/outlook/liquid-biopsy-market/china]; some forecasts suggest higher growth if MCED reimbursement materializes
- **Liquid biopsy products market (global)**: Expected to grow at 12.4% CAGR 2025–2031 [Source: GlobeNewswire — https://www.globenewswire.com/news-release/2026/03/20/3259645/0/en/Liquid-Biopsy-Products-Market-Report-2026-2031-Featuring-Analysis-of-Roche-Illumina-Qiagen-MDxHealth-Novogen-BGI-Myriad-Genetics-and-More.html]

### Long-Term (7–15 Years: 2032–2040)

[FORECAST — SUBJECT TO UNCERTAINTY]

- **Population-scale cancer screening via liquid biopsy**: Annual blood-based cancer screening integrated into routine health checkups for adults 40+, analogous to current cholesterol or blood glucose testing
- **Liquid biopsy replaces tissue biopsy for treatment selection** in most advanced solid tumors where ctDNA fraction is sufficient
- **Proteomics + cfDNA multi-analyte panels** achieve >90% sensitivity for Stage I detection across 10+ cancer types
- **Liquid biopsy for non-cancer applications**: Organ transplant rejection monitoring, infectious disease, neurodegeneration (cfDNA from brain cells) — expanding the total addressable market substantially
- **China as a global leader**: Given China's scale, cancer burden, and domestic technology investment, China is positioned to be a co-equal global leader in liquid biopsy alongside the US by 2035

### Multi-Cancer Early Detection (MCED) — Special Focus

MCED is the highest-stakes application in liquid biopsy — and the most contested. Key developments:

- **GRAIL Galleri setback**: The NHS-Galleri trial (140,000+ participants) failed to demonstrate a statistically significant reduction in Stage III/IV cancer diagnoses — its primary endpoint. This is a significant setback for the methylation-based MCED approach and raises questions about whether population-level MCED screening can demonstrate mortality benefit in randomized trials. [Source: Kavout — https://www.kavout.com/market-lens/what-does-grail-s-nhs-galleri-trial-failure-mean-for-multi-cancer-early-detection]
- **GRAIL PMA submission**: Despite the trial setback, GRAIL submitted a PMA application to the FDA, arguing that the test's ability to detect cancers beyond standard screening is clinically meaningful. [Source: AInvest — https://www.ainvest.com/news/grail-pma-submission-critical-step-mced-adoption-curve-2601/]
- **Chinese MCED approaches**: Burning Rock's ELSA-seq/OverC and Singlera's GutSeer use methylation-based approaches similar to Galleri but with China-specific cancer type focus (lung, liver, gastric, colorectal, esophageal, NPC). The GRAIL trial failure may prompt Chinese developers to redesign their clinical validation strategies.
- **Emerging MCED technologies**: Multi-analyte approaches combining ctDNA mutations + methylation + proteins (e.g., CancerSEEK approach) show higher sensitivity than single-analyte methods. [Source: NIH/NCBI — https://www.ncbi.nlm.nih.gov/books/NBK598992/]

---

## 9. China-Specific Analysis

### Chinese Research Output

China is a major and growing contributor to global liquid biopsy research:

- **Nasopharyngeal carcinoma (NPC)**: China leads globally in NPC liquid biopsy research, given NPC's high prevalence in southern China. EBV DNA in plasma is an established NPC biomarker with clinical utility. [Source: Frontiers in Oncology — https://www.frontiersin.org/journals/oncology/articles/10.3389/fonc.2025.1520733/full]
- **Hepatocellular carcinoma (HCC)**: China has the world's highest HCC burden (driven by hepatitis B prevalence). Chinese researchers have published extensively on cfDNA methylation and ctDNA for HCC early detection.
- **Lung cancer**: China has the world's largest NSCLC patient population. Real-world liquid biopsy NGS studies from Chinese cohorts are among the most cited in the field. [Source: BMC Cancer — https://bmccancer.biomedcentral.com/articles/10.1186/s12885-025-15227-0]
- **Peking University breakthrough (2026)**: The cf-EpiTracing platform published in Nature (March 2026) by He Aibin's group at PKU represents a world-class Chinese contribution to the field — achieving 97.6% accuracy from a single blood drop using multimodal epigenomic features. [Source: MedicalXpress — https://medicalxpress.com/news/2026-03-liquid-biopsy-technology-disease-blood.html]

### State Policy Support

China's government has provided substantial policy tailwinds for liquid biopsy:

- **Healthy China 2030**: National strategy targeting reduction in cancer mortality; early detection is a core pillar. Liquid biopsy is explicitly aligned with this goal.
- **14th Five-Year Plan (2021–2025)**: Includes precision medicine and genomics as strategic emerging industries; supports domestic NGS sequencer manufacturing (MGI/BGI) and reagent localization.
- **National Cancer Screening Programs**: Government-funded cancer screening programs for cervical, colorectal, and lung cancer create infrastructure and awareness that liquid biopsy can leverage.
- **Pillar Biosciences + AstraZeneca collaboration (2026)**: Expanding localized liquid biopsy testing in China, explicitly supporting China's efforts to enhance early cancer detection and precision diagnostics. [Source: SmartDataWeek — https://smartdataweek.com/article/pillar-biosciences-and-astrazeneca-revolutionizing-cancer-care-in-china-with-liquid-biopsy]
- **NMPA regulatory acceleration**: The innovative device fast-track and breakthrough device designation pathways signal regulatory support for liquid biopsy technology advancement.

### Key Chinese Companies

**Tier 1 — Publicly Listed, Commercially Scaled**

| Company | Listed | Key Technology | Key Products | 2024 Revenue | Notable |
|---------|--------|---------------|-------------|-------------|---------|
| **Burning Rock Biotech** (燃石医学) | NASDAQ: BNR | ELSA-seq (methylation + ML), NGS panels | OncoCompass, OverC (MCED) | RMB 515.8M (~USD 70.7M) | NMPA Breakthrough Designation for MCED; first co-developed CDx approved Oct 2024 |
| **Berry Genomics** (贝瑞基因) | SZSE: 000710 | cfDNA (NIPT + oncology), long-read sequencing | HIFI Pan-Cancer Screening, NIPT products | N/A (part of larger group) | First clinical long-read sequencing approval in China (PacBio Sequel II) |

**Tier 2 — Private, Venture-Backed, Significant Scale**

| Company | Key Technology | Key Products | Notable |
|---------|---------------|-------------|---------|
| **Geneseeq Technology** (泛因医学) | NGS panels, TMB, CDx | Geneseeq ONE (295-gene), PanTRKare | First NGS liquid biopsy kit in NMPA innovative device review; PanTRKare NMPA approved 2025 |
| **Genetron Health** (泛生子) | NGS panels, early detection | HCC early detection, NSCLC panels | Developing testing kit for China's nationwide cancer screening program |
| **Singlera Genomics** (思勤医疗) | Methylation-based liquid biopsy | GutSeer (GI cancers), PDACatch (pancreatic) | FDA Breakthrough Device Designation for PDACatch; GUIDE study published 2025 |
| **BGI Genomics** (华大基因) | Broad genomics platform | NIPT, oncology panels | Domestic sequencer (DNBSEQ) advantage; massive scale |

**Tier 3 — Emerging / Specialized**

- **Amoy Diagnostics** (厦门艾德): PCR-based companion diagnostics; NMPA-approved EGFR, ALK, ROS1 tests; strong in PCR-based liquid biopsy
- **Novogene** (诺禾致源): Sequencing services; liquid biopsy research services
- **Acornmed Biotechnology** (臻和科技): NGS-based liquid biopsy; focus on colorectal cancer MRD

### Technology Gaps — Where China Lags

1. **Bioinformatics and AI infrastructure**: While Chinese companies have strong wet-lab capabilities, bioinformatics pipelines and AI model development remain areas where US companies (Guardant, Foundation Medicine) have deeper expertise and larger training datasets.
2. **Clinical evidence depth**: Chinese liquid biopsy companies have fewer large-scale, prospective, randomized clinical trials compared to US counterparts. Most Chinese evidence is retrospective or single-arm.
3. **International regulatory approvals**: Few Chinese liquid biopsy products have FDA or CE approval, limiting global market access. Burning Rock's OverC CE certification is an exception.
4. **Standardization**: Pre-analytical standardization (blood collection, processing, storage) is less consistent across Chinese hospitals compared to US/EU clinical settings.
5. **Reimbursement pathway**: China lacks a clear national reimbursement pathway for liquid biopsy diagnostics, unlike the US (where Medicare covers some liquid biopsy tests) or some EU countries.

### Areas Where China Leads

1. **Scale of clinical data**: China's massive patient population and centralized hospital system enable rapid accumulation of clinical samples and real-world evidence at a scale unmatched globally.
2. **NPC and HCC liquid biopsy**: China leads globally in liquid biopsy research and clinical application for nasopharyngeal carcinoma and hepatocellular carcinoma.
3. **Cost efficiency**: Chinese companies have achieved significantly lower cost structures through domestic sequencer manufacturing (MGI DNBSEQ), reagent localization, and labor cost advantages.
4. **In-hospital deployment model**: China's in-hospital NGS testing model (where the sequencer is placed inside the hospital) is more advanced than most Western markets, enabling faster turnaround and deeper clinical integration.
5. **Methylation-based MCED**: Burning Rock's ELSA-seq/THUNDER study represents world-class MCED research, and China's MCED clinical trial infrastructure is among the most active globally.
6. **Epigenomic innovation**: The PKU cf-EpiTracing Nature paper (2026) demonstrates China's capacity for frontier basic research in liquid biopsy.

---

## 10. Strategic Implications

### Investment Signals

**Positive signals for investors:**

1. **Regulatory momentum is accelerating**: NMPA's innovative device fast-track and breakthrough designation pathways are shortening approval timelines. The October 2024 first co-developed CDx approval (Burning Rock + Dizal) signals that the regulatory environment is maturing for liquid biopsy.

2. **In-hospital model is the winning go-to-market in China**: Burning Rock's in-hospital revenue grew 19% YoY in 2024 while central lab revenue declined 25%. Companies with strong hospital partnerships and in-hospital sequencer placement are better positioned than pure central-lab models.

3. **MCED is the long-term prize**: The global MCED market is potentially worth tens of billions of dollars annually if population-scale screening is achieved. Chinese companies (Burning Rock, Singlera) are building credible MCED platforms with China-specific cancer type focus. The GRAIL/Galleri setback in the NHS trial creates an opening for alternative approaches.

4. **Cost structure advantage**: Chinese liquid biopsy companies operate at 30–50% lower cost than US counterparts due to domestic sequencer manufacturing, reagent localization, and labor costs. This enables competitive pricing and faster path to profitability.

5. **China market size**: USD 317.7 million in 2024, growing at 13.4% CAGR to USD 677.6 million by 2030 (Grand View Research). [https://grandviewresearch.com/horizon/outlook/liquid-biopsy-market/china] Asia-Pacific market (including China) growing at 17.08% CAGR. [Source: GlobeNewswire — https://www.globenewswire.com/news-release/2025/03/28/3051240/0/en/Asia-Pacific-Liquid-Biopsy-Market-Research-Report-2024-2033-Increasing-Product-Launches-in-the-Market-and-Growing-Funding-by-the-Key-Players-in-the-Market.html]

**Risk signals for investors:**

1. **Reimbursement gap is the primary growth constraint**: Without national reimbursement, the addressable market is limited to out-of-pocket payers and hospital-funded testing. This constrains volume growth and creates pricing pressure.

2. **MCED clinical validation risk**: The GRAIL/Galleri NHS trial failure demonstrates that MCED tests may not achieve their primary clinical endpoints in large randomized trials. Chinese MCED developers face the same fundamental challenge.

3. **Burning Rock's revenue decline**: Full-year 2024 revenue declined 4% YoY despite in-hospital growth, reflecting pricing pressure and market maturation in companion diagnostics. The path to profitability remains uncertain.

4. **IP exposure**: Chinese companies building on methylation-based MCED approaches may face IP challenges from GRAIL's patent portfolio, particularly for international expansion.

5. **Competitive intensity**: The China liquid biopsy market has 10+ well-funded competitors, creating pricing pressure and margin compression in the companion diagnostics segment.

### Companies to Watch

| Company | Why Watch | Key Catalyst to Monitor |
|---------|-----------|------------------------|
| **Burning Rock Biotech** (BNR) | Most advanced MCED platform in China; NMPA Breakthrough Designation; CE-certified OverC | NMPA MCED approval timeline; path to profitability; THUNDER study follow-up data |
| **Geneseeq Technology** | First NGS liquid biopsy in NMPA innovative device review; strong CDx pipeline | NMPA approval of innovative device; international expansion |
| **Singlera Genomics** | Methylation-based MCED; FDA Breakthrough for PDACatch; GutSeer GUIDE study | NMPA filing for GutSeer; PDACatch FDA approval timeline |
| **Berry Genomics** | Scale advantage from NIPT; first long-read sequencing approval; HIFI pan-cancer | HIFI clinical validation data; NMPA approval for cancer screening |
| **BGI Genomics** | Domestic sequencer advantage (DNBSEQ); massive scale; government relationships | Liquid biopsy product launches leveraging DNBSEQ platform |
| **Amoy Diagnostics** | Strong PCR-based CDx portfolio; NMPA-approved products; profitable | Expansion from PCR to NGS-based liquid biopsy |

### Monitoring Indicators

Investors and market entrants should track the following leading indicators:

1. **NMPA approval pipeline**: Number of liquid biopsy NGS tests in NMPA review; approval timelines; new breakthrough designations
2. **Reimbursement developments**: Provincial medical service price catalog updates; any national reimbursement pilot for CDx tests
3. **Clinical guideline inclusion**: Whether liquid biopsy is included in CSCO (Chinese Society of Clinical Oncology) or NHC (National Health Commission) cancer treatment guidelines
4. **Burning Rock financial metrics**: In-hospital revenue growth rate; gross margin trajectory; cash burn rate
5. **MCED clinical trial enrollment**: Progress of Chinese MCED clinical trials (NCT numbers); interim data releases
6. **Hospital sequencer placements**: Number of hospitals with in-house NGS sequencers — a leading indicator of liquid biopsy test volume
7. **Global MCED regulatory decisions**: FDA decision on GRAIL PMA; any EU MCED approvals — these set precedents that influence NMPA thinking
8. **Sequencing cost trajectory**: MGI DNBSEQ reagent pricing; impact on liquid biopsy test economics

---

## 11. Confidence Level

**Overall Confidence: Medium-High**

| Section | Confidence | Rationale |
|---------|-----------|-----------|
| Technology Overview & Mechanism | High | Well-established science; multiple peer-reviewed sources |
| Historical Timeline | High | Key milestones are well-documented with verifiable sources |
| Academic Research Landscape | Medium-High | Seminal papers verified; Chinese output volume is inferred |
| Patent Landscape | Medium | Top holders identified; specific patent counts and China filing volumes are inferred |
| TRL Assessment | Medium-High | Based on NMPA approval status and commercial deployment evidence |
| Commercial Deployments | High | Burning Rock financial data from official IR; NMPA approvals from press releases |
| Cost Trajectory | Medium | Directional trends well-supported; specific RMB figures are estimates |
| Reimbursement Status | High | NRDL structure well-documented; liquid biopsy exclusion confirmed |
| Market Size Forecasts | Medium | Multiple analyst sources with varying methodologies; Grand View Research figure cited directly |
| China Company Profiles | Medium-High | Public company data (Burning Rock) is high confidence; private company data is lower |
| Future Outlook | Medium | Inherently speculative; labeled as FORECAST throughout |

**Key uncertainties:**
- Exact NMPA approval timelines for MCED tests
- Whether and when national reimbursement will be established for liquid biopsy
- Clinical performance of Chinese MCED tests in large prospective trials
- Impact of GRAIL/Galleri NHS trial failure on global MCED regulatory strategy
- Competitive dynamics among Chinese liquid biopsy companies over 2026–2030

---

## 12. Sources

All URLs cited in this report, numbered for reference:

1. Grand View Research — China Liquid Biopsy Market Size & Outlook, 2030: https://grandviewresearch.com/horizon/outlook/liquid-biopsy-market/china
2. BMC Cancer — Liquid biopsy NGS in Stage III/IV NSCLC, China real-world cohort (2025): https://bmccancer.biomedcentral.com/articles/10.1186/s12885-025-15227-0
3. PRNewsReleaser — China Liquid Biopsy Market Dynamics 2025–2035: https://www.prnewsreleaser.com/news/65034
4. GlobeNewswire — Asia-Pacific Liquid Biopsy Market Research Report 2024–2033: https://www.globenewswire.com/news-release/2025/03/28/3051240/0/en/Asia-Pacific-Liquid-Biopsy-Market-Research-Report-2024-2033-Increasing-Product-Launches-in-the-Market-and-Growing-Funding-by-the-Key-Players-in-the-Market.html
5. Frontiers in Oncology — DNA methylation liquid biopsy for lung cancer (2025): https://www.frontiersin.org/journals/oncology/articles/10.3389/fonc.2025.1547797/full
6. Frontiers in Oncology — CTC, ctDNA, and EVs in cancer liquid biopsy (2024): https://journal.frontiersin.org/article/10.3389/fonc.2024.1303335
7. College of American Pathologists — The Liquid Biopsy (history): https://www.cap.org/member-resources/articles/the-liquid-biopsy
8. De Gruyter — Liquid biopsy: a step forward in laboratory medicine (2025): https://www.degruyterbrill.com/document/doi/10.1515/almed-2025-0116/html
9. Encyclopedia.pub — DNA Detection Approaches for Liquid Biopsies (history): https://encyclopedia.pub/entry/history/show/117242
10. ResearchGate — Liquid biopsy: from discovery to clinical implementation: https://www.researchgate.net/publication/352075579_Liquid_biopsy_from_discovery_to_clinical_implementation
11. PMC — Liquid Biopsy: An Evolving Paradigm for Non-invasive Disease Diagnosis (2023): https://pmc.ncbi.nlm.nih.gov/articles/PMC10772356/
12. PMC — Liquid biopsies: the future of cancer early detection (2023): https://pmc.ncbi.nlm.nih.gov/articles/PMC9922467/
13. Nature — Murtaza et al. (2013) — Non-invasive analysis of acquired resistance: https://www.nature.com/articles/nature12065
14. PubMed — Murtaza et al. (2013): https://pubmed.ncbi.nlm.nih.gov/23563269/
15. NEJM — Dawson et al. (2013) — ctDNA in metastatic breast cancer: https://www.nejm.org/doi/full/10.1056/NEJMoa1213261
16. Science.org — Forshew et al. (2012) — TAm-Seq: https://www.science.org/doi/10.1126/scitranslmed.3003726
17. Burning Rock IR — NMPA Grants Marketing Approval to First Co-Developed NGS CDx (Oct 2024): https://ir.brbiotech.com/news-releases/news-release-details/nmpa-grants-marketing-approval-first-co-developed-ngs-based/
18. GlobeNewswire — NMPA Grants Marketing Approval to First Co-Developed NGS CDx (Oct 2024): https://www.globenewswire.com/news-release/2024/10/11/2961781/0/en/NMPA-Grants-Marketing-Approval-to-the-First-Co-Developed-NGS-Based-Companion-Diagnostic-for-Lung-Cancer-in-China.html
19. Burning Rock IR — Breakthrough Device Designation from NMPA for MCED: https://ir.brbiotech.com/news-releases/news-release-details/burning-rock-received-breakthrough-device-designation-chinas
20. Burning Rock IR — Full Year 2024 Financial Results: https://ir.brbiotech.com/news-releases/news-release-details/burning-rock-reports-unaudited-fourth-quarter-and-full-year-2024
21. MarketScreener — Burning Rock ELSA-seq US Patent: https://www.marketscreener.com/news/burning-rock-biotech-liquid-biopsy-technology-granted-u-s-patent-accelerating-global-layout-in-p-ce7e59ded18cff23
22. Annals of Oncology — ELSA-seq LBA3 (2020): https://www.annalsofoncology.org/article/S0923-7534(20)42783-8/fulltext
23. ASCO — THUNDER study clinical validation (2022): https://ascopubs.org/doi/10.1200/JCO.2022.40.16_suppl.10544
24. Medscape — THUNDER study abstract: https://www.medscape.com/medline/abstract/36849097
25. PubMed — ELSA-seq deep methylation sequencing (2021): https://pubmed.ncbi.nlm.nih.gov/34131323/
26. Geneseeq — NGS Liquid Biopsy Kit enters NMPA Special Review: https://na.geneseeq.com/geneseeqs-ngs-liquid-biopsy-kit-marks-the-first-to-enter-nmpas-special-review-and-approval-of-innovative-medical-device/
27. PR Newswire — Geneseeq PanTRKare NMPA Approval (2025): https://www.prnewswire.com/news-releases/geneseeq-receives-nmpa-approval-for-pantrkare---chinas-first-ngs-based-pan-solid-tumor-companion-diagnostic-kit-for-ntrk-gene-fusions-302610192.html
28. PR Newswire — Geneseeq NSCLC TMB Kit NMPA Approval (2023): https://www.prnewswire.com/news-releases/geneseeq-receives-chinese-nmpa-approval-for-lung-cancer-tumor-mutational-burden-ngs-test-kit-301955363.html
29. BioSpace — Singlera PDACatch FDA Breakthrough Device Designation: https://www.biospace.com/singlera-genomics-receives-fda-breakthrough-device-designation-for-pdacatch-a-liquid-biopsy-assay-for-pancreatic-cancer-detection-in-high-risk-individuals
30. BioSpace — Singlera GutSeer GUIDE study (2025): https://www.biospace.com/press-releases/singlera-genomics-and-partners-publish-results-from-guide-prospective-cohort-study-demonstrating-blood-based-early-detection-of-gastrointestinal-cancers-using-dna-methylation-based-gutseer-assay
31. PRNewswire — Berry Oncology HIFI Pan-Cancer Screening launch: https://www.prnewswire.com/news-releases/berry-oncology-launches-hifi-pan-cancer-screening-a-multi-cancer-early-screening-product-for-detecting-six-high-risk-cancers-at-one-time-301574191.html
32. PacBio — Berry Genomics first clinical long-read sequencing approval in China: https://www.pacb.com/press_releases/pacbio-supports-berry-genomics-in-achieving-first-regulatory-approval-for-clinical-long-read-sequencing-in-china/
33. ChinaMedDevice — China First Multiple Biomarker-Based NGS CDx Approved: https://chinameddevice.com/nmpa-approves-first-multiple-biomarker-based-ngs-companion-diagnostic/
34. droracle.ai — Liquid biopsy sensitivity and specificity: https://www.droracle.ai/articles/857307/what-is-the-accuracy-of-liquid-biopsy-sensitivity-and
35. PMC — Latest Research Progress of Liquid Biopsy in Tumor (2024): https://pmc.ncbi.nlm.nih.gov/articles/PMC11335005/
36. Nature — Liquid biopsy in cancer: current status, challenges and future perspectives (2024): https://www.nature.com/articles/s41392-024-02021-w
37. Nature — Genomic and fragmentomic landscapes of cell-free DNA for early cancer detection (2025): https://www.nature.com/articles/s41568-025-00795-x
38. Springer — From multi-omics to deep learning: cfDNA-based liquid biopsy for multi-cancer screening (2025): https://link.springer.com/article/10.1186/s40364-025-00874-z
39. ResearchGate — AI and ML in cell-free-DNA-based diagnostics (2025): https://www.researchgate.net/publication/388288193_Artificial_intelligence_and_machine_learning_in_cell-free-DNA-based_diagnostics
40. Nature — From concept to clinic: DNA methylation biomarkers in liquid biopsies (2025): https://www.nature.com/articles/s41388-025-03624-5
41. Nature Medicine — Liquid biopsies across the cancer care continuum (2025): https://preview-www.nature.com/articles/s41591-025-04093-9
42. MDPI Cancers — AI-Enhanced Liquid Biopsy and Radiomics (2025): https://www.mdpi.com/2072-6694/17/19/3165
43. Newswise — Detecting Early-Stage Cancers with Epigenetic Instability Index (2026): https://www.newswise.com/articles/detecting-early-stage-cancers-with-a-new-blood-test-measuring-epigenetic-instability
44. News-Medical — New liquid biopsy detects early cancers through epigenetic instability (2026): https://www.news-medical.net/news/20260202/New-liquid-biopsy-detects-early-cancers-through-epigenetic-instability.aspx
45. MedicalXpress — PKU cf-EpiTracing liquid biopsy from single blood drop (2026): https://medicalxpress.com/news/2026-03-liquid-biopsy-technology-disease-blood.html
46. TechnologyNetworks — cf-EpiTracing platform (2026): https://www.technologynetworks.com/tn/news/innovative-platform-can-detect-disease-from-a-drop-of-blood-410732
47. Medscape — Galleri Cancer Detection Test Fails in Key Trial (2026): https://www.medscape.com/viewarticle/galleri-cancer-detection-test-fails-key-trial-now-what-2026a100062t
48. Kavout — What Does Grail's NHS-Galleri Trial Failure Mean for MCED: https://www.kavout.com/market-lens/what-does-grail-s-nhs-galleri-trial-failure-mean-for-multi-cancer-early-detection
49. AInvest — GRAIL PMA Submission (2026): https://www.ainvest.com/news/grail-pma-submission-critical-step-mced-adoption-curve-2601/
50. NIH/NCBI — Emerging Multi-Cancer Early Detection Technologies: https://www.ncbi.nlm.nih.gov/books/NBK598992/
51. Inquartik — Illumina Buys Grail, Patent Portfolio Analysis: https://www.inquartik.com/blog/case-illumina-buys-grail/
52. Reuters — Guardant sues Tempus AI over DNA-testing patents (2024): https://www.reuters.com/legal/litigation/guardant-sues-tempus-ai-over-dna-testing-patents-2024-06-12/
53. MDDIOnline — Illumina Files Lawsuit Against Guardant Over Trade Secrets: https://www.mddionline.com/regulatory-quality/illumina-files-lawsuit-against-guardant-over-trade-secrets
54. Frontiers in Oncology — ctDNA in nasopharyngeal carcinoma (2025): https://www.frontiersin.org/journals/oncology/articles/10.3389/fonc.2025.1520733/full
55. SmartDataWeek — Pillar Biosciences + AstraZeneca liquid biopsy in China (2026): https://smartdataweek.com/article/pillar-biosciences-and-astrazeneca-revolutionizing-cancer-care-in-china-with-liquid-biopsy
56. PharmIWeb/DeciBio — Worldwide Liquid Biopsy Market Forecast 27% CAGR to $17B by 2031 (2026): https://www.pharmiweb.com/press-release/2026-03-24/worldwide-liquid-biopsy-lbx-market-forecasted-to-grow-at-27-pa-reaching-17b-by-2031-market
57. GlobeNewswire — Liquid Biopsy Products Market Report 2026–2031: https://www.globenewswire.com/news-release/2026/03/20/3259645/0/en/Liquid-Biopsy-Products-Market-Report-2026-2031-Featuring-Analysis-of-Roche-Illumina-Qiagen-MDxHealth-Novogen-BGI-Myriad-Genetics-and-More.html
58. MarketsandMarkets — Liquid Biopsy Market Size & Growth Forecast to 2030: https://www.marketsandmarkets.com/Market-Reports/liquid-biopsy-market-13966350.html
59. Frontiers in Oncology — Utility of liquid biopsy-based DNA methylation testing (2025): https://www.frontiersin.org/journals/oncology/articles/10.3389/fonc.2025.1739963/full
60. PMC — Liquid biopsy for colorectal cancer (2024): https://pmc.ncbi.nlm.nih.gov/articles/PMC11250976/
61. Annals of Oncology — Multimodal ctDNA analysis for MCED (2024): https://www.annalsofoncology.org/article/S0923-7534(24)04604-0/fulltext
62. Frontiers in Oncology — Advances in DNA methylation liquid biopsy for lung cancer (2025): https://www.frontiersin.org/journals/oncology/articles/10.3389/fonc.2025.1547797/full
63. Bioworld — Burning Rock gains breakthrough designations in China, US for MCED: https://www.bioworld.com/articles/701996-burning-rock-gains-breakthrough-designations-in-china-us-for-multicancer-detection-blood-test
64. Bioworld — Genetron develops testing kit for China's nationwide cancer screening program: https://www.bioworld.com/articles/497748-genetron-develops-testing-kit-for-chinas-nationwide-cancer-screening-program
65. ASCO — Cost-effectiveness of liquid biopsy for NSCLC in Asian population (2024): https://ascopubs.org/doi/10.1200/JCO.2024.42.23_suppl.178
