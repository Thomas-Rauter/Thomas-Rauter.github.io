---
layout: default
title: Packages
---
# Software Packages

I have developed the following software packages:


---
<br>

## **kpnn2**  

![Python](https://img.shields.io/badge/Python-yellow?style=flat&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=flat&logo=pytorch&logoColor=white)

[Website](https://thomas-rauter.github.io/kpnn2/)

**Overview**  
A Python package on PyPI (since September 2026) for building knowledge-primed neural networks (KPNNs), which are interpretable neural networks whose nodes correspond to named entities such as proteins or genes. It turns a named edgelist from prior knowledge into sparsely connected PyTorch layers, including edges that skip layers. Throughout, it keeps each node name tied to its tensor position, so attribution scores are always reported for the correct entity. Activations, losses, and the training loop stay in an ordinary PyTorch module that the user writes.

---
<br>

## **scholidonline**  

![R](https://img.shields.io/badge/R-blue?style=flat&logo=r&logoColor=white)

[Website](https://thomas-rauter.github.io/scholidonline/)

**Overview**  
An R package on CRAN (since April 2026) and the online companion to scholid. It queries external registries such as Crossref, NCBI, Europe PMC, arXiv, ORCID, and ROR to check whether scholarly identifiers exist, convert them across systems (e.g., PMID → DOI), retrieve bibliographic metadata, and discover identifiers linked to the same record.

---
<br>

## **scholid**  

![R](https://img.shields.io/badge/R-blue?style=flat&logo=r&logoColor=white)

[Website](https://thomas-rauter.github.io/scholid/)

**Overview**  
An R package on CRAN (since February 2026) with lightweight, dependency-free utilities for detecting, normalizing, classifying, and extracting scholarly identifiers. It supports twenty identifier types, including DOIs, ORCID iDs, ISBNs, ISSNs, arXiv and PubMed IDs, ROR, OpenAlex, and life-science accessions such as UniProt, RefSeq, SRA, and GEO. Its vectorized functions are designed as a small, well-tested foundation for other R packages and data workflows.

---
<br>

## **SplineOmics**  

![R](https://img.shields.io/badge/R-blue?style=flat&logo=r&logoColor=white) 
![HTML](https://img.shields.io/badge/HTML-orange?style=flat&logo=html5&logoColor=white) 
![JavaScript](https://img.shields.io/badge/JavaScript-yellow?style=flat&logo=javascript&logoColor=white)

[Website](https://csbg.github.io/SplineOmics/)

**Overview**  
An R package for finding significant features (hits) in time-series -omics data using splines and limma for hypothesis testing. It clusters hits based on spline shape and generates summary HTML reports.
