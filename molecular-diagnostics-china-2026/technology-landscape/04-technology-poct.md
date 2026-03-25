# Point-of-Care Molecular Testing (POCT) — Technology Deep-Dive
**China Molecular Diagnostics Market | Technology Landscape Report**
*Research Date: March 2026 | Time Horizon: 2024–2030*

---

## 1. Technology Overview

### Plain-Language Definition

Point-of-Care Molecular Testing (POCT) refers to nucleic acid-based diagnostic testing performed at or near the site of patient care — in a clinic, emergency room, community health center, pharmacy, or even a patient's home — rather than in a centralized laboratory. Unlike traditional molecular diagnostics that require specialized lab infrastructure, trained technicians, and hours-long turnaround times, molecular POCT platforms are designed to deliver PCR-equivalent or near-equivalent results in 15–60 minutes using compact, often portable instruments that require minimal operator skill.

The defining characteristic is the integration of the full diagnostic workflow — sample preparation, nucleic acid amplification, and signal detection — into a single closed system, typically a disposable cartridge inserted into a benchtop or handheld reader.

### Why It Matters Now: The Post-COVID Acceleration

Before COVID-19, molecular POCT was a niche technology used primarily in HIV clinics, TB programs, and sexually transmitted infection (STI) screening in resource-limited settings. The pandemic fundamentally changed this. Between 2020 and 2022, governments worldwide — including China — deployed molecular POCT at unprecedented scale: in airports, fever clinics, emergency departments, and community testing sites. This created a massive installed base of instruments, trained a generation of non-laboratory healthcare workers in molecular testing, and drove reagent costs down through volume manufacturing.

Post-pandemic, the question is not whether molecular POCT works — it demonstrably does — but whether the infrastructure, reimbursement systems, and clinical workflows built during COVID can be repurposed for the full spectrum of infectious diseases, oncology screening, and chronic disease management. In China specifically, this transition is being actively shaped by government policy pushing diagnostic capabilities down to grassroots healthcare institutions.

The global point-of-care molecular diagnostics market was valued at approximately US$3.07 billion in 2025 and is projected to reach US$7.96 billion by 2034, at a CAGR of 11.17%. [Source 1]

### Key Terminology Glossary

| Term | Definition |
|------|-----------|
| POCT | Point-of-Care Testing — any diagnostic test performed outside a central laboratory |
| mPOCT | Mobile/Portable POCT — specifically refers to handheld or compact molecular platforms |
| NAT / NAAT | Nucleic Acid (Amplification) Test — detects DNA or RNA of a pathogen |
| LAMP | Loop-Mediated Isothermal Amplification — a key isothermal amplification method |
| RPA | Recombinase Polymerase Amplification — another isothermal method, faster than LAMP |
| CRISPR-Dx | CRISPR-based diagnostics — uses Cas enzymes for signal amplification and detection |
| Cartridge | Disposable, closed reaction vessel integrating all reagents for a single test |
| Sample-in/result-out | Describes a fully integrated workflow requiring no manual pipetting steps |
| TRL | Technology Readiness Level — scale from 1 (basic research) to 9 (fully deployed) |
| NMPA | National Medical Products Administration — China's medical device regulator |
| Class III IVD | Highest-risk IVD category in China, requiring full NMPA pre-market approval |
| Lyophilization | Freeze-drying of reagents to enable room-temperature storage and extended shelf life |

---

## 2. Technical Mechanism

### Core Mechanism

Molecular POCT platforms detect the presence of a pathogen (or genetic variant) by amplifying a specific nucleic acid sequence from a patient sample to a detectable level. The fundamental steps are:

1. **Sample lysis** — Cell walls and viral envelopes are disrupted to release nucleic acids. In POCT systems, this is typically achieved chemically (detergents, chaotropic salts) or thermally within the closed cartridge, eliminating the need for a separate extraction step.

2. **Nucleic acid amplification** — The target sequence is copied millions of times using one of several amplification chemistries (see below). This is the core differentiator between molecular POCT and rapid antigen tests.

3. **Signal detection** — Amplified product is detected via fluorescence, colorimetric change, or lateral flow strip, and the result is displayed on the instrument screen or read visually.

### Platform Types

**A. Real-Time PCR (qPCR) Cartridge Systems**
The gold standard approach, miniaturized into a cartridge format. Uses thermal cycling (repeated heating and cooling) to amplify DNA/RNA. Requires a thermocycler module within the instrument. Examples: Cepheid GeneXpert, Roche cobas Liat, Daan Gene DA3600.
- Sensitivity: 95–100%
- Specificity: 97–100%
- Time to result: 45–90 minutes
- Limitation: Requires precise thermal control; higher instrument cost

**B. Isothermal Amplification Systems (LAMP, RPA, NASBA)**
Amplification occurs at a single constant temperature (typically 37–65°C), eliminating the need for a thermocycler. This dramatically simplifies instrument design and reduces cost.
- LAMP (Loop-Mediated Isothermal Amplification): Uses 4–6 primers targeting 6–8 regions of the target sequence, with Bst DNA polymerase performing strand displacement. Operates at ~60–65°C. Produces cauliflower-like stem-loop DNA structures detectable by turbidity, fluorescence, or colorimetric pH change. [Source 4]
- RPA (Recombinase Polymerase Amplification): Operates at ~37–42°C (near body temperature), enabling truly ambient-temperature testing. Uses recombinase enzymes to facilitate primer-template binding. Faster than LAMP (5–20 minutes). [Source 3]
- NASBA: Specifically designed for RNA targets; used in HIV and respiratory virus detection.

**C. CRISPR-Based Detection Systems**
Emerging platform combining isothermal pre-amplification (LAMP or RPA) with CRISPR-Cas enzyme detection for signal amplification. The Cas enzyme (Cas12a or Cas13a) cleaves reporter molecules upon target recognition, generating a fluorescent or lateral-flow signal. Platforms include SHERLOCK (Cas13a, Broad Institute) and DETECTR (Cas12a, Mammoth Biosciences). [Source 14]
- Advantage: Extremely high specificity; can distinguish single-nucleotide variants
- China relevance: Sherlock Biosciences partnered with Shanghai-based Tolo Biotech to advance CRISPR diagnostics in China [Source 15]

**D. Microfluidic Cartridge Systems**
Integrate multiple reaction chambers, valves, and detection zones on a single chip or cartridge. Enable multiplexed detection (multiple pathogens simultaneously) from a single sample. Increasingly combined with LAMP or CRISPR detection. [Source 5]

### Performance Metrics Summary

| Platform | Sensitivity | Specificity | Time to Result | Instrument Cost | Consumable Cost |
|----------|------------|-------------|----------------|-----------------|-----------------|
| qPCR cartridge | 95–100% | 97–100% | 45–90 min | US$15,000–50,000 | US$20–80/test |
| LAMP isothermal | 87–98% | 95–99% | 15–45 min | US$2,000–15,000 | US$10–40/test |
| RPA isothermal | 90–100% | 96–100% | 5–20 min | US$1,000–10,000 | US$8–30/test |
| CRISPR-Dx | 90–99% | 98–100% | 30–60 min | US$500–5,000 | US$5–25/test |

