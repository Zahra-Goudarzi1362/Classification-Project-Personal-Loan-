# Classification-Project-Personal-Loan-
Prediction of will new custome accept the Personal Loan offer? Based on some customer's personal information
Firstly I imported Libraries and then import Bank dataset which includes customer information. 
Then I did some preprocessing in my data. for example: # in column 'CCAvg' cahnged: / to . in notepad++ 
There were some neagtive values in 'Experience' column, so I changed them to positive value, by abs on. 
In this dataset all data are per year, but CCavg is permonth so we change it to per month, by *12 
we donot need 'ID' column so delete it. 
Now check missing value. 
checking Nose with plot seperately for Categorical data and Numerical data. 
Based on plot, There was a noise in Zip Code column and I delete it. 
We added new columns for each zip code which include Place,Latitude,Longitude to see in which location prople get more loan. (to analysing our data) 
result: Los Angeles is the location that recorded the most data (not that they loan more)
I also draw correlation subplot--> result: we could check Big numbers.. 
for example: personal loan have correlation (Direct relationship) with Income (0.5) /CCAvg/Education/CD account
CCAvg & Income have direct correlation # As one increases, the other increases
Then I analyzed relation between 3 parameters: Income,Age,Personal Loan by sns.kdeplot resulted ---> for example: age:43~46 / income : 4-~50 get more loan 
It shows people who had lower CCAVg can get loan better ,no matter age.
now I started creat my machine learning model for prediction, I used LogRegression/KNN/Naive Base algorithm to select better one 
LogRegression's Accuracy =0.9(That is good)
KNN  Accuracy : 0.906
# result : Logre & KNN both accuracy are the same , but THeir result is the same. I mean their confusion matrix are not the same 
# error & cost is important.. 
Naive Bayes algorithm is not suitable for this data¶
# 
