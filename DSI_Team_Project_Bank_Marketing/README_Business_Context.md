**Business context and project undrestanding**

Before starting the data analysis, I always recommend to understand the business context, the data collection process, and the issues that arose from the project.

An initial review of the data reveals that the bank has a relatively low conversion rate. Out of 41,188 calls, only 11% received positive responses:

Yes: 4,640
No: 36,548

This made me curious about the budget the bank allocated for such a low result

The calculation is simple. Let’s assume the project took place last year. The average salary in Portugal is approximately €1,463 after taxes (according to data from the Ministry of Labor, Solidarity, and Social Security: https://www.theportugalnews.com/news/2024-02-06/what-is-the-average-wage-in-portugal/85747).

Based on this, we can estimate the total cost of the hourly rate using the following standard assumptions:

43% taxes
100% overheads
15% margin
100% labor utilization
These parameters are conservative, so the real cost could be 15-20% higher than my estimate.

With these assumptions, we calculate the cost per minute at €0.61.

From the dataset, we see that the total time spent was 10,638,243 seconds for 4,640 subscriptions. This means the bank spent €23.50 for each subscription !!!

However, by using predictive models and increasing the Prediction Accuracy by just 10% at each step, the bank could significantly improve its results and reduce costs. 

Prediction Acc.	Cost per 1 subs.
11.3%	        € 23.50
20%	            € 13.24
30%	            € 8.82
40%	            € 6.62
50%	            € 5.29
60%	            € 4.41
70%	            € 3.78
80%	            € 3.31
90%	            € 2.94
100%	        € 2.65

also we can see that on the chart:

![alt text](image-1.png)

As we can see, with a prediction accuracy of 50% (which is quite low), we can save around 77.5% of the budget, which is a significant reduction. If the accuracy increases further towards 100% (which is nearly impossible), we could save an additional 21.5% of the budget.

This means that achieving great results doesn't require complicated models or expensive teams.

As a first step, we can start with simple models, and then, based on the results, we can improve not only models but recommend further improvements for the bank's operations. These could include enhancing data collection (such as additional features, seasonal activity patterns, number and length of calls, contact frequency, etc.).

The next step is outlined in the data analysis README.

![image](https://github.com/user-attachments/assets/f5f6f4f2-9192-4ffd-b997-fde6148ece67)
