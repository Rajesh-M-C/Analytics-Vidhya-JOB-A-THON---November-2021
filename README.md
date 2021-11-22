# Analytics-Vidhya-JOB-A-THON - November-2021

# Problem Statement

You are working as a data scientist with HR Department of a large insurance company focused on sales team attrition. Insurance sales teams help insurance companies generate new business by contacting potential customers and selling one or more types of insurance. The department generally sees high attrition and thus staffing becomes a crucial aspect.

To aid staffing, you are provided with the monthly information for a segment of employees for 2016 and 2017 and tasked to predict whether a current employee will be leaving the organization in the upcoming two quarters (01 Jan 2018 - 01 July 2018) or not, given:

Demographics of the employee (city, age, gender etc.)
Tenure information (joining date, Last Date)
Historical data regarding the performance of the employee (Quarterly rating, Monthly business acquired, designation, salary)

Private Leaderboard Rank - 129

# Approach

Finding the target variable for the data was the challenging part. Train data contains the monthly information of employees for 2016 and 2017, as the data is about employee attrition the test data consist of employee id of employees who have not left the company in 2017. Need to predict whether the employee is going to resign in the next 2 quarters of 2018(6 months), so created an indicator variable wherever the LastWorkingDate is present or not (1,0)

# Data Pre-processing and Feature Engineering
1. Categorical features are encoded
2. Average for each numerical features
3. all numerical features are normalized using min-max scaler
4. Employee tenure, Salary Hike, Promotion are the new features created

# Observations
1. There are 364 employees who were promoted but no salary change. out of which 60% (218) of employees have left the organisation
2. There are employees who have joined and left the organisation before 2016 with the tenure of less than 6 months
3. No Employees were Demoted

# Model Building
Tried Logistic regression, Random Forest, SVC. Out of this Logistic regression gave a better score in leaderboard of 0.67
