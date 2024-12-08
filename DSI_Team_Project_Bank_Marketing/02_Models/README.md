# Models trainings and testings 

As mentioned in the 'business analysis' file, there is no need to use complicated models for prediction in the initial stage. Additionally, given the relatively small size of the dataset, complex methods may not be suitable. Therefore, I used simple KNN classification and Logistic Regression methods.

** KNN classification **

all code and results are in the 01_Model_training_KNN.ipynb

Steps of modelling  
1/ create dataframe from 'cleaned-data' dataset  
2/ Encode the target variable 'y' (binary)  
3/ Convert categorical columns to numerical using one-hot encoding  
4/ Split the data into features (X) and target (y)  
5/ Normalize/Scale the data for KNN (important for distance-based models)  
6/ Split into training and test datasets  
7/ Initialize KNN and fit the model  
8/ Make predictions and evaluate the model  
9/ Evaluate the performance of the model  

Results:  
Accuracy: 0.887

              precision      recall    f1-score     

           0       0.90      0.98      0.94      
           1       0.63      0.21      0.32      

10/ Test different k values
k=10 is the good one 

11/ Cross validation scoring with KNeighborsClassifier n_neighbors=10 and cv=10

Mean cross-validation score:  0.548 !!!! 
quite low !!! probably because of the high weight of 'no' result (90%) and data does not destributed evenly

12/ next step with scaling scaler = StandardScaler()

Mean cross-validation score:  0.769
much better! 

13/ Visualizing the feature importances - features correlation with the target variable
 - Calculate correlation matrix
 - Get correlation with target variable (y)
 - print plot

** Logistic regression**

 all code and results are in the 02_Model_Training_LogReg.ipynb

 Steps of modelling
1/ Create dataframe from 'cleaned-data' dataset
2/ Split the data into features (X) and target (y)
3/ Encode categorical features ('job', 'marital', 'education', etc.)
4/ Apply Label Encoding to categorical features
5/ Scale the features
6/ Split the dataset into training and testing sets (70% training, 30% testing)
7/ Initialize the Logistic Regression model 
8/ Train the model
9/ Evaluate the model on the test set
10/ Print performance metrics
11/ Visualize the features wights 
12/ Save the trained model using joblib, model_filename = 'logreg_model.pkl'

Accuracy on Test Set:  0.888 Good result!!! we can use it for further Bank' promos 

Classification Report:
               precision    recall  f1-score   

          no       0.90      0.98      0.94     
         yes       0.64      0.22      0.32
