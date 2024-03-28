



### All code and data used for 

## Analytical Bayesian Framework for Differential Gene Expression Analysis using RNA-Seq Data

by 

Franziska Hoerbst and fellow bayesian friends


# Using bayexpress
All basic functions to use our Bayesian framework for differential gene expression analysis can be found in [bayexpress_function.py].

# Reproducing the Figures in the paper

### Figure 2
In Figure 2 we explore the analytical Bayesian framework using synthetic data. All plots from the paper (and more) can be found in [SIM.ipynb].

### Figure 3
Venn diagrams of identified differentially expressed genes between WT and mutant (Snf2) yeast using _DESeq2_, _edgeR_ and our new Bayesian framework _bayexpress_. The Venn diagrams can be produced with [package_comparison_RALL.ipynb]. RALL stands for Replicates ALL, meaning all 44/42 clean yeast replicates have been used. The data is imported from [DGE_results] which in turn has been carried out via [do_DGE.ipynb].

### Figures 4, 5 and 7
We found the representation in these Figures so useful, we automized it in [stalking_genes.ipynb]. Use the stalk(genes) function to look at one gene ('LSR1') or a list of genes (e.g. ['LSR1', 'YLL039C', 'YJL098W', 'YLL026W']) to get read counts in WT and Snf2 mutant, q-value visualisation, and more. 

In [explore_clean_yeast.ipynb] we identified the example genes we discuss in Figures 4, 5 and 7. 

### Figure 6
Calculating Bayes factors for consistency (nBF) and performing bootstrapping experiments to identify very inconsistent genes (list of genes marked as AOTP = All Over The Place) has been carried out using [explore_clean_yeast_consistency.ipynb]. We explored these sets of genes in later parts of the notebook. 


### Figure 8 a.k.a. the fun section
For the control experiments DGE analysis has only been done in bayexpress. The analysis has been done in [do_DGE.ipynb], we recycled bootstrapping data created for the comparison experiment. The figures have been created in [FUNSECTION_R3.ipynb] for 3 replicates and [FUNSECTION_R10.ipynb] for 10 replicates. 


### Figure S9
Can be reproduced via [explore_clean_yeast.ipynb]

### Figure S10
Can be reproduced via [timing_plots.ipynb]. However, the timings have been measured in do_DGE.ipynb by VScode's built-in function. 


### Figure S11
Can be reproduced via [package_comparison_RALL.ipynb].


### Figure S12 and S13
In Figure S12 and S13 we explore the analytical Bayesian framework using synthetic data a bit further to Figure 2. All plots from the paper (and more) can be found in [SIM.ipynb].


# File by file
[do_DGE.ipynb] is a notebook doing all Differential Gene Expression analysis discussed in the paper. For running DESeq2 and edgeR we are calling R scripts (e.g. 'Do_DGE-DESeq2.R') to carry out the analysis. This is where the parameters for the packages are set. 

For bootstrapping experiments we created 100 shuffled data sets consisting of 3, 6, 12, and 20 replicates of the pool of 44/42 which we used for package comparison. This was done in [comparison_data.ipynb].




All code is written in Python 3.10.6, the conda environment export can be found in [environment.yml].