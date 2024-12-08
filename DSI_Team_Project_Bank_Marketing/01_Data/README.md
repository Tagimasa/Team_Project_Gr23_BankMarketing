# Data Analysis

**Downloaded data**

I used the latest dataset, bank-additional-full.csv, which contains a larger number of features. According to the authors' description, the other datasets are simply random 10% selections of rows from versions 1 and 2.

**I made the following steps to analyse the data**

The steps and main conclusions are outlined below.

1/ number of rows and colomns 
41188 rows × 21 columns

2/ conversion rate - percent of positive responce to total calls made 
no     36548
yes     4640

3/anlysis of calls and subscriptions by months - important note!!! the dataset has no rows identification by actual calendar date!!! so it can lead to significant problems with modelling outcome!

4/ Analysed mean, max, min, std. # !!!!! there's a problem with "pdays" column - incorrect data with 999 for all rows present. recommendation to exclude the column

5/ Calculated the sum of the 'duration' column - Total sum of the 'duration' column: 10,638,243 

6/ # Definition of age groups and count 'yes' and 'no' in each age group. Definition of positive conversion rate in each group.
Older people have the highest conversion.

7/ The definition of professional groups and the count of 'yes' and 'no' responses in each group, along with the percentage of positive conversions, are provided. All professional groups, except for students and retirees, have similar results, so we should keep them in the dataset.

8/ The same analysis was conducted for each feature. Below, I will provide information only for the features that were excluded.

9/ The features 'housing', 'default', 'loan', 'day of week'  - to exclude, the same conversion r. for all groups

10/ The feature "contact" was excluded due to the rapidly increasing availability of cellular phones.

11/ **!!! Important Note - Clients with more than 4 contacts were excluded**. According to the author's description, the dataset includes all calls made by the bank to clients during the campaign, as well as calls from clients to the bank when trying to resolve other issues. These types of calls can significantly influence the modeling results.

12/ **!!! Important Note - The "duration" feature was excluded**. The "duration" feature, which represents the contact length in seconds, was excluded, as it is not possible to predict the length of a call in advance. However, this feature could be useful for further analysis, as it may help identify client groups that are more loyal to longer discussions and more responsive to bank managers' recommendations.

**Data cleaning**

The data cleaning code is provided in the file Data_Cleaning_Code.ipynb, where all the steps can be found.

Some rows and columns were excluded (the reasons for these exclusions are explained above in the Data Analysis section).

As a result of the cleaning process, I obtained a new dataset named Cleaned_Data.csv, which contains 33,553 rows and 12 columns.
33553 rows × 12 columns