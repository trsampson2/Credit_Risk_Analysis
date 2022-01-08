# Credit Risk Analysis
Credit Risk Analysis using Machine Learning

## Overview

Credit Risk is used by every financial institution when considering giving issuing a loan for a consumer.  This analysis runs data through machine learning algorithms to discover which one can be used to accurately predict if a person is a credit risk. 

## Results

### Oversampling
Oversampling is used when there is a severe skew in distribution in a data set.  Oversampling duplicates examples from the data in the datastet that is under represented. 

#### Random Naive Oversampling
Using Naive Random Oversampling on this data set, the accuracy score is 68%.  

![Naive_Random_Sampling_Acc_Score](https://user-images.githubusercontent.com/86331812/148651699-ec00086d-0f0d-48cd-9f79-4ce629e67072.png)

The confusion matrix is 

![Naive_Random_Samppling_Confusion](https://user-images.githubusercontent.com/86331812/148651969-8db3f525-730a-459c-bb7e-99b6d4a9c8ff.png)

The classification report shows the precision and recall of the model as 100% and 59%, respectively, for predicting low risk credit. 

![Naive_Random_Sampling_Class_Report](https://user-images.githubusercontent.com/86331812/148652796-f7462528-a0ef-42e1-81d4-d3d74486e30c.png)

#### SMOTE Oversampling
Using SMOTE oversampling on this data set, the accuracy score is 66%.

![SMOTE_Acc_Score](https://user-images.githubusercontent.com/86331812/148653104-ee5b3b9b-e441-4845-85f5-b4b005126913.png)

The confusion matrix:

![SMOTE_Confusion](https://user-images.githubusercontent.com/86331812/148653124-77021ae6-6d1c-4627-9f98-f1758a3aedea.png)

The classification report shows the precision and recall of the model as 100% and 69%, respectively, for predicting low risk credit.

![SMOTE_Class_Report](https://user-images.githubusercontent.com/86331812/148653163-fd899a92-bf27-480d-86fa-1b85eb47031a.png)

#### Undersampling
Undersampling increases the number of the minority data while decreasing the size of the majority data in the data set. There is a lost of data from the majority data.  
Using undersampling on this data set, the accuracy score is 68%.

![Undersampling_Acc_Score](https://user-images.githubusercontent.com/86331812/148653219-11cecf0f-fd8b-43f1-b9e1-cceef07814f7.png)

The confusion matrix:

![Undersampling_Confusion](https://user-images.githubusercontent.com/86331812/148653232-090813fc-e213-4b8f-8533-36b25fc67753.png)

The classification report shows the precision and recall of the model as 100% and 55%, respectively, for predicting low risk credit.

![Undersampling_Class_Report](https://user-images.githubusercontent.com/86331812/148653274-954c2e0e-5692-4808-99e7-293f6e882076.png)


#### SMOTEEN Combination Sampling
SMOTEEN combines the SMOTE and the Edited Nearest Neighbors (EEN) algorithms.  It oversamples the minority data with SMOTE and then it cleas the resulting data with an undersampling strategy. Using SMOTEEN Combination on this data set, the accuracy score is 59%. 

![SMOTEEN_Acc_Score](https://user-images.githubusercontent.com/86331812/148653337-6227fbd9-876a-4a5c-b661-f1774170f58a.png)

The confusion matrix:

![SMOTEEN_Confusion](https://user-images.githubusercontent.com/86331812/148653366-4ac42895-3cc6-4f09-b82f-335d51ad212e.png)

The classification report shows the precision and recall of the model as 100% and 59%, respectively, for predicting low risk credit.

![Undersampling_Class_Report](https://user-images.githubusercontent.com/86331812/148653400-607f025c-0b5e-48d7-ba42-ddab9f0ac8ba.png)


#### Balanced Random Forest Classifier 
Balanced Random Forest Classifier fits a number of decision tree classifiers on various sub-samples of the dataset and averages to improve the accuracy. 
Using Balanced Random Forest Classifier on this data set, the accuracy score is 68%.

![BRFC_Acc_Score](https://user-images.githubusercontent.com/86331812/148653554-8f0c455c-53ff-4a34-bfb7-2446d7ab6d8d.png)

Confusion Matrix:

![BRFC_Confusion](https://user-images.githubusercontent.com/86331812/148653462-8f1dfb4b-0ece-4279-aacf-343d9ef5e234.png)

The classification report shows the precision and recall of the model as 100% and 100%, respectively, for predicting low risk credit.

![BRFC_Class_Report](https://user-images.githubusercontent.com/86331812/148653480-c98ad0c4-bd83-401a-b38c-b423a146800f.png)


#### Easy Ensemble AdaBoost Classifer
Easy Ensemble AdaBoost combines multiple classifiers to increase the accurracy of the the classifiers.  It is iterative in nature and builds up on the stronger classifier that from the multiple poorly performing classifiers. 
Using the Easy Ensemble AdaBoost Classifier, the accuracy score is 92%.

![EEAC_Acc_Score](https://user-images.githubusercontent.com/86331812/148653566-7490114c-70ac-43d3-9627-ffc87f389f90.png)

Confusion Matrix: 

![EEAC_Confusion](https://user-images.githubusercontent.com/86331812/148653576-701c23ff-f999-4b91-b786-5f051d466052.png)

The classification report shows the precision and recall of the model as 100% and 92%, respectively, for predicting low risk credit.

![EEAC_Class_Report](https://user-images.githubusercontent.com/86331812/148653597-a3c46e15-2b9c-44c0-88fa-55824c724fe2.png)

## Summary

The analysis shows that as the models use more iterations and complexity, they become more accurate.  Based on this analysis, I would recommend using Easy Ensemble AdaBoost Classifier. It shows a 92% accuracy while also showing an impressive precision and recall score when for the prediction of low risk credit. 