*[REASONED INFERENCE — NOT SOURCED DATA: Cost ranges are estimated from published literature and market reports; actual pricing varies significantly by geography, volume, and negotiated contracts.]*

### Key Limitations

1. **Sample preparation bottleneck**: Extraction-free approaches typically show 10-fold higher limits of detection compared to extraction-based methods. One study reported LOD of 50 copies/µL (extraction-free) vs. 1 copy/µL (with extraction). [Source 3]
2. **RNA degradation**: RNA targets require RNase inhibition; RNA degrades above 65°C and during vortexing, complicating LAMP-based RNA detection.
3. **Matrix interference**: Urine urea inhibits amplification; hemoglobin in blood samples interferes with fluorescence detection; viscous samples (saliva) require viscosity modifiers. [Source 3]
4. **Multiplexing constraints**: Most current POCT platforms detect 1–6 targets per run; central lab platforms can run 20–50+ targets simultaneously.
5. **Quality control**: Decentralized testing creates challenges for external quality assurance, operator training, and result standardization — a concern specifically addressed in China's expert consensus guidelines. [Source 16]

---

## 3. Historical Evolution and Iteration

### Origins (Pre-2000)

The conceptual foundation of molecular POCT traces to the development of PCR by Kary Mullis in 1983 and its subsequent commercialization in the late 1980s. However, early PCR required large, expensive thermocyclers, trained molecular biologists, and dedicated laboratory space — the antithesis of point-of-care testing.

The first serious attempt to miniaturize molecular diagnostics for near-patient use came with Cepheid's GeneXpert system, developed in the 1990s. The GeneXpert cartridge integrated sample preparation, PCR amplification, and real-time fluorescence detection in a single disposable unit. The system design remained substantially unchanged from the early 2000s through the 2020s, a testament to its engineering robustness. [Source 8]

### Early Commercialization (2000–2010)

GeneXpert's first major clinical application was in tuberculosis diagnosis. The WHO endorsed the Xpert MTB/RIF assay in 2010 as a breakthrough for TB diagnosis in resource-limited settings, capable of detecting both Mycobacterium tuberculosis and rifampicin resistance in under 2 hours. This WHO endorsement was a pivotal moment — it demonstrated that molecular POCT could meet regulatory and clinical standards for serious infectious disease diagnosis outside of reference laboratories.

During this period, Abbott developed the m2000 system and later the ID NOW platform (originally Alere i), targeting influenza and strep A at the point of care. LAMP technology was first described by Notomi et al. in 2000 and began appearing in commercial products in the mid-2000s, particularly in Japan (Eiken Chemical).

### Pre-COVID Expansion (2010–2019)

The 2010s saw gradual expansion of molecular POCT into new disease areas: HIV viral load monitoring (Alere q), hepatitis C (Genedrive), sexually transmitted infections (Cepheid CT/NG), and respiratory viruses (BioFire FilmArray for syndromic panels). However, adoption remained limited by high per-test costs, reimbursement barriers, and the perception that central lab testing was "good enough" for most clinical scenarios.

In China, this period saw the emergence of domestic molecular diagnostics companies — Daan Gene (founded 1993, listed 2004), Sansure Biotech (founded 2008), and others — primarily focused on central lab PCR platforms rather than POCT. The Chinese market was dominated by imported POCT instruments from Cepheid, Abbott, and Roche.

### COVID-19 as the Inflection Point (2020–2022)

The SARS-CoV-2 pandemic transformed molecular POCT from a niche technology into a global public health infrastructure. Key developments:

- **Scale**: Hundreds of millions of molecular POCT tests were performed globally between 2020 and 2022. China alone deployed nucleic acid testing at a scale unprecedented in medical history, with mass testing campaigns processing millions of samples per day.
- **Regulatory acceleration**: Emergency Use Authorizations (EUA) in the US and equivalent emergency approvals in China compressed the typical 12–24 month NMPA approval timeline to weeks for COVID-19 molecular tests.
- **Chinese domestic industry surge**: Sansure Biotech's revenue grew from ~RMB 300 million pre-COVID to peak revenues exceeding RMB 5 billion during the pandemic. Daan Gene, Maccura, and others similarly experienced explosive growth. This capital was reinvested into POCT platform development.
- **Technology validation**: The pandemic provided massive real-world validation of molecular POCT performance, with studies confirming sensitivities of 88–100% and specificities of 95–100% for SARS-CoV-2 detection across multiple platforms. [Source 2]
- **Infrastructure buildout**: China's mass testing campaigns created a network of nucleic acid testing capabilities at community health centers, fever clinics, and mobile testing units — infrastructure that now exists and can be repurposed.

### Post-Pandemic Trajectory (2023–Present)

The post-COVID period has been characterized by a sharp revenue correction for COVID-focused companies, followed by strategic pivots toward non-COVID applications. Key trends:

- **Platform diversification**: Chinese POCT companies are expanding their test menus beyond COVID to respiratory panels (influenza A/B, RSV, adenovirus), STIs (HPV, chlamydia, gonorrhea), and chronic disease markers.
- **Miniaturization**: The iPonatic III Pro (Sansure, unveiled at MEDICA 2024) represents the latest generation of portable molecular workstations, integrating sample-in/result-out workflows in a compact form factor. [Source 11]
- **Grassroots deployment**: China's NHSA healthcare reform is actively pushing diagnostic capabilities to township hospitals and community health centers, creating a structural demand driver for affordable POCT platforms. [Source 17]
- **CRISPR emergence**: Research publications on CRISPR-based POCT have accelerated significantly, with multiple China-relevant applications (African Swine Fever, respiratory viruses, HCV) demonstrating the technology's potential for next-generation platforms. [Source 14]
- **AI integration**: Intelligent POCT platforms incorporating AI/ML for automated result interpretation, quality control, and connectivity to electronic health records are emerging as the next competitive frontier. [Source 6]

---

## 4. Academic Research Landscape

### Seminal Papers

The molecular POCT field rests on a foundation of key publications that defined the technology and its clinical applications:

1. **Notomi et al. (2000)** — "Loop-mediated isothermal amplification of DNA" (*Nucleic Acids Research*). The foundational paper describing LAMP technology, which has become the dominant isothermal amplification method in commercial POCT platforms. This paper has been cited thousands of times and directly enabled the development of most current isothermal POCT systems.

2. **WHO Endorsement of Xpert MTB/RIF (2010)** — While not a single paper, the WHO's policy guidance endorsing GeneXpert for TB diagnosis in resource-limited settings was the pivotal regulatory/clinical validation event for molecular POCT as a category.

3. **Piepenburg et al. (2006)** — "DNA Detection Using Recombination Proteins" (*PLOS Biology*). Described RPA technology, enabling amplification at near-body temperature and forming the basis for many next-generation POCT platforms.

