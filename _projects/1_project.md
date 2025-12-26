---
layout: page
title: "A Bidirectional Mendelian Randomization Study on Causal Biomarkers of Multiple Sclerosis Progression"
description: "Genetic dissection of mitochondrial DNA copy number and leukocyte telomere length in multiple sclerosis progression"
img: assets/img/projects/published_mr_ms/hero.jpg
importance: 1
category: mendelian-randomization
related_publications: true
---

## A Bidirectional Mendelian Randomization Study on Causal Biomarkers of Multiple Sclerosis Progression

<p>
  <strong>Status:</strong> Published &nbsp;·&nbsp;
  <strong>Category:</strong> Mendelian Randomization / Genetic Epidemiology &nbsp;·&nbsp;
  <strong>Data:</strong> UK Biobank, IMSGC
</p>

<div class="row justify-content-sm-center">
  <div class="col-sm-10 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/projects/published_mr_ms/workflow.png" title="Bidirectional Mendelian Randomization workflow" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  Bidirectional two-sample Mendelian Randomization framework for assessing causal relationships between mtDNA-CN, leukocyte telomere length, and MS progression.
</div>

---

### 1. Statement of the Problem and Rationale
Multiple Sclerosis (MS) is a chronic inflammatory disease of the central nervous system characterized by progressive neuronal loss that primarily affects young adults (1). The pathogenesis involves the dysregulation of both adaptive and innate immune cells targeting CNS autoantigens, which drives chronic neuroinflammation and subsequent neuronal damage (2). The clinical course is variable; most patients are diagnosed with relapsing-remitting MS (RRMS), defined by episodes of acute neurological dysfunction followed by recovery. Over time, however, a majority transition to secondary progressive MS (SPMS), a stage of continuous neurodegeneration without distinct relapses. A smaller subset (~10–15%) experience primary progressive MS (PPMS), with a steady accumulation of disability from onset (3). This transition from inflammation-driven relapses to relentless neurodegeneration represents the core clinical challenge in MS and an area of urgent unmet need. Biological aging and associated cellular dysfunction are recognized as critical drivers of MS progression. Two key biomarkers of these processes are mitochondrial DNA copy number (mtDNA-CN) and leukocyte telomere length (LTL) (4–6).

mtDNA-CN is a critical indicator of cellular bioenergetic health. Mitochondria play central roles in cellular proliferation, maintaining mitochondrial membrane potential, regulating apoptosis, managing oxidative stress, storing energy, and producing adenosine triphosphate (ATP). Fluctuations in mtDNA-CN signal potential bioenergetic deficits and impaired respiratory capacity in neurons, which may directly contribute to the neuronal loss seen in MS (7–9).

Leukocyte telomere length (LTL) is a well-established biomarker of biological aging. Telomeres are nucleoprotein structures that protect the ends of chromosomes, regulating cellular senescence and maintaining genomic stability (6). Observational studies have linked shorter LTL to progressive MS forms (10), higher disability scores, and reduced brain volume (11), suggesting accelerated biological aging contributes to disease severity.

Despite these associations, prior observational research has yielded inconsistent findings and is methodologically incapable of establishing causality. These studies are highly susceptible to confounding variables and reverse causation (12), making it impossible to determine if alterations in mtDNA-CN and LTL are a cause of MS progression or merely a consequence of the disease process. This ambiguity has stalled progress in understanding the fundamental mechanisms of neurodegeneration in MS, creating a critical barrier to developing effective, targeted therapies.

To overcome these limitations, this study will employ Mendelian Randomization (MR), a robust genetic epidemiology method that uses randomly inherited genetic variants as instrumental variables. Analogous to a randomized controlled trial, MR mitigates confounding and allows for the inference of causal directionality (13). This project outlines a methodologically rigorous investigation designed to leverage the power of MR to dissect the causal roles of mtDNA-CN and LTL in the progression of multiple sclerosis.

---

### 2. Research Objectives
The overarching goal of this research is to dissect the causal relationships between key biomarkers of cellular function and biological aging—namely, mtDNA-CN and LTL—and the progression of MS.

1. **Objective 1:** To investigate the causal effect of mtDNA-CN on MS progression.  
2. **Objective 2:** To investigate the causal effect of leukocyte telomere length on MS progression.  
3. **Objective 3:** To assess reverse causality using a bidirectional MR framework.

---

### 3. Methodological Framework

<div class="table-responsive">
<table class="table table-sm table-hover align-middle">
<thead>
<tr>
<th>Trait</th>
<th>Resource</th>
<th>Sample Size</th>
<th>Key Covariates</th>
</tr>
</thead>
<tbody>
<tr>
<td>mtDNA Copy Number</td>
<td>UK Biobank</td>
<td>383,476</td>
<td>Blood cell counts, age, sex, 20 PCs, chip</td>
</tr>
<tr>
<td>Leukocyte Telomere Length</td>
<td>UK Biobank</td>
<td>472,174</td>
<td>Methodological factors, age, sex, ethnicity</td>
</tr>
<tr>
<td>ARMSS</td>
<td>IMSGC</td>
<td>12,584</td>
<td>Age at onset, sex, platform, PCs</td>
</tr>
</tbody>
</table>
</div>

---

### 4. Expected Outcomes and Scientific Significance
This study provides genetically validated evidence clarifying whether mitochondrial dysfunction and telomere biology are causal drivers or downstream consequences of MS progression, offering mechanistic insight into neurodegenerative processes beyond disease susceptibility.

---

### Reproducible Analysis Reports

<div class="row">
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/projects/published_mr_ms/report_mtDNAcn.png" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/projects/published_mr_ms/report_LTL.png" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

- <a href="/assets/reports/mtDNAcn_MS_prog.html" target="_blank">mtDNA-CN ↔ MS progression (HTML)</a>  
- <a href="/assets/reports/LTL_MS_prog.html" target="_blank">LTL ↔ MS progression (HTML)</a>

---

### Related Publications

<p>
  Full bibliographic details are available in the <a href="/publications/">Publications</a> section.
</p>

- **Sabaie H et al.** Molecular Neurobiology (2025)  
- **Sabaie H et al.** Multiple Sclerosis and Related Disorders (2025)

---

### References
1. Friese MA, Schattling B, Fugger L. *Nat Rev Neurol*. 2014.  
2. Ellwardt E, Zipp F. *Exp Neurol*. 2014.  
3. Doshi A, Chataway J. *Clin Med*. 2016.  
4. Bektas A et al. *Exp Gerontol*. 2018.  
5. Graves JS et al. *Lancet Neurol*. 2023.  
6. Blackburn EH et al. *Science*. 2015.  
7. Gustafsson CM et al. *Annu Rev Biochem*. 2016.  
8. Guha M, Avadhani NG. *Mitochondrion*. 2013.  
9. Cerantonio A et al. *Int J Mol Sci*. 2024.  
10. Guan JZ et al. *Mol Cell Biochem*. 2015.  
11. Krysko KM et al. *Ann Neurol*. 2019.  
12. Grimes DA, Schulz KF. *Lancet*. 2002.  
13. Sekula P et al. *JASN*. 2016.
