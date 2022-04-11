# BankChurnersPrediction
The purpose of this project is to provide guidance on possible churners and preventive actions bank can take to avoid customer leaving. Analysis is based on “BankChurners.csv” dataset using python and its packages.

1.	Quick overview of dataset:
Below figure shows the brief information of dataset used for the analysis, such as total columns, columns data types, null counts in the rows. 
i.	There is total 21 columns in the dataset from which 6 are categorical and 15 are numerical type. 
ii.	Total rows are 10127 in which 0 null values for all the columns.

![image](https://user-images.githubusercontent.com/91941680/162762986-ea3c51b3-26ec-4780-b041-fda813ca36fd.png)

1.1 Quick statistics of all the numerical variables:
i.	CLIENTNUM: 10127 total customers.
ii.	Customer_Age: the range of customer’s age is from 26 to 73. 
iii.	Dependent_count: on average a customer has 2.35 dependents on a credit card for financial support with a range of 0 to 5.
iv.	Months_on_book: range of customer’s months on book is from 13 to 56. 
v.	Total_Relationship_Count: average total relationship count is 1.55 with range from 1 to 6. 
vi.	Months_Inactive_12_mon: average customers inactive month in 12 months is 2.34 with range of 0 to 6.
vii.	Contacts_Count_12_mon: customer contact count in 12 months ranges from 0 to 6.
viii.	Credit_Limit: average credit limit is 8631.95 which greater number of variations within the dataset. 
ix.	Total_Trans_Amt: the range of customer’s total transaction amount is from 510 to 18484 with average of 3397.13.
x.	Total_Trans_Ct: the range of customer’s total transaction count is from 10 to 139.
xi.	Avg_Utilization_Ratio: utilization ratio of credit card ranges from 0 to 1. 
![image](https://user-images.githubusercontent.com/91941680/162763064-0ff5dd9d-5961-4dc7-8d06-2312841c7d3f.png)

1.2 Counts different values for all the categorial variables: 
i.	Attrition_Flag: 1627 Attrited Customer and 8500 Existing Customer. 
ii.	Card_Category: 4 types of card category (Platinum, Gold, Silver & Blue)
iii.	Education_Level: Majority of customers are Graduate, followed by High School, Unknown, Uneducated, College, Post-graduate and Doctorate. 
iv.	Gender: Female customers are higher than male
![image](https://user-images.githubusercontent.com/91941680/162763148-50ddaaf1-c232-4c95-a65e-9d7571e90cff.png)

2.	Comparison of variables
2.1 Comparing selected variables with existing and attrited customers
Below table shows the summarized comparison of different variables with existing and attrited customer. 
![image](https://user-images.githubusercontent.com/91941680/162763202-53fb65ce-45a7-4050-b8ec-ac5fe9883caf.png)

2.2 Graphical comparison 
i.	Age distribution with existing and attrited customer: There are some outliers in existing customer with age above 70. Both customer types age is fairly symmetrically distributed. However, median age of Attrited is slightly higher than Existing customer. 
![image](https://user-images.githubusercontent.com/91941680/162763244-287228e4-e9b2-45c5-b9bd-d0194810fb71.png)
ii.	Gender distribution with existing and attrited customer: Number of female customers are higher than male customer in both group of customers. However, number of existing customers is relatively higher than attrited customer in both genders.  
![image](https://user-images.githubusercontent.com/91941680/162763302-01efca32-a7e1-441f-b4e5-dcdd28d2d036.png)
iii.	Income category comparison with existing and attrited customer: Income category distribution of existing customer is higher than attrited customer. However, in both existing and attrited customer income group of less than $40K is higher than other income category. Similarly, for income category of $120K has the lowest number of both existing and attrited customer.
![image](https://user-images.githubusercontent.com/91941680/162763342-0bc65d0e-bfa7-458d-8f3b-21cc37bd0c21.png)
iv.	Credit limit comparison of existing and attrited customer: Both existing and attritted customer has contains outliers beyond upper whisker. Credit limit is lower to attrited customer group. 
![image](https://user-images.githubusercontent.com/91941680/162763395-55445f71-0b2d-44e5-b713-018edc4bef1f.png)
v.	Transaction amount comparison of existing and attrited customer: Majority of transaction amount of attrited customer is lower than existing customer. Although both customer group has outlying data which represents the total transaction amount varied from customer to customer.
![image](https://user-images.githubusercontent.com/91941680/162763448-a983a33d-d84f-4d6e-a558-3161d573140e.png)
vi.	Total transaction count comparison of existing and attrited customer: Existing customer’s transaction frequency is higher than attrited customer. 
![image](https://user-images.githubusercontent.com/91941680/162763495-9c807fda-8e6a-4d9b-92ec-6b637360719e.png)
vii.	Average utilization ratio comparison of existing and attrited customer: Existing customer’s average utilization ratio is higher than attrited customer. However, attrited customer group average utilization ratio has outlier which suggests variation among attrited group of customers compared to existing customer group. 
![image](https://user-images.githubusercontent.com/91941680/162763547-ef174b3b-1b61-4c8d-a785-628f3193094b.png)

3.	Analyze customer age & gender: 
3.1 Check age difference between existing customers and churners
The aim of the hypothesis test is to conclude whether two variables “Customer_Age” and “Attrition_Flag” are related to each other.
Hypothesis Test using T-Test: 
Null Hypothesis (H0): mean difference between age and existing customers & churners is 0
Alternative Hypothesis (H1): mean difference between age and existing customers & churners is not 0
By using python, statistics = 1.831959, p-value = 0.066986 (alpha/significance level = 0.05)

Concluded: Do not reject null hypothesis. There is not enough evidence to conclude customer age and existing customer & churners are different from the given data. 

3.2 Check gender difference between existing customers and churners
The aim of the hypothesis test is to conclude whether two variables “Gender” and “Attrition_Flag” are related to each other.
Hypothesis Test using Chi-square test:
Null Hypothesis (H0): There is no relation in gender difference between existing customer and churners.
Alternative Hypothesis (Ha): There is a relation in gender difference between existing customer and churners.
By using python, chi-square statistics = 14.068218, p-value = 0.000716 (alpha/significance level = 0.05)

Concluded: Reject null hypothesis. There is a sufficient evidence to conclude gender difference between existing customers and churners from the given data. 

4.	Analyze pattern of customer groups 
4.1 Check patten of “average_utilization_ratio” are different for attrited and existing customers.
The aim of the hypothesis test is to conclude whether two variables “Avg_Utilization_Ratio” and “Attrition_Flag” are related to each other.
Hypothesis Test using T-Test: 
Null Hypothesis (H0): mean difference between average utilization ratio and existing customers & churners is 0
Alternative Hypothesis (H1): mean difference between average utilization ratio and existing customers & churners is not 0
By using python, statistics = -18.244911, p-value = 3.35768932824574e-73 (alpha/significance level = 0.05)

Concluded: Reject null hypothesis. There is enough evidence to conclude average utilization ratio is different for existing customers and churners in the provided data. 

4.2 Check patten of “average_utilization_ratio” of customer groups of different education level 
The aim of the hypothesis test is to conclude whether two variables “Avg_Utilization_Ratio” and “Education_Level” are related to each other.
Hypothesis Test using T-Test: 
Null Hypothesis (H0): mean difference between average utilization ratio and education level (graduated from universities & others) is 0
Alternative Hypothesis (H1): mean difference between average utilization ratio and education level (graduated from universities & others) is not 0
By using python, statistics = -0.309060, p-value = 0.757281 (alpha/significance level = 0.05)

Concluded: Do not reject null hypothesis. There is not enough evidence to conclude average utilization ratio is different for customers education level i.e, graduated from universities and other groups from the provided data. 
Conclusion
In summary, report showcased the given data set’s list of columns, data types, descriptive statistics of numerical variables and categorical variable’s count of values. Chart are showed for the visual representation of selected variables compared with existing customer and churners to analyze the behavior of customers. It is proved that there is no difference in customer age and average utilization ratio of existing customers and churners. However, there is difference in existing customer and churner in terms of customer gender. Also, in terms of education level when aggregated the group into graduated in universities and others, there is no difference in average utilization ratio. 
