# Commands Used in the WES Analysis Pipeline

This folder contains the major Linux and bioinformatics commands used throughout the Whole Exome Sequencing (WES) analysis workflow.

---

## 1. Quality Control

```bash
fastqc SRR14684620_1.fastq.gz SRR14684620_2.fastq.gz
```

---

## 2. Read Trimming

```bash
java -jar Trimmomatic-0.39.jar PE \
SRR14684620_1.fastq.gz \
SRR14684620_2.fastq.gz \
R1_paired.fastq.gz \
R1_unpaired.fastq.gz \
R2_paired.fastq.gz \
R2_unpaired.fastq.gz \
SLIDINGWINDOW:4:20 \
MINLEN:50
```

---

## 3. Quality Check After Trimming

```bash
fastqc R1_paired.fastq.gz R2_paired.fastq.gz
```

---

## 4. Reference Genome Preparation

```bash
bwa index GCF_000001405.40_GRCh38.p14_genomic.fna

samtools faidx GCF_000001405.40_GRCh38.p14_genomic.fna

gatk CreateSequenceDictionary \
-R GCF_000001405.40_GRCh38.p14_genomic.fna
```

---

## 5. Sequence Alignment

```bash
bwa mem \
GCF_000001405.40_GRCh38.p14_genomic.fna \
R1_paired.fastq.gz \
R2_paired.fastq.gz \
> patient.sam
```

---

## 6. SAM to BAM Conversion

```bash
samtools view -Sb patient.sam > patient.bam
```

---

## 7. Sorting and Indexing

```bash
samtools sort patient.bam -o patient_sorted.bam

samtools index patient_sorted.bam

samtools flagstat patient_sorted.bam
```

---

## 8. Variant Calling

```bash
gatk HaplotypeCaller \
-R GCF_000001405.40_GRCh38.p14_genomic.fna \
-I patient_sorted.bam \
-O patient_chr.vcf
```

---

## 9. Variant Annotation

```bash
convert2annovar.pl \
-format vcf4 patient_chr.vcf \
> patient.avinput

table_annovar.pl \
patient.avinput humandb/ \
-buildver hg38 \
-out patient_chr_complete \
-remove \
-protocol refGene,clinvar_20240917,gnomad41_exome,dbnsfp47a \
-operation g,f,f,f \
-nastring . \
-polish
```

---

## 10. Variant Filtering

```bash
grep -c "exonic" patient_chr_complete.hg38_multianno.txt

grep -c "nonsynonymous SNV" patient_chr_complete.hg38_multianno.txt

grep -Ei "Pathogenic|Likely_pathogenic" patient_chr_complete.hg38_multianno.txt
```

---
