# Whole Exome Sequencing (WES) Variant Analysis

## Project Overview

This repository contains the complete workflow of a Whole Exome Sequencing (WES) analysis performed during a 7-week online Genomics and Next Generation Sequencing (NGS) internship. The project demonstrates the end-to-end bioinformatics pipeline, from raw sequencing data to the identification and interpretation of clinically relevant genetic variants.

## Project Objective

To analyze Whole Exome Sequencing data using standard bioinformatics tools for quality assessment, sequence alignment, variant calling, variant annotation, and candidate variant prioritization.

## Workflow

Raw FASTQ Files
↓
Quality Control (FastQC)
↓
Read Trimming (Trimmomatic)
↓
Quality Control After Trimming
↓
Reference Genome Preparation
↓
Sequence Alignment (BWA-MEM)
↓
SAM to BAM Conversion
↓
Sorting & Indexing (SAMtools)
↓
Variant Calling (GATK HaplotypeCaller)
↓
Variant Annotation (ANNOVAR)
↓
Variant Filtering
↓
Candidate Gene Prioritization
↓
Clinical Interpretation

## Tools Used

- Linux (Ubuntu)
- FastQC
- MultiQC
- Trimmomatic
- BWA-MEM
- SAMtools
- GATK
- ANNOVAR
- IGV

## Repository Structure

Each folder represents one step of the WES analysis pipeline and contains the commands used, screenshots, and output files.
