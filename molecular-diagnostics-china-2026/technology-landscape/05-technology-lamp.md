# Technology Deep-Dive: Loop-Mediated Isothermal Amplification (LAMP)
**China Molecular Diagnostics Market | Technology Landscape Report**
*Prepared: March 2026 | Horizon: 2024–2026 current state, 2030 forecast*
*Perspective: Investor / Market Entrant*

---

## 1. Technology Overview

### Plain-Language Definition

Loop-Mediated Isothermal Amplification (LAMP) is a nucleic acid amplification method that copies DNA or RNA targets at a single, constant temperature — typically 60–65°C — without the temperature cycling required by conventional PCR. The reaction is driven by a strand-displacing DNA polymerase (Bst polymerase) and a set of 4–6 specially designed primers that recognize 6–8 distinct regions on the target sequence. The result is a rapid, exponential amplification producing up to 10⁹ copies of the target within 15–60 minutes.

The defining practical advantage: **no thermal cycler is needed**. A simple heat block, water bath, or even a thermos flask can maintain the required temperature. This makes LAMP deployable in settings where PCR infrastructure is absent — rural clinics, field laboratories, border checkpoints, and low-resource environments.

### Why It Matters

LAMP sits at the intersection of three converging trends in diagnostics:
1. **Decentralization** — healthcare systems globally are pushing diagnostic capability out of central labs and into primary care, community settings, and homes
2. **Speed** — clinical decisions increasingly require same-visit results, not next-day lab reports
3. **Accessibility** — emerging markets and rural populations need molecular-grade accuracy without molecular-grade infrastructure

For China specifically, LAMP is strategically relevant to the government's push to strengthen grassroots (基层) healthcare capacity, where PCR infrastructure remains uneven across the country's 600,000+ village clinics and township health centers.

### Key Terminology Glossary

| Term | Definition |
|------|-----------|
| **LAMP** | Loop-Mediated Isothermal Amplification — the core DNA amplification method |
| **RT-LAMP** | Reverse Transcription LAMP — variant that first converts RNA to cDNA, enabling detection of RNA viruses (e.g., SARS-CoV-2, influenza) |
| **Bst polymerase** | Bacillus stearothermophilus DNA polymerase — the strand-displacing enzyme that drives LAMP reactions |
| **Isothermal** | Occurring at a single constant temperature, as opposed to the temperature cycling of PCR |
| **FIP / BIP primers** | Forward Inner Primer / Backward Inner Primer — the two critical primers that initiate loop formation |
| **Loop primers** | Additional primers (F-Loop, B-Loop) that accelerate the reaction by 30–50% |
| **Stem primers** | Optional primers providing design flexibility without sacrificing speed |
| **Colorimetric detection** | Visual result reading via pH-indicator color change (e.g., purple → yellow) — no instrument needed |
| **Turbidimetry** | Detection method monitoring magnesium pyrophosphate precipitation as a proxy for amplification |
| **TRL** | Technology Readiness Level — a 1–9 scale measuring technology maturity from concept to full deployment |
| **POCT** | Point-of-Care Testing — diagnostic testing performed at or near the patient |
| **CRISPR-LAMP** | Hybrid assay combining LAMP amplification with CRISPR-Cas detection for enhanced specificity |

---

## 2. Technical Mechanism

### Core Mechanism

LAMP exploits the strand displacement activity of Bst DNA polymerase to amplify a target sequence under isothermal conditions. The reaction proceeds in three phases:

**Phase 1 — Initiation:** The Forward Inner Primer (FIP) hybridizes to the target and initiates synthesis. The Backward Inner Primer (BIP) does the same on the complementary strand. Strand displacement by Bst polymerase releases single-stranded products.

**Phase 2 — Cycling:** The released single-stranded products form stem-loop structures at their ends (the "loops" in LAMP). These self-priming structures allow continuous, self-sustaining amplification without temperature changes. The reaction becomes autocatalytic.

**Phase 3 — Exponential amplification:** Multiple primer sets (F3/B3 outer primers, FIP/BIP inner primers, and optional loop primers) work simultaneously, generating a complex mixture of stem-loop DNA structures of varying lengths. This produces the characteristic "ladder" pattern on gel electrophoresis.

