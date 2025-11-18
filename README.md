# In Silico Design and Immunoinformatics Analysis of a Novel Multi-Epitope Vaccine Against Human Metapneumovirus (HMPV)

## 🎓 Project Information
- **Student:** Akhil V (Register Number: 24MSBI143)
- **Institution:** Garden City University, Bangalore
- **Department:** Bioinformatics, School of Life Sciences
- **Guide:** Dr. L. A. Rama Chandra Prasad (Assistant Professor)
- **Submission Date:** July 2024

---

## 📋 Abstract

Human metapneumovirus (HMPV), a member of the Pneumoviridae family, is a significant pathogen responsible for respiratory tract infections including pneumonia, asthma exacerbations, and complications in individuals with chronic obstructive pulmonary disease (COPD). **HMPV accounts for approximately 10%–12% of respiratory infections in children**, with about 5% progressing to lower respiratory infections such as pneumonia. As of now, **no licensed vaccines are available** for clinical use against HMPV.

This study employs a **computational vaccine design strategy** using immunoinformatics tools to create a multi-epitope vaccine candidate.

### Key Achievements:
- ✅ **96.92% global population coverage**
- ✅ Antigenic, non-allergenic, and non-toxic
- ✅ Favorable physicochemical properties
- ✅ Structural stability confirmed through molecular dynamics
- ✅ Strong binding affinity with immune receptors (TLR4, MHC-I, MHC-II)

---

## 🎯 Objectives

1. Design a multi-epitope vaccine against HMPV using reverse vaccinology approach
2. Identify immunogenic B-cell, CTL, and HTL epitopes from viral proteins
3. Validate vaccine construct through computational analysis
4. Assess population coverage across global ethnic groups
5. Evaluate structural stability and receptor binding potential
6. Simulate immune response using computational tools

---

## 🧬 Target Proteins Selected

Eight HMPV proteins were selected based on their critical roles in viral pathogenesis:

| Protein | UniProt ID | Role in Virus | Justification for Inclusion |
|---------|-----------|---------------|-----------------------------|
| **Phosphoprotein (P)** | Q8B9Q8 | Viral replication & immune modulation | Conserved and essential for replication; interacts with N protein and interferes with immune signaling |
| **Protein M2-2** | Q6WB97 | Regulates transcription/replication | Controls the balance between transcription and replication; potential for regulatory disruption |
| **Fusion glycoprotein F0** | Q6WB98 | Viral entry and membrane fusion | Highly conserved, immunogenic, essential for host cell attachment and syncytium formation |
| **Major Surface Glycoprotein (G)** | Q6WB94 | Attachment to host & immune evasion | Surface protein involved in host cell binding and suppressing immune response |
| **Nucleoprotein (N)** | - | RNA encapsidation | Forms ribonucleoprotein complex; essential for replication |
| **Matrix protein (M)** | - | Assembly and budding | Central role in inflammatory response and pathogenesis |
| **Small hydrophobic protein (SH)** | - | Viroporin activity | Modulates membrane permeability and fusion protein function |
| **M2-1 protein** | - | Transcription antitermination | Zinc binding activity essential for virus replication |

---

## 🔬 Methodology

