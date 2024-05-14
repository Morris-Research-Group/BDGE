There are 2 papers related to the work in this repository, here is a description what to find where from which paper. 

-----------------------------


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


### Figure 4
Plot q-plots gene by gene and find the examples from the paper in [example_genes.ipynb]. For more detailed analyses we also created the stalk(genes) function to look at one gene ('LSR1') or a list of genes (e.g. ['LSR1', 'YLL039C', 'YJL098W', 'YLL026W']) to get read counts in WT and Snf2 mutant, q-value visualisation, and more [stalking_genes.ipynb].

### Figure 5 and 6
In Figure 5 and 6 we explore the analytical Bayesian framework using synthetic data a bit further to Figure 2. All plots from the paper (and more) can be found in [SIM.ipynb].

### Figure 7
Can be reproduced via [package_comparison_RALL.ipynb].

### Figure 8
Can be reproduced via [investigating_length_bias.ipynb].


-----------------------------


### All code and data used for 

## What is a differentially expressed gene?

by 

Franziska Hoerbst and fellow bayesian friends


### Figures 1, 2 and 3
We found the representation in these Figures so useful, we automized it in [stalking_genes.ipynb]. Use the stalk(genes) function to look at one gene ('LSR1') or a list of genes (e.g. ['LSR1', 'YLL039C', 'YJL098W', 'YLL026W']) to get read counts in WT and Snf2 mutant, q-value visualisation, and more. 

In [explore_clean_yeast.ipynb] we identified the example genes we discuss in Figures 1, 2 and 3. 

### Figure 6
Calculating Bayes factors for consistency (nBF) and performing bootstrapping experiments to identify very inconsistent genes (list of genes marked as AOTP = All Over The Place) has been carried out using [explore_clean_yeast_consistency.ipynb]. We explored these sets of genes in later parts of the notebook. 

### Figure 4 + 6, 7, 8: Control experiment
For the control experiments DGE analysis has only been done in bayexpress. The analysis has been done in [do_DGE.ipynb], we recycled bootstrapping data created for the comparison experiment. The figures have been created in [CONTROL_R3_BF1.ipynb], [CONTROL_R3_BF10.ipynb], and [CONTROL_R3_BF100.ipynb] for 3 replicates and [CONTROL_R10_BF1.ipynb], [CONTROL_R10_BF10.ipynb], and [CONTROL_R10_BF100.ipynb] for 10 replicates. 

### Figure 5
Can be reproduced via [explore_clean_yeast_consistency.ipynb].



# File by file
[do_DGE.ipynb] is a notebook doing all Differential Gene Expression analysis discussed in the paper. For running DESeq2 and edgeR we are calling R scripts (e.g. 'Do_DGE-DESeq2.R') to carry out the analysis. This is where the parameters for the packages are set. 

For bootstrapping experiments we created 100 shuffled data sets consisting of 3, 6, 12, and 20 replicates of the pool of 44/42 which we used for package comparison. This was done in [comparison_data.ipynb].

All code is written in Python 3.10.6, the conda environment export can be found in [environment.yml].