The net result: up to 10⁹ copies of the target sequence within 15–60 minutes at 60–65°C. [Source: Notomi et al., Nucleic Acids Research, 2000](https://academic.oup.com/nar/article/28/12/e63/2359194)

### RT-LAMP Variant

For RNA targets (viruses, gene expression), a reverse transcriptase enzyme is added to the reaction mix. The RT-LAMP reaction first converts RNA to complementary DNA (cDNA), which then serves as the LAMP template. This single-tube, one-step format is critical for respiratory virus diagnostics (COVID-19, influenza, RSV) and has been the primary driver of LAMP's commercial expansion since 2020.

### Detection Methods

**1. Colorimetric (naked-eye):** pH-sensitive dyes change color as the reaction produces acidic byproducts. Phenol red shifts from red/orange to yellow; hydroxy naphthol blue (HNB) shifts from violet to sky blue. No instrument required — results readable by eye. Sensitivity is slightly lower than fluorescent methods and can be affected by sample pH.

**2. Fluorometric:** Intercalating dyes (SYTO-9, SYBR Green I, EvaGreen) bind double-stranded DNA and fluoresce. Enables real-time monitoring analogous to qPCR. Requires a fluorescence reader but provides quantitative data and earlier detection.

**3. Turbidimetry:** Magnesium pyrophosphate precipitates as a byproduct of amplification, causing visible turbidity. Can be monitored in real-time with a turbidimeter or observed visually. Simple but less sensitive than fluorometric methods.

**4. Lateral flow assay (LFA) integration:** LAMP products can be detected on lateral flow strips using labeled primers, enabling dipstick-format results. Combines LAMP's molecular sensitivity with the simplicity of a pregnancy-test-style readout.

### Performance Metrics

| Metric | LAMP Performance | Notes |
|--------|-----------------|-------|
| Sensitivity | 100× higher than standard PCR | Per PMC8393631 |
| Detection limit | 0.1–100 copies/µL depending on assay | Varies by target and method |
| Time to result | 15–60 minutes | Newer assays achieve 15–30 min |
| Specificity | Near-100% for well-designed assays | Multiple primer binding sites increase specificity |
| RT-LAMP for SARS-CoV-2 | 96% sensitivity, 99.99% specificity (RNA-extracted samples) | Pirbright Institute clinical validation |
| Temperature requirement | 60–65°C constant | Simple heat block sufficient |
| Equipment cost | $200–$2,000 for basic setup | vs. $5,000–$50,000 for PCR thermocycler |

### Limitations

1. **Primer design complexity:** Designing 4–6 primers targeting 6–8 regions is significantly more complex than PCR primer design. Requires specialized software and expertise.
2. **Aerosol contamination risk:** The massive amplification product volume creates high contamination risk if tubes are opened post-reaction. Closed-tube detection methods (colorimetric, fluorescent) mitigate this.
3. **Multiplexing challenges:** Running multiple targets simultaneously in a single tube is technically difficult due to primer interactions. Most commercial LAMP assays remain single-target.
4. **Short target limitation:** LAMP is unsuitable for very short gene sequences (<200 bp) due to primer spacing requirements.
5. **Inhibitor sensitivity:** LAMP can be inhibited by components in complex samples (blood, soil, food matrices), though Bst 3.0 polymerase variants show improved tolerance.
6. **Post-amplification analysis:** LAMP products are not suitable for direct cloning or sequencing, limiting downstream applications.

[Source: Frontiers in Microbiology comprehensive overview, 2024](https://www.frontiersin.org/journals/microbiology/articles/10.3389/fmicb.2024.1406632/full)

---

## 3. Historical Evolution and Iteration

### Origin: Notomi et al., 2000

LAMP was invented by Tsugunori Notomi and colleagues at Eiken Chemical Co., Ltd. (Japan). The foundational paper — *"Loop-mediated isothermal amplification of DNA"* — was published in Nucleic Acids Research on June 15, 2000 (Vol. 28, No. 12, e63). The paper demonstrated amplification of a hepatitis B virus (HBV) target with high specificity and efficiency under isothermal conditions using four primers and Bst polymerase.

The paper has become one of the most cited molecular biology publications of its era, with tens of thousands of citations. [Source: Nucleic Acids Research, 2000](https://academic.oup.com/nar/article/28/12/e63/2359194)

### Key Milestones Timeline

**2000 — Invention:** Notomi et al. publish the foundational LAMP paper. Eiken Chemical files core patents.

**2002 — Loop primers introduced:** Nagamine et al. (also at Eiken) introduce loop primers (F-Loop, B-Loop), accelerating the reaction by 30–50% and reducing time to result from ~60 minutes to ~30 minutes. This significantly improved practical utility.

**2004 — RT-LAMP for RNA targets:** Mori et al. demonstrate one-step RT-LAMP for RNA detection, opening the door to viral diagnostics. This is the variant that would later power COVID-19 testing.

**2004–2008 — First commercial products:** Eiken Chemical launches the Loopamp product line, including reagent kits and the Loopamp EXIA turbidimeter. First commercial LAMP kits for tuberculosis, malaria, and other infectious diseases enter the market.

**2008–2015 — Expansion into tropical disease diagnostics:** LAMP gains traction for malaria (Plasmodium spp.), dengue, and neglected tropical diseases. WHO and FIND (Foundation for Innovative New Diagnostics) evaluate LAMP for low-resource settings. Colorimetric detection methods are refined, enabling truly instrument-free results.

**2015–2019 — Polymerase engineering:** Next-generation Bst polymerase variants (Bst 2.0, Bst 3.0, OmniAmp) are developed with improved thermal stability, salt tolerance, and reverse transcriptase activity. OmniAmp reduces amplification time by ~20%. These advances improve performance in complex sample matrices.

**2020 — COVID-19 acceleration:** The SARS-CoV-2 pandemic creates massive demand for rapid, decentralized molecular testing. On March 18, 2020, Eiken Chemical launches the Loopamp 2019-nCoV Detection Kit — one of the earliest commercial LAMP-based COVID-19 tests. [Source: Eiken Chemical press release, March 2020](https://www.eiken.co.jp/uploads/en/news/common/20200318-1.pdf)

**2020–2022 — Regulatory validation at scale:** RT-LAMP COVID-19 tests receive emergency use authorizations (EUAs) from FDA, CE marking in Europe, and NMPA approval in China. Large-scale clinical validation studies confirm RT-LAMP sensitivity of 92–98% and specificity of ~100% compared to RT-qPCR. [Source: PMC review, RT-LAMP for COVID-19, 2021](https://pmc.ncbi.nlm.nih.gov/articles/PMC8182821/)

**2021–2023 — CRISPR-LAMP hybrid assays:** Researchers combine LAMP amplification with CRISPR-Cas12a or Cas13a detection (LAMP-CRISPR), achieving attomolar sensitivity and eliminating false positives from non-specific amplification. This hybrid approach becomes a major research frontier. [Source: Frontiers in Bioengineering and Biotechnology, 2023](https://www.frontiersin.org/journals/bioengineering-and-biotechnology/articles/10.3389/fbioe.2023.1273988/full)

**2023–2025 — Microfluidic integration and multiplexing:** LAMP is integrated into microfluidic chips enabling simultaneous detection of 4–6 targets. Portable, battery-powered LAMP devices with smartphone readout emerge. The field transitions from single-target to multi-target platforms. [Source: RSC Analyst, portable 4-pathogen LAMP device, 2024](https://pubs.rsc.org/en/content/articlehtml/2024/an/d4an00748d)

**2024–2026 — Post-pandemic normalization:** LAMP market consolidates after COVID-19 peak. Focus shifts to endemic infectious diseases, food safety, agricultural diagnostics, and chronic disease monitoring. Chinese companies accelerate domestic LAMP product development for non-COVID applications.

### COVID-19 as a Technological Inflection Point

The pandemic was transformative for LAMP in ways that extend beyond COVID-19 testing itself:

- **Regulatory pathways were established** in major markets (FDA, CE, NMPA) for LAMP-based molecular diagnostics, reducing future approval timelines
- **Manufacturing scale-up** demonstrated that LAMP reagents could be produced at industrial volumes
- **Clinical validation data** accumulated rapidly, with hundreds of peer-reviewed studies establishing LAMP's performance characteristics
- **Awareness and adoption** among clinicians, public health officials, and policymakers increased dramatically
- **Investment** flowed into LAMP-adjacent technologies (CRISPR-LAMP, microfluidic LAMP, portable LAMP devices)

A 2022 review in MDPI Biosensors concluded that COVID-19 had "accelerated LAMP from a niche tool to a mainstream diagnostic platform" and asked whether LAMP had finally rivaled PCR. [Source: MDPI Biosensors, 2022](https://mdpi.com/2079-6374/12/7/492/htm)

---

## 4. Academic Research Landscape

### Seminal Papers

The LAMP literature is anchored by a small number of foundational papers that have shaped the entire field:

**1. Notomi et al. (2000) — The founding paper**
*"Loop-mediated isothermal amplification of DNA"*
Nucleic Acids Research, 28(12): e63
[https://academic.oup.com/nar/article/28/12/e63/2359194](https://academic.oup.com/nar/article/28/12/e63/2359194)
The original description of LAMP using four primers and Bst polymerase. Demonstrated on HBV target. Tens of thousands of citations. All subsequent LAMP work builds on this foundation.

**2. Nagamine et al. (2002) — Loop primers**
*"Accelerated reaction by loop-mediated isothermal amplification using loop primers"*
Molecular and Cellular Probes, 16(3): 223–229
Introduced the loop primer concept, reducing reaction time by 30–50%. Critical practical advance enabling sub-30-minute assays.

**3. Mori et al. (2004) — RT-LAMP**
*"Real-time turbidimetry of LAMP reaction for quantifying template DNA"*
Journal of Biochemical and Biophysical Methods, 59(2): 145–157
Established real-time turbidimetric monitoring and laid groundwork for RT-LAMP quantification.

**4. Tomita et al. (2008) — Colorimetric LAMP**
*"Loop-mediated isothermal amplification (LAMP) of gene sequences and simple visual detection of products"*
Nature Protocols, 3(5): 877–882
Introduced calcein-based colorimetric detection, enabling naked-eye results without instruments. Transformative for low-resource settings.

**5. Soroka et al. (2021) — Comprehensive review**
*"Loop-Mediated Isothermal Amplification (LAMP): The Better Sibling of PCR?"*
Genes, 12(9): 1-22
[https://pmc.ncbi.nlm.nih.gov/articles/PMC8393631/](https://pmc.ncbi.nlm.nih.gov/articles/PMC8393631/)
Comprehensive review covering mechanism, applications, limitations, and comparison with PCR. Widely cited post-COVID reference.

**6. Frontiers in Microbiology (2024) — Current state review**
*"Advancements and applications of loop-mediated isothermal amplification technology: a comprehensive overview"*
[https://www.frontiersin.org/journals/microbiology/articles/10.3389/fmicb.2024.1406632/full](https://www.frontiersin.org/journals/microbiology/articles/10.3389/fmicb.2024.1406632/full)
Most current comprehensive review as of 2024. Covers polymerase engineering, detection methods, multiplexing, and emerging applications.

### Research Frontier (2023–2026)

The active research frontier has moved well beyond basic LAMP assay development into four main areas:

**1. CRISPR-LAMP hybrid systems:** Combining LAMP's rapid amplification with CRISPR-Cas12a or Cas13a's collateral cleavage activity for signal amplification and specificity enhancement. SHERLOCK (Cas13a) and DETECTR (Cas12a) platforms both use isothermal amplification (often LAMP or RPA) as a preamplification step. [Source: Frontiers in Bioengineering and Biotechnology, 2023](https://www.frontiersin.org/journals/bioengineering-and-biotechnology/articles/10.3389/fbioe.2023.1273988/full)

**2. Multiplexed LAMP:** Methods enabling simultaneous detection of 2–6 targets in a single reaction. Approaches include molecular beacons, LAMP-sequencing, and microfluidic compartmentalization. A 2024 PMC review found no multiplex LAMP method had yet been validated under field conditions — a significant gap. [Source: PMC Multiplexing LAMP review, 2024](https://pmc.ncbi.nlm.nih.gov/articles/PMC11203869/)

**3. Microfluidic integration:** LAMP reactions integrated into centrifugal microfluidic chips, rotary platforms, and 3D-printed devices. A 2025 Nature Microsystems & Nanoengineering paper demonstrated a fully automated rotary microfluidic platform for high-throughput multiplex respiratory pathogen detection. [Source: Nature Microsystems & Nanoengineering, 2025](https://preview-www.nature.com/articles/s41378-025-01044-9)

**4. Extraction-free and direct sample LAMP:** Eliminating the RNA/DNA extraction step to enable truly rapid, minimal-equipment testing. Performance trade-offs (reduced sensitivity) are being addressed through improved polymerase formulations and sample preparation buffers.

### Key Researchers

- **Tsugunori Notomi** (Eiken Chemical) — inventor of LAMP; foundational patents and papers
- **Harumi Okayama** (Eiken Chemical) — co-inventor, original 2000 paper
- **Kentaro Nagamine** (Eiken Chemical) — loop primer development
- **Yasuyoshi Mori** (Eiken Chemical) — RT-LAMP and turbidimetric detection
- **Norio Tomita** (Eiken Chemical) — colorimetric detection methods
- **Broad Institute / MIT / Harvard researchers** — CRISPR-LAMP hybrid systems (19 patents each at Broad and MIT per PMC11394392 analysis)

### Research Output by Geography

Based on patent analysis data from the 2024 PMC study on LAMP commercial opportunity:

- **United States:** ~40% of global LAMP patents (excluding China-only filings); dominated by academic institutions (Broad Institute, MIT, Harvard) and commercial players (Thermo Fisher, NEB)
- **Asia (Japan, South Korea, China):** ~36% of global patents; Japan leads in foundational IP (Eiken), South Korea and China active in application-specific patents
- **Europe:** ~14% of patents; Germany, UK, Netherlands active
- **China (domestic filings):** The PMC study noted that when Chinese-only CNIPA filings are included, the total patent count rises from 1,134 to 3,479 — meaning China accounts for a very large share of domestic filings, though many are driven by government subsidy incentives rather than pure innovation

[Source: PMC11394392 — Commercial Opportunity or Addressing Unmet Needs, 2024](https://pmc.ncbi.nlm.nih.gov/articles/PMC11394392/)

China's academic LAMP output has grown substantially since 2020, with Chinese institutions contributing to research on:
- Veterinary and agricultural pathogen detection (porcine deltacoronavirus, avian influenza, foot-and-mouth disease)
- Food safety (Salmonella, Cronobacter in infant formula, GMO detection)
- Infectious disease diagnostics (tuberculosis, HIV, respiratory viruses)
- Environmental monitoring (waterborne pathogens)

[Source: Frontiers in Microbiology, porcine deltacoronavirus LAMP, 2024](https://www.frontiersin.org/journals/microbiology/articles/10.3389/fmicb.2024.1465923/full)

---

## 5. Patent Landscape

### Total Volume and Growth

As of 2022, the global LAMP patent landscape (excluding China-only domestic filings) comprised approximately **1,134 patents**, up from a much smaller base in the early 2000s. When Chinese CNIPA-only filings are included, the total rises to approximately **3,479 patents** — reflecting China's prolific domestic filing activity.

Patent filing rates have exceeded 100 new applications annually in recent years, with acceleration post-COVID-19. The technology entered a "growth phase" in its patent lifecycle roughly 20 years after its 2000 invention, likely driven by expiration of Eiken's foundational patents reducing licensing barriers.

[Source: PMC11394392 — LAMP patent analysis, 2024](https://pmc.ncbi.nlm.nih.gov/articles/PMC11394392/)

### Top Patent Holders

Based on the 2024 PMC analysis of the global LAMP patent landscape:

**Industry:**
| Company | Patent Count | Notes |
|---------|-------------|-------|
| Toshiba | 24 | Largest industrial holder; device/instrument patents |
| Eiken Chemical | 17 | Foundational method patents; many now expiring |
| New England Biolabs | 13 | Polymerase and reagent patents |
| Meridian Bioscience | Active | Diagnostic kit patents |
| Thermo Fisher Scientific | Active | Reagent and instrument patents |

**Academic Institutions:**
| Institution | Patent Count | Notes |
|-------------|-------------|-------|
| Broad Institute | 19 | CRISPR-LAMP hybrid systems |
| MIT | 19 | CRISPR-LAMP and microfluidic integration |
| Harvard | 18 | Diagnostic applications |

[Source: PMC11394392](https://pmc.ncbi.nlm.nih.gov/articles/PMC11394392/)

### Geographic Distribution

- **US applicants:** ~40% of global patents (excluding China-only)
- **Asia (Japan, South Korea, China):** ~36%
- **Europe:** ~14%
- **Other:** ~10%

### Key Patents

**Foundational (Eiken Chemical):**
- Core LAMP method patent (Notomi et al., filed ~1999–2000) — the foundational IP. Many jurisdictions have seen this patent expire or approach expiry, opening the field.
- Loop primer patents (Nagamine et al., ~2002) — accelerated reaction method

**Recent Notable Patents:**
- **WO2024073740A2** — "Improved LAMP methods, compositions, kits, and systems for detecting nucleic acids" — filed September 29, 2023. Covers next-generation LAMP improvements. [Source: Google Patents](https://patents.google.com/patent/WO2024073740A2/en)
- **US11345970B2** — Rapid diagnostic test integrating LAMP for point-of-care use. [Source: Google Patents](https://patents.google.com/patent/US11345970B2/en)
- **CN118621045A** — Chinese LAMP patent filed/published September 2024, reflecting active domestic R&D. [Source: Patent Images](https://patentimages.storage.googleapis.com/6c/20/79/a871b773633638/CN118621045A.pdf)
- **CN102154477B** — Chinese LAMP kit for detecting Mycoplasma hyopneumoniae (veterinary application) — illustrates China's long-standing LAMP IP in agricultural diagnostics. [Source: Google Patents](https://patents.google.com/patent/CN102154477B/en)

### China Filing Trends

China's LAMP patent filing activity is characterized by:

1. **Volume:** China accounts for the majority of the gap between the 1,134 "quality-filtered" global patents and the 3,479 total patents — implying ~2,345 China-only domestic filings
2. **Incentive structure:** Chinese LAMP patents are partly driven by government R&D subsidies and tax benefits tied to patent counts, not purely commercial innovation
3. **Application focus:** Chinese filings concentrate on specific pathogen applications (veterinary, agricultural, food safety, infectious disease) rather than platform/method improvements
4. **Quality gap:** The PMC study explicitly noted that Chinese patent filings were excluded from their "innovation-quality" analysis due to concerns about filing motivations — a structural issue in China's IP ecosystem that affects how to interpret raw filing numbers

[REASONED INFERENCE — NOT SOURCED DATA]: As Eiken's foundational LAMP patents expire globally (most core patents filed ~1999–2002 have 20-year terms, placing expiry around 2019–2022), Chinese companies face reduced licensing barriers and are accelerating their own LAMP product development and IP filing activity.

---

## 6. Technology Readiness and Commercialization

### TRL Assessment

LAMP as a technology platform sits at **TRL 8–9** (system complete and qualified / actual system proven in operational environment) for its core applications:

| Application | TRL | Rationale |
|-------------|-----|-----------|
| Single-target infectious disease diagnostics (clinical) | TRL 9 | Multiple NMPA/FDA/CE-approved products; large-scale deployment during COVID-19 |
| RT-LAMP for respiratory viruses | TRL 9 | Validated at scale; regulatory approvals in major markets |
| Colorimetric LAMP for field use | TRL 8 | Commercially available; validated in multiple settings; some field deployment gaps remain |
| Multiplexed LAMP (2–4 targets) | TRL 6–7 | Demonstrated in research; limited commercial products; no field validation |
| CRISPR-LAMP hybrid systems | TRL 4–6 | Proof-of-concept demonstrated; clinical validation ongoing; no major commercial products |
| Microfluidic LAMP chips | TRL 5–7 | Research prototypes to early commercial products; limited regulatory approvals |
| Extraction-free direct LAMP | TRL 6–7 | Demonstrated; performance trade-offs limit clinical adoption |

### Commercial Deployments

**Global:**
- **Eiken Chemical (Japan):** Loopamp product line — the commercial standard. Kits for tuberculosis, malaria, influenza, COVID-19, and other pathogens. Loopamp EXIA turbidimeter for automated reading. [Source: Eiken Genome Site](https://loopamp.eiken.co.jp/en/)
- **New England Biolabs (US):** WarmStart LAMP Kit — widely used in research and clinical labs
- **Meridian Bioscience (US):** LAMP reagent components and kits
- **HiberGene Diagnostics (Ireland):** LAMP-based respiratory pathogen tests
- **Lucira by Pfizer (US):** At-home molecular test (LAMP-based) for COVID-19/influenza; ~$39.99 per test [Source: CBS News](https://www.cbsnews.com/news/free-covid-tests-accuracy/)

**China:**
- **Beijing Lanpu Biotechnology (北京蓝谱生物技术开发有限公司):** China-based company specifically focused on LAMP diagnostics [Source: Beijing Lanpu](http://www.beijinglanpu.com/)
- **Tianlong Science & Technology (西安天隆科技):** Leading Chinese IVD company; selected to lead National Key R&D Program under China's 14th Five-Year Plan for molecular diagnostics; products include nucleic acid extractors and diagnostic kits [Source: Tianlong](https://www.medtl.net/about/about-us)
- **Sansure Biotech (圣湘生物):** Major Chinese IVD company with NMPA-approved molecular diagnostic kits; primarily PCR-based but with LAMP-adjacent POCT products (iPonatic portable system) [Source: Sansure Global](https://www.sansureglobal.com/)
- **Daan Gene (达安基因):** Sun Yat-sen University spinout; broad molecular diagnostics portfolio including NMPA-approved kits [Source: Daan Gene](https://en.daangene.com/)

### Market Size and Cost Trajectory

**Global LAMP Market:**
- 2025 market size: **USD 111.62–115.7 million** (Research Nester / Future Market Insights)
- 2026 projected: **USD 116.74 million**
- 2035 projected: **USD 183.56–184.8 million**
- CAGR 2026–2035: **4.9–5.1%**

[Source: Research Nester LAMP Market Report](https://www.researchnester.com/reports/loop-mediated-isothermal-amplification-lamp-market/4595) | [Source: Future Market Insights LAMP Market](https://www.futuremarketinsights.com/reports/loop-mediated-isothermal-amplification-market)

**Cost per test trajectory:**
- Early LAMP kits (2005–2015): $10–$30 per test (research-grade)
- COVID-era LAMP tests (2020–2022): $5–$20 per test (high-volume production)
- Current commercial LAMP tests (2024–2026): $3–$15 per test depending on format and volume
- At-home LAMP tests (Lucira-type): ~$40 per test (consumer retail)
- [REASONED INFERENCE — NOT SOURCED DATA]: Chinese domestic LAMP kits likely priced at $1–$5 per test at scale, consistent with China's broader IVD pricing dynamics

**Cost comparison context:**
- Rapid antigen tests: $5–$15 per test
- Standard RT-PCR: $25–$300 per test (lab-based)
- At-home molecular tests: $20–$40 per test

[Source: BetterCare COVID testing costs](https://bettercare.com/costs/covid-test-cost-without-insurance)

### Regulatory Status in China

**NMPA (National Medical Products Administration) framework:**
- LAMP-based diagnostic kits are regulated as Class II or Class III in vitro diagnostic devices (IVDs) in China, depending on the intended use and risk classification
- COVID-19 LAMP kits received emergency approvals during 2020–2022 under China's expedited review pathway
- Post-pandemic, LAMP kits for non-COVID applications (respiratory viruses, STIs, food safety) are being submitted through standard NMPA review pathways
- China's 2024 diagnostic reagent industry policy explicitly encourages development of "advanced diagnostic technologies and products," which includes isothermal amplification methods [Source: Sina Finance, 2024 China diagnostics policy](https://finance.sina.com.cn/roll/2024-08-21/doc-inckkuya2613145.shtml)

**POCT regulatory pathway:**
- China's 14th Five-Year Plan (2021–2025) explicitly prioritizes POCT development in the national medical equipment sector plan [Source: Fosun Diagnostics, 14th FYP POCT](https://www.fosundiagnostics.com/en/web/newsDetails.do?id=2205031815521970743541)
- This creates a favorable regulatory environment for LAMP-based POCT products seeking NMPA approval

---

## 7. Competitive Technology Comparison

### LAMP vs. RT-qPCR (Gold Standard)

RT-qPCR (reverse transcription quantitative PCR) remains the gold standard for molecular diagnostics. LAMP's competitive position against PCR is nuanced:

| Dimension | RT-qPCR | RT-LAMP | Advantage |
|-----------|---------|---------|-----------|
| Sensitivity | ~100 copies/mL | ~10–100 copies/mL | Comparable; LAMP slightly better in some assays |
| Specificity | Very high (2 primers) | Very high (4–6 primers, 6–8 binding sites) | LAMP theoretically higher due to more binding sites |
| Time to result | 2–4 hours (lab) | 15–60 minutes | LAMP wins decisively |
| Equipment cost | $5,000–$50,000 | $200–$2,000 | LAMP wins decisively |
| Equipment complexity | High (thermocycler + reader) | Low (heat block + optional reader) | LAMP wins |
| Multiplexing | Excellent (up to 4–5 targets) | Limited (1–2 targets commercially) | PCR wins |
| Quantification | Excellent (Ct values) | Limited (semi-quantitative at best) | PCR wins |
| Primer design | Moderate (2 primers) | Complex (4–6 primers) | PCR wins |
| Contamination risk | Moderate | Higher (massive amplicon production) | PCR wins |
| Regulatory acceptance | Established gold standard | Growing; COVID validated at scale | PCR wins (for now) |
| Cost per test | $25–$300 | $3–$40 | LAMP wins |

**Verdict:** LAMP is not a replacement for PCR in high-complexity laboratory settings requiring quantification or multiplexing. It is a compelling alternative for rapid, decentralized, single-target testing where speed and equipment simplicity matter more than quantitative precision.

Clinical validation data for SARS-CoV-2: RT-LAMP achieved 96% sensitivity and 99.99% specificity on RNA-extracted samples, essentially matching RT-qPCR. On direct (extraction-free) samples, sensitivity drops to 70–85%. [Source: Pirbright Institute RT-LAMP validation](https://www.pirbright.ac.uk/publications/reverse-transcription-loop-mediated-isothermal-amplification-has-high-accuracy)

### LAMP vs. CRISPR-Based Diagnostics (SHERLOCK, DETECTR)

CRISPR-based diagnostics (SHERLOCK using Cas13a, DETECTR using Cas12a) represent the next generation of molecular diagnostics. Most CRISPR diagnostic platforms actually use LAMP or RPA as a preamplification step before CRISPR detection.

| Dimension | LAMP alone | CRISPR-LAMP hybrid | CRISPR alone (amplification-free) |
|-----------|-----------|-------------------|----------------------------------|
| Sensitivity | High (10–100 copies/mL) | Attomolar (10⁻¹⁸ M) | Lower without amplification |
| Specificity | High | Very high (dual recognition) | Very high |
| Time to result | 15–60 min | 30–90 min | 30–60 min |
| Equipment | Minimal | Minimal + fluorescence reader | Minimal |
| Multiplexing | Limited | Limited | Limited |
| Cost | Low | Moderate | Moderate |
| Regulatory status | Established | Early stage | Early stage |
| Commercial products | Many | Very few | Very few |

**Verdict:** CRISPR-LAMP hybrids offer superior sensitivity and specificity but add complexity and cost. They are a research frontier, not yet a commercial reality at scale. For the 2024–2026 window, LAMP alone remains the more commercially relevant technology. CRISPR-LAMP is the technology to watch for 2027–2030.

[Source: Frontiers in Bioengineering and Biotechnology, CRISPR-isothermal synergy, 2023](https://www.frontiersin.org/journals/bioengineering-and-biotechnology/articles/10.3389/fbioe.2023.1273988/full)

### LAMP vs. Rapid Antigen Tests (RATs)

Rapid antigen tests detect viral proteins rather than nucleic acids. They are the dominant format for consumer/home testing.

| Dimension | Rapid Antigen Test | LAMP |
|-----------|-------------------|------|
| Sensitivity | 50–85% (varies by viral load) | 90–98% (with extraction) |
| Specificity | 95–99% | ~100% |
| Time to result | 10–30 minutes | 15–60 minutes |
| Equipment | None | Heat block (minimal) |
| Cost per test | $5–$15 | $3–$40 |
| User complexity | Very low (home use) | Low-moderate (some training needed) |
| Regulatory pathway | Simpler | More complex |
| Suitable for home use | Yes (established) | Emerging (Lucira-type products) |

**Verdict:** Rapid antigen tests win on simplicity, cost, and consumer accessibility. LAMP wins on sensitivity and specificity. The market segments are distinct: RATs for mass screening and home use; LAMP for clinical confirmation and settings where molecular accuracy is needed without lab infrastructure.

[Source: Nature — future of at-home molecular testing, 2024](https://www.nature.com/articles/d41586-024-00854-7)

### Comparison Matrix Summary

| Technology | Sensitivity | Speed | Cost | Equipment | Multiplex | Regulatory Maturity |
|-----------|------------|-------|------|-----------|-----------|-------------------|
| RT-qPCR | ★★★★★ | ★★ | ★★ | ★ | ★★★★★ | ★★★★★ |
| RT-LAMP | ★★★★ | ★★★★★ | ★★★★ | ★★★★★ | ★★ | ★★★★ |
| CRISPR-LAMP | ★★★★★ | ★★★ | ★★★ | ★★★★ | ★★ | ★★ |
| Rapid Antigen | ★★ | ★★★★★ | ★★★★★ | ★★★★★ | ★ | ★★★★★ |
| NGS | ★★★★★ | ★ | ★ | ★ | ★★★★★ | ★★★ |

---

## 8. Future Outlook

### Near-Term (1–3 Years: 2026–2028) [FORECAST — SUBJECT TO UNCERTAINTY]

**Technology developments:**
- Multiplexed LAMP (2–4 targets) will achieve first commercial products and regulatory approvals, particularly for respiratory pathogen panels (COVID-19 + influenza A/B + RSV)
- Microfluidic LAMP chips will move from research prototypes to early commercial deployment in China and developed markets
- Extraction-free LAMP protocols will improve, reducing the sensitivity gap with extraction-based methods
- LAMP-lateral flow assay combinations will become the dominant format for field-deployable molecular diagnostics

**Market dynamics:**
- Post-COVID normalization will continue; LAMP market growth will be driven by endemic infectious disease, food safety, and agricultural applications rather than pandemic response
- Chinese domestic LAMP product development will accelerate as Eiken's foundational patents expire and domestic companies build their own IP
- LAMP will gain share in China's grassroots healthcare network as NMPA approvals accumulate and costs decline

**Regulatory:**
- NMPA will establish clearer POCT regulatory pathways, benefiting LAMP-based products
- FDA and CE frameworks for LAMP-based home testing will mature, following the Lucira precedent

### Mid-Term (3–7 Years: 2028–2032) [FORECAST — SUBJECT TO UNCERTAINTY]

**Technology developments:**
- CRISPR-LAMP hybrid systems will achieve first commercial regulatory approvals for high-value applications (rare pathogen detection, antimicrobial resistance profiling)
- AI-assisted primer design will reduce the complexity barrier for new LAMP assay development
- Smartphone-integrated LAMP readers will become mainstream, enabling truly decentralized molecular diagnostics
- Multiplexed LAMP (4–6 targets) will be validated under field conditions and deployed in resource-limited settings

**Market dynamics:**
- LAMP market CAGR of 4.9–5.1% will compound to a global market of ~$140–150 million by 2030
- Asia-Pacific (led by China, India, Southeast Asia) will be the fastest-growing region
- Chinese companies will emerge as significant global LAMP players, competing with Eiken and NEB on cost and application breadth

**China-specific:**
- LAMP will be integrated into China's national infectious disease surveillance network
- Agricultural and food safety LAMP applications will scale significantly, driven by China's food safety regulatory tightening
- Chinese LAMP companies will begin exporting to Southeast Asia, Africa, and other emerging markets

### Long-Term (7–15 Years: 2032–2040) [FORECAST — SUBJECT TO UNCERTAINTY]

- LAMP may be partially displaced by next-generation isothermal methods (CRISPR-based, toehold switch biosensors) for high-complexity applications
- For simple, rapid, low-cost single-target detection, LAMP will remain the dominant molecular method — its simplicity is a durable advantage
- The LAMP market will likely consolidate around a few dominant platforms (instrument + reagent ecosystems) rather than remaining fragmented
- China will be a major global supplier of LAMP reagents and instruments, leveraging manufacturing cost advantages

---

## 9. China-Specific Analysis

### Chinese Research Output

China has become a significant contributor to LAMP research, particularly in applied diagnostics:

**Veterinary and agricultural diagnostics:**
- Chinese researchers have published extensively on LAMP assays for porcine deltacoronavirus, avian influenza (H5N1, H7N9), foot-and-mouth disease, African swine fever, and other economically important animal pathogens
- A 2024 Frontiers in Microbiology paper from Chinese researchers developed a visual RT-LAMP method for porcine deltacoronavirus detection [Source: Frontiers in Microbiology, 2024](https://www.frontiersin.org/journals/microbiology/articles/10.3389/fmicb.2024.1465923/full)

**Food safety:**
- LAMP for Salmonella, Cronobacter, and other foodborne pathogens in Chinese food matrices (infant formula, meat products) is an active research area
- Detection of Cronobacter and Salmonella in powdered infant formula using LAMP provides next-day results vs. 3–5 days for standard GB methods [Source: Longdom Open Access](https://www.longdom.org/open-access/rapid-detection-of-emcronobacterem-and-emsalmonellaem-in-powdered-infant-formula-and-related-matrices-using-loopmediated-isotherma-87915.html)

**Infectious disease:**
- Chinese institutions have contributed to LAMP assay development for tuberculosis, HIV, hepatitis B/C, and respiratory viruses
- Post-COVID, Chinese researchers are publishing on LAMP for endemic respiratory pathogens (influenza, RSV, mycoplasma pneumoniae)

**Patent output:**
- China accounts for the majority of domestic LAMP patent filings globally, though quality and innovation content vary significantly
- [REASONED INFERENCE — NOT SOURCED DATA]: Chinese LAMP patent filings likely number in the hundreds annually at CNIPA, driven by both genuine innovation and government subsidy incentives

### State Policy Support

China's policy environment is strongly supportive of LAMP and isothermal amplification technologies:

**14th Five-Year Plan (2021–2025):**
- POCT explicitly prioritized in the national medical equipment development plan [Source: Fosun Diagnostics](https://www.fosundiagnostics.com/en/web/newsDetails.do?id=2205031815521970743541)
- National Key R&D Programs fund molecular diagnostics infrastructure; Tianlong Science & Technology was selected to lead one such program [Source: Tianlong / medtl.net](https://www.medtl.net/news/default/tianlong-to-lead-national-key-rampd-program-for-chinas-14th-fyp.html)

**2024 Diagnostics Policy:**
- China's national and provincial diagnostic reagent industry policies explicitly encourage development of "advanced diagnostic technologies and products" [Source: Sina Finance, 2024](https://finance.sina.com.cn/roll/2024-08-21/doc-inckkuya2613145.shtml)

**Grassroots healthcare expansion:**
- China's ongoing push to strengthen primary healthcare capacity (基层医疗) creates structural demand for LAMP-type technologies that deliver molecular accuracy without PCR infrastructure
- Plans to expand community hospitals and rural clinics create a natural deployment pathway for LAMP-based POCT [Source: China Daily HK, grassroots healthcare](https://www.chinadailyhk.com/hk/article/581687)

**Biosecurity and pandemic preparedness:**
- Post-COVID, China has invested heavily in infectious disease surveillance and rapid response capabilities, where LAMP plays a role as a deployable field diagnostic

### Key Chinese Companies

| Company | Focus | LAMP Relevance | Status |
|---------|-------|---------------|--------|
| Beijing Lanpu Biotechnology (北京蓝谱生物) | LAMP-specific diagnostics | Core business | Active; LAMP-dedicated |
| Tianlong Science & Technology (西安天隆) | Molecular diagnostics instruments & kits | LAMP-compatible instruments | National Key R&D Program leader |
| Sansure Biotech (圣湘生物) | Molecular diagnostics | POCT platform (iPonatic) | Listed company; NMPA-approved products |
| Daan Gene (达安基因) | Molecular diagnostics | Broad IVD portfolio | Sun Yat-sen University spinout; listed |
| BGI Genomics (华大基因) | Genomics & diagnostics | Large-scale testing infrastructure | Global player; WHO EUL-approved COVID kits |
| Maccura Biotechnology (迈克生物) | IVD reagents | Broad diagnostics portfolio | NMPA-approved; active in COVID testing |

[Sources: Sansure Global](https://www.sansureglobal.com/) | [Daan Gene](https://en.daangene.com/) | [Tianlong](https://www.medtl.net/about/about-us) | [Beijing Lanpu](http://www.beijinglanpu.com/)

### Technology Gaps — Where China Lags

1. **Foundational IP:** Eiken Chemical holds the core LAMP method patents. Chinese companies are building application-specific IP but lack foundational platform patents.
2. **Polymerase engineering:** Advanced Bst polymerase variants (Bst 3.0, OmniAmp) are primarily developed by US/Japanese companies (NEB, Eiken). Chinese companies largely rely on licensed or reverse-engineered polymerases.
3. **Multiplexed LAMP platforms:** No Chinese company has yet commercialized a validated multiplexed LAMP platform. This is a global gap, but Chinese companies are not leading the solution.
4. **CRISPR-LAMP integration:** The leading CRISPR-LAMP research comes from US academic institutions (Broad, MIT, Harvard). Chinese researchers are active but not at the frontier.
5. **Regulatory harmonization:** Chinese LAMP products face barriers to international market entry due to limited CE/FDA approvals. Most Chinese LAMP IP is domestically focused.

### Areas Where China Leads or Is Competitive

1. **Agricultural and veterinary LAMP:** China's large agricultural sector and history of animal disease outbreaks (ASF, avian influenza) have driven significant applied LAMP research and product development
2. **Food safety LAMP:** China's stringent food safety regulations post-2008 melamine scandal have created strong domestic demand for rapid food pathogen detection
3. **Manufacturing cost:** Chinese LAMP reagent manufacturers can produce at significantly lower cost than Japanese or US competitors, enabling price-competitive products for domestic and emerging market deployment
4. **Scale of deployment:** China's COVID-19 testing infrastructure demonstrated the ability to deploy molecular diagnostics at unprecedented scale — a capability that can be leveraged for LAMP-based surveillance
5. **Domestic market size:** China's 1.4 billion population and expanding healthcare coverage create a large captive market for LAMP-based diagnostics, supporting domestic product development economics

---

## 10. Strategic Implications

### Investment Signals

**Positive signals for LAMP investment in China:**

1. **Policy tailwind is real and durable:** China's 14th FYP POCT prioritization, National Key R&D Programs, and grassroots healthcare expansion all create structural demand for LAMP-type technologies. This is not a one-cycle policy — it reflects a multi-decade healthcare infrastructure buildout.

2. **Patent expiry opens the field:** As Eiken's foundational LAMP patents expire (most core patents filed ~1999–2002), Chinese companies face reduced licensing barriers. The window to build competitive LAMP IP and products is open now.

3. **COVID-19 created regulatory infrastructure:** NMPA pathways for LAMP-based molecular diagnostics are now established. Future products will face shorter approval timelines than the first generation.

4. **Agricultural and food safety demand is underserved:** China's massive agricultural sector and food safety regulatory environment create large, underserved demand for rapid pathogen detection. LAMP is well-suited to these applications and Chinese companies have home-field advantage.

5. **Cost structure favors Chinese manufacturers:** At $1–$5 per test at scale, Chinese LAMP kits can compete globally on price while maintaining acceptable margins domestically.

**Caution signals:**

1. **Post-COVID market normalization:** The LAMP market contracted from its 2020–2022 peak as COVID-19 testing demand collapsed. The 4.9–5.1% CAGR forecast reflects modest, not explosive, growth.

2. **Multiplexing gap limits clinical utility:** Until multiplexed LAMP is commercially validated, LAMP remains a single-target tool, limiting its appeal for complex clinical panels where PCR dominates.

3. **CRISPR-LAMP disruption risk:** If CRISPR-LAMP hybrid systems achieve commercial scale by 2028–2030, they could displace standalone LAMP in high-value clinical applications.

4. **Chinese IP quality concerns:** The gap between China's raw patent filing numbers and "innovation-quality" patents is a structural issue. Investors should look beyond patent counts to actual product approvals and clinical validation data.

### Companies to Watch

**China:**
- **Beijing Lanpu Biotechnology** — the most LAMP-focused Chinese company; worth monitoring for product pipeline and NMPA approvals
- **Tianlong Science & Technology** — National Key R&D Program leadership signals government backing; watch for LAMP-compatible instrument launches
- **Sansure Biotech** — listed company with POCT platform (iPonatic); positioned to add LAMP-based assays to existing instrument ecosystem
- **[REASONED INFERENCE — NOT SOURCED DATA]:** Watch for new entrants from China's university spinout ecosystem (Tsinghua, Peking University, Fudan) developing CRISPR-LAMP platforms

**Global:**
- **Eiken Chemical** — still the LAMP standard-bearer; watch for next-generation Loopamp products and China market strategy
- **New England Biolabs** — polymerase innovation leader; Bst polymerase improvements drive the entire LAMP ecosystem
- **HiberGene Diagnostics** — European LAMP-focused company; potential acquisition target for larger IVD players
- **Lucira by Pfizer** — at-home LAMP testing; watch for expansion beyond COVID/influenza

### Monitoring Indicators

Track these metrics to assess LAMP's trajectory in China's molecular diagnostics market:

| Indicator | What to Watch | Frequency |
|-----------|--------------|-----------|
| NMPA approvals | Number of new LAMP-based IVD approvals per year | Quarterly |
| Chinese LAMP patent filings | Quality-filtered filings (not just raw CNIPA counts) | Annually |
| Grassroots healthcare POCT adoption | Government procurement data for POCT devices | Annually |
| Multiplexed LAMP clinical trials | ClinicalTrials.gov and Chinese clinical trial registry | Quarterly |
| CRISPR-LAMP regulatory submissions | FDA/CE/NMPA submissions for hybrid platforms | Quarterly |
| Chinese LAMP export data | Customs data for IVD kit exports from China | Annually |
| Eiken China revenue | Eiken annual report China segment data | Annually |

---

## 11. Confidence Level

### Overall Confidence: **Medium-High**

**High confidence areas:**
- Technical mechanism and performance metrics — well-established in peer-reviewed literature with extensive clinical validation data
- Historical evolution — documented in primary sources (original papers, Eiken press releases)
- COVID-19 acceleration narrative — extensively documented
- Global patent landscape structure (top holders, geographic distribution) — sourced from 2024 PMC analysis
- Market size estimates (global LAMP market ~$112–116M in 2025) — consistent across multiple independent market research sources
- China policy environment — sourced from official government documents and credible secondary sources

**Medium confidence areas:**
- China-specific LAMP market size — no isolated China figure available; extrapolated from Asia-Pacific data and China's share of global molecular diagnostics
- Chinese company LAMP product specifics — limited English-language documentation; Beijing Lanpu and others have limited public disclosure
- Cost per test estimates for Chinese domestic products — reasoned inference based on China IVD pricing patterns, not direct sourcing
- Future outlook forecasts — inherently uncertain; based on technology trajectory and market dynamics

**Lower confidence areas:**
- China LAMP patent filing volumes — the gap between quality-filtered and raw CNIPA data is documented, but precise annual filing numbers for LAMP specifically are not publicly available
- Specific NMPA approval counts for LAMP products — NMPA database is not easily searchable in English; exact numbers require Chinese-language database access
- Chinese company revenue from LAMP specifically — most Chinese IVD companies do not break out LAMP revenue separately

**Key data gaps:**
1. China-specific LAMP market size (RMB/USD)
2. Number of NMPA-approved LAMP diagnostic kits as of 2025
3. Beijing Lanpu Biotechnology financial and product details
4. Chinese LAMP export volumes and destination markets
5. Clinical adoption rates of LAMP vs. PCR in Chinese primary care settings

---

## 12. Sources

All URLs cited in this report, numbered for reference:

1. Notomi et al. (2000) — Foundational LAMP paper, Nucleic Acids Research: https://academic.oup.com/nar/article/28/12/e63/2359194
2. PMC version of Notomi et al. (2000): https://pmc.ncbi.nlm.nih.gov/articles/PMC102748/
3. Frontiers in Microbiology — LAMP comprehensive overview (2024): https://www.frontiersin.org/journals/microbiology/articles/10.3389/fmicb.2024.1406632/full
4. PMC — LAMP: The Better Sibling of PCR? (Soroka et al., 2021): https://pmc.ncbi.nlm.nih.gov/articles/PMC8393631/
5. PMC — Commercial Opportunity or Addressing Unmet Needs — LAMP (2024): https://pmc.ncbi.nlm.nih.gov/articles/PMC11394392/
6. MDPI Diagnostics — Commercial Opportunity or Addressing Unmet Needs — LAMP (2024): https://www.mdpi.com/2075-4418/14/17/1845
7. MDPI Biosensors — Progression of LAMP as a Result of COVID-19 Pandemic (2022): https://mdpi.com/2079-6374/12/7/492/htm
8. PMC — RT-LAMP for COVID-19 systematic review and meta-analysis (2021): https://pmc.ncbi.nlm.nih.gov/articles/PMC8182821/
9. Pirbright Institute — RT-LAMP high accuracy for SARS-CoV-2: https://www.pirbright.ac.uk/publications/reverse-transcription-loop-mediated-isothermal-amplification-has-high-accuracy
10. Nature Scientific Reports — Colorimetric RT-LAMP SARS-CoV-2 (2021): https://www.nature.com/articles/s41598-021-88506-y
11. Nature Scientific Reports — Clinical validation of optimised RT-LAMP (2021): https://www.nature.com/articles/s41598-021-95607-1
12. PLOS ONE — Multicenter international assessment of SARS-CoV-2 RT-LAMP (2022): https://dx.plos.org/10.1371/journal.pone.0268340
13. Eiken Chemical — Loopamp 2019-nCoV Detection Kit launch press release (March 2020): https://www.eiken.co.jp/uploads/en/news/common/20200318-1.pdf
14. Eiken Genome Site — LAMP product information: https://loopamp.eiken.co.jp/en/
15. Eiken Chemical — LAMP products page: https://www.eiken.co.jp/en/products/lamp/
16. Research Nester — LAMP Market Report 2025–2037: https://www.researchnester.com/reports/loop-mediated-isothermal-amplification-lamp-market/4595
17. Future Market Insights — LAMP Market 2025–2035: https://www.futuremarketinsights.com/reports/loop-mediated-isothermal-amplification-market
18. Strategic Market Research — LAMP Market Report 2024–2030: https://www.strategicmarketresearch.com/market-report/loop-mediated-isothermal-amplification-market
19. Grand View Research — China Molecular Diagnostics Market 2025–2030: https://www.grandviewresearch.com/horizon/outlook/molecular-diagnostics-market/china
20. MarketsandMarkets — Molecular Diagnostics Market $30.74B by 2030: https://www.marketsandmarkets.com/PressReleases/molecular-diagnostic.asp
21. Industry Today — Point-of-Care Molecular Diagnostics Market growth through 2034: https://industrytoday.co.uk/health_and_safety/point-of-care-molecular-diagnostics-market-rapid-growth-ahead-through-2034
22. Google Patents — WO2024073740A2 (Improved LAMP methods, 2023): https://patents.google.com/patent/WO2024073740A2/en
23. Google Patents — US11345970B2 (Rapid diagnostic test for LAMP): https://patents.google.com/patent/US11345970B2/en
24. Google Patents — CN102154477B (Chinese LAMP kit for Mycoplasma hyopneumoniae): https://patents.google.com/patent/CN102154477B/en
25. Patent Images — CN118621045A (Chinese LAMP patent, 2024): https://patentimages.storage.googleapis.com/6c/20/79/a871b773633638/CN118621045A.pdf
26. Frontiers in Bioengineering and Biotechnology — CRISPR-isothermal amplification synergy (2023): https://www.frontiersin.org/journals/bioengineering-and-biotechnology/articles/10.3389/fbioe.2023.1273988/full
27. Frontiers in Pediatrics — LAMP-CRISPR/Cas12a for respiratory pathogens (2025): https://www.frontiersin.org/journals/pediatrics/articles/10.3389/fped.2025.1533100/full
28. PMC — Multiplexing LAMP Assays review (2024): https://pmc.ncbi.nlm.nih.gov/articles/PMC11203869/
29. Nature Microsystems & Nanoengineering — Rotary microfluidic LAMP platform (2025): https://preview-www.nature.com/articles/s41378-025-01044-9
30. RSC Analyst — Portable 4-pathogen LAMP microfluidic device (2024): https://pubs.rsc.org/en/content/articlehtml/2024/an/d4an00748d
31. Nature — Future of at-home molecular testing (2024): https://www.nature.com/articles/d41586-024-00854-7
32. Fosun Diagnostics — 14th FYP POCT prioritization: https://www.fosundiagnostics.com/en/web/newsDetails.do?id=2205031815521970743541
33. Tianlong — National Key R&D Program leadership: https://www.medtl.net/news/default/tianlong-to-lead-national-key-rampd-program-for-chinas-14th-fyp.html
34. Sina Finance — 2024 China diagnostics policy roundup: https://finance.sina.com.cn/roll/2024-08-21/doc-inckkuya2613145.shtml
35. China Daily HK — Grassroots healthcare expansion: https://www.chinadailyhk.com/hk/article/581687
36. Sansure Biotech — Company and products: https://www.sansureglobal.com/
37. Daan Gene — Company information: https://en.daangene.com/
38. Tianlong Science & Technology — Company information: https://www.medtl.net/about/about-us
39. Beijing Lanpu Biotechnology — Company website: http://www.beijinglanpu.com/
40. PMC — Recent progress on rapid diagnosis of COVID-19 by POCT (2023): https://pmc.ncbi.nlm.nih.gov/articles/PMC10266891/
41. Virologica Sinica — Summary of SARS-CoV-2 detection kits approved by NMPA (2020): https://www.virosin.org/article/doi/10.1007/s12250-020-00331-1
42. BGI — WHO Emergency Use Listing for RT-PCR kit (2020): https://www.prnewswire.com/news-releases/bgis-real-time-fluorescent-rt-pcr-kit-for-detecting-2019-ncov-eligible-for-who-emergency-use-listing-301056874.html
43. Frontiers in Microbiology — Porcine deltacoronavirus visual RT-LAMP (2024): https://www.frontiersin.org/journals/microbiology/articles/10.3389/fmicb.2024.1465923/full
44. Longdom — LAMP for Cronobacter and Salmonella in infant formula: https://www.longdom.org/open-access/rapid-detection-of-emcronobacterem-and-emsalmonellaem-in-powdered-infant-formula-and-related-matrices-using-loopmediated-isotherma-87915.html
45. BetterCare — COVID testing costs 2026: https://bettercare.com/costs/covid-test-cost-without-insurance
46. CBS News — Lucira at-home molecular test pricing: https://www.cbsnews.com/news/free-covid-tests-accuracy/
47. DataInsightsMarket — LAMP Reagent market report: https://www.datainsightsmarket.com/reports/loop-mediated-isothermal-amplificationlamp-reagent-1749261
48. Frontiers in Microbiology — Progress in isothermal amplification for infectious disease diagnosis (2025): https://www.frontiersin.org/journals/microbiology/articles/10.3389/fmicb.2025.1601644/pdf
49. NMPA — Database of approved medical products: https://english.nmpa.gov.cn/database.html
50. Patsnap Synapse — Eiken Chemical patent portfolio: https://synapse.patsnap.com/organization/adde5167ebce75de2320e1d394b8e3a1

---

*Report prepared by Technology Research Analyst | March 2026*
*Classification: Market Research — Investor/Market Entrant Use*
