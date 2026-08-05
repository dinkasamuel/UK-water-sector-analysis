# Investigating Environmental Investment and Operational Performance in the UK Water Sector

**An MSc Data Science research project by [Dinka Samuel](https://github.com/dinkasamuel)**

> **Project status:** In progress — data collection and source validation  
> **Expected completion:** 7 January 2027

## About this project

I am developing this project as part of my MSc Data Science degree. It brings together my interest in environmental data with a practical question: **when water companies report greater environmental investment, is that investment associated with better operational performance?**

Water companies are expected to invest in infrastructure and environmental improvements, but higher expenditure does not automatically mean that pollution, leakage, customer complaints or compliance outcomes will improve. I want to examine that relationship using company-level data rather than assuming that investment alone leads to better results.

This is a live research repository. I will update it as I collect the data, test its comparability, complete the analysis and develop the final Power BI dashboard. Findings have not yet been produced.

## Aim

To investigate the relationship between environmental investment and operational performance across UK water companies using statistical analysis, predictive modelling and interactive data visualisation.

## Research questions

1. What relationship exists between environmental investment and operational performance in the UK water sector?
2. Which operational performance indicators are most strongly associated with environmental investment?
3. To what extent can statistical and machine-learning models predict operational performance using environmental investment and company characteristics?

## Project objectives

- Build a reliable company-by-year dataset from publicly available regulatory sources.
- Explore how investment and operational performance differ between companies and across time.
- Measure the direction and strength of relationships between environmental investment and selected performance indicators.
- Use mixed-effects modelling to account for repeated observations from the same water companies.
- Develop and evaluate predictive models for operational performance.
- Create a Power BI dashboard that makes the results easier to explore and understand.

## Planned data

The final variables and study period will be confirmed only after the datasets have been checked for consistent definitions, company coverage and reporting periods.

| Data area | Possible measures | Planned source |
|---|---|---|
| Environmental investment | Environmental expenditure, capital investment and related company-level measures | Ofwat reports, regulatory tables and company annual performance reports |
| Operational performance | Leakage, supply interruptions, sewer flooding and other performance commitments | [Ofwat Water Company Performance data](https://www.ofwat.gov.uk/regulated-companies/company-obligations/outcomes/water-company-performance-report-2024-25/) |
| Environmental performance | Pollution incidents, compliance measures and Environmental Performance Assessment ratings | [Environment Agency environmental performance data](https://www.gov.uk/government/publications/water-and-sewerage-companies-in-england-environmental-performance-report-2024) |
| Customer experience | Complaint volumes, complaint rates and satisfaction measures | [Consumer Council for Water performance publications](https://www.ccw.org.uk/publication/water-mark-2025/) |
| Company characteristics | Company, reporting year, service type and other relevant controls | Regulatory and company publications |

### Important coverage note

The working title refers to the UK water sector, but the principal regulators do not all cover the same geography. Ofwat reports on companies in England and Wales, while the Environment Agency dataset covers England. The final empirical scope may therefore be narrower than the title suggests. I will define the study population after completing the data-compatibility assessment and explain any exclusions.

## Planned methodology

### 1. Data collection and validation

I will record the source, reporting period, unit, definition and licence or reuse terms for every dataset. Company names and reporting periods will be standardised before datasets are joined.

### 2. Data cleaning and integration

Python will be used to identify missing values, duplicates, inconsistent units and changes in reporting definitions. Both raw and processed data will be documented so that each transformation can be traced.

### 3. Exploratory data analysis

Summary statistics and visualisations will be used to examine distributions, trends, outliers, missingness and differences between companies. This stage will also determine whether variables need to be normalised or transformed.

### 4. Statistical analysis

Correlation analysis will provide an initial view of the relationships between investment and performance measures. Mixed-effects models will then be used to account for the repeated company-level observations across years. The model specification will depend on the structure and distribution of the final outcomes.

### 5. Predictive modelling

Suitable regression and machine-learning models will be compared using a baseline model and more flexible alternatives. Validation will respect the grouping and time structure of the data where ordinary random splitting would risk information leakage.

### 6. Dashboard development

The final Power BI dashboard will allow users to explore investment trends, compare company performance and view the main statistical and predictive findings.

## Evaluation plan

The planned evaluation includes:

- Correlation coefficients, uncertainty estimates and significance tests where appropriate
- Marginal and conditional \(R^2\), AIC, BIC and residual diagnostics for mixed-effects models
- MAE, RMSE and \(R^2\) for predictive models
- Train-test evaluation and cross-validation suited to the final panel structure
- Accuracy, functionality, usability and clarity checks for the Power BI dashboard

These measures will be interpreted together. No single metric will be treated as sufficient evidence that a model is useful or valid.

## Tools and technologies

- **Python:** data cleaning, analysis, statistical modelling and machine learning
- **pandas and NumPy:** data preparation and calculation
- **Matplotlib and Seaborn:** exploratory and explanatory visualisation
- **statsmodels:** statistical and mixed-effects modelling
- **scikit-learn:** predictive modelling and model evaluation
- **Jupyter Notebook:** transparent, step-by-step analysis
- **Power BI:** interactive dashboard development
- **Git and GitHub:** version control, documentation and progress tracking

The final package list will be recorded in `requirements.txt` once the modelling workflow has been confirmed.

## Planned repository structure

The repository will separate source data, reusable code, notebooks and final outputs so that the analysis remains easy to follow.

```text
uk-water-sector-analysis/
├── README.md
├── LICENSE
├── .gitignore
├── requirements.txt
├── data/
│   ├── README.md
│   ├── raw/
│   └── processed/
├── notebooks/
│   ├── 01_data_collection.ipynb
│   ├── 02_data_cleaning.ipynb
│   ├── 03_exploratory_analysis.ipynb
│   ├── 04_statistical_modelling.ipynb
│   └── 05_predictive_modelling.ipynb
├── src/
│   ├── data_cleaning.py
│   ├── analysis.py
│   └── modelling.py
├── visuals/
├── dashboard/
├── reports/
└── references/
```

Raw datasets will only be committed when their licences and file sizes permit redistribution. Otherwise, the repository will provide source links and reproducible download instructions.

## Project timeline

| Stage | Planned period | Current position |
|---|---|---|
| Project initiation and planning | 2–31 July 2026 | Completed |
| Data collection | 1–20 August 2026 | In progress |
| Data cleaning and integration | 21 August–30 September 2026 | Not started |
| Exploratory data analysis | 1–15 October 2026 | Not started |
| Statistical modelling | 16 October–15 November 2026 | Not started |
| Predictive modelling and validation | 16 November–10 December 2026 | Not started |
| Power BI dashboard | 11 November–22 December 2026 | Not started |
| Evaluation, interpretation and writing | 23 December 2026–7 January 2027 | Not started |

## Results

Results will be added after the data has been validated and the analyses have been completed. This section will eventually contain:

- Main statistical findings
- Model performance comparisons
- Clear visual summaries
- Dashboard screenshots or access information
- Practical interpretation and limitations

## Research integrity, ethics and privacy

This study uses secondary data from publicly available sources and does not intend to collect personal or confidential information. Sources will be acknowledged, and the data will be handled in line with UWE research ethics guidance and the relevant providers' reuse terms.

The public repository will not include my student ID, private university documents, credentials or restricted data.

## Interpretation and limitations

The observational design can identify relationships and predictive patterns, but it does not automatically establish that investment **causes** changes in performance. Company size, regional conditions, infrastructure age, regulatory requirements, reporting changes and time delays between spending and outcomes may affect the results. These issues will be assessed and reported openly.

## Licence

Code created for this project is intended to be released under the MIT Licence. Third-party datasets and publications remain subject to their original providers' terms and are not covered by the repository's software licence.

## Author

**Dinka Samuel**  
MSc Data Science student with interests in data analytics, environmental data, machine learning, data governance and clear data storytelling.

[GitHub profile](https://github.com/dinkasamuel)