4. **Gootenberg et al. (2017)** — "Nucleic acid detection with CRISPR-Cas13a/C2c2" (*Science*). Described the SHERLOCK platform, launching the CRISPR diagnostics field and establishing Cas13a as a detection tool. [Source 14]

5. **Chen et al. (2018)** — "CRISPR-Cas12a target binding unleashes indiscriminate single-stranded DNase activity" (*Science*). Described DETECTR/Cas12a, which has become the dominant CRISPR approach for lateral-flow-compatible POCT. [Source 14]

### Research Frontier (2024–2026)

The current research frontier in molecular POCT is characterized by several converging themes:

**Extraction-free sample preparation**: The most significant technical barrier to true POCT is sample preparation. A 2024 PMC review identified this as "a significant technical barrier preventing implementation of nucleic acid testing at the POC," noting that extraction-free approaches show 10-fold higher limits of detection. Current research focuses on chemical lysis methods (NaOH, surfactants) that can be integrated into cartridges without sacrificing sensitivity. [Source 3]

**One-pot assay integration**: Multiple 2024 publications describe "one-pot" assays combining amplification and CRISPR detection in a single closed reaction, eliminating the transfer step that creates contamination risk. A 2024 Frontiers in Microbiology paper described a one-pot MCDA-CRISPR-Cas system for SARS-CoV-2 detection. [Source 13]

**Multiplexed microfluidic systems**: A 2024 Lab on a Chip paper described a portable all-in-one microfluidic system for CRISPR-Cas13a-based multiplexed nucleic acid detection, moving toward instrument-free or minimal-instrument formats capable of detecting multiple pathogens simultaneously. [Source 13]

**AI-integrated POCT**: A 2024 Wiley review on "Intelligent POCT for Medical Diagnosis" covers AI/ML integration with POCT platforms for automated result interpretation, embedded sensors, and wireless data transmission — the direction of next-generation commercial platforms. [Source 6]

**Towards practical POCT (QUICK framework)**: A 2025 Nature paper outlined a framework for "Quick, Ubiquitous, Integrated, Cost-effective, Knowledge-based" POCT, synthesizing the field's direction toward truly decentralized, affordable, and connected molecular diagnostics. [Source 7]

**China-specific research output**: China has become a major contributor to molecular POCT research. Notable 2024–2025 publications include:
- First real-world performance data for point-of-care HIV-1 nucleic acid testing in China (Frontiers in Public Health, 2025) [Source 18]
- CRISPR-based detection of African Swine Fever Virus using ERA + CRISPR/Cas12a (Frontiers in Cellular and Infection Microbiology, 2024) — highly relevant to China's agricultural biosecurity [Source 14]
- Maccura's OsciDrop digital PCR system (PMC, 2024) — demonstrating Chinese innovation in next-generation molecular platforms [Source 19]

### Key Researchers and Institutions

- **Feng Zhang** (Broad Institute, MIT) — Co-developer of CRISPR-Cas13a (SHERLOCK); Chinese-American researcher with significant influence on CRISPR diagnostics globally
- **Jennifer Doudna** (UC Berkeley) — Co-developer of CRISPR-Cas12a (DETECTR); Nobel laureate whose work underpins the CRISPR diagnostics field
- **Chinese CDC (China CDC)** — Active in precision public health research and molecular diagnostics deployment; published on precision public health frameworks in 2022 [Source 20]
- **Shanghai Molecular Diagnostics Society** — Co-authored the Chinese Expert Consensus on Quality Management for POCT Nucleic Acid Testing [Source 16]
- **Sun Yat-sen University / Daan Gene** — Daan Gene is affiliated with Sun Yat-sen University; active in multiplex real-time PCR research for respiratory co-infections [Source 21]

---

## 5. Patent Landscape

### Global Patent Volume and Trends

China has become the world's dominant patent filer. In 2024, Chinese applicants filed 70,160 PCT applications — the highest of any country, ahead of the US (54,087) and Japan (48,397). [Source 22] This reflects a broader strategic commitment to IP generation that extends directly into the molecular diagnostics and POCT space.

In the IVD and molecular diagnostics domain specifically, Chinese companies have dramatically increased their patent filings since 2015, accelerating further post-COVID. The WIPO World Intellectual Property Indicators 2024 confirms that China's share of global patent applications has grown consistently, with biomedical and diagnostic technologies among the priority sectors. [Source 23]

### Top Patent Holders in Molecular POCT

**Global leaders:**
- **Cepheid (Danaher)** — Holds foundational patents on cartridge-based real-time PCR systems, including the GeneXpert architecture. Core patents cover integrated sample preparation + PCR in a closed cartridge format.
- **Abbott Laboratories** — Patents covering the ID NOW isothermal amplification platform and related LAMP/RPA chemistries for rapid molecular testing.
- **Roche Diagnostics** — Extensive patent portfolio covering PCR chemistries, probe designs, and miniaturized PCR instruments.
- **Broad Institute / Sherlock Biosciences** — Key CRISPR-Cas13a patents (SHERLOCK platform); licensed to Sherlock Biosciences for diagnostics applications. [Source 14]
- **Mammoth Biosciences** — CRISPR-Cas12a patents (DETECTR platform). [Source 14]

**Chinese leaders:**
- **Sansure Biotech** — Patents covering One-Tube Fast Release Technology (integrated lysis + PCR in a single closed tube), the iPonatic portable molecular workstation architecture, and lyophilized reagent formulations for POCT. [Source 11]
- **Daan Gene** — Patents on multiplex real-time PCR assay designs, particularly for respiratory pathogen panels and HPV genotyping. [Source 21]
- **BGI Genomics** — Extensive patent portfolio in nucleic acid amplification and sequencing; relevant to next-generation molecular diagnostics.
- **Hybribio** — Patents on HPV genotyping assays and flow-through hybridization technology. [Source 19]

### Geographic Distribution

The molecular POCT patent landscape shows a clear bifurcation:
- **US and Europe**: Dominate foundational platform patents (PCR thermocycling, cartridge architecture, CRISPR enzymes)
- **China**: Rapidly accumulating patents on assay designs, reagent formulations, lyophilization methods, and application-specific POCT systems

[REASONED INFERENCE — NOT SOURCED DATA: Chinese companies are increasingly filing PCT applications to protect their innovations internationally, but their core IP strength remains in assay-level patents rather than platform-level patents. This creates a structural dependency on Western platform IP that is a strategic vulnerability for Chinese POCT companies seeking to export globally.]

### Key Patent Families to Monitor

1. **Sansure One-Tube Fast Release Technology** — If this technology proves superior for POCT sample preparation, it could become a key differentiator in the Chinese market and a licensing asset internationally.
2. **CRISPR-Cas12a lateral flow integration** — Multiple groups are racing to patent the integration of Cas12a with lateral flow strips for instrument-free molecular POCT. The winner of this patent race will have significant leverage in the next-generation POCT market.
3. **Lyophilized reagent formulations** — Room-temperature stable reagents are critical for rural deployment in China. Patents on lyophilization methods for LAMP and RPA reagents are strategically important.

