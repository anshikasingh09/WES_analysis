# Whole Exome Sequencing (WES) Analysis – Parkinson Sample (SRR1946638)

This repository presents a comprehensive Whole Exome Sequencing (WES) analysis of a Parkinson’s disease sample (SRR1946638). The pipeline covers raw data quality control, preprocessing, alignment, variant calling, and final annotation.

---

## Tools Used

- **FastQC**: Quality control of raw reads  
- **fastp**: Adapter trimming and quality filtering  
- **SAMtools**: BAM/SAM file manipulation  
- **GATK**: Variant calling pipeline  
- **ANNOVAR**: Functional annotation of variants

---

## Project Structure

```
wes-analysis/
├── fastqc_reports/        # Raw FASTQ quality report (HTML)
├── fastp_reports/         # Filtered read report (HTML)
├── annovar_results/       # Final variant annotation output (.txt and .csv)
└── wes_summary.md         # Summary of analysis and interpretation
```

---

## Key Variants Identified

| Gene   | Mutation | Effect             | Disease                          |
|--------|----------|--------------------|----------------------------------|
| ATAD3A | R528Q    | Nonsynonymous SNV  | Harel-Yoon syndrome              |
| IRF6   | N88S     | Nonsynonymous SNV  | Van der Woude syndrome           |
| GJB2   | V37I     | Nonsynonymous SNV  | Genetic hearing loss             |
| SMAD6  | G365S    | Nonsynonymous SNV  | Tracheoesophageal fistula        |
| SOX9   | R177W    | Nonsynonymous SNV  | Camptomelic dysplasia            |
| PLCD1  | R352Q    | Nonsynonymous SNV  | Likely pathogenic                |

> These variants were identified based on exonic impact and clinical relevance.

---

## Pipeline Summary

1. **Quality Control**: Raw reads assessed using FastQC  
2. **Filtering**: fastp used to remove low-quality reads and adapters  
3. **Alignment**: Reads aligned to GRCh37 using BWA-MEM (assumed step)  
4. **Post-processing**: BAM files indexed and sorted using SAMtools  
5. **Variant Calling**: GATK used for SNP and Indel calling  
6. **Annotation**: ANNOVAR annotated variants using RefGene and dbSNP

---

## Sample Details

- **Sample ID**: SRR1946638  
- **Organism**: Homo sapiens  
- **Condition**: Parkinson's Disease  
- **Reference Genome**: GRCh37/hg19  
- **Read Type**: Paired-end (PE)

---

## Disclaimer

This analysis is based on a single WES dataset and is intended for academic and research use only.
