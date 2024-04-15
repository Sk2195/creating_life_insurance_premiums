Introduction
- The goal of this research is to create a model that will evaluate the risk of mortality based on personal traits and outside factors. This model's output is used to compute and compare insurance premiums efficiently, offering vital information for insurance pricing tactics.

# Datasets
- The dataset
  
## Variables and Descriptions

| Variable            | Description                                                                                                           |
|---------------------|-----------------------------------------------------------------------------------------------------------------------|
| `ID`                | Unique identification code of the policy/insured (an integer number).                                                 |
| `Gender`            | Gender of the insured (M = male, F = female).                                                                         |
| `Birth_Date`        | Date of birth of the insured (DD/MM/YYYY).                                                                             |
| `Effective_Date`    | Effective start date of the contractual relationship between the insurance company and the insured (DD/MM/YYYY).       |
| `Capital`           | Capital at risk, to be received by beneficiaries when the insured person dies (in €).                                  |
| `Renewal_Date`      | Date of renewal during the year of the insurance contract (DD/MM/YYYY).                                                |
| `Age`               | Exact age of the insured, measured in years, at the renewal date (a real number). The time elapsed since the date of birth. |
| `t`                 | Fractional age in years (0≤t<1) of the insured at the moment of the Renewal_Date.                                       |
| `Age_Actuarial`     | Age of the insured, measured in whole years, obtained by rounding approximating his/her exact age to the closest integer. |
| `Birthday`          | Birthday date in 2009 (DD/MM/YYYY).                                                                                    |
| `x`                 | Time elapsed in years (0≤x<1) between the start of the year and the moment of the Renewal_Date.                         |
| `r`                 | Aging quarter (1 = 1Q, 2= 2Q, 3 = 3Q, 4 = 4Q). Age-quarter of the insured at the time of renewal.                       |
| `s`                 | Seasonal quarter (1 = Winter, 2= Spring, 3= Summer and 4=Autumn). Season-quarter of the moment of renewal.             |
| `Age_actuarial_quarter` | Age of the insured, measured in years, after approximating his/her exact age to the closest integer age-quarter.     |
| `Month`             | Month of renewal date (1 = January, 2 = February, etc.).                                                               |

# Installation:
- Clone this repositiory: https://github.com/Sk2195/creating_life_insurance_premiums/tree/main

  # Project Folder
## Folder Structure
```
Mortality-Risk-Assessment-Model/
├── data/
│   ├── raw/                        # Contains the initial, unprocessed datasets
│   └── processed/                  # Contains datasets after cleaning and processing
│
├── src/
│   ├── task1/
│   │   ├── eda/                    # Scripts for exploratory data analysis
│   │   │   └── data_visualization.ipynb
│   │   └── data_cleaning/          # Scripts for data cleaning
│   │       └── clean_data.ipynb
│   │
│   └── task2/
│       ├── preprocessing/          # Scripts for data preprocessing
│       │   └── preprocess_data.ipynb
│       ├── feature_engineering/    # Scripts for feature engineering
│       │   └── engineer_features.ipynb
│       └── modeling/               # Scripts for modeling
│           └── model_training.ipynb
│
├── docs/                           # Documentation files
│   └── model_documentation.md
│
├── tests/                          # Automated tests for the project
│   └── test_models.py
│
├── .gitignore                      # Specifies intentionally untracked files to ignore
├── requirements.txt                # All necessary dependencies for the project
└── README.md                       # The README file for the project

