# Pollen-MIGseq
Analyzing single cell pollen sequencing with MIGseq libraries

Our goal is to genotype single pollen grains - better than single cell because pollen is hapolid and has 3 cells each - to detect the location of recombination. This project is a work in progress. 

MIGseq uses degnerate primers in a multiplexed PCR reaction to amplify and sequence ISSR (inter-simple sequence repeat) markers by the hundreds or thousands. I modified the MIGseq library prep of Suyama and Matsuki, 2015 to include Adapterama I barcodes (Glenn et al, 2019a) and Adapterama II style primers (Glenn et al, 2019b). 

### How many pollen grains do I haev to sequence?

We did a power analysis to determine how many pollen grains we would have to sequence.  Imputing missing data for pollen is easy if we assume 1 or 2 crossover events per chromosome because pollen is hapolid. 

* Assume less recomb near telomeres/centromeres: cosine distribution
* simulate parents as just 0 or 1 (2 alleles)
* sample games as combination of 0, 1
* recode gametes to represent parents
* Draw gamete haplotypes
* infer recomb rate between each SNP position
