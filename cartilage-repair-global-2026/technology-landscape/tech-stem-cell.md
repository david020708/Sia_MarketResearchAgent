# Technology Deep-Dive: Stem Cell and iPSC Approaches for Cartilage Repair

**Technology Family:** Cell-Based Cartilage Repair — Mesenchymal Stem Cells (MSC) and Induced Pluripotent Stem Cells (iPSC)
**TRL Range:** MSC Autologous: 7–8 | MSC Allogeneic: 5–7 | iPSC-Derived Chondrocytes: 3–5
**Horizon Classification:** MSC Autologous: H1–H2 | MSC Allogeneic and iPSC: H2–H3

---

## 1. Technology Overview

**Plain-Language Definition**

Stem cell therapies for cartilage repair use cells with the ability to self-renew and differentiate into specialized cartilage cells (chondrocytes). Two fundamentally different types of stem cells are under development:

**Mesenchymal Stem Cells (MSCs)**: Adult stem cells found in bone marrow, adipose tissue (fat), synovial membrane (joint lining), and umbilical cord blood. They can be isolated from the patient (autologous) or a donor (allogeneic), expanded in the laboratory, and delivered into the joint by injection or surgical implantation. MSCs can differentiate into cartilage, bone, and fat cells, and also release anti-inflammatory molecules (paracrine effects) that may suppress the inflammatory environment in an arthritic joint.

**Induced Pluripotent Stem Cells (iPSCs)**: Adult cells (commonly skin or blood cells) reprogrammed to an embryonic-like stem cell state by introduction of specific transcription factors (Yamanaka factors: Oct4, Sox2, Klf4, c-Myc). iPSCs can then be directed to differentiate into chondrocytes. Because iPSCs can be derived from any donor and expanded almost indefinitely, they offer the possibility of an unlimited supply of off-the-shelf chondrocytes — the key limitation of autologous ACI/MACI approaches.

**Why It Matters Now**

- MSC autologous approaches (particularly adipose-derived MSC — ADSC — therapy) are the furthest advanced, with Nature Cell's JointStem (autologous ADSC injection) receiving FDA Breakthrough Therapy Designation in March 2025, following RMAT designation in October 2023. Three-year clinical data from Korean trials demonstrates sustained pain relief and cartilage regeneration.
- MSC approaches address OA broadly — not just focal defects — dramatically expanding the addressable patient population beyond MACI's focal defect indication.
- iPSC research reached large animal validation in 2025, with the first miniature pig study comparing iPSC-derived chondrocyte implants head-to-head versus MSC-derived implants published in Stem Cell Research and Therapy.

**Key Terminology Glossary**

- **Mesenchymal Stem Cell (MSC)**: An adult multipotent stem cell found primarily in bone marrow and fat tissue. Multipotent means it can become several (but not all) cell types — specifically cartilage, bone, and fat. Also called mesenchymal stromal cells in some literature, acknowledging the debate about true "stemness."
- **Adipose-Derived Stem Cell (ADSC)**: MSC sourced from adipose (fat) tissue via lipoaspiration — a less invasive harvest procedure than bone marrow aspiration.
- **Bone Marrow Aspirate Concentrate (BMAC)**: Concentrated bone marrow containing MSCs and other growth factors, used as an autologous biologic treatment via injection or combined with scaffolds.
- **Induced Pluripotent Stem Cell (iPSC)**: An adult cell reprogrammed to a pluripotent state (capable of becoming any cell type in the body) using the Yamanaka transcription factors. First demonstrated by Shinya Yamanaka (Kyoto University) in 2006, earning the 2012 Nobel Prize in Physiology or Medicine.
- **Chondrogenesis**: The biological process by which stem cells differentiate into chondrocytes and produce cartilage extracellular matrix (collagen Type II, aggrecan).
- **Paracrine effect**: The secretion of signaling molecules by MSCs that influence nearby cells — suppressing inflammation, reducing cell death, stimulating resident stem cells — without the MSCs themselves becoming permanent cartilage.
- **Hypertrophic chondrocyte**: A chondrocyte that has undergone undesirable terminal differentiation toward bone-forming phenotype, producing Type X collagen and alkaline phosphatase — a known risk in some MSC and iPSC chondrogenesis protocols.
- **DMOAD (Disease-Modifying Osteoarthritis Drug)**: A therapy that demonstrably slows or reverses the progression of osteoarthritis at the tissue level (not just pain relief). No therapy has yet received this regulatory designation in the US.
- **RMAT (Regenerative Medicine Advanced Therapy) designation**: An FDA designation for cell and gene therapies that show preliminary clinical evidence of treating serious conditions — provides expedited development and review programs.
- **Breakthrough Therapy Designation (BTD)**: FDA designation for drugs/biologics that show substantial improvement over available therapies in treating serious conditions — enables intensive FDA guidance during development.

