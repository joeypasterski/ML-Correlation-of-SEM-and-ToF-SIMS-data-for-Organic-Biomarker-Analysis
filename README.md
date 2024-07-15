# ML-Correlation-of-SEM-and-ToF-SIMS-data-for-Organic-Biomarker-Analysis
Code for the manuscript "Machine Learning Correlation of Electron Micrographs and ToF-SIMS  for the Analysis of Organic Biomarkers in Mudstone"

## General Descirptions and Notes on ToF-SIMS ML Code

- This code performs supervised ML on ToF-SIMS data sets. There are multiple steps to data curation performed here. All ToF-SIMS data was integrated outside of R and the values for integration were imported for supervised ML. 
-- Peak height and peak area data were recorded for each of the curated peaks listed in "Creating Dataframes" section of this code.  
- min_lab labels were defined from via unsupervised ML on SEM-EDS datasets in the code folder "ML_sem_eds_unsupervised.Rmd"
-- In this doc, each min_lab has it's own corresponding data table in the home folder. 
- Personal progress was tracked the "Project Log" notepad doc. 

### Importing the data

- Here I create a "full" dataset of all of the integrated peaks
-- Data is located in the tof_sims_data folder
-- This dataset is in long form
-  First each dataset is imported, then columns are selected, the min_lab column column is then appended, and all columns are then combine into two final documents (peak area and peak height datasets)
