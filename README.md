# Evaluating Diabetes, Metabolic Dysfunction, and Lifestyle Indicators for Early Liver Injury Risk Stratification
A Population-Level Feasibility Study Using NHANES

**Project Overview**

This repository contains the analytical workflow for a population-level feasibility study assessing whether diabetes-related markers, metabolic dysfunction indicators, and lifestyle factors can be used to stratify risk of early liver injury using data from the National Health and Nutrition Examination Survey (NHANES).

The study is explicitly framed as a risk stratification and early warning feasibility analysis, not as a diagnostic or disease prediction model. Given the absence of direct early-stage liver cancer labels in NHANES, a clinically motivated early liver injury proxy is used to evaluate whether multivariable metabolic and lifestyle signals can meaningfully separate higher-risk individuals at a population level.

**Research objectives**

The primary objectives of this study are to:
	1.	Evaluate associations between diabetes, metabolic dysfunction, and lifestyle indicators with early liver injury risk.
	2.	Assess whether multivariable combinations of these indicators can stratify risk beyond single-factor analyses.
	3.	Examine the feasibility of producing calibrated probabilistic risk scores suitable for early warning or screening prioritisation contexts.
	4.	Provide evidence to inform future longitudinal modelling and digital health risk-stratification applications.

**Data source**
	•	Dataset: National Health and Nutrition Examination Survey (NHANES)
	•	Data domains used:
	•	Demographics
	•	Examination measures
	•	Laboratory biomarkers
	•	Diabetes history
	•	Lifestyle indicators (smoking, alcohol use, physical activity)
	•	Clinical history variables

NHANES is a nationally representative, publicly available dataset designed for population health research. All analyses are conducted in accordance with NHANES analytic guidance.

**Outcome definition**

Because NHANES does not provide a direct label for early-stage liver cancer, the study uses a sex-specific elevated AST threshold as a proxy for early liver injury. This proxy is intended to capture early biochemical liver stress rather than established disease and is used solely for feasibility assessment.

**Analytical approach**

The analysis follows a structured, stepwise framework:
	1.	Data preparation and variable harmonisation
	•	Merging multiple NHANES data files
	•	Consistent variable renaming and standardisation
	•	Missingness assessment and sample derivation
	2.	Exploratory data analysis
	•	Distributional assessment
	•	Identification of skewness and sparsity
	•	Informing appropriate statistical tests and modelling strategies
	3.	Unadjusted association testing
	•	Mann–Whitney U tests for continuous variables
	•	Chi-square tests for categorical variables
	4.	Adjusted multivariable modelling
	•	Logistic regression with L1 regularisation
	•	Regularisation used to address sparsity and high-dimensional categorical encoding
	5.	Risk stratification and evaluation
	•	Predicted probability estimation
	•	Risk decile analysis and lift assessment
	•	Model discrimination using ROC AUC
	6.	Calibration assessment
	•	Calibration curves
	•	Brier score evaluation

The results are interpreted strictly within a risk stratification and feasibility context.


**Reproducibility**

To reproduce the analysis:
	1.	Clone the repository.
	2.	Ensure a Python environment with standard data science libraries (pandas, numpy, scipy, statsmodels, scikit-learn, matplotlib, seaborn).
	3.	Open and run the Jupyter notebook sequentially.

All analytical steps are contained within the notebook and are designed to be reproducible from start to finish.


**Collaboration statement**

This project was developed collaboratively.

The core analytical pipeline, including data preparation, statistical modelling, and risk stratification, was implemented by the repository owner. Group members contributed through methodological review, validation of assumptions, interpretation of findings, figure refinement, and manuscript development. Collaboration and iteration were managed using GitHub to ensure transparency and version control.


**Intended use**

This repository supports:
	•	Academic coursework submission
	•	Manuscript preparation for publication
	•	Reproducible population health analysis
	•	Methodological demonstration of early warning feasibility using public health data


**Limitations**
	•	Cross-sectional design limits causal inference.
	•	Early liver injury is represented using a biochemical proxy rather than confirmed clinical diagnosis.
	•	Missingness and low prevalence of some clinical conditions constrain subgroup analysis.

These limitations are explicitly acknowledged and inform the interpretation of results.


**Contact**

For questions regarding the analysis or methodology, please contact the repository owner.

