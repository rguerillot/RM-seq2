# RM-seq2

## SYNOPSIS
This pipeline is designed to accurately identify and quantify rare genetic variants (SNP or INDEL) from barcoded amplicon sequencing libraries. It has bees specifically designed for the analysis of Resistance Mutation sequencing experiments (RM-seq) but it can be used with any other barcoded libraries

Guérillot, R., Li, L., Baines, S. et al. Comprehensive antibiotic-linked mutation assessment by resistance mutation sequencing (RM-seq). Genome Med 10, 63 (2018).
https://doi.org/10.1186/s13073-018-0572-z

## USAGE: 
```
rmseq2 -1=<READ1> -2=<READ2> -r=<REFERENCE.FASTA> -g=<REFERENCE.GFF3> -o=<OUTPUT_DIR> [options]

  OPTIONS:
	-o     Output directory (default = ./RMSEQ2-date-time)
	-b     barcode motif at 5' of read1 (default = NNNNNNNNNNNNNNNN)
	-d     minimum sequencing depth per barcode for demultiplexing and calling variants (default = 10)
	-f     minimum allele frequency for variant calling (default = 0.6)
	-s     start coordinate for variant calling (default = 1)
	-e     end coordinate for variant calling (default = 100000000)
	-t     number of threads to use (default = 4)
	-c     set to true to skip all read processing steps and only perform variants call (default = false)
```
