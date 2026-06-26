# Step 6: SAM to BAM Conversion (SAMtools)

## Objective

To convert the SAM file generated after sequence alignment into a compressed BAM file for efficient storage and downstream analysis.

---

## Tool Used

- SAMtools

---

## Input File

- patient.sam

---

## Command

```bash
samtools view -Sb patient.sam > patient.bam
```

---

## Output File

- patient.bam

---

## Description

The SAM file generated after sequence alignment was converted into BAM format using SAMtools. BAM is the compressed binary version of a SAM file, making it faster to process and requiring significantly less storage space. This conversion prepares the alignment file for sorting, indexing, and variant calling.

---

## Result

The alignment file was successfully converted from SAM format to BAM format, producing the file **patient.bam** for downstream genomic analysis.
Add Step 6: SAM to BAM Conversion
