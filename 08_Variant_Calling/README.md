# Step 8: Variant Calling

## Commands

### View VCF Header

```bash
head -30 patient_chr.vcf
```

### Count Total Variants

```bash
grep -vc "^#" patient_chr.vcf
```

### View First 10 Variants

```bash
grep -v "^#" patient_chr.vcf | head
```

### Search for Chromosome 17 Variants (Optional)

```bash
grep "^NC_000017" patient_chr.vcf | head
```
