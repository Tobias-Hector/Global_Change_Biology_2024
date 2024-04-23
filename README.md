# Global_Change_Biology_2024
Data and code for the manuscript: 'Acclimation to warmer temperatures can protect host populations from both further heat stress and the potential invasion of pathogens', published in Global Change Biology. Authors: Tobias E. Hector, Marta S. Shocket, Carla M. Sgrò &amp; Matthew D. Hall

Citation: Hector, T. E., Shocket, M. S., Sgrò, C. M., & Hall, M. D. (2024) Acclimation to warmer temperatures can protect host populations from both further heat stress and the potential invasion of pathogens. *Global Change Biology*, XXX.

[![DOI](https://zenodo.org/badge/790105956.svg)](https://zenodo.org/doi/10.5281/zenodo.11045834)

## Details

ALl data and code necessary to reproduce the analysis and figures in the manuscript is included. Raw data and posterior samples from models can be found in /data.

"final_heat_data.csv" contains the knockdown times for each individual used in the heat tolerance assays. In all phenotype data 'mat_temp' and 'acc_temp' refer to the maternal acclimation treatment and focal acclimation treatment, respectively. 

"final_phenotype_data.csv" contains summary individual-level host and pathogen fitness trait measures. This includes: host lifetime clutch number ('total_clutches'), host lifetime fecundity ('total_offspring'), host lifespan ('lifespan_days'), pathogen mature spore counts ('mature_spores'). For individuals in infection treatments, the 'infected' column denotes whether the pathogen had produced mature spores ('M'), only immature pre-spores ('P'), or was not infected ('N') based on visual microscope inspection of samples. 'mature_spores', 'pre_spores', and 'all_spores' are spore counts based on flowcytometry (see main text)

"full_offspring_data.csv" contains individual-level age-specific offspring counts. 'clutch' is the number of clutches present on day of counting, 'offspring' is the offspring count, 'alive_dead' is whether the focal animal was alive on the day of counting, 'cum_off' is the cumulative number of offspring for each individual, 'death_date' is the date on which the animal died, 'host_age' is the host age on day of counting.

"infection_prob_data.csv" is produced in the "pheno_data_analysis,Rmd" script and required for plotting host infection rate. 

"JAGS_birth_death_post_full.csv" & "JAGS_R0_derived_post_full.csv" are posterior estimates of variables from our epidemiological model. These data are produced in the script "JAGS_R0_calcs.Rmd". 

To run these analysis and visulisations from scratch the scripts should be run in the order:

1. pheno_data_analysis.Rmd
2. JAGS_R0_calcs_Rmd
3. plotting.Rmd

I hope this is helpful! :)

