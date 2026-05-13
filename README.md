# AI/ML/DL for OSA/SDB Review: Included-Paper Metadata and Visualization Files

This repository provides the metadata, official access links, screening records, and visualization-support files used for the review paper:

**Artificial Intelligence for Sleep-Disordered Breathing: A Taxonomy of Methods, Data Modalities, and Clinical Applications**

The review focuses on recent applications of artificial intelligence, machine learning, deep learning, data mining, wearable sensing, multimodal analytics, and large language models for the diagnosis, screening, prediction, monitoring, and management of obstructive sleep apnea (OSA) and sleep-disordered breathing (SDB).

This repository does **not** store copyrighted full-text PDF files. Instead, it provides structured metadata and official DOI or publisher links for the included papers.

---

## Repository contents

### Core-paper metadata

- `osa_sdb_218_core_papers_download_manifest.csv`  
  Metadata table for the 218 core included papers. This file includes paper identifiers, titles, publication years, journals or sources, DOI or official URLs, publisher/source information, taxonomy-group assignments, and review-derived tags.

- `osa_sdb_218_core_papers_official_urls.txt`  
  One official DOI or publisher link per included paper. These links can be used for manual access through institutional subscriptions, open-access publisher pages, or other legitimate access routes.

### VOSviewer files

- `osa_sdb_core_papers_vosviewer_bibliographic.ris`  
  Bibliographic RIS file prepared for import into reference managers and VOSviewer.

- `osa_sdb_core_papers_vosviewer_enriched_tags.ris`  
  RIS file enriched with review-derived tags, including technique terms, task terms, data-modality terms, taxonomy groups, and publisher/source labels. This file is recommended for VOSviewer term maps and keyword co-occurrence visualizations.

### Documentation

- `README.md`  
  Description of the repository, file contents, usage notes, and copyright/licensing guidance.

---

## Review corpus

The repository describes the **218 core studies** retained after screening in the review. These papers were selected from a broader multi-publisher search and were organized according to the taxonomy used in the manuscript.

The seven taxonomy groups are:

1. **G1:** Polysomnography and home sleep apnea testing signal analysis  
2. **G2:** Wearable, smartphone, and contactless technologies for SDB screening  
3. **G3:** Audio, oximetry, ECG, PPG, and respiratory-signal-based diagnosis  
4. **G4:** Imaging, craniofacial, and anatomical analysis for OSA risk prediction  
5. **G5:** Phenotyping, endotyping, and risk stratification for precision sleep medicine  
6. **G6:** Treatment management, CPAP adherence, and remote monitoring  
7. **G7:** Explainable, trustworthy, and clinically deployable AI for SDB  

Because one paper may contribute to more than one topic, taxonomy assignments are multi-label rather than mutually exclusive.

---

## Core-paper count by source

The 218 core papers are distributed as follows:

| Source / publisher | Core papers |
|---|---:|
| Elsevier | 98 |
| IEEE | 65 |
| Dove Medical Press | 24 |
| Springer | 15 |
| Springer Nature | 10 |
| Frontiers Media SA | 4 |
| Taylor & Francis | 1 |
| American Academy of Sleep Medicine | 1 |
| **Total** | **218** |

---

## How to use the files

### For checking included papers

Use:

```text
osa_sdb_218_core_papers_download_manifest.csv
