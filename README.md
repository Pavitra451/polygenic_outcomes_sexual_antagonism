# polygenic_outcomes_sexual_antagonism
Simulation code for pre-print "Polygenic outcomes of sexually antagonistic selection" (doi: 10.1101/2023.03.02.530911)

This repository contains simulation code used in the biorxiv preprint "Polygenic outcomes of sexually antagonistic selection" by P. Muralidhar & G. Coop (https://www.biorxiv.org/content/10.1101/2023.03.02.530911v1)

This text file will provide a basic overview of the simulation code. For more details, please see the Methods section of the preprint. 

In this repository, there are three scripts - 'Autosome_only_simulations.slim', 'X_chrom_only_no_dosage.slim', 'X_chrom_only_with_dosage.slim' - which correspond to the 'Single inheritance mode' simulations described in the manuscript. These scripts simulate a polygenic phenotype encoded by 1000 freely recombining loci on an entirely autosomal genome, on an non-dosage-compensated X-linked genome, and on a dosage-compensated X-linked genome.

There are two scripts - 'Drosophila_like_sims_no_X_dosage.slim' and 'Drosophila_like_sims_with_X_dosage.slim' - which correspond to simulations of a polygenic phenotype encoded by 1000 loci on a Drosophila melanogaster-like genome, in cases in which dosage compensation either is not or is in effect on the X chromosome. 

In order to set up a recombination process in SLiM which corresponds to the linkage map of a Drosophila-like genome, we used input files that describe how a Drosophila-like linkage map would translate to recombination probabilities between 1000 loci. These files are also in this repository. SLiM requires two input files which describe the female and male recombination process. The input file for females is labelled "linkage_data_dros_female.txt". We have provided two possible input files for the male recombination process. The first of these, "linkage_data_dros_male_with_male_auto_rec.txt", allows for autosomal recombination in males at rates equal to that in females (see Methods) and was used for the majority of simulations in the pre-print. The second, "linkage_data_dros_male_no_male_auto_rec.txt", does not allow male autosomal recombination. 

The last script - 'Drosophila_like_no_X_dosage_moving_optimum.slim' - also simulates a polygenic phenotype encoded by 1000 loci on a Drosophila melanogaster-like genome in an evolutionary scenario in which the male-female fitness optimum changes every 500 generations after the burn-in period. 

All simulations in the pre-print were run in SLiM 3.3. However, since these simulations were preformed, SLiM 4 was released. This release involved changes to the syntax used in SLiM scripts. For convenience, these scripts in this repository have been updated to use the syntax of SLiM 4, rather than SLiM 3. However, the syntax changes between SLiM 3 and 4 are relatively minor and could be easily reverted if usage in SLiM 3 is preferred. 

