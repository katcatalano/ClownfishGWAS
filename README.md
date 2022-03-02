# ClownfishGWAS
Katrina Catalano's data and code for project investigating associations between larval traits and genotypes from Expressed Exome Capture Sequencing in Amphiprion percula. Run on Annotate, using miniconda environment "commandline" for bash code and "r4.0" for R code. Analysis workflow is as follows,
1. notebooks/demultiplex.ipynb- bash- download sequencing data from Princeton Genomics Core, check read counts, demultiplex based on PCR index and inline adapter barcodes and perform basic read quality trimming.
2. notebooks/qc_seq.ipynb- bash- screen for contamination, check read quality, map to reference genome, mark and remove duplicates, merge bam files, call genotypes. If interested in genotype calls (not included in current analysis because of low depth), notebooks/plot_filtering_stats.ipynb, notebooks/plot_coverage.ipynb, and notebooks/filtering.ipynb have some basic steps and plots. Also explored a preliminary GWAS in plink, but ANGSD is the method of choice here- notebooks/plink_assoc.ipynb and notebooks/plot_plink_gwas.ipynb
4. notebooks/ANGSD_genolike.ipynb- bash- calculate genotype likelihoods, output posterior probabilities for GWAS with ANGSD.
5. notebooks/pcangsd.ipynb- bash- PCA of genotype likelihoods from ANGSD, note this is in miniconda environment "pcangsd"! not "commandline"
7. notebooks/populate_fam.ipynb- R- add phenotype data to Plink .fam files for GWAS, also use the output phenotype/metadata files from this code for ANGSD phenotype input.
8. notebooks/ANGSD_assoc.ipynb- bash- run the GWAS analyses.
9. notebooks/plot_pcangsd_assoc.ipynb- R- check out the PCA from PCAngsd, look at genotype likelihoods, maf, and posterior probabilities. Plot the ANGSD association results and evaluate model fit.
10. notebooks/candidates.ipynb- bash- assess potential functions of candidate SNPs