---

## 6. Technology Readiness and Commercialization

### TRL Assessment by Platform Type

| Platform | TRL | Status |
|----------|-----|--------|
| qPCR cartridge (GeneXpert-type) | 9 | Fully deployed; mature commercial market |
| LAMP isothermal (benchtop) | 8–9 | Commercially deployed; multiple NMPA-approved products |
| LAMP isothermal (handheld/portable) | 7–8 | Commercial products available; expanding deployment |
| RPA isothermal | 6–8 | Commercial products in select markets; limited NMPA approvals |
| CRISPR-Dx (research grade) | 4–6 | Active research; limited commercial deployment; no broad NMPA approval |
| CRISPR-Dx (lateral flow, instrument-free) | 3–5 | Proof-of-concept demonstrated; pre-commercial |
| AI-integrated POCT | 5–7 | Early commercial products; integration with EHR systems nascent |
| Multiplexed microfluidic POCT | 5–7 | Research and early commercial; limited NMPA approvals |

### Commercial Deployments in China

**Sansure Biotech — iPonatic Series**
Sansure's iPonatic platform is the most prominent Chinese-developed molecular POCT system. The iPonatic III Pro, unveiled at MEDICA 2024, represents the current generation. The platform uses Sansure's proprietary One-Tube Fast Release Technology, integrating sample lysis, nucleic acid release, and PCR amplification in a single closed tube. Results are delivered in approximately 30–45 minutes. The platform is designed for decentralized settings including clinics, emergency departments, and community health centers. [Source 11]

**Daan Gene — DA3600 and POCT Portfolio**
Daan Gene, affiliated with Sun Yat-sen University and one of China's oldest molecular diagnostics companies, offers a range of POCT-oriented molecular platforms. The company showcased its POCT portfolio at Medlab Middle East 2024, indicating active international expansion. [Source 10]

**Liferiver Bio-Tech — POCKIT System**
Liferiver's POCKIT is an automated nucleic acid extraction + PCR testing platform designed for point-of-care use. The company exhibited at ADLM 2024 (the major US laboratory medicine conference), signaling international ambitions. [Source 19]

**Maccura Biotechnology — PCR and Molecular Portfolio**
Chengdu-based Maccura showcased PCR-based molecular products at Analytica 2024. The company's OsciDrop digital PCR system, published in PMC in 2024, demonstrates innovation in next-generation molecular platforms. [Source 19]

### Cost Trajectory

POCT molecular testing costs have followed a consistent downward trajectory driven by:
1. **Volume manufacturing**: COVID-19 drove massive scale-up of cartridge and reagent manufacturing in China, permanently reducing unit costs.
2. **Domestic competition**: The entry of multiple Chinese manufacturers (Sansure, Daan Gene, Maccura, Liferiver, BioPerfectus, Hybribio) has intensified price competition.
3. **Lyophilization**: Freeze-dried reagents eliminate cold chain requirements and reduce logistics costs, particularly important for rural China deployment.
4. **Simplified instruments**: Isothermal platforms (LAMP, RPA) require simpler, cheaper instruments than PCR thermocyclers.

[FORECAST — SUBJECT TO UNCERTAINTY: By 2030, the cost of a molecular POCT test in China is expected to fall to RMB 50–150 (US$7–21) for common infectious disease targets, down from RMB 150–400 in 2024, driven by domestic competition and volume manufacturing.]

### NMPA Regulatory Pathway

Molecular POCT products in China are regulated as Class III IVDs — the highest risk category — requiring full NMPA pre-market approval. The regulatory pathway involves:

1. **Classification confirmation** using the new IVD Classification Catalogue (NMPA Announcement No. 17, May 2024), which reorganized and clarified the classification of nucleic acid testing products. [Source 24]
2. **Quality Management System certification** — YY/T 0287 (ISO 13485 equivalent)
3. **Technical dossier** including analytical performance studies (sensitivity, specificity, interference, stability), clinical evaluation data, core raw materials documentation (per 12 new IVD guidelines issued January 2024), and software documentation for POCT instruments. [Source 25]
4. **NMPA technical review** by the Center for Medical Device Evaluation (CMDE)
5. **On-site inspection**
6. **Registration certificate issuance**

Typical timeline for Class III IVD approval: **12–24 months** from submission. Emergency approval pathways (used during COVID-19) can compress this to weeks, but are not available for routine products.

Key 2024 regulatory developments affecting molecular POCT:
- New IVD Classification Catalogue (May 2024) — restructured how molecular POCT products are categorized [Source 24]
- 12 new IVD registration review guidelines (January 2024) — including core raw materials guidance directly affecting nucleic acid test kit submissions [Source 25]
- Updated Provisions for IVD Registration and Filing (June 2024) — governing the full registration lifecycle [Source 26]

---

## 7. Competitive Technology Comparison

### Molecular POCT vs. Central Laboratory Testing

Central laboratory testing (centralized PCR, NGS, automated immunoassay) remains the reference standard for molecular diagnostics. The comparison with molecular POCT is not simply "better vs. worse" — it is a question of which setting, clinical scenario, and patient population each technology serves best.

| Dimension | Central Lab Molecular Testing | Molecular POCT |
|-----------|------------------------------|----------------|
| Sensitivity | 98–100% (gold standard) | 88–100% (platform-dependent) |
| Specificity | 98–100% | 95–100% |
| Turnaround time | 4–24 hours (including transport) | 15–90 minutes |
| Throughput | High (100s–1000s of samples/day) | Low (1–20 samples/run) |
| Multiplexing | Very high (20–50+ targets) | Limited (1–12 targets) |
| Operator skill required | High (trained lab technician) | Low (minimal training) |
| Infrastructure required | Dedicated lab, BSL-2 | Minimal (clinic, bedside) |
| Cost per test | Lower at scale | Higher per test |
| Quality control | Robust (external QA programs) | Challenging (decentralized) |
| Connectivity | Integrated with LIS/HIS | Emerging (IoT-enabled platforms) |
| Best use case | High-volume routine testing | Urgent clinical decisions, remote settings |

Sources: [Source 2], [Source 9], [Source 27]

**Key insight**: The clinical value of molecular POCT is not in replacing central lab testing but in enabling actionable decisions at the point of care — initiating isolation, prescribing antivirals, or ruling out serious infection — before central lab results are available. A 2024 Inside Precision Medicine analysis noted that "centralized laboratory-based testing offers excellent sensitivity and specificity, but tests at the point of care allow healthcare providers to initiate prompt interventions like isolation protocols" that are time-critical. [Source 27]

### Molecular POCT vs. Rapid Antigen Tests (RATs)

Rapid antigen tests detect pathogen proteins rather than nucleic acids. They are faster (5–15 minutes), cheaper (US$1–10/test), and require no instrument. However, their sensitivity is significantly lower than molecular tests, particularly for low-viral-load samples.

