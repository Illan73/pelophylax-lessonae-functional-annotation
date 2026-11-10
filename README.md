# pelophylax-lessonae-functional-annotation
Reproducible bioinformatics workflow for functional annotation and Gene Ontology profiling of the predicted Pelophylax lessonae proteome, presented at SEBiBC 2026.

# Functional Characterisation of the *Pelophylax lessonae* Genome

### A comparative framework for future annotation of *Pelophylax perezi*

**Author:** Gonzalo Illán  
**Affiliation:** GSNOOK S.L., Spain  
**Conference:** II Congreso de la Sociedad Española de Bioinformática y Biología Computacional (SEBiBC 2026)

---

## 1. Project Overview

Functional genomic resources remain limited for many non-model amphibians, despite their ecological, evolutionary and biotechnological relevance.

The availability of a chromosome-level reference genome and annotation for the pool frog (*Pelophylax lessonae*) provides an opportunity to investigate its predicted functional repertoire and establish a foundation for future comparative studies within the genus *Pelophylax*.

This project presents a preliminary functional characterisation of the annotated *P. lessonae* proteome using sequence similarity searches and Gene Ontology (GO) annotations.

The study also explores the potential of this framework to support future functional annotation studies in *Pelophylax perezi*.

## 2. Study Objectives

- Characterise the predicted functional repertoire of the annotated *P. lessonae* proteome.
- Identify sequence similarities with reviewed UniProtKB/Swiss-Prot protein records.
- Associate matched protein identifiers with Gene Ontology annotations.
- Analyse the distribution of GO terms across Biological Process (BP), Molecular Function (MF) and Cellular Component (CC).
- Establish a reproducible methodological foundation for future comparative genomic analyses within *Pelophylax*.

## 3. Reference Genome

| Resource | Description |
|---|---|
| Organism | *Pelophylax lessonae* |
| Common name | Pool frog |
| Database | NCBI RefSeq |
| Assembly accession | GCF_965119305.1 |
| Assembly name | aPelLes1.hap1.1 |
| Input data | Predicted protein sequences |
| Sequence format | FASTA (.faa) |

**Reference assembly:** [NCBI RefSeq GCF_965119305.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_965119305.1/)

## 4. Bioinformatics Workflow

The functional characterisation workflow was implemented under Ubuntu and comprises the following stages.

### 4.1. Protein sequence retrieval

Predicted protein sequences from the annotated *P. lessonae* genome were used as the query proteome.

### 4.2. Reference protein database

Reviewed protein sequences from UniProtKB/Swiss-Prot were used as the reference dataset.

### 4.3. Sequence similarity search

DIAMOND BLASTP was used to compare the predicted *P. lessonae* proteins against the Swiss-Prot reference database.

The search was configured with a maximum of one reported target sequence per query and an E-value threshold of 1e-5.

Sequence similarity does not, by itself, establish orthology or functional equivalence.

### 4.4. Functional annotation

Matched UniProt identifiers were associated with Gene Ontology terms.

Annotations were classified into three GO domains:

- **Biological Process (BP)**
- **Molecular Function (MF)**
- **Cellular Component (CC)**

### 4.5. Functional profiling

GO term frequencies were analysed and visualised using R, including quantitative summaries and treemap representations.

## 5. Main Results

The functional annotation workflow generated **396,813 protein–GO associations** and identified **16,784 distinct GO terms** across the three GO domains.

| GO domain | Protein–GO associations | Distinct GO terms |
|---|---:|---:|
| Biological Process (BP) | 184,835 (46.6%) | 10,698 |
| Cellular Component (CC) | 120,026 (30.2%) | 1,763 |
| Molecular Function (MF) | 91,952 (23.2%) | 4,323 |
| **Total** | **396,813 (100%)** | **16,784** |

The Biological Process profile included frequently represented annotations associated with transcriptional regulation, signal transduction, cell differentiation, innate immune response and apoptosis.

These findings describe predicted functional associations and should not be interpreted as experimental evidence of the corresponding biological activities.

## 6. Conference Poster

**Functional characterisation of the pool frog (*Pelophylax lessonae*) genome as a comparative framework for future annotation of *Pelophylax perezi*.**

Presented at SEBiBC 2026.

[View the conference poster (PDF)](poster/SEBiBC2026_Pelophylax_lessonae_Poster.pdf)

## 7. Reproducibility and Data Availability

This repository is intended to provide the bioinformatics workflow, scripts, supporting documentation, figures and selected results associated with the study.

The original reference datasets are available from their respective providers:

- [NCBI RefSeq](https://www.ncbi.nlm.nih.gov/refseq/)
- [UniProtKB/Swiss-Prot](https://www.uniprot.org/)
- [Gene Ontology](https://geneontology.org/)

The conference poster is available in the `poster/` directory.

**Reproducibility status:** The original analysis scripts, software versions, reference database release information and intermediate results are being progressively reviewed for inclusion. Complete independent reproduction cannot yet be assumed from the materials currently available in this repository.

## 8. Limitations

Functional assignments are based on sequence similarity and annotation transfer.

Important limitations include:

- Sequence similarity does not necessarily imply identical biological function.
- GO annotations may derive from different evidence types.
- Functional predictions have not been experimentally validated in *P. lessonae*.
- The applicability of this framework to *P. perezi* has not yet been evaluated.
- Additional analyses are required to assess annotation accuracy and investigate specific candidate genes.

## 9. Future Research

Potential extensions include:

- Targeted investigation of genes associated with innate immunity.
- Identification and characterisation of candidate antimicrobial peptide (AMP) precursors and other potentially bioactive proteins.
- Comparative functional genomics within the genus *Pelophylax*.
- Assessment of annotation transferability to *P. perezi*.
- Integration of additional genomic and functional evidence.

These represent future research directions rather than completed analyses.

## 10. References

Kosch TA, et al. (2025). Comparative analysis of amphibian genomes: An emerging resource for basic and applied research. *Molecular Ecology Resources*, 25(1), e14025.

Liedtke HC, et al. (2022). Chromosome-level assembly, annotation and phylome of *Pelobates cultripes*, the western spadefoot toad. *DNA Research*, 29(3), dsac013.

*Bibliographic details are reproduced from the conference poster and should be checked against the original publications before further reuse.*

## 11. License

The repository includes an MIT License. Applicability to third-party data, figures and reference resources must be assessed separately.

---

**Project repository:** [pelophylax-lessonae-functional-annotation](https://github.com/Illan73/pelophylax-lessonae-functional-annotation)
