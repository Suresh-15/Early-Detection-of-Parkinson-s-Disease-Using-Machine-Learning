# Early-Detection-of-Parkinsons-Disease-Using-Machine-Learning
PD is a neurodegenerative disorder affecting 60% of people over the age of 50 years. PD can be treated through early detection. Research has been carried out on the MDVP audio data of 30 PWP and healthy people during training of 5 ML models. Comparison of results of classification by SVM, KNN, Logistic Regression, Random Forest and Naive Bayes Classifier is performed to determine the efficient algorithm and approach.

# Dataset used 
Link: https://archive.ics.uci.edu/dataset/174/parkinsons
Oxford Parkinson's Disease Detection Dataset.
This dataset is composed of a range of biomedical voice measurements from 31 people, 23 with Parkinson's disease (PD). Each column in the table is a particular voice measure, and each row corresponds one of 195 voice recording from these individuals ("name" column).

# Additional Variables Information
name - ASCII subject name and recording number
MDVP:Fo(Hz) - Average vocal fundamental frequency
MDVP:Fhi(Hz) - Maximum vocal fundamental frequency
MDVP:Flo(Hz) - Minimum vocal fundamental frequency
MDVP:Jitter(%),MDVP:Jitter(Abs),MDVP:RAP,MDVP:PPQ,Jitter:DDP - Several measures of variation in fundamental frequency
MDVP:Shimmer,MDVP:Shimmer(dB),Shimmer:APQ3,Shimmer:APQ5,MDVP:APQ,Shimmer:DDA - Several measures of variation in amplitude
NHR,HNR - Two measures of ratio of noise to tonal components in the voice
status - Health status of the subject (one) - Parkinson's, (zero) - healthy
RPDE,D2 - Two nonlinear dynamical complexity measures
DFA - Signal fractal scaling exponent
spread1,spread2,PPE - Three nonlinear measures of fundamental frequency variation

# How the models are trained
The Dataset is split into 75% as training data and 25% as test data

# Approach 1
Collect MDVP audio data from PPMI and UCI databases
Perform data analysis to detect skew, imbalance and distribution of variables in data
Scale the data to common range using Standard Scaler
Split dataset into testing and training sets, where training data is 75% of total
Train SVM, logistic regression, random forest and KNN models

# Approach 2 
Collect MDVP audio data from PPMI and UCI databases
Perform data analysis to detect skew, imbalance and distribution of variables in data
Scale the data to a common range using Standard Scaler
Apply PCA to identify 5 most relevant features to model training, out of 22 attributes.
Split dataset into testing and training sets, where training data is 75% of total
Retrain SVM, logistic regression, random forest and KNN models. 
Compare classification results using confusion matrix, ROC-AUC curve and accuracy

# Approach 3
Collect MDVP audio data from PPMI and UCI databases
Perform data analysis to detect skew, imbalance and distribution of variables in data
The dataset is imbalanced, with 109 records of PWP and 40 records of normal people.
The imbalance is resolved by up sampling the minority class to reach 109 records each.
Scale the data to common range using Standard Scaler
Split dataset into testing and training sets, where training data is 75% of tota
Retrain SVM, Logistic regression, Random forest, KNN Models
Compare classification results using confusion matrix, ROC-AUC curve and accuracy