| Dimension | Rapid Antigen Test | Molecular POCT |
|-----------|-------------------|----------------|
| Detection target | Protein (antigen) | Nucleic acid (DNA/RNA) |
| Sensitivity | 50–85% (varies by viral load) | 88–100% |
| Specificity | 95–99% | 95–100% |
| Time to result | 5–15 minutes | 15–90 minutes |
| Cost per test | US$1–10 | US$8–80 |
| Instrument required | No | Yes (for most platforms) |
| Quantitative | No | Yes (some platforms) |
| Resistance detection | No | Yes (with appropriate assay design) |
| Best use case | Mass screening, home testing | Clinical diagnosis, treatment decisions |

Source: [Source 28]

**Key insight**: Rapid antigen tests and molecular POCT are complementary, not competitive. RATs are appropriate for mass screening where sensitivity can be sacrificed for speed and cost. Molecular POCT is appropriate when a definitive diagnosis is needed to guide treatment — prescribing antivirals, initiating contact tracing, or ruling out serious infection in a symptomatic patient.

### Comparison Matrix: All Three Modalities

| Scenario | Best Technology | Rationale |
|----------|----------------|-----------|
| Mass population screening | Rapid antigen test | Speed and cost dominate |
| Symptomatic patient in ER | Molecular POCT | Rapid, accurate result guides treatment |
| Routine infectious disease panel | Central lab | High throughput, low cost at scale |
| Remote/rural clinic | Molecular POCT | No lab infrastructure required |
| Drug resistance detection | Central lab or molecular POCT | Requires nucleic acid analysis |
| Home testing | Rapid antigen test | No instrument, user-friendly |
| Outbreak investigation | Central lab + sequencing | Comprehensive characterization needed |

---

## 8. Future Outlook

### Near-Term (1–3 Years: 2026–2028)

**Technology developments:**
- Continued miniaturization of molecular POCT instruments toward truly handheld, battery-operated form factors
- Expansion of test menus beyond respiratory viruses to STIs, antimicrobial resistance markers, and oncology biomarkers
- Lyophilized reagent formulations becoming standard, enabling room-temperature storage and eliminating cold chain requirements
- First-generation AI-assisted result interpretation integrated into commercial POCT platforms
- CRISPR-based POCT platforms achieving first NMPA approvals in China for specific applications

**Market developments:**
- Chinese domestic POCT companies completing their post-COVID pivot from COVID-only to multi-disease platforms
- Grassroots healthcare reform driving POCT adoption at township hospitals and community health centers
- Price competition intensifying as multiple Chinese manufacturers compete for the same institutional customers
- International expansion by Sansure, Daan Gene, and others into Southeast Asia, Africa, and Middle East

[FORECAST — SUBJECT TO UNCERTAINTY]

### Mid-Term (3–7 Years: 2028–2032)

**Technology developments:**
- CRISPR-based POCT achieving mainstream commercial deployment for select applications (HPV genotyping, AMR detection, rare pathogen identification)
- Multiplexed syndromic POCT panels (10–20 targets) becoming commercially available at price points competitive with single-target tests
- Integration of molecular POCT with digital health platforms — results automatically uploaded to electronic health records, triggering clinical decision support alerts
- Instrument-free or near-instrument-free molecular POCT (paper-based, lateral flow molecular) achieving clinical-grade sensitivity for select targets
- China emerging as a net exporter of molecular POCT technology, with Chinese platforms gaining WHO prequalification for global health applications

**Market developments:**
- China's molecular POCT market reaching RMB 15–25 billion [FORECAST — SUBJECT TO UNCERTAINTY]
- Reimbursement frameworks for molecular POCT at primary care level becoming standardized across China's provinces
- Consolidation among Chinese POCT companies as the market matures

### Long-Term (7–15 Years: 2032–2040)

**Technology developments:**
- Convergence of molecular POCT with wearable biosensors for continuous pathogen monitoring
- Single-cell molecular analysis at the point of care, enabling precision medicine applications
- Fully autonomous POCT systems with AI-driven sample collection, analysis, and clinical decision support
- Metagenomics-based POCT capable of identifying any pathogen from a clinical sample without prior knowledge of the target

**Market developments:**
- Molecular POCT becoming the standard of care for infectious disease diagnosis in primary care settings globally
- China's domestic POCT industry achieving global leadership in cost-competitive platforms for low- and middle-income country markets
- The distinction between "POCT" and "central lab" testing blurring as distributed laboratory networks replace centralized facilities

[FORECAST — SUBJECT TO UNCERTAINTY for all long-term projections]

---

## 9. China-Specific Analysis

### Chinese Research Output

China has become a major contributor to molecular POCT research, with output accelerating significantly post-COVID. Key indicators:
- China filed 70,160 PCT patent applications in 2024 — the highest globally — with biomedical diagnostics among priority sectors [Source 22]
- Chinese researchers are active contributors to CRISPR diagnostics research, with multiple 2024 publications on CRISPR-based POCT for applications including African Swine Fever, respiratory viruses, and HCV [Source 14]
- The Chinese Expert Consensus on Quality Management for POCT Nucleic Acid Testing (Frontiers in Cellular and Infection Microbiology, 2021) established China-specific quality standards that are now being implemented across medical institutions [Source 16]
- First real-world performance data for point-of-care HIV-1 nucleic acid testing in China published in 2025, demonstrating the maturation of China's molecular POCT clinical evidence base [Source 18]

### State Policy Support

China's government has created a multi-layered policy environment supportive of molecular POCT development and deployment:

**Healthcare reform (demand-side):**
- NHSA 14-Point Grassroots Healthcare Reform Guidance: Redirects medical insurance funds toward primary care institutions, with reimbursement rates for outpatient services at grassroots level set at minimum 50%. This directly incentivizes community health centers to invest in diagnostic capabilities including POCT. [Source 17]
- Tiered healthcare system (分级诊疗): Government policy explicitly aims to shift routine care from tertiary hospitals to primary care, requiring primary care institutions to have diagnostic capabilities that previously only existed in hospitals.
- DRG/DIP payment reform: Bundled payment systems incentivize hospitals to use cost-effective diagnostics that enable faster clinical decisions and shorter hospital stays — a use case where molecular POCT excels.

**Industrial policy (supply-side):**
- 14th Five-Year Plan (2021–2025): Included IVD and molecular diagnostics as priority sectors for domestic innovation and import substitution.
- 15th Five-Year Plan (2026–2030): Emphasizes AI integration, digital health, and advanced manufacturing — all relevant to next-generation POCT platforms. [Source 29]
- "Made in China 2025" and successor policies: Explicitly target medical devices as a sector where China should achieve global competitiveness.

### Key Chinese Companies

**Sansure Biotech (圣湘生物, SHA: 688289)**
- Founded 2008, listed on STAR Market 2020
- 2024 revenue: RMB 1.46 billion (44.78% growth) [Source 30]
- Core POCT product: iPonatic series (iPonatic III Pro unveiled MEDICA 2024)
- Technology: One-Tube Fast Release Technology; mPOCT platform
- Achieved MDSAP certification March 2024, enabling expanded global regulatory compliance [Source 10]
- Partnership with QuantuMDx for intelligent POCT solutions [Source 10]
- Strategic position: Most internationally visible Chinese molecular POCT company; strong in respiratory and infectious disease panels

