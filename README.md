# ClownfishGWAS
Katrina Catalano's data and code for project investigating associations between larval traits and genotypes from Expressed Exome Capture Sequencing in Amphiprion percula. Using miniconda environment "commandline" on Annotate.
1. demultiplex.ipynb- download sequencing data from Princeton Genomics Core, check read counts, demultiplex based on PCR index and inline adapter barcodes and perform basic reead quality trimming.
2. qc_seq.ipynb- screen for contamination, check read quality, map to reference genome, mark and remove duplicates, merge bam files, call genotypes.
3. genolike_imputation.ipynb- imputation, calculate genotype likelihoods.
4. filtering.ipynb- filter genotypes for GWAS.
5. populate_fam.ipynb- add phenotype data to Plink .fam files for GWAS.
