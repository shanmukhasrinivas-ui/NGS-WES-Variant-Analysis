# Step 4: Quality Control After Trimming

## Objective

To assess the quality of the trimmed paired-end reads and verify that low-quality bases and adapter contamination have been effectively removed after trimming.

---

## Tool Used

- FastQC

---

## Input Files

- R1_paired.fastq.gz
- R2_paired.fastq.gz

---

## Command

```bash
fastqc R1_paired.fastq.gz R2_paired.fastq.gz
```

---

## Output Files

- R1_paired_fastqc.html
- R1_paired_fastqc.zip
- R2_paired_fastqc.html
- R2_paired_fastqc.zip

---

## Results

### Per Base Sequence Quality
The quality scores across most read positions remained above Phred score 30, indicating high-quality sequencing reads after trimming. A slight reduction in quality was observed towards the end of the reads, but it remained within the acceptable range.

### GC Content
The GC distribution showed a single major peak around 60–65%, closely matching the theoretical distribution. This indicates that trimming preserved the biological composition of the sequencing reads.

### Adapter Content
No significant adapter contamination was detected across the read length, confirming the effectiveness of the trimming process.

---

## Conclusion

The FastQC analysis after trimming demonstrated that the paired-end reads are of high quality and free from significant adapter contamination. These cleaned reads are suitable for downstream analyses such as sequence alignment and variant calling.

---

## Screenshots

Upload the following screenshots:

- FastQC Per Base Sequence Quality (R1)
- FastQC GC Distribution (R1)
- FastQC Adapter Content (R1)
- FastQC Per Base Sequence Quality (R2)
- FastQC GC Distribution (R2)
- FastQC Adapter Content (R2)
- FastQC Terminal Command Output