---

## 2. Technical Mechanism

**MSC Autologous Approach (Adipose MSC Example — JointStem)**

1. Lipoaspiration: 50–100 mL of adipose tissue harvested from the patient (minor procedure).
2. Cell isolation and GMP expansion: ADSCs isolated and expanded in validated GMP bioreactor over 2–4 weeks to therapeutic doses (~100–200 million cells per injection).
3. Intra-articular injection: Cells suspended in saline or hyaluronic acid vehicle, injected directly into the knee joint in a single procedure.
4. Mechanism of action: Injected MSCs primarily act through paracrine signaling rather than direct engraftment and differentiation. They release anti-inflammatory cytokines (IL-10, TGF-beta-3), suppress synovial inflammation, reduce cartilage-degrading enzyme activity (MMPs, ADAMTS), and stimulate resident chondrocytes and progenitor cells to produce matrix. Some direct differentiation into chondrocytes at the defect site occurs but is not the primary mechanism.
5. Clinical outcomes: Sustained pain relief, improved function scores (KOOS, VAS), and MRI evidence of cartilage thickness preservation up to 3 years (JointStem Phase 3 data, Korea).

**MSC Allogeneic Approach**

Off-the-shelf MSC products use donor-derived MSCs cryopreserved in vials, thawed and injected at point of care. Manufacturing leverages a master cell bank from a single donor lot — dramatically improving scalability and cost versus autologous approaches. The immunomodulatory and paracrine mechanisms are similar to autologous MSC, but allogeneic MSCs may trigger immune recognition over time. Key companies: Medipost (CARTISTEM — allogeneic umbilical cord blood MSC, approved in Korea), various companies in Phase 2 globally.

**iPSC-Derived Chondrocyte Approach**

1. Cell reprogramming: Patient or donor somatic cells (skin fibroblasts, blood cells) transduced with Yamanaka factors (typically via Sendai virus vectors, which are non-integrating) to generate iPSC colonies.
2. Quality control and banking: iPSC lines are banked, karyotyped, and tested for pluripotency markers (OCT4, NANOG, SSEA-4).
3. Directed chondrogenesis: iPSCs are cultured through a sequential protocol mimicking embryonic cartilage development — mesoderm induction (BMP4, Activin A), then chondroprogenitor induction (TGF-beta-3, GDF-5), then chondrocyte maturation (ascorbic acid, insulin, dexamethasone) — over 21–42 days in 3D pellet or hydrogel systems.
4. Construct formation: Resulting chondrocytes are embedded in a scaffold (collagen, GelMA, fibrin) for implantation.
5. Critical challenge: Preventing hypertrophic differentiation (iPSC-derived chondrocytes have a tendency to upregulate Type X collagen and calcify) — an active area of research; multiple groups have developed protocols using TGF-beta signaling suppression and parathyroid hormone-related peptide (PTHrP) during the maturation phase.

**Key Performance Parameters (MSC)**

- Cell dose: 10–200 million MSCs per injection (dose-dependent outcomes observed)
- Injection volume: 2–5 mL intra-articular
- Clinical response rate: 60–80% reporting improved pain scores at 1 year (meta-analysis of MSC trials)
- Cartilage volume change: JointStem data shows cartilage preservation vs. control at 3 years by quantitative MRI

**Key Performance Parameters (iPSC-Chondrocyte)**

