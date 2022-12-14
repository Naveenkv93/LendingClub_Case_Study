# Lending Club Case Study
> Using EDA to understand how consumer attributes and loan attributes influence the tendency of default.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
**Lending Club** is a consumer finance company which specialises in lending various types of loans to urban customers. When the company receives a loan application, the company has to make a decision for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:
* If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company

* If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company


### Background
This company is the largest online loan marketplace, facilitating personal loans, business loans, and financing of medical procedures. Borrowers can easily access lower interest rate loans through a fast online interface. 

Like most other lending companies, lending loans to ‘risky’ applicants is the largest source of financial loss (called credit loss). The credit loss is the amount of money lost by the lender when the borrower refuses to pay or runs away with the money owed. In other words, borrowers who default cause the largest amount of loss to the lenders. In this case, the customers labelled as 'charged-off' are the 'defaulters'. 

If one is able to identify these risky loan applicants, then such loans can be reduced thereby cutting down the amount of credit loss. Identification of such applicants using EDA is the aim of this case study.

In other words, the company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default.  The company can utilise this knowledge for its portfolio and risk assessment.

### Data
The data given contains the information about past loan applicants and whether they ‘defaulted’ or not. The aim is to identify patterns which indicate if a person is likely to default, which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc.


## Conclusions
### From Univariate Analysis

![plot](./images/univariate_term_ownership.png)
![plot](./images/univariate_emp_Verification_loan.png)

1. **Term** : People opting for short team loan (36 months) are relatively higher compated to long term loans (60 months)
2. **Home ownership** : Applicant who are having Rent or Mortage property are more intended to take loan over others
3. **Grade** : People from grade A and B are among the most who take the loan
4. **Employment Length** - Among applicants employees having maximum group of people are having 10+ years years experience
5. **Verification Status** - For provided data we can infer majority of the loans are issued without verification
6. **Loan Status** : About 85% of loans are fully paid and 15% of loans are Charged off

![plot](./images/univariate_month.png)
![plot](./images/univariate_grade_and_state.png)

1. **Loan issue month** : Number of people opting for loan increases as month progresses from Jan to Dec\
2. **Loan applicant State** : People are from CA and NY are most who applied for the loan\
3. **Pupose** : Debt consolidation is the most purpose for people who are applying for the loans

### From Bivariate Analysis

![plot](./images/bivar_higherloaninterest.png)

**People belonging to Charged off category are having higher interest rate than fully paid ones**

![plot](./images/bivar_duration.png)

**Number of people Charged off are more in long term loan(60 months) compared to short term. Also number of people fully paid is more in short term loan(36 months)**

![plot](./images/bivar_grade.png)

**Number of people belong to Group F & G are Charged off more compared to other group. Also from as we move from Group A to G proportion of charged off people increases**

![plot](./images/bivar_subGroup.png)

**As a proof of our observation from loan status vs group analysis, we see incremental curve for charged off people from subgroup A to G\ Among the sub group there are more people from F4,F5,G2,G3 and G5 belongs to Charged Off category**

![plot](./images/bivar_purpose.png)

**People having purpose of the loan as 'small_business' have higher proportion of Charged off people compared to others**

![plot](./images/bivar_state.png)

**Among the people who belong to Charged off category, frequency of people belong to State 'CA' is more compared to other status. Also there are very less people under charged off category for states 'AK','DC','TN' and 'WY'**

![plot](./images/bivar_correl.png)

**Below are the observations for relation between columns for Charged off loans**
1. There is strong positive correlation between loan amount with funded amount and funded amount is invested, this is because almost all loan amount request will be funded close to requested amount 
2. Positive correlation between loan amount with installments - installment increases with increase in loan amount 
3. There is negative correlation between annual incomes with DTI, increase in annual incomes decreases DTI

## Technologies Used
- pandas - version 1.5
- numpy - version 1.23.3
- matplotlib - version 3.6.0
- seaborn - 0.12.0

## Acknowledgements
- This project was done as a case study for Executive AI/ML Post Graduate Program by IIITB and upgrad.


## Contact
Created by [@Naveenkv93](https://github.com/Naveenkv93) & [@prabhats97](https://github.com/prabhats97) - feel free to contact us!
