# Human resources analytics

## Possibles research questions...

### 1. Is there any relationship between who a person works for and their performance score?

|![Imagen1](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_Salary_vs_PerformanceScore_by_Department.png)|![Imagen2](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_Salary_vs_PerformanceScore_by_Sex.png)
|----|----|

- Yes, people in the IT/IS (4.06) and Software (4.09) Departments have on average better PerformanceScore than the Sales (3.7) and Production (3.9) Departments.
- In general terms, the departments with the best Performance score also have a better Salary.
- The Sales department has an average Performance score of 3.7 with an average Salary of $69,061. While the Production department has a Performance score of 3.9 and a Salary of $59,953. Why?
- Excluding the Executive office, people in the Software Engineering and IT/IS departments earn approximately $23,000, $35,000 and $25,000 more than the Admin office, Production and Sales departments.
- On average, men ($ 70.629) have a better salary than women ($ 67.786).
- Women have an average Performance score of 4.0 while men have an average Performance score of 3.9.
- Most of the outliers are in the Salary of women. Why?

### 2. What is the overall diversity profile of the organization?

|![Imagen1](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_Department_vs_RaceDesc.png)|![Imagen2](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_Sex_vs_Department.png)
|----|----|

- 60% of the total number of employees are White within the RaceDesc variable. The department with the most White RaceDesc employees is Production (209).
- 26% of the total number of employees are Black or African American within the RaceDesc variable. The department with the most Black or African American type RaceDesc employees is Production (5).
- 9% of all employees are Asian within the RaceDesc variable. The department with the most Asian RaceDesc employees is Production (21).
- The Department with the most RaceDesc is Production (6). The Department with the least RaceDesc is Admin Offices (2).
- 57% of the payroll are Female and 43% are Male.
- The Department with the least number of women is IT/IS with 44%. The department with the most women is Admin Offices with 67%.

### 3. What are our best recruiting sources if we want to ensure a diverse organization?

|![Imagen1](https://github.com/sdforero/Human-resources-analytics/blob/main/Variable_racedesc_recruitmentsource_terminated_heatmap.png)|![Imagen2]()
|----|----|

- RecruitmentSource's top three sources are Indeed (27.9%), LinkedIn (24.4%) and GoogleSearch (15.7%).
- The most frequent race in hiring is White, at 60.1%. These hires are mostly made through Indeed (54), LinkedIn (47) and GoogleSearch (35). Of the 187 people who were hired, 124 (39.8%) are no longer with the company, while 63 (20.2%) are still working there.
- The second most frequent race in hiring is Black or African American, at 25.7%. These hires are mostly made through Diversity Job Fair (29), Indeed (17) and LinkedIn (16). Of the 80 people who were hired, 51 (16.4%) are no longer with the company, while 29 (9.3%) are still working there.
- The third most frequent race in hires is Asian, with 9.3%. These hires are mostly made through Indeed (10), LinkedIn (8) and GoogleSearch (7). Of the 29 people who were hired, 20 (6.4%) are no longer with the company, while 9 (2.8%) are still working there.

### 4. Can we predict who is going to terminate and who isn't? What level of accuracy can we achieve on this?
### 5. Are there areas of the company where pay is not equitable?

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
