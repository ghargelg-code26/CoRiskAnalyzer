# CoRiskAnalyzer

CoRiskAnalyzer explores the Patient_Comorbidity_Risk_Assessment_Dataset to investigate clinical risk factors related to heart attack and mortality. The project uses a notebook-based workflow for data cleaning, feature engineering, and visualization, making it easier to explore patterns and test health-related hypotheses.

## Dataset Content
The dataset contains patient-level information related to comorbidities, lifestyle factors, and clinical risk indicators. It includes variables such as BMI, smoking status, blood pressure, physical activity, diabetes, medication adherence, and risk percentages used for analysis and hypothesis testing.

- Source: https://www.kaggle.com/datasets/velvetcrystal/patient-comorbidity-risk-assessment-dataset
- Size: Approximately 10,000 rows with multiple clinical and lifestyle features

## Business Requirements
CoRiskAnalyzer is designed for educational purposes to help learners understand and explore key clinical and lifestyle factors associated with cardiovascular risk. The project provides insights into how variables such as BMI, family history, smoking, blood pressure, physical activity, diabetes, and medication adherence relate to heart attack and mortality risk.

The analysis supports learning by identifying patterns, highlighting risk factors, and presenting findings through simple visualizations and notebook-based exploration.

## Hypothesis and how to validate

- Higher BMI is associated with higher `Heart_Attack_Risk_Percentage`.
- Positive `Family_History_CVD` is associated with higher `Heart_Attack_Risk_Percentage`.
- High BMI and family history together are associated with elevated heart attack risk.
- Current smoking is associated with higher `Heart_Attack_Risk_Percentage`.
- High `Systolic_BP` (>= 140) is associated with higher `Mortality_Risk_Percentage`.
- Low physical activity is associated with higher heart attack and mortality risk.
- `Diabetes` is associated with higher `Mortality_Risk_Percentage`.
- Low medication adherence is associated with higher `Mortality_Risk_Percentage`.

To validate these hypotheses, the notebook compares the average risk percentages across relevant groups using summary statistics, visualizations, and exploratory analysis. For example, BMI categories can be compared with bar plots, binary factors such as family history or smoking can be examined through grouped summaries, and continuous measures such as blood pressure can be evaluated by splitting values into meaningful ranges.

## Project Plan
1. Load and inspect the clinical dataset to understand its structure and variables.
2. Clean the data by handling missing values and preparing appropriate data types.
3. Engineer simple features such as BMI categories and risk flags for easier analysis.
4. Explore and validate the core hypotheses through grouped summaries and visualizations.
5. Document the workflow, findings, and next steps in the notebook and README.

## The rationale to map the business requirements to the Data Visualisations
The project is designed as an educational analysis of cardiovascular risk factors, so the visualizations are chosen to make complex clinical relationships easier to understand. Bar charts are used to compare average risk across categories, while violin and box plots help show distributions and differences between groups. This directly supports the business requirement of making patterns in the data clear, interpretable, and easy to communicate.

## Analysis techniques used
- Data cleaning and missing value handling
- Type conversion and feature engineering
- Grouped summary statistics using pandas
- Exploratory data visualization with seaborn and matplotlib
- Comparison of risk outcomes across clinical and lifestyle variables

## Unfixed Bugs
- Some notebook cells rely on the working directory being set correctly for file loading.
- Plot formatting may need minor adjustments depending on the environment or display size.
- If the dataset is updated, some categorical assumptions may need to be reviewed.

## Development Roadmap
- Improve notebook reproducibility and documentation.
- Add more statistical validation such as simple comparisons or confidence intervals.
- Expand the analysis with additional visualizations and feature engineering.
- Consider turning the workflow into a small interactive dashboard in the future.

## Main Data Analysis Libraries
- pandas for data manipulation and summaries
- numpy for numerical operations
- matplotlib for static plotting
- seaborn for visual exploration and statistical charts
- jupyter for notebook-based analysis

### Content
The repository contains the dataset, notebook-based analysis workflow, and supporting documentation for exploring cardiovascular risk factors and validating the project hypotheses.

### Media
The project uses charts and plots such as bar charts, box plots, and violin plots to communicate patterns in heart attack and mortality risk across different patient characteristics.

## AI Usage
This project was supported with AI-assisted tools during development to help structure the analysis workflow, refine the notebook explanations, and improve the clarity of the README documentation. The core analysis and visualizations were still completed using Python libraries such as pandas, numpy, matplotlib, and seaborn.

## Files
- `data/Patient_Comorbidity_Risk_Assessment_Dataset.csv` — dataset.
- `analysis_predict_hypotheses.ipynb` — notebook that performs ETL, feature engineering, and hypothesis visualizations using only numpy & pandas.

## How to run
1. Activate the project's venv (Windows PowerShell):

```powershell
.venv\Scripts\Activate.ps1
```

2. Install dependencies (if not already installed):

```powershell
python -m pip install -r requirements.txt
```

or directly:

```powershell
python -m pip install pandas numpy matplotlib seaborn
```

3. Open and run `analysis_predict_hypotheses.ipynb` or `etl_bmi_family_analysis.ipynb` in VS Code/Jupyter to view analysis and visualizations.

## Credits
- The credits goes to code Institute staff for their support and learning guidance and resources provided for achieving this knowledge for demonstarting data analysis project.

### Acknowledgements

my acknowledgement goes to vasi.pavaloi@codeinstitute.net & Rory Patrick sheridian for Guidance and support.

## Notes & next steps
- The notebooks now focus on data analysis with pandas and numpy, while still capturing modeling insights.
- For deeper validation, consider cross-validation, additional feature engineering, and clearer metric comparison across hypotheses.

## Conclusion
This project demonstrates how clinical risk hypotheses can be evaluated with a notebook-first workflow using pandas and numpy. The analysis highlights relationships between BMI, family history, smoking, blood pressure, activity level, diabetes, medication adherence, and risk percentages. The notebooks are designed to be easy to run and extend without requiring heavy modeling dependencies.