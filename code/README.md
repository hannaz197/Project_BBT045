# Code used in the project
# These codes correspond to a mixture of individual team members R-code, along with the final, merged code used to generate the results. # The steps in the data analysis involved:
# 1. Loading raw counts obtained from artremis
# 2. Extract columns only corresponding with the total counts, dismissing the sense/antisense counts.
# 3. Run DESeq analysis according to the procedure outline in;

vignette('DESeq')

# which gives the following link: http://15.236.44.5:8787/files/R/x86_64-pc-linux-gnu-library/3.6/DESeq/doc/DESeq.pdf where the steps taken included, following making of the condition factor described in the documentation; making the newCountDataSet(counts, condition/times), estimation of size factors for the TMM normalization used by DESeq and the dispersion estimation. Running a negative binomial test, the padj with FDR < 0.05 was calculated along with fold-changes, and the significant genes extract for all three time points. 

# The differentially expressed genes where then analyzed using visualization tools such as a hierarchical clustring, a venn diagramme and a dot-plot, and their functions analyzed by doing a metabollic profiling.

