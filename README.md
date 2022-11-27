# Drug-Review-Prediction
CSC-180 Final Project. A drug review prediction.

## Description
   This is a CSC-180 Final project to do prediction on drug reviews. This project tends to present the sentiment of the reviews of a drug using machine learning models.
     It uses vectorization process like Word2Vec, TF-IDF, which can help recommend the top drug for a given disease by different classification algorithms. 
     The data is trained upon Neural Network, Logistic Regression and SVM. 

## Model Design
 Flowchart for the purposed model
 ```mermaid
 graph TD
    data_proc[Data Cleaning and Visualization]
    tfidf[TF-IDF Vectorizer]
    traintest[Train Test Split]
    train[Train Data]
    test[Test Data]
    smote[Smote]
    classifier[Classifiers]
   p[Precision]
   r[Recall]
   f[F1 Score]
   a[Accuracy]
   c[confusion matrix]
    eval[Metrics]
    data_proc -->tfidf-->traintest-->train -->smote-->classifier
    traintest-->test -->classifier -->eval 
    eval-->p
    eval-->r
    eval-->f
    eval -->a
    eval -->c 
  
 ```
## Results