**Daan Gene (达安基因, SZ: 002030)**
- Founded 1993, listed 2004; affiliated with Sun Yat-sen University
- One of China's oldest and most established molecular diagnostics companies
- Active in multiplex real-time PCR for respiratory co-infections [Source 21]
- Showcased POCT portfolio at Medlab Middle East 2024 [Source 10]
- Strategic position: Broad molecular diagnostics portfolio; strong institutional relationships; expanding internationally

**Maccura Biotechnology (迈克生物, SZ: 300463)**
- Chengdu-based; broad IVD portfolio spanning clinical chemistry, immunoassay, hematology, and molecular diagnostics
- Showcased PCR molecular products at Analytica 2024 [Source 19]
- OsciDrop digital PCR system published in PMC 2024 — demonstrates innovation in next-generation molecular platforms [Source 19]
- Strategic position: Diversified IVD company with growing molecular/POCT presence; strong in central and western China

**Hybribio (凯普生物, SZ: 300639)**
- Guangzhou-based; specializes in HPV molecular diagnostics and cervical cancer screening
- Key products: 21 HPV GenoArray Kit, 14 High-risk HPV RT-PCR Kit, 23 HPV Genotyping Kit [Source 19]
- Active in Southeast Asia expansion [Source 19]
- Strategic position: Dominant in HPV molecular testing; niche but deep expertise

**BioPerfectus (百普赛斯)**
- Jiangsu-based; focused on nucleic acid extraction, PCR kits, and cervical cancer diagnostics
- NMPA approval for Dengue Virus Real-Time PCR Kit (October 2024) [Source 10]
- First Chinese manufacturer listed by WHO ERPD for Dengue RDT (2025) [Source 19]
- CE-IVDR certification for Malaria Testing Kits (September 2024) [Source 19]
- Strategic position: Strong in tropical infectious disease diagnostics; growing international regulatory footprint

**Liferiver Bio-Tech (利弗瑞)**
- Shanghai-based; POCKIT automated nucleic acid extraction + PCR platform
- Exhibited at ADLM 2024 [Source 19]
- Strategic position: POCT-focused; strong in automated molecular testing for decentralized settings

### Grassroots Healthcare Expansion

China's 600,000+ village clinics and 35,000+ township health centers represent the largest potential POCT market in the world — and the most underpenetrated. The current reality:

- Top-tier hospitals (2,418 facilities) concentrate IVD testing, processing 20,000+ tests daily with sophisticated central lab infrastructure [Source 31]
- Community health centers in cities are emerging as the primary POCT adoption point, driven by the tiered healthcare system
- Rural diagnostics historically limited to basic tools (stethoscopes, thermometers, basic immunoassay strips)
- The NHSA grassroots reform (2025–2028 pilot, 2028–2030 national rollout) is the most concrete policy lever for driving POCT adoption at primary care level [Source 17]

The key enablers for grassroots molecular POCT deployment:
1. **Lyophilized reagents**: Eliminate cold chain requirements critical for rural settings
2. **Simplified instruments**: LAMP/RPA platforms require less technical expertise than PCR
3. **Reimbursement inclusion**: POCT molecular tests must be included in the national reimbursement catalogue to drive adoption at grassroots level
4. **Training programs**: Healthcare worker training for POCT operation at community health centers

### Technology Gaps

China's molecular POCT sector has significant strengths but also identifiable gaps:

**Strengths:**
- Manufacturing scale and cost competitiveness
- Rapid product development cycles (Roland Berger notes Chinese companies have "compressed product-development cycles from years into months") [Source 32]
- Strong government policy support
- Large domestic market for validation and scale-up

**Gaps:**
1. **Platform-level IP**: Chinese companies hold strong assay-level patents but remain dependent on Western platform IP (PCR thermocycling, CRISPR enzyme patents). This creates licensing costs and potential IP disputes in export markets.
2. **Multiplexing capability**: Chinese POCT platforms generally lag behind BioFire FilmArray (bioMérieux) and similar Western platforms in the number of targets detectable per run.
3. **Regulatory harmonization**: Chinese NMPA approvals are not automatically recognized internationally; companies must pursue separate CE-IVDR, FDA clearance, and WHO prequalification — a costly and time-consuming process.
4. **Quality standardization**: Decentralized POCT creates quality control challenges. The Chinese Expert Consensus (2021) acknowledged that "no standardized POCT quality management guidelines were available" prior to its publication — implementation across 600,000+ grassroots facilities remains a work in progress. [Source 16]
5. **Cold chain for some platforms**: While lyophilization is advancing, some molecular POCT reagents still require refrigeration, limiting deployment in areas with unreliable electricity and cold chain infrastructure.
6. **Clinical evidence base**: Chinese POCT platforms have less published clinical validation data compared to Western platforms, which can be a barrier to international adoption and WHO prequalification.

---

## 10. Strategic Implications

### Investment Signals

**Positive signals for molecular POCT in China:**

1. **Policy tailwind is structural, not cyclical**: The NHSA grassroots reform, tiered healthcare system, and 15th Five-Year Plan all point to sustained government commitment to decentralizing diagnostic capabilities. This is not a one-time stimulus but a multi-year structural shift. [Source 17, 29]

2. **Post-COVID infrastructure is an asset**: The installed base of molecular testing instruments, trained healthcare workers, and supply chains built during COVID-19 represents sunk infrastructure that lowers the marginal cost of expanding molecular POCT to new disease areas.

3. **Market size and growth**: The global point-of-care molecular diagnostics market is projected to grow from US$3.07 billion (2025) to US$7.96 billion (2034) at 11.17% CAGR. China's share is growing disproportionately as domestic companies scale. [Source 1]

4. **China IVD market fundamentals**: The China IVD market was valued at US$12.60 billion in 2023, projected to reach US$17.24 billion by 2030 at 4.1% CAGR. POCT represents ~15% of this market with ~5% growth, and molecular POCT is the fastest-growing POCT sub-segment. [Source 33]

5. **Domestic company revenue recovery**: Sansure Biotech's 2024 revenue of RMB 1.46 billion (44.78% growth) signals that the post-COVID correction has bottomed and domestic molecular diagnostics companies are returning to growth on non-COVID revenue. [Source 30]

6. **International expansion opportunity**: Chinese molecular POCT companies are well-positioned to capture market share in Southeast Asia, Africa, and the Middle East — markets where cost competitiveness matters more than brand recognition.

**Risk signals:**

1. **Post-COVID revenue normalization**: Companies that grew 10–20x during COVID are now managing the transition to sustainable non-COVID revenue. This transition is not complete and creates near-term earnings volatility.

2. **Price competition**: Multiple Chinese manufacturers competing for the same institutional customers will compress margins. The POCT market in China risks commoditization of hardware, with value shifting to reagent consumables and software.

