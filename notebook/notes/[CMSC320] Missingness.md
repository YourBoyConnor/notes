# Missingness

Created: 2023-03-07 15:33:08 -0500

Modified: 2023-03-07 16:25:34 -0500

---

Missing Completely at Random IMCAR)

Missing at Random (MAR)

Missing Not at Random (MNAR)

Single Imputation:

- Mean Imputation: imputing the avg from observed cases for all missing values of a var
- Hot-deck imputation: imputing a value from another subject, or "donor," that is most like the subject in terms of observed variables
- Cold-deck imputation: bring in other datasets (Old and bad)

Multiple Imputation: Developed to deal with noise during imputation

- Generate several random values for each missing data point during imputation

Types of values in a table:

- Binary: 1 or 0, Yes or No
- Categorical: Education status, Grades
- Continuous: Salary, Age

Strategy: MICE (Multiple Imputation through Chained Equations)

Bayes Theorem
