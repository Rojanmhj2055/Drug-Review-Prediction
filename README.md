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
In this work each review was divided into Positive
and Negative. TF-IDF vectorizer is used to represent
review text. The complexity of the training is
increased since we have input dimension of 2052. The
Tf-Idf vectorizer and One hot encoding from the
condition increased the dimension significantly.
From the table, DNN and SVC came close for the
highest accuracy of 0.92 and 0.93. The CNN did the
worse with the accuracy of 0.78. The metrics of the
positive class is higher than the Negative class which
can be an indication of the data imbalance during the
training. Randomized search shows that the best
model is the one with n_neurons 100 and 2 hidden
layers.

## Conclusion 
Reviews shows the important aspect how an item is
viewed in the population. Even when people do
anything on the internet, people check the reviews
that the given item/ place have. The drug review
prediction can be used to predict whether the review
is positive or negative and to analyze the sentiment of
the review. In this research, Logistic Regression,
DNN, CNN and SVC are trained and evaluated on
different metrics. SVC and DNN outperformed all
other model with the accuracy of 92% and 93%
respectively. CNN did the worse which can be due to
the complexity of the data. 

## Future Improvements
Even though this research went through a deep dive
of training and evaluation, there is always a way to
improve the model. Following are the ways the model
can be improved.
1. Using TF-IDF model with different max
features.
2. Using data sampling techniques like SMOTE,
up sampling and down sampling to decrease
the data imbalance.
3. This model has not gone for uni gram and bi
gram model for TF-IDF.