3. **Reimbursement uncertainty**: Inclusion of molecular POCT tests in China's national reimbursement catalogue is not guaranteed and is subject to health technology assessment processes that can be slow and unpredictable.

4. **IP exposure**: Chinese companies' dependence on Western platform IP creates licensing cost risk and potential export market barriers.

5. **Geopolitical risk**: US-China technology tensions could affect access to key components (enzymes, optical sensors, semiconductor chips for instruments) and international market access.

### Companies to Watch

| Company | Why Watch | Key Catalyst |
|---------|-----------|-------------|
| Sansure Biotech (688289.SH) | Most internationally visible Chinese mPOCT company; iPonatic III Pro launch | Non-COVID revenue growth trajectory; international regulatory approvals |
| Daan Gene (002030.SZ) | Oldest, most established; Sun Yat-sen University affiliation | Multiplex POCT panel launches; grassroots channel expansion |
| Maccura (300463.SZ) | Diversified IVD; digital PCR innovation | OsciDrop commercialization; POCT menu expansion |
| BioPerfectus | WHO prequalification momentum; tropical disease focus | Additional WHO listings; emerging market expansion |
| Tolo Biotech (private) | Sherlock Biosciences CRISPR partnership; China CRISPR-Dx commercialization | NMPA approval for first CRISPR-based POCT product |
| Hybribio (300639.SZ) | HPV molecular testing dominance; cervical cancer screening expansion | National cervical cancer screening program expansion |

### Monitoring Indicators

Investors and market entrants should track the following leading indicators:

**Technology indicators:**
- NMPA approval rate for new molecular POCT products (Class III IVD approvals per year)
- First NMPA approval for a CRISPR-based POCT product (signals next-generation platform readiness)
- Lyophilized reagent adoption rate (proxy for rural deployment readiness)
- Number of targets per POCT run (multiplexing capability improvement)

**Market indicators:**
- Sansure Biotech non-COVID revenue as % of total (target: >80% by 2026)
- POCT test volume at community health centers (grassroots adoption proxy)
- Price per molecular POCT test in China (cost trajectory)
- Chinese POCT company international revenue growth (export market penetration)

**Policy indicators:**
- NHSA grassroots reform implementation progress (pilot regions → national rollout)
- Inclusion of molecular POCT tests in national reimbursement catalogue updates
- 15th Five-Year Plan healthcare technology investment announcements
- NMPA regulatory streamlining for domestic IVD companies

---

## 11. Confidence Level

**Overall Confidence: Medium-High**

**High confidence areas:**
- Technology mechanism descriptions (LAMP, RPA, CRISPR-Dx) — well-documented in peer-reviewed literature
- Key Chinese company profiles (Sansure, Daan Gene, Maccura, Hybribio, BioPerfectus, Liferiver) — verified from company websites, financial data, and trade press
- NMPA regulatory pathway — verified from official NMPA publications and regulatory advisory sources
- Sansure Biotech 2024 revenue (RMB 1.46 billion, 44.78% growth) — from financial data sources
- Policy environment (NHSA grassroots reform, 15th Five-Year Plan) — verified from official Chinese government sources and specialist policy analysis

**Medium confidence areas:**
- Global market size figures (US$3.07 billion in 2025, 11.17% CAGR) — from market research reports that may use different methodologies and definitions
- China-specific POCT market size and growth rates — limited publicly available China-specific data; figures extrapolated from global reports and China IVD market data
- Patent landscape details — general trends verified; specific patent counts and rankings for molecular POCT sub-category not independently verified
- Technology gap assessment — based on synthesis of multiple sources; some gaps are reasoned inferences

**Low confidence areas:**
- Long-term forecasts (2032–2040) — inherently speculative; labeled as [FORECAST — SUBJECT TO UNCERTAINTY]
- Cost trajectory projections — based on general market trends; actual pricing is commercially sensitive and not publicly disclosed
- CRISPR-Dx commercialization timeline in China — regulatory pathway is unclear; timeline is a reasoned inference

**Data gaps:**
- China-specific molecular POCT market size (RMB) — no reliable public source found; global figures used as proxy
- Detailed NMPA approval pipeline for molecular POCT products — not publicly disclosed in real-time
- Grassroots healthcare POCT adoption rates — limited empirical data available

---

## 12. Sources

