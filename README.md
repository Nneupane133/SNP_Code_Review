# SNP Code Review

## Summary of paper

The manuscript that I will be focusing for my code review will be based on the paper entitled "A bench-to-data analysis workflow for respiratory syncytial virus whole-genome sequencing with short and long-read approaches." This paper using respiratory suncytial virus (RSV) perform genomic surveillance to detect and monitor circulating lineage and the emergence of amino acid substitutions affecting transmission. For my project, I will be focusing on emergence of amino acid substitution part and illumina sequencing approaches bioinformatic pipelines. The github for this paper has the well documented scripts mostly in the bash scripts while also contains the python scripts. I will be using most of the scripts used in the paper with some changes and additional input.

Some of the similar scripts that I will be using are FASTQC for determining the quality control of raw reads and trimmed reads. The authors have used fastp for trimming the reads that contain adapters, low quality reads and short reads. However, I will be using cutadapt scripts that is more recent and updated compared to fastq. For host removal, kraken2 tool is being used, however, I will be using bwa-dmem for remove host reads and also alignment of viral reads to the reference viral genome. Furhthermore, iVar is used for variant-calling and creating consensus sequence, however I am planning to use bcftools for variant calling and SNP detection. 

**Link to the paper**

The paper that I will be base my methodology will be from the paper `Data analysis` section of this paper [Whole genome sequencing](https://link.springer.com/article/10.1186/s13073-025-01597-4).

**Link to the code**

I will be using the following code and pipeline with modifications and script addition based on this pipeline in this script [Variant Calling](https://github.com/genomicsITER/nf-rsvpipeline). 

