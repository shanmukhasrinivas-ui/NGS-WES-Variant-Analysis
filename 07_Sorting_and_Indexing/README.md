# Step 7: Sorting and Indexing

## Commands

### Sort BAM

```bash
samtools sort patient.bam -o patient_sorted.bam
```

### Index BAM

```bash
samtools index patient_sorted.bam
```

### Alignment Statistics

```bash
samtools flagstat patient_sorted.bam
```
