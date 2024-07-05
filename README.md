# Human resources analytics

## Possibles research questions...

- Is there any relationship between who a person works for and their performance score?

|----|----|
|![Imagen1](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_Salary_vs_PerformanceScore_by_Department.png)|![Imagen2](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_Salary_vs_PerformanceScore_by_Sex.png)
|----|----|
|![Imagen3]()|![Imagen4]()
  
- What is the overall diversity profile of the organization?
- What are our best recruiting sources if we want to ensure a diverse organization?
- Can we predict who is going to terminate and who isn't? What level of accuracy can we achieve on this?
- Are there areas of the company where pay is not equitable?

## For now:

1. Data loading and cleaning:
- Data is loaded into a dataframe and checked for null values.
- Rows with specific indices (132 and 292) are dropped.
- The dataframe size is verified post-deletion to ensure no null values exist in the 'Employee_Name' column.

2. Initial exploration:
- The last rows of the dataframe are visualized for a quick review.
- The dataframe is sorted alphabetically by 'LastName'.

3. Data type analysis:
- Variables in the dataframe are described.
- Data types for the 'LastName', 'Employee_Name', and 'EmpID' columns are visualized and adjusted.
- Specific column analysis: EmpID: Statistical description and distribution visualization (boxplot) + MarriedID: Description, conversion to boolean type, and bar chart + MaritalStatusID: Description, conversion to integer type, and pie chart + GenderID: Description, conversion to integer type, and bar chart + EmpStatusID: Description, conversion to integer type, and bar chart + DeptID: Description, conversion to integer type, and bar chart + PerfScoreID: Description, conversion to integer type, and bar chart + FromDiversityJobFairID: Description, conversion to integer type, and bar chart + Salary: Statistical description, conversion to float type, boxplot, and distribution plots + Termd: Description, conversion to boolean type, and verification of current employees + PositionID: Description, conversion to integer type, and bar chart + Position: Description, conversion to string type, and duplicate data cleaning.

## Moving forward (30 / 37 columns):
4. Review and normalization of other variables.

## Visualization 
|----|----|
|![Imagen1](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_Department_Terminated0_bar.png)|![Imagen2](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_TermReason_wordcloud.png)
|----|----|
|![Imagen3](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_dateofhire_line.png)|![Imagen4](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_dateofhire_month_bar.png)
|![Imagen5](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_dob_distribution_boxplot.png)|![Imagen6](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_recruitmentsource_actives_nonactives.png)
|![Imagen7](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_salary_distribution_boxplot.png)|![Imagen8](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_duration_department_bar.png)
|![Imagen9](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_turnoverrate_monthly_line.png)|![Imagen10]()

## Next steps:

5. Analyze the distribution of 'GenderID' and 'MaritalStatusID', which may be useful for understanding the demographic composition of the workforce.
6. Analyze variable correlations.
7. Analyze temporal data trends: dismissal dates, hiring dates, etc. Visualize workforce growth and employee turnover.
8. Analyze employee retention: Identify patterns in terminated employee data ('Termd'). Create a survival model to predict employee termination risk.
9. Analyze performance: Evaluate how variables such as department ('DeptID') and position ('PositionID') affect performance ('PerfScoreID').
10. Analyze diversity: Assess workforce diversity in terms of gender, marital status, and other demographic variables. Create diversity charts to visualize workforce composition.
11. Create new variables: Tenure: Calculate each employee's length of service. Performance Rating: Categorical variable based on 'PerfScoreID' to classify employee performance into categories like 'Low', 'Medium', and 'High'. Work-Life Balance Index: Develop an index based on variables such as hours worked, commute time, and other relevant metrics.
12. Charts: Heatmap + temporal trends + Kaplan-Meier + bars + boxplot + cluster analysis.
13. Prediction: Turnover Prediction Model + Performance Prediction Model.
14. Prepare technical documentation and executive report (insights and conclusions).
