# ML-Correlation-of-SEM-and-ToF-SIMS-data-for-Organic-Biomarker-Analysis
Code for the manuscript "Machine Learning Correlation of Electron Micrographs and ToF-SIMS  for the Analysis of Organic Biomarkers in Mudstone"

## General Descriptions and Notes on SEM-EDS and ToF-SIMS ML Code
### Unsupervised ML on SEM-EDS Data
- The ML_sem_eds_unsupervised code is used for a statistical analysis on the compositional variability in the mudstone sample, with a specific interest on determining potential drivers of variability in the presence of both organic carbon and detectable organic biomarkers. Labels created using unsupervised ML performed on the SEM-EDS datasets are then applied to the ToF-SIMS datasets for supervised ML.
  - min_lab labels defined from via unsupervised ML on SEM-EDS datasets include: 
    - org_0_20, org_20_40, org_40_60, org_60_100, S_rich, P_rich, Ca_rich, epoxy
    - "org_" values are wt% C in those regions; S_, P_, and Ca_rich are sulfur, phosphorous, and calcium rich measurement, epoxy was used to prepare the sample.
### Supervised ML on ToF-SIMS Data
- The ML_tof_sims_supervised code is designed to test the ability of supervised ML algorithms to classify the ToF-SIMS spectra by composition.
  - Composition includes the labels assigned via SEM-EDS, the presence of ToF-SIMS detectable biomarkers, or an "organic" or "inorganic" label assigned via SEM-EDS datasets.  
- For supervised ML on ToF-SIMS data sets, there are multiple steps to data curation performed. All ToF-SIMS peak integration was performed outside of R and values were imported for supervised ML. 
  - Peak height and peak area data were recorded for each of the curated peaks listed in "Creating Dataframes" section of this code.

- Personal progress for all analysis was tracked in a "Project Log" doc available upon request. 

### Notes the Data
Each data set is within the respective data folder
- These data are pre-processed to some degree, but are largely representative of the raw data.
SPecific notes on the SEM-EDS dataset
- Spot, mineralogy, and location variables need to be factors
- Spot 10 and spot 11 are the same location (improper naming in early analysis)
- For this publication, spots were renamed for clarity. 
_____Labels Key______
Publication number: This code number
Spot 1: Spot 15
Spot 2: Spot 16
Spot 3: Spot 9
Spot 4: Spot 10

Specifics notes on importing the ToF-SIMS data
- The data is in the form of a "full" dataset of all of peak integration and peak height data.
  - Again, peak integration was performed in a separate program (OriginPro).
