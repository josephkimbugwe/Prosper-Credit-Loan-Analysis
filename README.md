# (Prosper Credit Loan)
## by (Joseph Kimbugwe)


## Dataset

> The Prosper loan dataset contains 113,937 observations with 81 loan attributes and information on peer to peer loans facilitated by Prosper credit company.

> As earlier observed, there are 81 loan attributes but we narrowed down to 13 attributes that aided this investigation effectively. Reference was made to the data dictionary available on the link below to aid selection of the features of interest.
Link: https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0

> The selected features include: Term, LoanStatus, BorrowerAPR, ProsperScore, ListingCategory, EmploymentStatus,EmploymentStatusDuration, IsBorrowerHomeowner, DebtToIncomeRatio, StatedMonthlyIncome, LoanOriginalAmount, LoanOriginationDate, and MonthlyLoanPayment.


## Summary of Findings

> The Borrower Annual Percentage Rate distribution seems to have more than one mode and thus we can conclude that its multimodal
> We can observe that the loans to be paid in 36 months account for 76.58% of all loans followed by loans to be paid in 60 months at 21.98% and finally loans to be paid in a year at 1.45%. This shows that Prosper credit company majorly offers midterm loans as oppossed to short or longterm loans. 
> The bigger the loan amount, the bigger the monthly repayment amount. This signals a direct proportionality between loan amount and monthly loan repayment.
> The higher the loan amount the lower the Borrowers Annual Percentage Rate. Longer loan terms are given for higher loan amounts. 
> Borrowers with higher monthly income apply for loans with bigger loan amounts. Borrowers with who own homes have longer employment durations.
> Borrowers with higher monthly income are can afford to pay higher monthly loan repayment installments. 
> We can see that most home owner loan amounts are spread out with majority of it above $$5000 and below $5000 for most borrowers that don't own homes.
> We can see that the loan amounts are right skewed and that the most frequently offered loan amount is $4k
> Most of the loans are in current status with another sizeable number of loans in completed status. 
> Employment status categories are Self-employed, Employed, Not available, Full-time, Other, Not employed, Part-time, and Retired with the Employed people taking up most of the loans. 
> The most frequentlyloan category applied for is Debt Consolidation(1).
> The borrowers monthly income is right skewed with the most frequent monthly income being close to \$4200

## Key Insights for Presentation

> What factors affect the borrower's APR or interest rate? Answering this question was the focus of this presentation.

> The original Prosper credit loan dataset had 81 features but all were not relevant to answering the core question and as such I subset the dataset to 13 relevant features. These subset dataset was investigated for presence of duplicates, missing values and tidiness issues.

> I proceeded to the data cleanin phase to handle the missing values identified in ProsperScore, BorrowerAPR, DebtToIncomeRatio, EmploymentStatusDuration, and EmploymentStatus features, renaming the ListingCategory (numeric) feature to ListingCategory and changing the LoanOriginationDate feature type from string to datetime. A clean dataset was written to csv file named loan_data_cleaned.csv

> I then investigated the distribution of the observation in all features individually using distplots, piecharts, histplots and countplots. 

> During bivariate analysis, I calculated the correlation matrix for all features that I then plotted on a heatmap to allow for easy intepretation. I discovered that some features were strongly positively correlated and some others had weak negative correlation. This prompted me to further investigate the relationships between this features.

> I dived deeper into analysing the relationships between feature pairs using boxplots, regplots, violin plots, and scatter plots.What stood out for me was that borrowers with higher monthly income are can afford to pay higher monthly loan repayment installments. We can see that most home owner loan amounts are spread out with majority of it above $5000 and below $5000 for most borrowers that don't own homes.

> Finally, I was able to identify StatedMonthlyIncome, MonthlyLoanPayment, and LoanOriginalAmount as the most effective features on Borrowers Annaual  Percentage Rate.