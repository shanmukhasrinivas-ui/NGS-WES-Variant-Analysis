# Step 10: Variant Filtering and Candidate Variant Prioritization

## Commands

### Count Total Annotated Variants

```bash
wc -l patient_chr_complete.hg38_multianno.txt
```

### Count Exonic Variants

```bash
grep -c "exonic" patient_chr_complete.hg38_multianno.txt
```

### Count Nonsynonymous Variants

```bash
grep -c "nonsynonymous SNV" patient_chr_complete.hg38_multianno.txt
```

### Count Pathogenic Variants

```bash
grep -Ei "Pathogenic|Likely_pathogenic" patient_chr_complete.hg38_multianno.txt | wc -l
```

### View Candidate Variants

```bash
grep -Ei "Pathogenic|Likely_pathogenic" patient_chr_complete.hg38_multianno.txt | head
```

### View Final Candidate Report

```bash
cat candidate_report.csv
```
