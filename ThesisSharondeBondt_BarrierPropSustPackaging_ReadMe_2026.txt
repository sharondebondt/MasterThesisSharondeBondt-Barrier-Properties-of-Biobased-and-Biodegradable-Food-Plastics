============================================================================================================
START readme
============================================================================================================

This file focuses on the details of the data package. For 'administrative' metadata on this data,
please view the metadata files within the parent folder of this data package (where this readme file
is also found).

The materials described in this readme are all published in Zenodo.


============================================================================================================
# General
============================================================================================================

- Author(s): Sharon de Bondt (1049429)
- Project: "Barrier Properties of Biobased and Biodegradable Food Plastics: a Systematic Review"
- Supervisor: Deniz Turan-Kunter
- Institution: Wageningen University and Research (WUR)
- Chair Group: Food Quality and Design (FQD)
- Contact: sharon.debondt@wur.nl
- DOI: https://doi.org/10.5281/zenodo.19350674


============================================================================================================
# Title
============================================================================================================

"Barrier Properties of Biobased and Biodegradable Food Plastics: a Systematic Review".


============================================================================================================
# TableOfContents
============================================================================================================

- General
- Title
- TableOfContents
- Methods
    - Introduction
    - Description
- FolderStructure
- FolderContents
- FileFormats
- CodeBook
- ResearchSoftware
    - RSLanguage
    - RSRequirements
    - RSInstallation
    - RSOperatingInstructions
- Citation
- Other


============================================================================================================
# Methods
============================================================================================================

## Introduction

 This systematic review compares the barrier properties of biobased and biodegradable packaging materials with those of conventional plastics, following the PRISMA framework. In addition, this review compares these barrier properties to different food category requirements. 
The review focuses on water the transmission rates of water vapour, oxygen and carbon dioxide of biodegradable and/or biobased polymers normalized for a thickness of 100 µm (WVTR₁₀₀, OTR₁₀₀, and CO₂TR₁₀₀. )

Please view https://doi.org/10.5281/zenodo.19350674 for added information on materials and methods.


## Description

- Article Collection:

 A structured search query was designed to capture studies on biobased or biodegradable polymers
  with relevant barrier properties for food packaging. The search was conducted in the SCOPUS
  database (24 November 2025 - 4 January 2026) and limited to peer-reviewed, open-access articles
  published in English between 2024 and 2025. 
The search returned 93 unique articles.

- Article screening:

Articles were screened in two stages following the PRISMA framework (Page et al., 2021). In the
  first stage, articles were assessed on title and abstract for relevance. In the second stage,
  full-text screening was performed. Studies were excluded if they did not report test conditions
  for barrier properties, focused on multilayer/composite/active materials, or lacked quantitative
  barrier data. Each remaining article was assessed for methodological quality using a seven-item
  appraisal rubric scored on a 0-1 scale. Articles with a quality score below 0.8 were excluded.
  After screening, 19 studies met all inclusion criteria.

- Data extraction:

From the 19 included studies, data were extracted into a structured Excel dataset following FAIR
  principles (Wilkinson et al., 2016). For each material entry, the following was recorded: polymer
  name, type, and material family; biobased and biodegradable status; additives and processing
  method; barrier properties (OTR, CO2TR, WVTR, and corresponding permeability values PO2, PCO2,
  WVP); measurement conditions (temperature, relative humidity, film thickness, test standard); and
  reference polymer data where reported. The dataset was imported into Python for cleaning and
  standardisation, including correcting data types, standardising terminology, and verifying values
  against the original publications.

- Data analysis

 Transmission rate values were standardised to a film thickness of 100 µm (denoted WVTR100,
  OTR100, CO2TR100) to enable cross-study comparison. Unit conversions are documented in the
  ConversionFactors sheet. The standardised dataset was analysed using exploratory data analysis,
  including descriptive statistics, scatter plots, heatmaps, and bar charts. Barrier values were
  compared between biobased and conventional reference polymers and evaluated against barrier
  requirements for different food categories. All code for data processing and visualisation was
  documented to ensure reproducibility.

============================================================================================================
# FolderStructure
============================================================================================================

- BarrierProperties_SharondeBondt
-- ThesisSharondeBondt_BarrierPropSustPackaging_ReadMe_2026.txt
-- ThesisSharondeBondt_Report_BarrierPropSustPackaging_vfinal_2026.docx
--- Data
---- ThesisSharondeBondt_RawData_BarrierPropSustPackaging_vRAW_2026
---- ThesisSharondeBondt_Data_BarrierPropertiesSustPackaging_vfinal_2026.xlsx
--- Scripts
---- ThesisSharondeBondt_Coding_Visualizing_vfinal_2026.ipynb
---- ThesisSharondeBondt_Coding_DataCleaning_vfinal_2026.ipynb
--- AI Prompts
---- ThesisSharondeBondt_AIPrompts_coding_Datacleaning_Claude_2026.pdf
---- ThesisSharondeBondt_AIPrompts_coding_Visualizations_Claude_2026.pdf
---- ThesisSharondeBondt_AIPrompts_coding_Visualizations_Gemini_2026.pdf
---- ThesisSharondeBondt_AIPrompts_sparring_differencesTRandP_ChatGPT_2026.pdf
---- ThesisSharondeBondt_AIPrompts_sparring_organizationalframeworks_ChatGPT_2026.pdf
---- ThesisSharondeBondt_AIPrompts_sparring_Startup_ChatGPT_2026.pdf
---- ThesisSharondeBondt_AIPrompts_Sparring_Visualizations_Claude_2026.pdf
---- ThesisSharondeBondt_AIPrompts_UnitConversions_Claude_2026.pdf



