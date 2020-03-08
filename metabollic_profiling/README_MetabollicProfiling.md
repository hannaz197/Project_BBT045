The metabollic profiling was done using textfiles containing GeneIDs as well as statistical data. Since the original study used manually curated values and some other features when doing their profiling, it was decided that new references for the original study were needed. These were made from the processed RNA-seq data found in Table 1 amongst the "supporting information" files in the original study. To get the reference files the following steps were done;

1.  select columns corresponding to the "GeneID" and the statistical values (log changes, basemeans, p-values) from the original processed fields
2. Sort column based on smallest to largest padj for a given condition

3. Select containing all column values where the padj < 0.05, including GeneID, "baseMean"	"baseMeanA"	"baseMeanB"	"foldChange"	"log2FoldChange"	"pval"	"padj" from each conditon. Create a txt-file from these values (found in Project_BBT045/metabollic_profilling folder on this GitHub). 

# Follwing steps are regardless if its actual data analyzed or references, where the actual data should have the same format as the txt-file found in the directory (with  GeneID, "baseMean"	"baseMeanA"	"baseMeanB"	"foldChange"	"log2FoldChange"	"pval"	"padj"). 

4. Open https://biocyc.org/overviewsWeb/celOv.shtml, with the reference organism "Salmonella enterica serovar Typhi str. CT18", and go to Metabolism>Cellular Overvier > Overlay Experimental Data (Omics Viewer)

5. Use the "Upload Data from File", and paste the txt-file for the given gene condition in the experimental data field. 
6. Choose column '5' corresponding to the log2FC, and generate the map. 

NOTE: all steps above are done using default settings, with no changes. 
