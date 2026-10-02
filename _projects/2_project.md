---
layout: page
title: "Aging-Driven Fibro-Adipogenic Progenitor Dysregulation in Inguinal Hernia"
description: "An integrative single-cell and genetic multi-omics study to identify aging-related FAP mechanisms underlying inguinal hernia susceptibility."
img: assets/img/adipo.jpg
importance: 1
category: Selected Projects
status: "Ongoing"
permalink: /projects/aging-fap-inguinal-hernia/
---

<p>
  <strong>Status:</strong> Ongoing &nbsp;·&nbsp;
  <strong>Category:</strong> Research / Multi-Omics / Single-Cell Genomics / Causal Inference &nbsp;·&nbsp;
  <strong>Includes:</strong> snRNA-seq &amp; snATAC-seq integration, FAP subpopulation analysis, SMR/HEIDI, hdWGCNA, fine-mapping (COJO, SuSiE), transcription factor and regulatory network analysis.
</p>

---

### 1. Statement of the Problem and Rationale

Inguinal hernia (IH) is a pervasive clinical condition resulting from degenerative weakness in the lower abdominal wall. Current management is exclusively surgical, an approach that treats the symptom, the anatomical defect, but fails to address the underlying molecular pathology [1–3]. The public health impact of IH is immense, placing a considerable burden on global healthcare systems as one of the most common indications for surgery worldwide. As hernias do not resolve spontaneously and tend to enlarge, surgical intervention is the only effective treatment. A major barrier to therapeutic advancement is the persistent gap in our understanding of the specific molecular mechanisms that orchestrate the underlying tissue failure. Identifying the key cellular drivers and pathogenic gene networks is the critical first step toward realizing this therapeutic opportunity [1,4,5].

The pathogenesis of IH is multifactorial, arising from a convergence of anatomical weakness, genetic predisposition, and degenerative changes in connective tissue. Among these, aging plays a crucial role [1,6,7]. Clinical data reveal a bimodal incidence of IH repairs, with a pronounced peak occurring between the ages of 70 and 80. Aging profoundly alters skeletal muscle and its associated connective tissues [1,8–10]. A hallmark of this process is the age-related decline in the number and proliferative capacity of muscle stem cells (MuSCs). This depletion disrupts the stem cell niche, fostering an environment that promotes the accumulation of fibrotic and adipose tissue, a degenerative cascade driven by a key population of interstitial progenitor cells [11].

This project centers on fibro-adipogenic progenitors (FAPs), a mesenchymal cell population within the muscle interstitium defined by high expression of markers like PDGFRα and the absence of NCAM1. In healthy tissue, FAPs are crucial for muscle regeneration and homeostasis, supporting MuSC function [12–14]. However, during aging and other pathological states, FAPs can aberrantly differentiate into fibroblasts and adipocytes, leading to two detrimental outcomes, including fibrosis, which is marked by an overproduction of extracellular matrix (ECM), and myosteatosis, defined by the abnormal deposition of fat within muscle tissue [6,7,11–14]. Beyond direct differentiation, these cells also influence the tissue microenvironment through their secretome, releasing pro-atrophic factors like IL-6 that can exacerbate muscle degeneration [11,12].

While FAPs are strongly implicated in age-related muscle decline, their specific contribution to the connective tissue failure defining IH remains uncharacterized. To dissect this uncharacterized link, this study will employ a multi-omics strategy to investigate how age-related FAP dysregulation relates to genetic susceptibility to IH.

To address the critical gap in our understanding of IH pathogenesis, this proposal outlines a targeted, multi-omics investigation. The study is strategically designed to dissect the cellular and genetic mechanisms that link aging-related changes in FAPs to an increased susceptibility to IH. By integrating cutting-edge single-cell genomics with genetically informed inference, we aim to build a comprehensive molecular model of the disease.

---

### 2. Research Objectives

1. **Objective 1: To characterize the cellular and transcriptional changes in FAPs associated with aging.**

   We will use single-nucleus RNA sequencing (snRNA-seq) and ATAC sequencing (snATAC-seq) data of human skeletal muscle samples from young and aged individuals. This will allow us to create a high-resolution map of age-related shifts in FAP subpopulations, gene expression programs, and chromatin accessibility landscapes.

2. **Objective 2: To investigate genetically supported links between gene expression and IH susceptibility.**

   Using Summary-data-based Mendelian Randomization (SMR), we will integrate gene expression data (eQTLs) from relevant tissues with large-scale genome-wide association study (GWAS) data for IH. This analysis will identify candidate genes whose genetically regulated expression is associated with IH susceptibility.

