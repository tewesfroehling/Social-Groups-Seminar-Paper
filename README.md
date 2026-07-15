# Seminar Paper Social Groups

## Research Topic and Goal

**Topic**: 

Influence of Right-Wing-Authoritarianism on Migrant's perceived Deservingness

To what extend do individual Right-Wing-Authoritarianism tendencies influence the deservingness perception regarding migrants? This is researched across all five CARIN criteria, following W. van Oorschot's (2000).

**Hypotheses:**

*H1:* Higher RWA is negatively associated with perceived migrant deservingness across all CARIN dimensions

*H2:* The negative association between RWA and migrant deservingness perception is stronger for norm-proximate dimensions (Control & Identity) than for need-based dimensions (Need).

## Repository Structure

```
Social-Groups-Seminar-Paper/
├── README.md
├── code/                                                    # (Quarto notebooks, ideally run in order)
│   ├── 01_data_exploration_manipulation.qmd                 # data exploration and recoding of variables
│   ├── 02_processed/processed_Dataset_DeConinck_et_al.csv   # fitting multivariate model and analysis
└── data/
    ├── 01_raw/                   
    │   ├── Dataset_DeConick_et_al.csv                       # original dataset
    ├── 02_processed/
    │   ├── processed_Dataset_DeConick_et_al.csv             # processed dataset
    ├── 03_model/  
    │   ├── fit_multivar.rds                                 # saved multivariate model
```

To allow quickly running the code, the model fitted with brms is saves in `data/fit_multivar.rds`. 

To run the full model by going through the fitting process simply delete line 343 (`file = here("data", "03_model", "fit_multivar")`) and delete the `,` in end of the line above.

Should you run into too long computation times, deleting the loo diagnostic code chunk (line 834-839) could help. 


## Tools used: 

The code is made sure to work with R 4.5.2.

The code was not tested with any other versions of R. 

All writing (code and term-paper) was done in Positron additionally using the following plugins:

* Quarto
* AIR - R Language Support
* Citation Picker for Zotero
* Code Spell Checker
* Markdown & Quarto Word Count

Quarto Setup was done using qqs():

Muno, Tristan (2026). qqs: A lightweight R package for streamlined research project setup with Quarto. [https://github.com/dertristan/qqs](https://github.com/dertristan/qqs)

## Ai-use: 

All code directly written by AI is marked in the .qmd files.

Besides that, AI was used for specific trouble-shooting in the code and github and for finding, further understanding and improving existing command options. 

Ai-models used:

* Claude Sonnet 5
* Gemini 3.5 Flash
* Gemini 3.1 Pro

## Source of Dataset:

De Coninck, David; Duque, Maria; Schwartz, Seth; d'Haenens, Leen (2021), “Public attitudes towards immigration, news and social media exposure, and political attitudes from a cross-cultural perspective”, Mendeley Data, V2, doi: [10.17632/8mgpmdstp2.2](https://doi.org/10.17632/8mgpmdstp2.2)