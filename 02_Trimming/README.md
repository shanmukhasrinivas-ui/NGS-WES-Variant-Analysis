# Step 2: Read Trimming

## Objective
To remove low-quality bases from paired-end sequencing reads.

## Tool
- Trimmomatic

## Command

```bash
java -jar Trimmomatic-0.39/trimmomatic-0.39.jar PE \
SRR14684620_1.fastq.gz \
SRR14684620_2.fastq.gz \
R1_paired.fastq.gz \
R1_unpaired.fastq.gz \
R2_paired.fastq.gz \
R2_unpaired.fastq.gz \
SLIDINGWINDOW:4:20 \
MINLEN:50
```

## Output
- R1_paired.fastq.gz
- R2_paired.fastq.gz
- R1_unpaired.fastq.gz
- R2_unpaired.fastq.gz

## Screenshots
Upload terminal output.
