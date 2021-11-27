# ML_Project_Code

Abstract :
Heart diseases (Cardiovascular diseases) are a group of heart and vessel disorders that are the leading cause of death globally, taking an estimated 17.9 million lives each year. Even if you feel fine right now, you may be a ticking time bomb for heart disease; therefore, it’s also essential to keep health risks in perspective. It is necessary to
regularly monitor various parameters like blood pressure, cholesterol, weight, etc. Being aware of these numbers should be a standard part of being engaged with your heart health. The main motive behind our machine learning project is to critically examine the available dataset and estimate the risk factors of CVDs and strokes with satisfactory accuracy. It aims to warn the people to prevent further deterioration of their heart health and ensure swift action to mitigate grievous health disorders.

Introduction :
Our project focuses on the prediction of heart diseases. We have a dataset of the residents of Framingham, Massachusetts, and we are predicting if they will suffer from heart disease or not based on 16 features. Additionally, we intend to find the impact of different factors on the output and find correlations between them. All of this is
performed as an attempt to raise awareness and take precautionary measures to try and prevent heart diseases.

Link to the dataset : https://www.kaggle.com/dileep070/heart-disease-prediction-using-logistic-regression

Dataset details : 
The dataset is from a cardiovascular study on residents of the town of Framingham, Massachusetts. It contains 4238 samples and 16 features that range from medical details like
cholesterol levels, blood pressure, BMI, heart rate, BP meds, etc., to personal information like sex, age, and cigarette consumption. Most of the features containing the medical
details were continuous while some were in binary(0,1) where one meant that the subject had the problem of the respective feature column. The feature "male" was encoded where 1 represented male and 0 represented female. All the features were either of type int64 or float64. The dataset did not contain duplicate data. Seven features had missing values, which were handled in pre-processing. We used other inbuilt functions to find some statistical values, like minimum value for each feature, the maximum value of each feature, count of unique values in each feature column, the number of missing and duplicate values, mean, datatype, etc. Further, we used matplotlib and seaborn to visualize the dataset's features better using plots like pie charts, histograms, density plots, etc. All this helped to explore the dataset, develop a better understanding, analyze and help pre-process.

Methodology and model details :
Firstly we performed exploratory data analysis (EDA) to obtain some statistical values and visualize the dataset. After exploring the dataset, we proceeded to try out different methods for preprocessing and selected the best based on the evaluation of the models. We have considered the following models: Logistic Regression, Decision Tree Classifier, SGD Classifier, Gaussian Naive Bayes classifier, AdaBoost Classifier, KNeighborsClassifier, Support Vector Machine, and Random Forest Classifier. We found the above-mentioned
preprocessing steps as the most appropriate and divided the dataset into train and tested with a ratio of 8:2. Then we trained all the models and tested their performance using
accuracy, precision, recall, confusion matrix. After this, we selected the best model according to our analysis. We followed this by making several different plots to support our analysis and describe the working of the chosen model on the dataset.

Result and Analysis :
We tried different ways for various steps and
obtained different results, consequently
drawing the following conclusions.

● Based on correlation of features
  Based on the heatmap, we performed feature selection considering a threshold of 0.65. This means we ignored the features having a correlation of greater than or equal to 0.65.
  
● Based on pre-processing steps
  We performed a combination of the following steps and obtained the following results on the four models.
  Step 1 :
  Filling the missing values in the feature columns "cigPerDay," "totChol," and "BPMeds" with their respective means.
  Step 2 :
  Dropping all the null values.
  Step 3 :
  Performing feature selection and consequent dropping of "education," "glucose," "diaBP," "currentSmoker" feature columns with the help of the heatmap formed.
  Step 4 :
  Finding outliers using the z-score method and removing them with the threshold 3.
  Step 5 :
  Performing SMOTE to balance data.
  Step 6 :
  Performing normalization using the "Min-Max Scaler" technique.
  Refer to “Table 1 and Table 3”

● Based on evaluation metrics
  After performing these preprocessing steps, we obtained the following results :
  Refer to “Table 2”
  Looking at the results mentioned in “Table 2”, we find KNN to be the best model for our dataset. From our evaluation till the midterm, we found the random forest to be the       best model; however, after changing preprocessing steps, various other analysis measures, and trying out several different models, we found KNN to be better because of high     recall. (Recall is important because we want fewer false negatives due to the disease-related dataset).
  
 Learnings :
● We each read a research paper which helped in discovering new ideas and guided our project.
  
● We learned about the different EDA techniques and tried various inbuilt functions to explore and visualize the dataset.
  
● Another takeaway was experimenting, analyzing, and deciding on the different preprocessing strategies to use.
  
● We compared heatmap before and after feature selection.
  
● This was followed by trying out different models and using various evaluation metrics to assess their performance.
  
● We compared random forest and KNN using plots to find KNN to be better for our dataset.
  
● We also used KMeans clustering to evaluate our model based on unsupervised learning.
  
 Analysis and results :
 ● We found the preprocessing strategies mentioned in “Table 1 and Table 3” to be the most appropriate based on accuracy, precision, recall and confusion matrix.
  
● Earlier we had established random forest to be the best model, however after addition of other preprocessing strategies and analyzing more models, we find KNN to be the most     suitable model for our dataset. This is because the recall value is significantly higher for KNN which is important for our dataset since we want to reduce the false             negatives.

● Using KMeans clustering for unsupervised evaluation, we see a reduction in the error as the number of clusters increases. This might be because when the number of clusters       increases, the number of points in a cluster decreases. If we consider circular points, then the error would be the distance from the median. So as the clusters increase,       there will come a time when there will be only one point in the cluster. Since that point would be the median itself, the error would become 0. This logic can help us develop   intuition about why error reduces as the number of clusters increases.

References :
Table 2 :

Model                         Accuracy                        Precision                     Recall
Logistic Regression       0.6303236797274276              0.6362098138747885          0.6319327731092437
Decision Tree             0.7879045996592845              0.7772435897435898          0.8151260504201681
Gaussian NB               0.6039182282793867              0.6450892857142857          0.4857142857142857
Random Forest             0.8620102214650767              0.8464                      0.8890756302521008
Ada Boost                 0.6908006814310051              0.6972789115646258          0.6890756302521008
KNN                       0.8415672913117547              0.7687253613666228          0.9831932773109243
SGD                       0.5178875638841567              0.5125324114088159          0.9966386554621849
SVM                       0.6448040885860307              0.6463815789473685          0.6605042016806723
