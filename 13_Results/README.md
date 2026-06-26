# Final Results

## Workflow Summary

The Whole Exome Sequencing (WES) data were successfully processed through a complete bioinformatics pipeline, starting from raw FASTQ files and ending with the identification and interpretation of clinically relevant genetic variants.

---

## Results Obtained

- Raw sequencing reads were assessed using FastQC.
- Low-quality bases and adapters were removed using Trimmomatic.
- Quality of trimmed reads was confirmed using FastQC.
- The reference genome was indexed using BWA, SAMtools, and GATK.
- High-quality reads were aligned to the GRCh38 reference genome using BWA-MEM.
- SAM files were converted into sorted and indexed BAM files using SAMtools.
- Variants were identified using GATK HaplotypeCaller.
- Identified variants were annotated using ANNOVAR.
- Annotated variants were filtered to prioritize biologically and clinically relevant candidate variants.
- Candidate variants were interpreted using ClinVar, OMIM, and HPO databases.

---

## Output Files

- patient.sam
- patient.bam
- patient_sorted.bam
- patient_sorted.bam.bai
- patient_chr.vcf
- patient_chr_complete.hg38_multianno.txt

---

## Key Outcome

The project demonstrated the successful execution of a standard Whole Exome Sequencing analysis workflow. Through systematic quality assessment, sequence alignment, variant calling, annotation, and filtering, clinically relevant candidate variants were prioritized for further biological interpretation.

---

## Skills Demonstrated

- Linux Command Line
- FastQC
- Trimmomatic
- BWA-MEM
- SAMtools
- GATK
- ANNOVAR
- Variant Filtering
- Clinical Variant Interpretation
