# loan-distribution-ai-model
This AI model predicts if a loan can be approved or not based on various features of loan applicant. The loan approval process is analyzed with three models. 1.Logistic Regression, 2.Decision Tree and 3.Random Forest.


Lending Club is a peer-to-peer lending company where individuals can borrow loans, and investors can fund those loans. Lending Club was founded in 2006 by Renaud Laplanche as a peer-to-peer (P2P) lending platform in San Francisco. It was one of the pioneers in the online lending space, where individual borrowers could obtain loans, and individual or institutional investors could invest in these loans to earn interest. The platform allowed for a more direct connection between lenders and borrowers, bypassing traditional banking intermediaries.

Read more here https://en.wikipedia.org/wiki/LendingClub

image.png

Problem Statement
Now, whenever Lending Club approves a loan, there are two ways in which it is at risk:

If LC approves a loan and the borrower fails to repay it on time
If LC rejects a loan despite the borrower being capable of repaying the loan
Defaulting on loans can lead to significant financial losses for both the platform and investors. Similarly, not providing loans to credit-worthy customers can lead to missing out on potential revenue and profits. Therefore, a robust loan approval system is the need of the hour.

In the current loan approval process, underwriters evaluate loan applications by manually reviewing credit scores, income, debt, etc. and then, based on several parameters, either approve or reject a loan. This process is time-consuming and prone to errors.

Hence, Lending Club wants to build a loan approval system using Machine Learning models to automatically assess whether a given loan is likely to be repaid or whether the borrower is likely to default.

This is where you come in! As a budding data scientist, your goal is to help out Lending Club in creating this ML model that helps them predict whether a loan is likely to default or not.

Data Understanding
You have been provided with around 38k loan application data from the Lending Club's website. The different columns and their description are mentioned below:

Column Name	Description
id:	A unique LC assigned ID for the loan listing. (Integer)
member_id:	A unique LC assigned ID for the borrower member. (Integer)
loan_amnt:	The listed amount of the loan applied for by the borrower. If at some point the credit department reduces the loan amount, it will be reflected in this value. (Float)
term:	The number of payments on the loan. Values are in months and can be either 36 or 60. (Integer)
int_rate:	Interest rate on the loan. (Float)
installment:	The monthly payment owed by the borrower if the loan originates. (Float)
grade:	LC assigned loan grade. (Categorical/String)
sub_grade:	LC assigned loan subgrade. (Categorical/String)
emp_length:	Employment length in years. Possible values are between 0 and 10, where 0 means less than one year and 10 means ten or more years. (Integer)
home_ownership:	The home ownership status provided by the borrower during registration. Values are: RENT, OWN, MORTGAGE, OTHER. (Categorical/String)
annual_inc:	The self-reported annual income provided by the borrower during registration. (Float)
verification_status:	Indicates if income was verified by LC, not verified, or if the income source was verified. (Categorical/String)
purpose:	A category provided by the borrower for the loan request. (Categorical/String)
dti(debt to income ratio:	A ratio calculated using the borrower’s total monthly debt payments (excluding mortgage and the requested LC loan), divided by the borrower’s self-reported income. (Float)
delinq_2yrs: The number of 30+ days past-due incidences of delinquency in the borrower's credit file for the past 2 years. (Integer)
inq_last_6mthsInquiries in last 6 months):	The number of inquiries in the past 6 months (excluding auto and mortgage inquiries). (Integer)
open_acc:	The number of open credit lines in the borrower's credit file. (Integer)
pub_rec:	Number of derogatory public records. (Integer)
revol_bal:	Total credit revolving balance. (Float)
revol_util:	Revolving line utilization rate, or the amount of credit the borrower is using relative to all available revolving credit. (Float)
total_acc:	The total number of credit lines currently in the borrower's credit file. (Integer)
last_pymnt_amnt:	Last total payment amount received. (Float)
loan_status:	Current status of the loan. (Categorical/String)