3. **Objective 3: To define the gene regulatory networks associated with IH pathogenesis.**

   We will employ high-dimensional weighted gene co-expression network analysis (hdWGCNA), transcription factor analysis, and fine-mapping at key genetic risk loci. This will enable us to elucidate the specific molecular pathways, co-expressed gene modules, and regulatory mechanisms associated with pathogenic changes in FAPs.

---

### 3. Methodological Framework

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/?.png" title="Integrated multi-omics analysis workflow" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/?.png" title="FAP and genetic integration framework" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Integrated analytical framework connecting age-related FAP alterations with genetic susceptibility to inguinal hernia.
</div>

This study will employ an innovative and robust multi-omics strategy to deliver a comprehensive view of IH pathogenesis. Our research plan integrates single-cell genomics, genetically informed inference, and advanced network biology to connect cellular changes in aging muscle to genetically driven disease risk.

Critically, our design ensures that findings are not siloed; high-resolution cellular changes identified via snRNA-seq will be directly interrogated using genetic analyses, and candidate genes emerging from these analyses will be placed into a functional context using network biology and complementary preclinical datasets.

#### 3.1 Data Sources

Our investigation will leverage a combination of publicly available, large-scale datasets. This approach maximizes statistical power and allows for cross-validation of key findings.

| Source | Description | Data Type |
|---|---|---|
| **Single-Cell Multi-Omics** | Paired snRNA-seq and snATAC-seq from young and aged human skeletal muscle (GEO: GSE268953) | Single-nucleus multi-omics |
| **IH GWAS Summary Statistics** | Data from UK Biobank (N=371,810) and FinnGen (N=207,653) | GWAS |
| **eQTL Data** | GTEx v8 summary statistics from adipose, muscle, and fibroblast tissues | eQTL |
| **Preclinical Validation Data** | Mouse IH datasets (GSE288662, GSE288663) including snRNA-seq, snATAC-seq, and spatial transcriptomics | Preclinical multi-omics |

#### 3.2 Integrated Multi-Omic Analysis Workflow

Our analytical pipeline consists of five interconnected stages designed to integrate these diverse data types into a cohesive biological narrative.

**1. Single-Cell Data Processing and Characterization**

Paired snRNA-seq and snATAC-seq data will be processed using the Seurat and Signac packages. This involves rigorous quality control, SCTransform normalization to mitigate technical variation, and Harmony integration to correct for batch effects. A weighted nearest neighbour (WNN) analysis will be used to combine both modalities for robust definition of cell populations, including distinct FAP subtypes.

**2. Differential Analysis and Trajectory Inference**

To identify age-related changes, we will perform pseudobulk differential expression analysis using edgeR and limma-voom and single-cell compositional analysis between young and aged samples. Furthermore, Monocle3 will be used for trajectory inference to map the lineage and differentiation states of FAP populations, revealing how aging alters their developmental paths.

**3. Genetically Supported Candidate Gene Identification**

We will implement Summary-data-based Mendelian Randomization (SMR) coupled with the HEIDI test. This statistical genetics approach will leverage the IH GWAS and GTEx eQTL datasets to identify genes where genetically regulated expression shows evidence of association with hernia risk and to distinguish shared genetic signals from patterns more consistent with linkage.

**4. Regulatory Network and Locus-Specific Dissection**

High-dimensional weighted gene co-expression network analysis (hdWGCNA) will be applied to the FAP single-cell data to identify modules of co-expressed genes associated with aging and disease risk. At key genetic loci, we will perform detailed fine-mapping (GCTA-COJO, SuSiE) and colocalization analyses to pinpoint candidate causal variants and their regulatory mechanisms.

**5. Complementary Preclinical Evidence**

Key findings related to gene expression patterns and regulatory activity will be cross-referenced with analyses of preclinical mouse models of IH. This step, which includes analysis of chromVAR motif activity and spatial transcriptomics, will assess the conservation and disease-context relevance of the identified mechanisms.

#### 3.3 Statistical Analysis Plan

Differential expression and compositional analyses will be performed to identify age-associated changes in FAP populations. SMR and HEIDI analyses will integrate eQTL and IH GWAS summary statistics to identify genetically supported candidate genes. Conditional and joint association analysis using GCTA-COJO, followed by fine-mapping with SuSiE and colocalization analyses, will be used to further dissect key IH-associated loci and evaluate whether molecular and genetic signals are consistent with shared underlying variants.

