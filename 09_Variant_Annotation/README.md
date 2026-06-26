# Step 9: Variant Annotation

## Commands

### Convert VCF to ANNOVAR Input

```bash
convert2annovar.pl \
-format vcf4 \
patient_chr.vcf \
> patient.avinput
```

### Run ANNOVAR Annotation

```bash
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

### View Annotation Output

```bash
head patient_chr_complete.hg38_multianno.txt
```

### Count Total Annotated Variants

```bash
wc -l patient_chr_complete.hg38_multianno.txt
```

### View Column Headers

```bash
head -1 patient_chr_complete.hg38_multianno.txt
```
