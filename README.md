## Code Review

During this process the samples will be taken from the infected tissue followed by RNA extraction and cDNA extraction. The cDNA will be used for the sequencing libraries preparation and samples will be sequenced and the resulting sequence reads will be further analyzed using bioinformatics pipeline. However, for this project, we will use the raw reads from the NCBI to process further for the bioinformatics pipeline and data analysis. For the bioinformatics pipeline description will be used based on the research paper attached below and the code will be used based on the github account linked below. The code attached includes pipeline for figuring out the singe nucleotide polymorphism in the dog species. However, I plan to use the modified version of that script to use for the avian reovirus in the chicken host. 
Briefly, the script plans to download the SRR files from the NCBI. The reads will then be checked for the quality and unnecessary, shorter read counts, adapters, etc. will be cleaned using the Trimmomatic code. The clean reads will be mapped with the chicken genome. The unmapped reads will then be referenced and mapped with the ARV S1133 genome. When the viral reads are mapped with reference genome, locations where the nucleotide bases have changed will give the SNP. This process is also called the variant calling and the SNPs can be visualized and analyzed. 

**Link to the paper**

The paper that I will be base my methodology will be from the paper `Data analysis` section of this paper (Whole genome sequencing)[https://bioone.org/journals/avian-diseases/volume-66/issue-4/aviandiseases-D-22-99999/A-Universal-Single-Primer-Amplification-Protocol-to-Perform-Whole-Genome/10.1637/aviandiseases-D-22-99999.full].

**Link to the code**

I will be using the following code and pipeline with modifications and script addition based on this pipeline in this script. (Variant Calling)[https://github.com/Schwartz-Lab-at-Auburn/FunGen2025/blob/mlob/main/DogIIS_map_variantcall_conc.sh]

