# Step 5: Reference Genome Preparation

## Objective

To prepare the human reference genome for sequence alignment and variant calling by generating the required index and dictionary files.

---

## Tools Used

- BWA
- SAMtools
- GATK

---

## Input File

- GCF_000001405.40_GRCh38.p14_genomic.fna

---

## Commands

### 1. Index the Reference Genome using BWA

```bash
bwa index GCF_000001405.40_GRCh38.p14_genomic.fna
```

### 2. Create FASTA Index using SAMtools

```bash
samtools faidx GCF_000001405.40_GRCh38.p14_genomic.fna
```

### 3. Create Sequence Dictionary using GATK

```bash
gatk CreateSequenceDictionary \
-R GCF_000001405.40_GRCh38.p14_genomic.fna \
-O GCF_000001405.40_GRCh38.p14_genomic.dict
```

---

## Output Files

### BWA Index Files

- GCF_000001405.40_GRCh38.p14_genomic.fna.amb
- GCF_000001405.40_GRCh38.p14_genomic.fna.ann
- GCF_000001405.40_GRCh38.p14_genomic.fna.bwt
- GCF_000001405.40_GRCh38.p14_genomic.fna.pac
- GCF_000001405.40_GRCh38.p14_genomic.fna.sa

### SAMtools Output

- GCF_000001405.40_GRCh38.p14_genomic.fna.fai

### GATK Output

- GCF_000001405.40_GRCh38.p14_genomic.dict

---

## Description

The human reference genome was indexed using BWA to facilitate rapid sequence alignment. A FASTA index (.fai) was generated using SAMtools, enabling quick access to genomic coordinates during downstream analysis. Finally, a sequence dictionary (.dict) was created using GATK, which is required for variant calling and other GATK-based analyses. These files ensure compatibility and efficient processing throughout the bioinformatics pipeline.

---

## Conclusion

The reference genome was successfully prepared by generating all the required index and dictionary files. The prepared reference genome is now ready for read alignment using BWA-MEM and subsequent variant analysis.

---

## Screenshots

Upload the following screenshots:

- BWA indexing terminal output
- SAMtools faidx terminal output
- GATK CreateSequenceDictionary terminal output
- `ls` command showing the generated index files
