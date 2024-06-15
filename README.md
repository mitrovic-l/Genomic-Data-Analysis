# Bioinformatics Project: Genomic Data Analysis

## Overview

This project focuses on the analysis of genomic data from two samples, sample7 and sample9. The main objective is to map the sequencing reads to a reference genome, identify and annotate genetic variants, and explore potential contamination by bacterial or viral DNA.

## Objectives

1. **Quality Control**: Assess the quality of sequencing reads and perform necessary filtering.
2. **Mapping Reads**: Align sequencing reads to the reference genome hg38.
3. **Post-Alignment Processing**: 
   - Mark duplicates and recalibrate base quality scores.
4. **Variant Calling**: Identify single nucleotide polymorphisms (SNPs) and insertions/deletions (INDELs).
5. **Variant Annotation**: Annotate variants using ClinVar database.
6. **Unmapped Reads Analysis**: Identify bacterial or viral contaminants by assembling and blasting unmapped reads.

## Key Steps

1. **Quality Control**:
    - Perform quality control using FastQC to check for issues such as low-quality reads and adapter contamination.
2. **Mapping**:
    - Use BWA to align the reads from sample7 and sample9 to the human reference genome hg38.
    - Convert SAM files to BAM, sort and index them for further analysis.
3. **Post-Alignment Processing**:
    - Use Picard tools to mark duplicates.
    - Recalibrate base quality scores using GATK.
4. **Variant Calling**:
    - Identify SNPs and INDELs using GATK's HaplotypeCaller.
5. **Variant Annotation**:
    - Annotate variants with ClinVar significance using GATK's Funcotator.
6. **Unmapped Reads Analysis**:
    - Extract unmapped reads, assemble them using ABySS, and identify potential contaminants using BLAST.

## Technologies and Tools

- **Programming Language**: Python
- **Bioinformatics Tools**: BWA, Samtools, Picard, GATK, FastQC, ABySS, BLAST
- **Reference Genome**: hg38