---

### 4. Expected Outcomes and Scientific Significance

The successful completion of this project will yield several contributions to the fields of musculoskeletal aging and hernia research:

- **Novel Cellular Atlas:** This study will generate a high-resolution cellular and transcriptional map detailing how aging impacts FAPs and other key cell types within the skeletal muscle niche relevant to hernia development.

- **Genetically Supported Candidate Genes:** By applying Mendelian Randomization and complementary genetic analyses, this research will identify genes with genetic evidence linking their regulation to IH susceptibility. These candidates can provide a foundation for future functional studies and therapeutic development.

- **Mechanistic Regulatory Insight:** The integrated network and locus-specific analyses will uncover key biological pathways, transcription factors, and gene regulatory networks associated with genetic risk for IH, providing a molecular framework for understanding the disease architecture.

---

### References

1. Rosenberg J, Baig S, Chen DC, Derikx J. Groin hernia. *Nature Reviews Disease Primers*. 2025;11(1):47. https://doi.org/10.1038/s41572-025-00631-4

2. Kingsnorth A, LeBlanc K. Hernias: inguinal and incisional. *The Lancet*. 2003;362(9395):1561–1571. https://doi.org/10.1016/S0140-6736(03)14746-0

3. Jenkins JT, O’Dwyer PJ. Inguinal hernias. *BMJ*. 2008;336(7638):269. https://www.bmj.com/content/336/7638/269.abstract

4. Ahmed WU, Patel MIA, Ng M, McVeigh J, Zondervan K, Wiberg A, Furniss D. Shared genetic architecture of hernias: A genome-wide association study with multivariable meta-analysis of multiple hernia phenotypes. *PLoS One*. 2022;17(12):e0272261.

5. Franz MG. The biology of hernia formation. *Surgical Clinics of North America*. 2008;88(1):1–15, vii.

6. You T, Zandigohar M, Potluri T, Piehl N, Coon VJ, Baker E, Kafali M, Dai Y, Stulberg JJ, Escobar DJ, Lieber RL, Zhao H, Bulun SE. Role of progesterone action in inguinal hernia formation via skeletal muscle fibrosis and atrophy. *JCI Insight*. 2025;10(14).

7. Potluri T, Taylor MJ, Stulberg JJ, Lieber RL, Zhao H, Bulun SE. An estrogen-sensitive fibroblast population drives abdominal muscle fibrosis in an inguinal hernia mouse model. *JCI Insight*. 2022;7(9).

8. Ruhl CE, Everhart JE. Risk factors for inguinal hernia among adults in the US population. *American Journal of Epidemiology*. 2007;165(10):1154–1161.

9. Quintas ML, Rodrigues CJ, Yoo JH, Rodrigues Junior AJ. Age related changes in the elastic fiber system of the interfoveolar ligament. *Revista do Hospital das Clínicas da Faculdade de Medicina de São Paulo*. 2000;55(3):83–86.

10. Öberg S, Andresen K, Rosenberg J. Etiology of Inguinal Hernias: A Comprehensive Review. *Frontiers in Surgery*. 2017;4.

11. Parker E, Hamrick MW. Role of fibro-adipogenic progenitor cells in muscle atrophy and musculoskeletal diseases. *Current Opinion in Pharmacology*. 2021;58:1–7.

12. Biferali B, Proietti D, Mozzetta C, Madaro L. Fibro–Adipogenic Progenitors Cross-Talk in Skeletal Muscle: The Social Network. *Frontiers in Physiology*. 2019;10.

13. Negroni E, Kondili M, Muraine L, Bensalah M, Butler-Browne GS, Mouly V, Bigot A, Trollet C. Muscle fibro-adipogenic progenitors from a single-cell perspective: Focus on their "virtual" secretome. *Frontiers in Cell and Developmental Biology*. 2022;10:952041.

14. Fitzgerald G, Turiel G, Gorski T, Soro-Arnaiz I, Zhang J, Casartelli NC, Masschelein E, Maffiuletti NA, Sutter R, Leunig M, Farup J, De Bock K. MME+ fibro-adipogenic progenitors are the dominant adipogenic population during fatty infiltration in human skeletal muscle. *Communications Biology*. 2023;6(1):111. https://doi.org/10.1038/s42003-023-04504-y
```
