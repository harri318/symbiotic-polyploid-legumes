# Analysis for "Symbiosis with rhizobia limits range expansion only in polyploid legumes"

Tia Harrison Oct 5 2021

This repository stores data and code for our analysis in our paper to be submitted to New Phytologist as a rapid report. 

## Summary 

- Both mutualism and polyploidy are thought to influence invasion success in plants. Mutualism can limit range expansion when plants cannot find a compatible partner in a novel habitat, or facilitate range expansion when mutualism increases a plant’s niche breadth. Polyploids are also expected to have greater niche breadth because of greater self-compatibility and phenotypic plasticity, increasing invasion success. Few studies test the joint effects of mutualism and ploidy on invasion success.
 - For 839 legume species, we compiled data from published sources to estimate ploidy, symbiotic status with rhizobia, specificity on rhizobia, and the number of introduced ranges.
- We found that symbiosis and ploidy interact to affect range expansion. Non-symbiotic polyploids and generalist symbiotic polyploids have spread to more ranges around the globe than specialist symbiotic polyploids or diploids. We also found evidence of a high rate of re-diploidization in symbiotic legume lineages.
- Our results suggest that symbiosis with rhizobia influences range expansion only when legumes are polyploids. Diploid species have limited spread around the globe regardless of symbiotic status. It is still unclear whether polyploidy evolved from diploidy first and symbiosis with rhizobia evolved afterward, or if symbiosis evolved directly from diploids.

## Contents 

This repository contains the data file of ploidy estimated for 839 different legume species and the R code to analyze the impacts of ploidy and symbiosis status on plant invasion which is presented in our paper. The phylogeny used in our analysis is the Zanne et al 2014 angiosperm phylogeny. 

### Ploidy_PGLS_analysis.Rmd 

R Markdown file detailing code to analyze the joint impacts of ploidy and symbiosis status on plant invasion.

### State_transitions_analysis.Rmd 

R Markdown file detailing code for estimating transitions between different states (diploid, polyploid, symbiotic, non-symbiotic) across the legume phylogeny.

### Legume_ploidy_dataset.csv

Dataset including information for legume species scraped from multiple papers and calculated in our own paper. Details on what data is included in each column is listed below. 

areaIntroduced – The total area of the species introduced range. 
areaIntroducedScaled – The total area of the introduced range for each legume species was mean-centred and scaled by the standard deviation. 
areaNative – The total area of the species native range. 
areaNativeScale – The total area of the native range for each legume species was mean-centred and scaled by the standard deviation. 
NumIntroduced – Number of ranges each species has been introduced to. Range data was calculated by Simonsen et al. 2017. 
Fixer – The 0s in the data represent legume species that do not form nodules with rhizobia and 1s represent species that do form nodules with rhizobia. Data was taken from Werner et al. 2014. 
numOTUs – Number of total rhizobia OTUs associated with each legume species calculated by Harrison et al. 2018. 
numGenera – Number of total rhizobia genera associated with each legume species. Data from Andrews & Andrews 2017. 
Specialist – The 1s in the dataset represents species that only associate with one rhizobia genus (specialists) and 0s represents species that associate with multiple rhizobia genera (generalists). 
Human_Uses – Number of human uses associated with each legume species. Data from Simonsen et al. 2018. 
AbsLatNative – The absolute value of the midpoint value of the species native range. 
LatNative – The value of the midpoint value of the species native range. 
ChromosomeCount – Total number of chromosomes in the species genomes (including copies). 
PloidyLow – Lowest base chromosome number used to calculate ploidy by genus. 
diPloidyLow – Ploidy levels calculated from genus-level base chromosome values. The 0s represent diploids and 1s represent polyploids. 
sfPloidy – Base chromosome number acquired on subfamily level (Caesalpinioideae, Mimosoideae, and Papilionoideae) 
disfPloidy – Ploidy levels calculated from subfamily-level base chromosome values. The 0s represent diploids and 1s represent polyploids. 
