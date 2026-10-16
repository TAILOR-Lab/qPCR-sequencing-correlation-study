# qPCR Sequencing Correlation Study

This repository contains the code, data, and analysis pipelines for the study titled:

*Four Years of Continuous Weekly Wastewater Analysis Reveals Sequencing as a Robust Alternative to PCR for Respiratory Virome Surveillance*

**Authors**: Harihara Prakash, Vasanthi Avadhanula, Michael J. Tisza, Juwan Cormier, Matthew C. Ross, Ryan K. Perez, James D. Chang, Camille R. Mazurek, Jennifer Deegan, Joseph F. Petrosino, Pedro A. Piedra, Justin R. Clark, Eric Boerwinkle, Anthony W. Maresso

**Author for Correspondence**: Dr. Justin R. Clark

**Status**: In Review 

**Link to Manuscript**: <'TBD'>

**Link to Preprint**: [Four Years of Continuous Weekly Wastewater Analysis Reveals Sequencing as a Robust Alternative to PCR for Respiratory Virome Surveillance](https://www.medrxiv.org/content/10.64898/2026.10.13.26364774v1)

This codebase is under active development and may change over time.

In this study, we develop a comparative framework between qPCR and sequencing of 5 known respiratory viruses in wastewater samples collected over 4 years of sampling across Texas. We analyzed samples from over 16 cities and 40 sites across Texas, and assessed the correlation between qPCR abundances with hybrid-capture sequencing abundances, along with statewide clinical cases.

# Repository Structure
```
qPCR-sequencing-correlation-study/
├── method_detection_vs_target_virus/
├── time_series_charts/
├── qPCR_positivity_vs_genome_bin_charts/
├── method_detected_sooner_charts/
├── qPCR_vs_sequencing_scatter_charts/
├── supplementary_tables/
└── README.md
```

# 1. Method detection rates vs. target virus
Folder: ***method_detection_vs_target_virus***

Code used for the visualization of method positivity rate with target respiratory virus.  
Each sample was binned based on whether it was detected by qPCR, sequencing, both or neither methods per target virus.  
Figure generated corresponds to Figure_2 of the manuscript.

Outputs:\
    - .png and .svg chart

# 2. Time-series charts of qPCR, sequencing and clinical outcomes per virus
Folder: ***time_series_charts***

Code used to generate time-series charts highlighting the presence of viral sequencing reads and qPCR copies/ml of each respiratory virus in Texas over 4 years of sampling.  
Clinical case prevalence per virus was also plotted within each viruses chart, and Spearman's rank correlation was computed.  
The raw charts were saved as .svg files and further enhanced with Inkscape.  
Figures generated correspond to Figure 4 and Supp Figure 2 in the manuscript.

Outputs:  
    - .png and .svg time-series plots showcasing sequencing RPKMF and qPCR copies/ml along with clinical ED rates per virus.

# 3. qPCR positivity rate vs. genomic sequencing breadth
Folder: ***qPCR_positivity_vs_genome_bin_charts***

Code used to generate bar charts of qPCR positivity rate vs genomic span bin. Lander-Waterman assumptions were used to measure the genomic breadth of sequenced reads.   
Logistic regression curve was fitted per virus and Odds Ratio was calculated per virus.  
Figures generated correspond to Figure 5 and Supp Figure 3 in the manuscript.

Outputs:  
    - .png and .svg bar charts showcasing qPCR positivity among sequencing positive samples vs genomic bin size

# 4. Identifying which method detected target virus first during start of respiratory illness season
Folder: ***method_detected_sooner_charts***

Code used to generate time-series plot of monthly sequencing and monthly qPCR positivity rates per virus.   
Dumbbell plots were overlaid beneath in Inkscape, and correlation scatter plots of monthly qPCR rate vs monthly sequencing rate were added.  
Figures generated correspond to Figure 6 in the manuscript.

Outputs:  
    - .png and .svg time-series plots showcasing monthly qPCR and sequencing positivity over time.  
    - .png and .svg correlation scatter plots of monthly qPCR positivity rate vs sequencing positivity.  
    - .png and .svg dumbbell plots showcasing which of qPCR and sequencing detected target virus first that October.

# 5. qPCR vs sequencing correlation scatter plots
Folder: ***qPCR_vs_sequencing_scatter_charts***

Code used to generate scatter plots of sequencing vs qPCR outcomes per target virus.  
Two conditions were tested. The first with all samples regardless of detection outcomes. The second with positive only detection outcomes.    
Figures generated correspond to Figure 3 and Supp Figure 1 in the manuscript.

Outputs:  
    - .png and .svg correlation scatter plots of qPCR vs sequencing outcomes per virus.
       
# Dependencies (Project-Wide)
  - Python 3.6+
  - pandas, numpy, matplotlib, SciPy, statsmodels
  - [EsViritu Viral Read Classifier](https://github.com/cmmr/EsViritu)

# Citation

If using this codebase, please cite: 

Prakash, H et al. Four Years of Continuous Weekly Wastewater Analysis Reveals Sequencing as a Robust Alternative to PCR for Respiratory Virome Surveillance

# Contact  
Authors: Justin R. Clark, Harihara Prakash   
Lab: TAILΦR Labs, Baylor College of Medicine

# License

This repository is released under the MIT License.