============================================================================================================
# FolderContents
============================================================================================================

-- ThesisSharondeBondt_BarrierPropSustPackaging_ReadMe_2026.txt
This file. Documents the contents, structure, and usage of the data package.

-- ThesisSharondeBondt_Report_BarrierPropSustPackaging_vfinal_2026.docx
The full thesis report for the systematic review.

--- Data/
Contains the raw and processed datasets.

---- ThesisSharondeBondt_RawData_BarrierPropSustPackaging_vRAW_2026.xlsx
The unprocessed dataset as extracted from the literature, prior to data cleaning and unit
standardisation. Contains two sheets:
  - Data: raw extracted barrier property values and metadata.
  - Critical appraisal: quality appraisal scores per screened study.

---- ThesisSharondeBondt_Data_BarrierPropertiesSustPackaging_vfinal_2026.xlsx
An Excel workbook containing six sheets:
  - ReadMe: brief overview of the workbook structure and how to read each sheet.
  - Data: extracted barrier property values and metadata for all screened and included studies
  - ConversionFactors: dimensional conversion factors for standardising barrier property units.
  - CriticalAppraisal: quality appraisal scores per included study.
  - LookUps: controlled vocabulary for categorical variables used in the Data sheet.
  - CodeBook: codebook documenting all column names, units, abbreviations, and data points.

--- Scripts/
Contains the Jupyter notebooks used for data processing and figure generation.

---- ThesisSharondeBondt_Coding_DataCleaning_vfinal_2026.ipynb
Notebook for data cleaning, unit conversion, and standardisation.

---- ThesisSharondeBondt_Coding_Visualizing_vfinal_2026.ipynb
Notebook for generating figures and performing analyses.

--- AI Prompts/
Contains PDF exports of AI-assisted conversations used during the project, organised by
purpose (coding, sparring) and tool (Claude, ChatGPT, Gemini).

---- ThesisSharondeBondt_AIPrompts_coding_Datacleaning_Claude_2026.pdf
AI-assisted coding for data cleaning and standardisation (Claude).

---- ThesisSharondeBondt_AIPrompts_coding_Visualizations_Claude_2026.pdf
AI-assisted coding for figure generation (Claude).

---- ThesisSharondeBondt_AIPrompts_coding_Visualizations_Gemini_2026.pdf
AI-assisted coding for figure generation (Gemini).

---- ThesisSharondeBondt_AIPrompts_sparring_differencesTRandP_ChatGPT_2026.pdf
Conceptual discussion on differences between transmission rate and permeability (ChatGPT).

---- ThesisSharondeBondt_AIPrompts_sparring_organizationalframeworks_ChatGPT_2026.pdf
Conceptual discussion on organisational frameworks for the project setup (ChatGPT)

---- ThesisSharondeBondt_AIPrompts_sparring_Startup_ChatGPT_2026.pdf
Conceptual discussion on project setup and initial direction (ChatGPT).

---- ThesisSharondeBondt_AIPrompts_Sparring_Visualizations_Claude_2026.pdf
Conceptual discussion on visualisation design and approach (Claude).

---- ThesisSharondeBondt_AIPrompts_UnitConversions_Claude_2026.pdf
AI-assisted development of unit conversion factors (Claude).


============================================================================================================
# FileFormats
============================================================================================================

- .txt
- .xlsx
- .docx
- .ipynb
- .pdf

============================================================================================================
# CodeBook
============================================================================================================

Please view the CodeBook sheet within ThesisSharondeBondt_SystematicReview_Data_vfinal.xlsx for
documentation of all column names, units, abbreviations, and data point descriptions used in this
dataset. The CodeBook contains 152 entries describing each variable in the Data sheet.


============================================================================================================
# ResearchSoftware
============================================================================================================

## RSLanguage

Data processing and figure generation scripts are written in Python (Jupyter Notebook).


## RSRequirements

- Python 3.x
- Jupyter Notebook
- Microsoft Excel (for viewing and editing the .xlsx data files)

- Python libraries
    - pandas
    - numpy
    - matplotlib
    - seaborn
    - plotly
    - openpyxl
    - Pillow


## RSInstallation

Python is open source and freely available at https://www.python.org/. Required libraries can be
installed via pip:

pip install jupyter pandas numpy matplotlib seaborn plotly openpyxl Pillow


## RSOperatingInstructions

The scripts can be run as is when the current folder structure is maintained after download of these
data. All file paths within the scripts are relative to the project directory.


============================================================================================================
# Citation
============================================================================================================

The materials described here are all published in Zenodo. Please view the information at the Zenodo DOI
(https://doi.org/10.5281/zenodo.19350674) to find the citation information.


============================================================================================================
# Other
============================================================================================================

Please view the associated metadata and codebook files within the data package (where you found this
readme file).

If you find any errors within the data or scripts, please contact sharon.debondt@wur.nl.


============================================================================================================
END readme
============================================================================================================
