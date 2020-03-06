# Covid-19 "Lineage Tracing" Analysis

Some basic Covid-19 analysis using FAMSA (https://github.com/refresh-bio/FAMSA), SNP-sites (https://github.com/sanger-pathogens/snp-sites), and Cassiopeia (https://github.com/YosefLab/Cassiopeia). The idea is that the recently developed single-cell lineage tracing algorithms might be useful to track phylogenetic history of the Covid-19 virus strains. Here I tried using Cassiopeia as a proof of concept.

The analysis was done as following:

1. Covid-19 sequences were downloaded from GISAID (from human, only full sequences)
2. Multiple sequence alignment was done by FAMSA
3. The alignment result was converted to VCF using SNP-sites (only cared about SNVs)
4. The strains with the exactly same variations were deduplicated.
5. The lineage network was constructed using Cassiopeia - unlike the phylogenetic tree, one node can have multiple children.
6. The network was visualized using NetworkX and Matplotlib
