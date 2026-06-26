# Step 6: Sequence Alignment (BWA-MEM)

## Objective

To align the high-quality paired-end sequencing reads to the human reference genome (GRCh38) using the BWA-MEM algorithm, generating a Sequence Alignment/Map (SAM) file for downstream processing.

---

## Tool Used

- BWA-MEM

---

## Input Files

- GCF_000001405.40_GRCh38.p14_genomic.fna
- R1_paired.fastq.gz
- R2_paired.fastq.gz

---

## Command

```bash
bwa mem -t 4 \
GCF_000001405.40_GRCh38.p14_genomic.fna \
R1_paired.fastq.gz \
R2_paired.fastq.gz > patient.sam
```

---

## Output File

- patient.sam

---

## Description

The BWA-MEM algorithm was used to align the trimmed paired-end sequencing reads against the human reference genome (GRCh38). This algorithm efficiently identifies the most probable genomic location for each read while supporting gapped alignments and split reads. The generated SAM file stores alignment information, including mapping position, mapping quality, CIGAR strings, and alignment flags, which are required for downstream BAM conversion, sorting, indexing, and variant calling.

---

## Results

- High-quality paired-end reads were successfully aligned to the reference genome.
- The generated SAM file contains alignment records for all mapped sequencing reads.
- Alignment information is preserved for subsequent processing using SAMtools.

---

## Conclusion

The trimmed sequencing reads were successfully aligned to the human reference genome using BWA-MEM. The resulting SAM file serves as the primary input for BAM conversion, sorting, indexing, and variant calling.

---

## Screenshots

Upload the following screenshots:

- BWA-MEM alignment command
- Alignment completion in terminal
- `ls -lh patient.sam`
- `head patient.sam`
