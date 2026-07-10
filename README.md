# CoRiskAnalyzer

CoRiskAnalyzer analyzes the `Patient_Comorbidity_Risk_Assessment_Dataset.csv` to test several clinical risk hypotheses. It includes two notebooks: one reproduces the model workflow using pandas and numpy, and another performs ETL and hypothesis visualizations using pandas, numpy, matplotlib, and seaborn.

## Hypotheses
- Higher BMI is associated with higher `Heart_Attack_Risk_Percentage`.
- Positive `Family_History_CVD` is associated with higher `Heart_Attack_Risk_Percentage`.
- High BMI and family history together are associated with elevated heart attack risk.
- Current smoking is associated with higher `Heart_Attack_Risk_Percentage`.
- High `Systolic_BP` (>= 140) is associated with higher `Mortality_Risk_Percentage`.
- Low physical activity is associated with higher heart attack and mortality risk.
- `Diabetes` is associated with higher `Mortality_Risk_Percentage`.
- Low medication adherence is associated with higher `Mortality_Risk_Percentage`.

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

## Notes & next steps
- The notebooks now focus on data analysis with pandas and numpy, while still capturing modeling insights.
- For deeper validation, consider cross-validation, additional feature engineering, and clearer metric comparison across hypotheses.

## Conclusion
This project demonstrates how clinical risk hypotheses can be evaluated with a notebook-first workflow using pandas and numpy. The analysis highlights relationships between BMI, family history, smoking, blood pressure, activity level, diabetes, medication adherence, and risk percentages. The notebooks are designed to be easy to run and extend without requiring heavy modeling dependencies.