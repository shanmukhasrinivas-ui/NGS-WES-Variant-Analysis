# Step 11: Clinical Interpretation

## Resources Used

- ClinVar
- OMIM
- Human Phenotype Ontology (HPO)

## Files Used

- candidate_report.csv
- patient_chr_complete.hg38_multianno.txt

## Interpretation Workflow

### View Candidate Report

```bash
cat candidate_report.csv
```

### Search Candidate Gene

```bash
grep "GENE_NAME" patient_chr_complete.hg38_multianno.txt
```

Replace **GENE_NAME** with the gene identified in your final candidate report.

### Preview Annotated Variants

```bash
head -20 patient_chr_complete.hg38_multianno.txt
```

### Count Total Candidate Variants

```bash
wc -l candidate_report.csv
```
