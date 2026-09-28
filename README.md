# Understanding Diabetes Progression

Final project, Scenario 1, Data Analytics and Statistics with Applications.

## About the project

This project looks at a dataset of 442 diabetes patients. The aim is to find out which patient characteristics are linked to diabetes progression one year after baseline, and what can and cannot be concluded from the data.

Research question: Which patient characteristics are associated with diabetes progression, what do the regression models tell us, and what conclusions can reasonably be drawn from the data?

## Files

diabetes_analysis.R: the R script with all the analysis code. Run it from top to bottom in a clean R session. Keep diabetes.tab.txt in the same folder.

diabetes.tab.txt: the dataset (442 rows, 11 columns).

Diabetes_Progression_Report.pdf: the written report, organised around the six project questions.

Diabetes_Progression_Presentation.pptx: a short presentation for a health service decision maker who is not a statistician.

README.md: this file.

## Data

The data has 442 patients. Each row is one patient. The columns are age, sex, BMI, blood pressure, six blood measures (s1 to s6), and the outcome, which is a diabetes progression score measured one year later.

Original source: https://www4.stat.ncsu.edu/~boos/var.select/diabetes.tab.txt

There are no missing values and no repeated rows. Sex is stored as 1 and 2 but is treated as a category, not a number. This is health data, so the results should be read as patterns in a group and not as advice for any one person.

## Analysis steps

1. Load the data and check its structure, missing values and duplicates.
2. Describe the data with summary statistics and plots.
3. Look at relationships using a correlation matrix, a heatmap and scatterplots.
4. Fit a simple regression (progression on BMI) and a multiple regression (progression on BMI, blood pressure and s5).
5. Check the models with a residuals plot, VIF values, confidence intervals and p values.
6. Discuss causality, other possible explanations and limits of the data.

## Main results

BMI and s5 have the strongest links with progression, followed by blood pressure.

The simple model with BMI alone explains about 34 percent of the differences between patients (R squared 0.344).

The multiple model with BMI, blood pressure and s5 explains about 48 percent (R squared 0.480).

The VIF values for the three predictors are all about 1.3, so overlap between them is not a problem.

The data is observational, so these results show links and do not prove cause and effect.

## Reflection

The main thing I learned is how careful you have to be when describing what a regression result means. A significant result does not mean a cause, and a higher R squared does not mean a model is good on its own. The hardest part was explaining the results in plain language for the presentation. With more time I would look at whether transforming the outcome improves the residuals plot.