- Chondrogenic differentiation efficiency: >80% SOX9+ chondrocyte yield with optimized protocols (2025 publications)
- Type II collagen and aggrecan production comparable to primary chondrocytes in optimized 3D culture
- Mechanical properties of engineered constructs: approaching but not yet meeting native cartilage compressive modulus (0.5–1.5 MPa range)

---

## 3. Historical Evolution

| Year | Event | Source |
|------|-------|--------|
| 1966 | Friedenstein first identifies bone marrow stromal cells with osteogenic capacity — founding observation of MSC biology | [Referenced in MSC review literature] |
| 1991 | Caplan coins term "mesenchymal stem cells" and proposes their multipotent differentiation capacity | [Referenced widely in MSC field reviews] |
| 2006 | Yamanaka and Takahashi demonstrate iPSC reprogramming from mouse fibroblasts — Nobel Prize 2012 | [Referenced in iPSC clinical trial review, Cell Stem Cell 2025](https://www.cell.com/cell-stem-cell/fulltext/S1934-5909(24)00445-4) |
| 2007 | Yamanaka group demonstrates iPSC from human fibroblasts — opens human therapeutic pathway | [Cell Stem Cell 2025](https://www.cell.com/cell-stem-cell/fulltext/S1934-5909(24)00445-4) |
| 2012 | CARTISTEM (allogeneic umbilical cord blood MSC, Medipost) approved in South Korea — first regulatory approval of allogeneic MSC for cartilage repair | [PMC: Cell therapy for cartilage repair](https://pmc.ncbi.nlm.nih.gov/articles/PMC8589441/) |
| 2017 | Japanese clinical trial demonstrates MSC synovial injection slows cartilage loss in knee OA — published data | [PMC: Advances in cartilage TE (2024)](https://pmc.ncbi.nlm.nih.gov/articles/PMC11464958/) |
| 2022 | NovaBay/Orthox: UK silk-based artificial cartilage implant raises ~USD 12.5M for clinical trials | [ORTHOWORLD: Orthopedic Startups 2024] |
| 2023 | Nature Cell JointStem receives FDA RMAT designation (October 2023) | [hitnews.co.kr: JointStem RMAT](http://www.hitnews.co.kr/news/articleView.html?idxno=58635) |
| 2025 | First miniature pig study comparing iPSC vs. MSC chondrocyte implants published — iPSC superior for hyaline cartilage regeneration | [Springer: iPSC + MSC miniature pig (2025)](https://link.springer.com/article/10.1186/s13287-025-04215-7) |
| 2025 | Long-term iPSC-derived cartilage evaluation (52 weeks) published in NPJ Regenerative Medicine | [NPJ: iPSC cartilage long-term (2025)](https://www.nature.com/articles/s41536-025-00447-6) |
| March 2025 | Nature Cell JointStem receives FDA Breakthrough Therapy Designation — first Korean cell therapy to do so | [AccessNewswire: Nature Cell BTD (2025)](https://www.accessnewswire.com/newsroom/en/biotechnology/nature-cells-jointstem-becomes-the-first-korean-company-to-acquire-breakthrough-thera-1003919) |
| 2025 | Cell Stem Cell publishes 2025 update on PSC-derived therapies: 115 trials, 83 hPSC products, >1,200 patients dosed, no generalizable safety concerns | [Cell Stem Cell: 2025 update](https://www.cell.com/cell-stem-cell/fulltext/S1934-5909(24)00445-4) |

---

## 4. Academic Research Landscape

**Seminal Papers**

1. **Takahashi K & Yamanaka S (2006).** "Induction of Pluripotent Stem Cells from Mouse Embryonic and Adult Fibroblast Cultures by Defined Factors." Cell 126(4):663–676. The founding iPSC paper — demonstrated cellular reprogramming with four transcription factors. Nobel Prize 2012. Foundational to all iPSC-derived cell therapy. Citation count: >25,000. Not directly a cartilage paper but essential foundation.

2. **Pittenger MF et al. (1999).** "Multilineage Potential of Adult Human Mesenchymal Stem Cells." Science 284(5411):143–147. Established the multipotent differentiation capacity of adult bone marrow MSCs including chondrogenic differentiation. Citations: >18,000. The foundational MSC paper.

3. **Caplan AI (2017).** "Mesenchymal Stem Cells: Time to Change the Name!" Stem Cells Translational Medicine 6(6):1445–1451. Proposes re-naming MSCs as "Medicinal Signaling Cells" to reflect that paracrine effects, not differentiation, are primary mechanism. Reframed the therapeutic understanding of MSC biology. URL: [PMC: Cell therapy for cartilage repair](https://pmc.ncbi.nlm.nih.gov/articles/PMC8589441/)

4. **Nguyen D et al. (2025).** "Long-term evaluation of human iPSC-derived cartilage for repairing chondral defects." npj Regenerative Medicine. The most recent landmark publication demonstrating 52-week durability of iPSC-derived cartilage constructs in animal models. URL: [NPJ Regenerative Medicine (2025)](https://www.nature.com/articles/s41536-025-00447-6)

5. **Pluripotent stem-cell-derived therapies in clinical trial: A 2025 update.** Cell Stem Cell 2025. Comprehensive survey of all PSC clinical programs globally: 115 trials, 83 products, >1,200 patients — provides the most current evidence base for iPSC safety across all indications. URL: [Cell Stem Cell 2025](https://www.cell.com/cell-stem-cell/fulltext/S1934-5909(24)00445-4)

**Company-Affiliated Research**

- **Nature Cell (Korea)**: Phase 3 clinical trials data for JointStem published in Korean medical journals. Three-year follow-up studies forming basis of BTD application. Company publishes outcomes data through clinical trial registries and partner institutions.
- **Medipost (Korea)**: Phase 2 clinical data for CARTISTEM in Korean journals; ongoing Phase 1/2 global expansion data.
- **MIT SMART Centre (Singapore)**: Published research in October 2024 demonstrating that ascorbic acid supplementation during MSC expansion enhances chondrogenic potential — directly applicable to MACI and MSC manufacturing. Source: [MIT News: MSC cartilage enhancement (October 2024)](https://news.mit.edu/2024/smart-researchers-method-enhance-effectiveness-msc-therapy-cartilage-repair-1024)

**Research Frontier (2024–2025)**

1. **iPSC hypertrophy prevention**: Suppressing Type X collagen upregulation in iPSC-derived chondrocytes using PTHrP, TGF-beta pathway modulation. Multiple groups published protocols in 2024–2025.
2. **Chondrogenic differentiation efficiency improvement**: CRISPR gene activation of SOX9 (master chondrogenic transcription factor) showing 4.8-fold increase in aggrecan expression — direct enhancement of chondrogenic output. Source: [PMC: Recent advancements in cartilage TE (2024)](https://pmc.ncbi.nlm.nih.gov/articles/PMC11524031/)
3. **Allogeneic iPSC cell banking**: HLA-matched iPSC banks (Kyoto University, RIKEN, UK Stem Cell Bank) to minimize immune rejection risk for allogeneic applications.
4. **MSC secretome / conditioned medium**: Using MSC-conditioned culture media (containing growth factors, exosomes) rather than cells — a bridge toward cell-free approaches.

**Key Researchers**

1. **Farshid Guilak, PhD** — Washington University in St. Louis. H-index: >100. Leader in cartilage mechanobiology and stem cell engineering for cartilage repair. His lab pioneered 3D woven scaffolds and demonstrated unlimited iPSC-derived chondrocyte production in mouse models. Profile: [Google Scholar](https://scholar.google.com/citations?user=CWj6pVcAAAAJ&hl=en)

2. **Shinya Yamanaka, MD, PhD** — Kyoto University / Gladstone Institutes. Nobel Laureate 2012. Pioneer of iPSC reprogramming. His foundational patents on iPSC technology are held by Kyoto University and licensed broadly. Holds relevance to any iPSC-derived cell therapy for cartilage.

3. **Rocky Tuan, PhD** — University of Hong Kong / formerly University of Pittsburgh. Pioneer in MSC chondrogenesis and cartilage tissue engineering. Extensive publication record spanning both ACI enhancement and stem cell-based repair.

4. **Arnold Caplan, PhD** — Case Western Reserve University. Pioneer of MSC biology; proposed the paracrine/secretome theory of MSC action now dominant in the field. h-index >100.

---

## 5. Patent Landscape

**MSC Patents**

- Core MSC isolation and expansion patents were filed by Osiris Therapeutics (acquired by Smith+Nephew, then divested) in the 1990s–2000s. Many of these foundational patents have expired or are approaching expiry, opening the field to new entrants.
- **Nature Cell**: Holds patents on autologous adipose MSC isolation protocols and GMP manufacturing methods for JointStem; specific patent family details in Korean patent database (KIPRIS).
- **Medipost**: Holds patents on umbilical cord blood MSC isolation, cryopreservation, and intra-articular delivery; CARTISTEM patents include cell characterization methods.
- **Celgene/BMS (via Cellular Dynamics)**: Holds patents on GMP-grade iPSC manufacturing processes (reprogram, characterize, bank).
- **Kyoto University**: Holds foundational Yamanaka factor reprogramming patents (licensed broadly via IP licensing agreements for non-commercial and commercial use).

**FTO Considerations**

- Autologous MSC (harvest, expand, re-inject) approaches: relatively open field given expiry of early MSC patents. Key IP differentiators now relate to specific cell source (adipose vs. bone marrow), expansion protocol, and delivery formulation.
- Allogeneic MSC: IP landscape more active — manufacturers are filing manufacturing process patents, cell characterization methods, and potency assays.
- iPSC: Foundational Yamanaka IP managed by Kyoto University; commercial licenses required. Method patents on directed chondrogenesis are being filed by academic groups and corporate labs (Fujifilm subsidiary Cellular Dynamics, BlueRock Therapeutics).

**Filing Trend:** Accelerating. The number of iPSC-related patent filings in the musculoskeletal space increased significantly 2020–2025 as preclinical results matured. Companies combining iPSC with biomaterial delivery are filing the most active patent families.

---

## 6. Technology Readiness and Commercialization

**MSC Autologous (JointStem, autologous adipose MSC)**
- TRL: 7–8 — Phase 3 completed in Korea; FDA BTD designation received; US Phase 3 planning underway.
- Commercial: Approved in South Korea. US approval path requires full FDA Phase 3 RCT.
- Regulatory: FDA BTD March 2025; RMAT October 2023. US BLA submission anticipated after US Phase 3.
- Cost: [REASONED INFERENCE] Autologous adipose MSC procedure estimated at USD 15,000–25,000 per patient including lipoaspiration and cell manufacturing — similar order of magnitude to MACI.

**MSC Allogeneic (CARTISTEM, others)**
- TRL: 6–7 in Korea (approved); TRL 5–6 in US/EU (Phase 2 ongoing).
- Commercial: CARTISTEM commercially available in South Korea. No FDA/EMA approved allogeneic MSC for cartilage as of February 2026.
- Regulatory: No FDA/EMA approval. Multiple Phase 1/2 trials ongoing globally.
- Manufacturing advantage: Master cell bank approach enables batch production at lower per-dose cost than autologous — potentially USD 5,000–10,000 per dose at commercial scale.

**iPSC-Derived Chondrocytes**
- TRL: 3–5. Large animal validation achieved (2025 miniature pig studies). No IND applications filed as of February 2026 for cartilage-specific iPSC product. IND filing expected 2027–2030 range from leading academic groups.
- Commercial: Pre-commercial. No approved products globally.
- Regulatory: FDA has established pathways for iPSC-derived cellular products under 21 CFR Part 1271 (HCT/P) or BLA pathway depending on manufacturing and manipulation.
- Safety concern: Tumorigenicity risk from residual undifferentiated iPSCs is the primary regulatory safety hurdle; manufacturing quality controls and finished product testing must demonstrate absence of undifferentiated cells.

---

## 7. Competitive Technology Comparison

| Technology | Mechanism | Defect Type | Stage | Key Advantage | Key Risk |
|---|---|---|---|---|---|
| MSC Autologous (JointStem) | Paracrine + some differentiation | OA (diffuse); focal | TRL 7–8 | Treats OA broadly; strong Phase 3 data; BTD | Two-stage (harvest + inject); patient-specific |
| MSC Allogeneic (CARTISTEM) | Paracrine + differentiation | OA; focal | TRL 5–7 | Off-the-shelf; lower cost potential | No FDA/EMA approval; immune recognition over time |
| iPSC-Chondrocyte | Direct hyaline chondrocyte replacement | Focal defect | TRL 3–5 | Unlimited scalable supply; hyaline cartilage quality | No clinical data; tumorigenicity risk; long timeline |
| MACI (autologous ACI) | Direct chondrocyte engraftment | Focal defect (1–10 cm²) | TRL 9 | FDA approved; strong 10-year data | Two-stage; focal only; expensive |
| PRP | Growth factor delivery | OA adjunct | TRL 9 | Low cost; simple; widely available | Modest effect size; not curative |

---

## 8. Future Outlook

**Near-Term (2025–2027)**

- JointStem US Phase 3 design submission to FDA following BTD guidance meetings (2025–2026). US Phase 3 IND/trial launch anticipated 2026.
- Publication of Kolon TG-C 2-year Phase 3 follow-up data (gene + cell approach) — comparative context for pure MSC approach.
- Multiple allogeneic MSC companies initiating US Phase 2 trials in OA.

**Mid-Term (2028–2032)**

- If JointStem US Phase 3 succeeds, US BLA filing and potential approval by 2029–2031.
- First iPSC-cartilage IND application filed — earliest US human trial of iPSC chondrocytes expected 2028–2030.
- [FORECAST]: Allogeneic MSC products from Korea and Japan may achieve EMA approval before FDA, serving as validation data for FDA pathway.

**Long-Term (2032–2035)**

- iPSC-derived chondrocyte products enter early Phase 1 human trials.
- Convergence of iPSC chondrocytes with bioprinted scaffolds creates third-generation cell-scaffold constructs.
- Potential for "off-the-shelf hyaline cartilage" — an allogeneic iPSC-derived chondrocyte product in a bioprinted scaffold — the ultimate therapeutic endpoint of the field.

**Bull / Base / Bear Cases**

- **Bull**: JointStem US approval by 2030; CARTISTEM or equivalent allogeneic MSC achieves FDA approval by 2032; OA indication opens a >5 million patient/year US market. Stem cell approaches replace MACI as standard of care for both focal and diffuse cartilage disease.
- **Base**: JointStem US approval delayed to 2031–2033 by FDA statistical requirements; allogeneic MSC approval in EU by 2030; iPSC enters Phase 1 by 2030. Stem cells become a meaningful market segment but do not displace MACI in focal defects by 2035.
- **Bear**: FDA requires longer-term OA disease modification data for DMOAD designation; US Phase 3 fails primary endpoint; stem cell therapies remain a niche adjunct to surgical repair; iPSC safety concerns delay IND filing to 2032+.

---

## 9. China-Specific Analysis

- China has significant academic research volume in MSC cartilage repair but limited GMP-grade clinical programs meeting FDA/EMA standards.
- Key Chinese institutions: Peking University Third Hospital (MSC clinical trials), Shanghai Ninth People's Hospital (chondrocyte tissue engineering), Zhejiang University (hydrogel-MSC combinations).
- NMPA (National Medical Products Administration) has approved CARTISTEM and some domestic cell therapy products under evolving ATMP regulations. China's 2019 Drug Administration Law reform created a new regulatory pathway for cell therapies.
- Chinese academic publications on iPSC chondrogenesis are high volume (estimated >200 papers 2022–2025) but predominantly preclinical.
- JointStem (Nature Cell, Korea) is pursuing regulatory approval across Asia including China through licensing partnerships.
- [REASONED INFERENCE]: A foreign iPSC or allogeneic MSC company with FDA approval pursuing a China licensing deal could command USD 50–150M milestone payments given the large OA patient population and limited domestic alternatives.

---

## 10. Strategic Implications

- **Highest near-term investment signal**: JointStem (Nature Cell) — BTD + RMAT + 3-year clinical data = the most de-risked stem cell approach for OA. Key risk: US Phase 3 design and statistical endpoint agreement with FDA.
- **Platform bet signal**: Companies building allogeneic MSC cell banks with GMP manufacturing — addressable beyond cartilage to other orthopedic applications (meniscus, rotator cuff, spine disc).
- **Long horizon bet**: iPSC platform companies with cartilage differentiation protocols — high upside, 2030+ commercial realization.
- **Key monitoring indicators**: (1) Nature Cell US Phase 3 IND filing timeline; (2) Kolon TG-C 2-year Phase 3 readout (2026); (3) Number of FDA RMAT/BTD designations for cell therapy approaches in cartilage; (4) iPSC IND filings for musculoskeletal indications.

---

## 11. Confidence Level

**Medium-High** overall. MSC commercial and regulatory data (Korea approvals, FDA designations) is high confidence. iPSC section is medium confidence — preclinical data is well-sourced but clinical translation timeline involves significant uncertainty. China-specific analysis is medium confidence due to limited English-language sources for domestic NMPA approvals.

---

## 12. Sources

1. [Nature: Long-term evaluation of iPSC-derived cartilage (2025)](https://www.nature.com/articles/s41536-025-00447-6)
2. [Cell Stem Cell: Pluripotent stem-cell-derived therapies — 2025 update](https://www.cell.com/cell-stem-cell/fulltext/S1934-5909(24)00445-4)
3. [Springer: Autologous iPSC and MSC-derived chondrocyte implants in miniature pig (2025)](https://link.springer.com/article/10.1186/s13287-025-04215-7)
4. [PMC: Advances in cartilage tissue regeneration — stem cell therapies (2024)](https://pmc.ncbi.nlm.nih.gov/articles/PMC11464958/)
5. [PMC: Cell therapy for cartilage repair (2021)](https://pmc.ncbi.nlm.nih.gov/articles/PMC8589441/)
6. [AccessNewswire: Nature Cell JointStem BTD — March 2025](https://www.accessnewswire.com/newsroom/en/biotechnology/nature-cells-jointstem-becomes-the-first-korean-company-to-acquire-breakthrough-thera-1003919)
7. [BioWorld: Nature Cell wins FDA BTD for JointStem](https://www.bioworld.com/articles/718522-nature-cell-wins-fda-breakthrough-designation-of-jointstem?v=preview)
8. [hitnews: JointStem RMAT designation](http://www.hitnews.co.kr/news/articleView.html?idxno=58635)
9. [PMC: Recent advancements in cartilage TE (2024)](https://pmc.ncbi.nlm.nih.gov/articles/PMC11524031/)
10. [PMC: Stem cell-based cartilage regeneration — engineering innovations and clinical translation](https://pmc.ncbi.nlm.nih.gov/articles/PMC12476812/)
11. [Nature: Mesenchymal stem cells in treating human diseases — clinical studies (2025)](https://www.nature.com/articles/s41392-025-02313-9)
12. [MIT News: New method to enhance MSC cartilage repair (October 2024)](https://news.mit.edu/2024/smart-researchers-method-enhance-effectiveness-msc-therapy-cartilage-repair-1024)
13. [Springer: Chondrogenic differentiation of stem cells — advances and future perspectives (2025)](https://link.springer.com/article/10.1007/s13770-025-00768-z)
14. [PMC: Latest advances in chondrocyte-based cartilage repair (2024)](https://pmc.ncbi.nlm.nih.gov/articles/PMC11201646/)
15. [Farshid Guilak — Google Scholar](https://scholar.google.com/citations?user=CWj6pVcAAAAJ&hl=en)
16. [Washington University in St. Louis: Guilak Lab](https://orthopaedicresearch.wustl.edu/labs/farshid-guilak/)
17. [PMC: Cartilage Repair in 2025 — Hope, Hype, or Horizon?](https://pmc.ncbi.nlm.nih.gov/articles/PMC12536974/)
