# SNP Code Review

## Summary of paper

The manuscript that I will be focusing for my code review will be based on the paper entitled "A bench-to-data analysis workflow for respiratory syncytial virus whole-genome sequencing with short and long-read approaches." This paper using respiratory suncytial virus (RSV) perform genomic surveillance to detect and monitor circulating lineage and the emergence of amino acid substitutions affecting transmission. For my project, I will be focusing on emergence of amino acid substitution part and illumina sequencing approaches bioinformatic pipelines. The github for this paper has the well documented scripts mostly in the bash scripts while also contains the python scripts. I will be using most of the scripts used in the paper with some changes and additional input.

Some of the similar scripts that I will be using are FASTQC for determining the quality control of raw reads and trimmed reads. The authors have used fastp for trimming the reads that contain adapters, low quality reads and short reads. However, I will be using cutadapt scripts that is more recent and updated compared to fastq. For host removal, kraken2 tool is being used, however, I will be using bwa-dmem for remove host reads and also alignment of viral reads to the reference viral genome. Furhthermore, iVar is used for variant-calling and creating consensus sequence, however I am planning to use bcftools for variant calling and SNP detection. 

**Link to the paper**

The paper that I will be base my methodology will be from the paper `Data analysis` section of this paper [Whole genome sequencing](https://link.springer.com/article/10.1186/s13073-025-01597-4).

**Link to the code**

I will be using the following code and pipeline with modifications and script addition based on this pipeline in this script [Variant Calling](https://github.com/genomicsITER/nf-rsvpipeline). 


## Review 

For the most part the code in the github were farily straightforward as there was the section 'Quick start' that will help for easy installment and cloning of the program. They have the schematic outline of the pipeline that needs to be followed. It was easy for me to obtain, install, and run the code for the project. They had provided the link for the secript that they had used from and it was very easy to follow. There was no road blocks while using the scripts and the only job that needed to be done was the changing the paths. However, I felt somewhere that the database was quite diffficult to follow. The authors could have added the dedicated database for the project with correct directory structure and the example configuration. The documentation for going through the Illumina workflow (which is mostly followed upon) was well documented with workflows, list of the major tools used, specified outputs, and the concrete run commands was present. But when you go to the inline documentation in the python scripts - docstrings were not present meaning it was not well-defined how each lines and functions present inside those commands lines will use. The authors have created a 'quick start' section that run through each process of cloing and running the scripts to get the result and the data are also reproducible. And as this was the part of the greater project, the link to the original github is also mentioned that includes the process from primer designs, results, coverage of samples and all. And all the process that is required with detailed examples and the scripts are divided based into multiple ones. The reference sequence files for the files is also and provided and also the result for that. They also have provided additional repositories that can be used for the study. The authors have provided the very well computational environment and also the examples and tutorials in the github. 

## Suggestions

*High level suggestions*

- Since, there are two different pipeline for Illumina sequencing and Nanopore sequencing, it was kind of overwhelming for to get through it. But it was detailed and made user friendly. I do feel they could have made some of the scripts to be single, minimal for each platform.

- Other point would to make it use lesser external "manual setup" and use automated help for the larger databse requirements

*More specific suggestions*

- The external documentation quality of the code was good but inside-code commands are not well documented - so, making that more documented will be other good thing to do. 

- More clear instruction on the kraken2 database as it is large. So, clearer instuction on how to fetch/verify it and instruction like checksums, expected folder layout and a downloader script could be added.