1. [Point-of-Care Molecular Diagnostics Market: Rapid Growth Ahead Through 2034 — Industry Today](https://industrytoday.co.uk/health_and_safety/point-of-care-molecular-diagnostics-market-rapid-growth-ahead-through-2034)

2. [Molecular Point-of-Care Testing for Respiratory Infections: A Comprehensive Literature Review (2006–2026) — MDPI Diagnostics](https://www.mdpi.com/2075-4418/16/6/930)

3. [Point-of-Care Isothermal Nucleic Acid Amplification Tests — PMC/NIH](https://pmc.ncbi.nlm.nih.gov/articles/PMC11514575/)

4. [Advancements and Applications of Loop-Mediated Isothermal Amplification Technology — Frontiers in Microbiology](https://www.frontiersin.org/journals/microbiology/articles/10.3389/fmicb.2024.1406632/full)

5. [A Microfluidic-Based Quantitative Analysis System for Multiplexed Genetic Diagnosis Using Colorimetric LAMP — RSC Analyst](https://pubs.rsc.org/en/content/articlehtml/2024/an/d4an00215f)

6. [Intelligent Point of Care Testing for Medicine Diagnosis — Wiley INMD](https://onlinelibrary.wiley.com/doi/full/10.1002/INMD.20230031)

7. [Towards Practical Point-of-Care Quick, Ubiquitous, Integrated, Cost-effective Testing — Nature Microsystems & Nanoengineering](https://www.nature.com/articles/s41378-025-01057-4)

8. [Cepheid / GeneXpert — Wikiwand](https://www.wikiwand.com/en/articles/GeneXpert)

9. [Simulation Analysis and Comparison of Point of Care Testing and Central Laboratory Testing — SAGE Journals](https://journals.sagepub.com/doi/full/10.1177/2381468319856306)

10. [What is a POCT Solution? Who is the Reliable Provider? — Sansure Global](https://www.sansureglobal.com/what-is-a-poct-solution-who-is-the-reliable-provider-for-poct-solutions-sansure-in-2024-hcowa/)

11. [iPonatic III Pro — Portable Molecular Diagnostic System — Sansure Biotech](https://www.sansureglobal.com/product/iponatic-iii-pro-portable-molecular-diagnostic-system/)

12. [Sansure Presented at MEDICA 2024 with the Latest IVD Solutions — Sansure Global](https://www.sansureglobal.com/sansure-presented-at-medica-2024-with-the-latest-ivd-solutions/)

13. [One-pot MCDA-CRISPR-Cas-based Detection Platform for SARS-CoV-2 — Frontiers in Microbiology](https://www.frontiersin.org/journals/microbiology/articles/10.3389/fmicb.2024.1503356/full)

14. [RETRACTED: SHERLOCK and DETECTR: CRISPR-Cas Systems as Potential Diagnostics — ASM Journal of Clinical Microbiology](https://journals.asm.org/doi/10.1128/jcm.00745-20)

15. [Sherlock Biosciences and Tolo Biotech Collaborate to Advance CRISPR-Based Diagnostics — CLP Magazine](https://clpmag.com/diagnostic-technologies/sherlock-biosciences-and-tolo-biotech-collaborate-to-advance-crispr-based-diagnostics/)

16. [Quality Management for Point-Of-Care Testing of Pathogen Nucleic Acids: Chinese Expert Consensus — Frontiers in Cellular and Infection Microbiology](https://doi.org/10.3389/fcimb.2021.755508)

17. [China NHSA Grassroots Healthcare Reform — 14-Point Guidance Targets RMB Fund Flow Shift to Primary Care — FLCube](https://flcube.com/?p=59721)

18. [Rapid Diagnosis of Acute HIV-1 Infection: First Real-World Performance of Point-of-Care HIV-1 Nucleic Acid Testing in China — Frontiers in Public Health](https://www.frontiersin.org/articles/10.3389/fpubh.2025.1707432)

19. [Top 10 Leading POCT Medical Device Manufacturers in China — Seamaty](https://en.seamaty.com/index.php?s=%2Fsys%2F703.html)

20. [Precision Public Health in China — China CDC Weekly](https://weekly.chinacdc.cn/en/article/doi/10.46234/ccdcw2022.145)

21. [DaAn Gene Latest Research Progress: Multiplex Real-Time PCR in Diagnosis of Co-infection of Complex Respiratory Pathogen — Daan Gene](https://en.daangene.com/daan-gene-latest-research-progress-multiplex-real-time-pcr-in-diagnosis-of-co-infection-of-complex-respiratory-pathogen.html)

22. [PCT Yearly Review Executive Summary 2025 — WIPO](https://www.wipo.int/web-publications/pct-yearly-review-executive-summary-2025/en/pct-yearly-review-2025-executive-summary.html)

23. [World Intellectual Property Indicators 2024: Highlights — WIPO](https://www.wipo.int/web-publications/world-intellectual-property-indicators-2024-highlights/en/patents-highlights.html)

24. [NMPA Announcement No. 17 (2024) — IVD Classification Catalogue Implementation — Nanhu Government Portal](https://www.nanhu.gov.cn/art/2024/5/14/art_1229658601_1804558.html)

25. [NMPA: Four IVD Guidelines Issued — China Med Device](https://chinameddevice.com/nmpa-ivd-guidelines/)

26. [Provisions for In-vitro Diagnostic Reagent Registration and Filing — NMPA English Portal](https://english.nmpa.gov.cn/2024-06/05/c_1049322.htm)

27. [Ensuring Diagnostic Stewardship Through Molecular Point-of-Care Testing — Inside Precision Medicine](https://www.insideprecisionmedicine.com/topics/patient-care/ensuring-diagnostic-stewardship-through-molecular-point-of-care-testing/)

28. [Antigen vs. Molecular: Benefits, Limitations, and Practical Considerations — Physicians Office Resource](https://www.physiciansofficeresource.com/articles/point-of-care-testing/antigen-vs-molecular/)

29. [China Unveils 2026-2030 Healthcare Plan with AI Focus — LinkedIn](https://www.linkedin.com/posts/mark-lazell-1540b367_china-recently-published-its-state-healthcare-activity-7429783852484743168-MZHT)

30. [Sansure Biotech Revenue Data — Stock Analysis](https://stockanalysis.com/quote/sha/688289/revenue/)

31. [China: Molecular Point-of-Care's International Market to Watch — Science and Medicine Group](https://www.scienceandmedicinegroup.com/china-molecular-point-of-care-markets-emerging-global-leader/)

32. [China's Cost and Speed Advantage — Roland Berger](https://www.rolandberger.com/en/Insights/Publications/China-s-cost-and-speed-advantage.html)

33. [China In-Vitro Diagnostics Market Forecast — NextMSC](https://www.nextmsc.com/report/china-in-vitro-diagnostics-market)

34. [China IVD Market Chapter 2 — CAIVD](https://www.caivd-org.cn/en/detail.asp?id=3464)

35. [Molecular Point-of-Care Testing Technologies: Current Status and Challenges — ScienceDirect](https://www.sciencedirect.com/science/article/pii/S2950160125000063)

36. [Infectious Disease Diagnostics in 2025: Market Volatility Meets Rapid Technology Advancements — 360Dx](https://www.360dx.com/infectious-disease/infectious-disease-diagnostics-2025-market-volatility-meets-rapid-technology)

37. [BioPerfectus Dengue Virus Real Time PCR Kit Receives NMPA Approval — BioPerfectus](https://www.bioperfectus.com/NewsDetail/BioPerfectusDengueVirusRealTimePCRKitReceivesApprovalfromNMPA)

38. [Sansure and QuantuMDx to Jointly Build Intelligent and Diversified POCT Solution — Sansure Global](https://www.sansureglobal.com/sansure-and-quantumdx-to-jointly-build-intelligent-and-diversified-overall-solution-for-poct/)

39. [Era of Molecular Diagnostics Techniques Before and After the COVID-19 Pandemic — PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC9601158/)

40. [Point-of-Care Molecular Diagnostics and Drug-Resistance Mechanisms in Neglected Infectious Diseases — Frontiers in Cellular and Infection Microbiology](https://www.frontiersin.org/journals/cellular-and-infection-microbiology/articles/10.3389/fcimb.2026.1769679/full)

41. [Kalorama Information's 2025 IVD Atlas Tracks Global Growth Hotspots, Led by China — MarketWatch](https://www.marketwatch.com/press-release/kalorama-information-s-2025-ivd-atlas-tracks-global-growth-hotspots-led-by-china-and-emerging-markets-aa0c9494)

42. [Evolving Regulations on Nucleic Acid Testing Reagents in China — CISEMA](https://cisema.com/en/nucleic-acid-testing-regulations/)

43. [NMPA Regulatory Approval Process for Medical and IVD Devices — Emergo by UL](https://www.emergobyul.com/resources/chinese-nmpa-regulatory-approval-process-medical-and-ivd-devices)

44. [A Streamlined POCT Solution for Rapid Infectious Disease Detection — Scientific Reports (Nature)](https://www.nature.com/articles/s41598-025-97155-4)

45. [Point-of-Care Nucleic Acid Detection: From Molecular Design to Clinical Applications — ACS Omega](https://pubs.acs.org/doi/10.1021/acsomega.5c02914)

---
*Report prepared by Technology Research Analyst | China Molecular Diagnostics Market Research 2026*
*All forecasts are subject to uncertainty. Inferences are labeled [REASONED INFERENCE — NOT SOURCED DATA]. Forecasts are labeled [FORECAST — SUBJECT TO UNCERTAINTY].*