### 1. Sequence Retrieval
- **Database:** UniProt (https://www.uniprot.org/)
- **Format:** FASTA format protein sequences

### 2. Epitope Prediction

#### Linear B-Lymphocyte Epitopes
- **Tool:** IEDB Analysis Resource
- **Method:** Bepipred Linear Epitope Prediction
- **Selection:** Based on antigenicity scores

#### Cytotoxic T-Lymphocyte (CTL) Epitopes
- **Tool:** IEDB Analysis Resource  
- **Target:** HLA Class I alleles
- **Method:** NetMHCpan EL 4.1
- **Selection:** Based on binding affinity and immunogenicity

#### Helper T-Lymphocyte (HTL) Epitopes
- **Tool:** IEDB Analysis Resource
- **Target:** MHC Class II alleles  
- **Method:** NetMHCIIpan 4.0
- **Selection:** Based on binding affinity

### 3. Epitope Screening & Validation

All predicted epitopes underwent rigorous screening:

| Parameter | Tool Used | Criteria |
|-----------|-----------|----------|
| **Antigenicity** | VaxiJen v2.0 | Threshold > 0.4 |
| **Allergenicity** | AllerTop 2.0 | Non-allergen |
| **Toxicity** | ToxinPred | Non-toxic |
| **IFN-γ Induction** | IFNepitope | Positive (HTL only) |
| **IL-4 Induction** | IL4Pred | Positive (HTL only) |

### 4. Population Coverage Analysis
- **Tool:** IEDB Population Coverage Tool v.2.22
- **Analysis:** Based on HLA allele distribution globally
- **Regions:** World, continents, individual countries

### 5. Multi-Epitope Vaccine Construction

**Final Selection:**
- 7 B-cell epitopes (LBL)
- 27 CTL epitopes  
- 8 HTL epitopes

**Linkers Used:**
- **EAAAK:** Connects adjuvant (CTxB) to first B-cell epitope
- **AAY:** Links B-cell epitopes together
- **KK:** Links CTL epitopes together
- **GPGPG:** Links HTL epitopes together

**Adjuvant:** Cholera toxin B subunit (CTxB, accession: P01556)
- Enhances immunogenicity
- Acts as TLR4 agonist
- Proven potential as viral adjuvant

**Additional Features:**
- 6×Histidine tag for purification
- Total construct length: 720 amino acids

### 6. Physicochemical Analysis

**Solubility Prediction:**
- **Tool:** SOLUprot 1.0
- **Threshold:** Score > 0.5 indicates soluble expression in E. coli

**Property Analysis:**
- **Tool:** ProtParam (ExPASy)
- **Parameters:** Molecular weight, pI, instability index, aliphatic index, GRAVY, half-life, extinction coefficient

### 7. Structure Prediction & Validation

**Secondary Structure:**
- **Tool:** PSIPRED
- **Output:** Alpha helices, beta strands, random coils

**3D Structure Modeling:**
- **Tool:** AlphaFold Colab
- **Method:** Deep learning-based structure prediction

**Refinement:**
- **Tool:** GalaxyRefine
- **Purpose:** Energy minimization and structural optimization

**Validation:**
- **Ramachandran Plot:** PROCHECK (SAVESv6.0)
- **Z-Score:** ProSA-web
- **Discontinuous B-cell Epitopes:** ElliPro server

### 8. Molecular Docking

**Receptors Tested:**
- **TLR4** (PDB ID: 4G8A) - Innate immunity receptor
- **MHC Class I** - CTL activation
- **MHC Class II** - HTL activation

**Docking Server:** HADDOCK 2.4
**Visualization:** UCSF Chimera
**Selection Criteria:** Lowest Z-score

### 9. Molecular Dynamics Simulation
- **Duration:** 100 nanoseconds
- **Parameters:** RMSD, RMSF, Radius of gyration, SASA
- **Purpose:** Assess structural stability over time

### 10. Immune Response Simulation
- **Tool:** C-ImmSim server (http://150.146.2.1/CIMMSIM/index.php)
- **Method:** Position-specific score matrix (PSSM) + machine learning
- **Components:** Simulates bone marrow, thymus, and lymph node

---

## 📊 Key Results

### Population Coverage Analysis

| Category | Coverage |
|----------|----------|
| **CTL epitopes alone** | 86.32% |
| **HTL epitopes alone** | 77.5% |
| **Combined (CTL + HTL)** | **96.92% 🌍** |

This exceptional global coverage ensures the vaccine would be effective across diverse ethnic populations worldwide.

### Selected Epitopes Summary

**Total: 42 epitopes selected**

#### B-cell Epitopes (7):
- NKNKCDID
- AAGINVAEQ  
- SAGADNDSSYALQDSESIN
- AEMMEEEMNQRTKINGNGSVKLT
- And 3 more...

#### CTL Epitopes (27):
- GVYGSSVIY
- ALSPGALV
- FGVIDTPCW
- KGFGILIGVY
- AIALGVAT
- IYLIINYTI
- And 22 more...

#### HTL Epitopes (8):
- GSVKLTEKAK
- VRRKGFGILIGVYGS
- AAAVTAGVAIAKTIR
- IALGVATAAAVTAGV
- LGVATAAAVTAGVAI
- And 3 more...

**All epitopes validated as:**
- ✅ Antigenic
- ✅ Immunogenic  
- ✅ Non-allergenic
- ✅ Non-toxic
- ✅ IFN-γ positive (HTL)

### Physicochemical Properties of Vaccine Construct

| Property | Value | Interpretation |
|----------|-------|----------------|
| **Number of amino acids** | 468 | Optimal size for expression |
| **Molecular weight** | 46.85 kDa | Suitable for vaccine development |
| **Theoretical pI** | 9.44 | Basic protein |
| **Negatively charged residues** | 31 (Asp + Glu) | Stable charge distribution |
| **Positively charged residues** | 51 (Arg + Lys) | Net positive charge |
| **Instability index** | 25.55 | **Stable** (< 40) |
| **Aliphatic index** | 85.90 | Highly thermostable |
| **GRAVY** | 0.009 | Hydrophilic (good solubility) |
| **Estimated half-life** | 30 hours | Long-lasting in mammalian cells |
| **Extinction coefficient** | 37,290 M⁻¹cm⁻¹ | Good for quantification |
| **Solubility score** | 0.812 | **Highly soluble** (> 0.5) |

### Secondary Structure Composition

- **α-Helices:** 224 amino acids (31.11%)
- **β-Strands:** 169 amino acids (23.47%)
- **Random Coils:** 327 amino acids (45.41%)

Balanced secondary structure indicates proper folding and stability.

### 3D Structure Validation

#### Ramachandran Plot Analysis:
- **Most favored regions:** 94.5%
- **Additionally allowed regions:** 5.5%
- **Generously allowed regions:** 0%
- **Disallowed regions:** 0%

✅ **Excellent model quality** - over 90% residues in favored region

#### ProSA Z-Score:
- **Z-score:** -3.0
- Indicates good overall model quality
- Within range of native protein structures

#### Discontinuous B-cell Epitopes:
- **Total predicted:** 14 epitopes
- **Residue range:** 6 to 39 residues
- **Prediction scores:** 0.552 to 0.692

### Molecular Docking Results

#### Vaccine-TLR4 Complex:
- **HADDOCK Score:** -183.2 ± 41.6
- **Cluster Size:** 14 structures
- **Interpretation:** Strong binding affinity; will trigger innate immune response

#### Vaccine-MHC Class I Complex:
- **HADDOCK Score:** -186.4 ± 11.5  
- **Cluster Size:** 5 structures
- **Interpretation:** Effective CTL epitope presentation

#### Vaccine-MHC Class II Complex:
- **HADDOCK Score:** -190.1 ± 16.9
- **Cluster Size:** 10 structures  
- **Interpretation:** Excellent HTL epitope presentation

✅ All three complexes show strong, stable binding interactions

### Molecular Dynamics Simulation (100 ns)

#### RMSD Analysis:
- Initial equilibration period: 0-20 ns
- Stable RMSD: 2.3-2.4 Å (after 20 ns)
- **Conclusion:** Minimal conformational drift; good structural stability

#### Radius of Gyration:
- Initial: 4.4 Å
- Final stable: ~3.3 Å  
- **Conclusion:** Structural compaction; optimization of intramolecular interactions

#### Solvent Accessible Surface Area (SASA):
- Initial: ~750 Ų
- Final stable: ~500 Ų
- **Conclusion:** Improved hydrophobic core formation; enhanced folding stability

#### RMSF Analysis:
- Baseline fluctuations: 0.2-0.4 Å (most residues)
- Peak fluctuations: up to 3.5 Å (residues 800-1000)
- **Interpretation:** Overall stability with flexible loops at binding interfaces

✅ **Vaccine-TLR4 complex is structurally stable** and suitable for further analysis

### Immune Response Simulation

The C-ImmSim server predicted robust immune responses:

#### Antibody Response:
- **IgM:** Rapid increase in primary response
- **IgG:** Strong secondary response (memory formation)
- **IgG1 + IgG2:** Sustained high levels
- **IgA (mucosal):** Gradual elevation (important for respiratory infections)

#### Cellular Response:
- **B-cell activation:** Steady increase in active B cells and plasma cells
- **T-helper cells:** Significant expansion of CD4+ T cells
- **Cytotoxic T cells:** Robust CD8+ T cell activation
- **Memory cells:** Long-term memory B and T cell formation

#### Antigen Presenting Cells:
- **Dendritic cells:** Elevated levels indicating competent antigen presentation
- **Macrophages:** Increased activation showing innate immune engagement

#### Cytokine Profile:
- **IFN-γ:** Strong production (antiviral immunity)
- **IL-2:** T cell proliferation
- **IL-10:** Immunoregulation (prevents excessive inflammation)
- **IL-23:** Th17 response
- **IFN-β:** Type I interferon response

✅ The vaccine is predicted to generate **comprehensive immune memory** and both humoral and cellular immunity

---

## 📚 Tools & Databases

### Sequence & Database Resources
| Tool/Database | Purpose | URL |
|---------------|---------|-----|
| UniProt | Protein sequence retrieval | https://www.uniprot.org/ |
| NCBI | Additional sequence data | https://www.ncbi.nlm.nih.gov/ |

### Epitope Prediction
| Tool | Purpose |
|------|---------|
| IEDB Analysis Resource | B-cell, CTL, HTL epitope prediction |
| VaxiJen v2.0 | Antigenicity prediction |
| AllerTop 2.0 | Allergenicity assessment |
| ToxinPred | Toxicity prediction |
| IFNepitope | IFN-γ inducing epitope prediction |
| IL4Pred | IL-4 inducing epitope prediction |

### Population & Physicochemical Analysis
| Tool | Purpose |
|------|----------|
| IEDB Population Coverage | HLA allele distribution analysis |
| ProtParam (ExPASy) | Physicochemical properties |
| SOLUprot | Solubility prediction |

### Structure Prediction & Validation
| Tool | Purpose |
|------|----------|
| PSIPRED | Secondary structure prediction |
| AlphaFold | 3D structure modeling |
| GalaxyRefine | Structure refinement |
| PROCHECK/SAVESv6.0 | Ramachandran plot validation |
| ProSA-web | Z-score calculation |
| ElliPro | Discontinuous B-cell epitope prediction |

### Molecular Interaction Analysis
| Tool | Purpose |
|------|----------|
| HADDOCK 2.4 | Protein-protein docking |
| UCSF Chimera | Molecular visualization |
| C-ImmSim | Immune response simulation |

---

## 💡 Discussion

### Why Reverse Vaccinology?

Traditional vaccine development is:
- ⏱️ Time-consuming (10-15 years)
- 💰 Expensive (billions of dollars)
- 🦠 Requires pathogen cultivation
- ⚠️ Safety concerns with live/attenuated vaccines

**Reverse vaccinology advantages:**
- ⚡ Rapid design (months vs years)
- 💻 Computational screening
- 🎯 Targeted epitope selection
- 🔒 Enhanced safety (no live pathogen)
- 🌐 Population coverage analysis
- 💵 Cost-effective

### Multi-Epitope Vaccine Benefits

1. **High Specificity:** Targets only immunogenic regions
2. **Safety:** No risk of reversion to virulence
3. **Broad Coverage:** Multiple epitopes = wider population coverage
4. **Dual Immunity:** Activates both humoral and cellular responses
5. **Stability:** Better than whole protein vaccines
6. **Cost-Effective:** Lower production costs

### Key Scientific Contributions

1. **First comprehensive computational vaccine design for HMPV** using all major structural proteins

2. **Exceptional population coverage (96.92%)** - among the highest reported for any respiratory virus vaccine

3. **Rigorous validation** through multiple computational approaches:
   - Antigenicity, allergenicity, toxicity screening
   - Structural validation (Ramachandran, Z-score)
   - Molecular dynamics (100 ns simulation)
   - Immune simulation (C-ImmSim)

4. **Novel combination** of epitopes with proven adjuvant (CTxB)

5. **Ready for experimental validation** - complete characterization provided

### HMPV: The Clinical Challenge

**Epidemiological Impact:**
- 10-12% of respiratory infections in children
- 5% progress to severe lower respiratory infections
- Majority of population exposed by age 5
- Reinfection possible throughout life
- High risk groups: elderly, immunocompromised, COPD patients

**Current Status:**
- ❌ No licensed vaccines available
- ❌ No specific antiviral treatments
- 💉 Only supportive care available

**Our Solution:**
- ✅ Computationally designed multi-epitope vaccine
- ✅ Targets conserved viral proteins
- ✅ Predicted to be safe and effective
- ✅ Ready for experimental validation

### Vaccine Safety Considerations

**Autoimmunity Risk Assessment:**
- BLASTp analysis against human proteome performed
- No significant similarity to human proteins
- Non-allergenic profile confirmed
- Non-toxic nature validated

**Immunogenicity Enhancement:**
- CTxB adjuvant proven safe in clinical studies
- Appropriate linkers prevent epitope interference
- Balanced epitope distribution

---

## 🎯 Conclusions

### Primary Findings:

1. ✅ **Successfully designed** a novel multi-epitope vaccine against HMPV using immunoinformatics

2. ✅ **Selected 42 high-quality epitopes** (7 B-cell + 27 CTL + 8 HTL) from 8 viral proteins

3. ✅ **Achieved 96.92% global population coverage** - suitable for worldwide deployment

4. ✅ **Favorable physicochemical properties:**
   - Stable (instability index: 25.55)
   - Thermostable (aliphatic index: 85.90)
   - Soluble (score: 0.812)
   - Optimal molecular weight (46.85 kDa)

5. ✅ **Excellent structural quality:**
   - 94.5% residues in favored Ramachandran region
   - Z-score: -3.0 (good quality)
   - Stable over 100 ns MD simulation

6. ✅ **Strong receptor binding:**
   - TLR4: -183.2 ± 41.6
   - MHC-I: -186.4 ± 11.5
   - MHC-II: -190.1 ± 16.9

7. ✅ **Robust predicted immune response:**
   - Both humoral and cellular immunity
   - Memory formation
   - Appropriate cytokine profile

### Scientific Significance:

This study demonstrates that **computational vaccine design** is a viable, efficient approach for developing vaccines against emerging respiratory pathogens. The methodology can be applied to other viruses lacking vaccines.

### Limitations:

1. **Computational study only** - experimental validation required
2. **In vitro testing needed** - protein expression, immunogenicity assays
3. **Animal studies required** - safety and efficacy testing
4. **Clinical trials necessary** - before human use
5. **Long-term immunity unknown** - requires longitudinal studies

### Recommendations:

The designed vaccine shows excellent potential and should proceed to:
1. 🧪 **Experimental synthesis**
2. 🔬 **In vitro validation**
3. 🐁 **Animal model testing**
4. 👨‍⚕️ **Clinical trials** (if successful)

---

## 🔮 Future Scope

### Immediate Next Steps (In Silico):

1. **Codon Optimization**
   - Optimize for E. coli expression system
   - Calculate CAI (Codon Adaptation Index)
   - Avoid rare codons

2. **In Silico Cloning**
   - Clone into pET-28a(+) vector
   - Design primers
   - Verify restriction sites

3. **Expression Prediction**
   - Predict expression levels
   - Identify potential bottlenecks

### Laboratory Validation (Short-term):

1. **Gene Synthesis & Cloning**
   - Synthesize optimized gene
   - Clone into expression vector
   - Transform into E. coli BL21(DE3)

2. **Protein Expression**
   - IPTG induction
   - Optimization of expression conditions
   - SDS-PAGE analysis

3. **Protein Purification**
   - Ni-NTA affinity chromatography (using His-tag)
   - Size exclusion chromatography
   - Western blot confirmation

4. **Biophysical Characterization**
   - CD spectroscopy (secondary structure)
   - DLS (size distribution)
   - Thermal stability analysis

### Preclinical Studies (Medium-term):

1. **In Vitro Immunogenicity**
   - PBMC stimulation assays
   - Cytokine profiling (ELISA)
   - T-cell proliferation assays
   - B-cell activation assays

2. **Animal Model Studies**
   - Mouse immunization (BALB/c)
   - Antibody titer measurement
   - T-cell response evaluation
   - Challenge studies with HMPV
   - Toxicity and safety assessment

3. **Efficacy Testing**
   - Viral load reduction
   - Symptom scoring
   - Histopathology
   - Long-term immunity assessment

### Clinical Development (Long-term):

1. **Phase I Clinical Trials**
   - Safety in healthy volunteers
   - Dose escalation studies
   - Adverse event monitoring

2. **Phase II Clinical Trials**
   - Immunogenicity in target population
   - Optimal dosing regimen
   - Preliminary efficacy

3. **Phase III Clinical Trials**
   - Large-scale efficacy studies
   - Different age groups
   - High-risk populations

4. **Regulatory Approval**
   - FDA/EMA submission
   - Manufacturing scale-up
   - Quality control protocols

5. **Post-Market Surveillance**
   - Adverse event reporting
   - Real-world effectiveness
   - Long-term safety monitoring

### Additional Considerations:

- **Formulation Development:** Suitable adjuvant selection, delivery system optimization
- **Cold Chain Requirements:** Temperature stability studies, storage protocols
- **Dosage Optimization:** Single vs multiple doses, booster requirements
- **Target Populations:** Children < 5 years, elderly, immunocompromised, COPD patients
- **Manufacturing:** GMP facility requirements, scale-up strategies

---

## 👨‍🎓 Acknowledgments

This project would not have been possible without the support and guidance of:

### Academic Guidance:
- **Dr. L. A. Rama Chandra Prasad** (Project Guide, Assistant Professor) - For his invaluable guidance, insights, and continuous support throughout the project
- **Dr. Preethi Rajesh** (Head of Department, Life Sciences) - For providing the opportunity and resources
- **Garden City University Faculty** - For their academic support and expert knowledge

### Institutional Support:
- **Dr. Joseph V.G.** (Chancellor, Garden City University)
- **Prof. G R Naik** (Vice Chancellor)
- **Professor Sheeja MS** (Registrar)
- **Professor Sibi Shaji** (Controller of Examinations)

### Personal:
- **Family and Friends** - For their unwavering support and encouragement
- **Batch Mates** - For collaboration and discussions

### Tools & Resources:
- Open-source bioinformatics community
- IEDB, UniProt, NCBI databases
- All software developers who made this research possible

---

## 📚 Key References

### HMPV Discovery & Epidemiology:
1. van den Hoogen BG et al. (2001). A newly discovered human pneumovirus. *Nat Med* 7(6):719-24.
2. Hermos CR et al. (2010). Human metapneumovirus. *Clin Lab Med* 30(1):131-48.
3. Matsuzaki Y et al. (2013). Human metapneumovirus infection among family members. *Epidemiol Infect* 141(4):827-32.

### Virus Biology:
4. Rima B et al. (2017). ICTV Virus Taxonomy Profile: Pneumoviridae. *J Gen Virol* 98(12):2912-2913.
5. van den Hoogen BG et al. (2002). Analysis of the genomic sequence of human metapneumovirus. *Virology* 295(1):119-32.
6. Uche IK & Guerrero-Plata A (2018). Interferon-Mediated Response to HMPV. *Viruses* 10(9):505.

### Vaccine Development:
7. Ren J et al. (2015). Recent vaccine development for human metapneumovirus. *J Gen Virol* 96(7):1515-20.
8. Ogonczyk-Makowska D et al. (2024). Mucosal bivalent live attenuated vaccine. *npj Vaccines* 9:111.
9. Ma S et al. (2023). Development of novel multi-epitope mRNA vaccine candidate. *Hum Vaccin Immunother* 19(3):2293300.

### Reverse Vaccinology:
10. Bidmos FA et al. (2018). Bacterial Vaccine Antigen Discovery in Reverse Vaccinology 2.0 Era. *Front Immunol* 9:2315.
11. Delany I et al. (2013). Vaccines, reverse vaccinology, and bacterial pathogenesis. *Cold Spring Harb Perspect Med* 3(5):a012476.
12. Zhang L (2018). Multi-epitope vaccines against tumors and viral infections. *Cell Mol Immunol* 15(2):182–4.

### Immunoinformatics:
13. Nosrati M et al. (2019). Multi-epitope recombinant vaccine against CCHF virus. *J Biomed Inform* 93:103160.
14. Sanami S et al. (2023). Universal multi-epitope vaccine against monkeypox virus. *PLoS One* 18(5):e0286224.
15. Chao P et al. (2024). Proteomics-based vaccine targets against Streptococcus gallolyticus. *Sci Rep* 14:4836.

*Complete reference list with 30 citations available in the full project report*

---

## 📊 Project Statistics

- **📄 Report Pages:** 40
- **📑 Figures:** 13
- **📊 Tables:** 3
- **🧬 Proteins Analyzed:** 8
- **🔬 Epitopes Identified:** 42 (7 B-cell + 27 CTL + 8 HTL)
- **⏱️ Project Duration:** July 2024
- **💻 Tools Used:** 15+
- **🌍 Population Coverage:** 96.92%
- **📚 References:** 30

---

## 📞 Contact Information

**Student:**
- **Name:** Akhil V
- **Register Number:** 24MSBI143
- **Program:** MSc Bioinformatics
- **Institution:** Garden City University, Bangalore - 560049
- **Department:** Bioinformatics, School of Life Sciences

**Project Guide:**
- **Name:** Dr. L. A. Rama Chandra Prasad
- **Designation:** Assistant Professor
- **Department:** Bioinformatics, School of Life Sciences
- **Institution:** Garden City University, Bangalore

---

## 📜 Repository Structure

```
HMPV-MultiEpitope-Vaccine-Design/
│
├── README.md                    # This file - Complete project documentation
├── Project_Report.pdf           # Full 40-page project report
├── data/
│   ├── protein_sequences.fasta  # HMPV protein sequences
│   ├── selected_epitopes.txt    # Final epitope list
│   └── vaccine_construct.fasta  # Final vaccine sequence
│
├── results/
│   ├── figures/                 # All figures from report
│   ├── tables/                  # All tables
│   ├── population_coverage.xlsx # Coverage analysis
│   ├── docking_results/         # Molecular docking outputs
│   └── MD_simulation/           # Molecular dynamics data
│
├── scripts/
│   ├── epitope_analysis.py      # Epitope screening scripts
│   ├── structure_validation.py  # Structural analysis
│   └── visualization.R          # Data visualization
│
└── LICENSE                      # License information
```

---

## 📝 How to Cite This Work

### APA Format:
```
Akhil, V. (2024). In Silico Design and Immunoinformatics Analysis of a Novel 
Multi-Epitope Vaccine Against Human Metapneumovirus (HMPV). [Master's thesis, 
Garden City University]. GitHub. https://github.com/Akhilv143/HMPV-MultiEpitope-Vaccine-Design
```

### BibTeX Format:
```bibtex
@mastersthesis{akhil2024hmpv,
  title={In Silico Design and Immunoinformatics Analysis of a Novel Multi-Epitope Vaccine Against Human Metapneumovirus (HMPV)},
  author={Akhil, V},
  year={2024},
  month={July},
  school={Garden City University},
  address={Bangalore, Karnataka, India},
  type={MSc Bioinformatics Minor Project},
  note={Register Number: 24MSBI143}
}
```

---

## ⚖️ License

This project was submitted in partial fulfillment of the requirements for the award of Master of Science in Bioinformatics at Garden City University, Bangalore.

**Academic Use:** This work is available for academic reference and educational purposes.

**Copyright:** © 2024 Akhil V, Garden City University. All rights reserved.

---

## ⚠️ Disclaimer

**Important Notice:**

1. This is a **computational/in silico study**.
2. **No experimental validation has been performed yet**.
3. The vaccine candidate requires:
   - In vitro validation
   - In vivo animal studies
   - Clinical trials
4. **This is not a clinically approved vaccine**.
5. **DO NOT USE** for treatment or medical purposes.
6. Experimental validation is essential before any practical application.

The predictions and results presented are based on computational analysis and should be interpreted accordingly.

---

## ⭐ Keywords & Tags

`Bioinformatics` `Vaccine Design` `HMPV` `Human Metapneumovirus` `Multi-Epitope Vaccine` `Immunoinformatics` `Reverse Vaccinology` `In Silico` `Computational Biology` `Epitope Prediction` `Molecular Docking` `Molecular Dynamics` `Population Coverage` `TLR4` `MHC-I` `MHC-II` `CTL Epitopes` `HTL Epitopes` `B-cell Epitopes` `AlphaFold` `HADDOCK` `Respiratory Virus` `Vaccine Development` `MSc Project` `Garden City University` `Bangalore`

---

## 📢 Project Status

🟢 **Status:** Computational Design Complete  
🟡 **Next Phase:** Experimental Validation (Pending)  
📅 **Last Updated:** July 2024  
🎯 **Completion:** 100% (Computational Phase)

---

## 👁️ Visitors

![Views](https://komarev.com/ghpvc/?username=Akhilv143&repo=HMPV-MultiEpitope-Vaccine-Design&color=blue&style=flat-square&label=Repository+Views)

---

## 🌟 Star This Repository

If you find this work useful for your research or studies, please consider giving it a star ⭐

---

**Built with ❤️ by Akhil V | MSc Bioinformatics | Garden City University, Bangalore**

**Project Completed:** July 2024 | **Repository Created:** November 2024

---

*"Computational vaccine design represents the future of rapid response to emerging infectious diseases."*

---

## 🔗 Quick Links

- [🏠 Garden City University](https://www.gardencityuniversity.edu.in/)
- [📋 Full Project Report](./Project_Report.pdf) *(To be uploaded)*
- [📄 Protein Sequences](./data/protein_sequences.fasta) *(To be uploaded)*
- [🧬 Vaccine Construct](./data/vaccine_construct.fasta) *(To be uploaded)*
- [📊 Results & Figures](./results/) *(To be uploaded)*

---

**End of Documentation**

*This README was comprehensively prepared based on the complete 40-page MSc Bioinformatics Minor Project Report.*
