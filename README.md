# Bengali-Handwriting-Using-EL
A Python-based project on Bengali Handwritten character recognition using Ensemble Learning that integrates CNN and SVM models into a single image recognition model for a boost in accuracy

**Objectives of the Project**
- To select a group of ML algorithms that can be utilized for an Ensemble Learning model that can learn and predict handwritten Bengali characters and collect the performance data from the resulting model. 
- This data can be used as a reference for bigger and more complex systems.

**Method Used**
- “Averaging Ensemble Learning” and “Voting-based Ensemble Learning” were explored to train ML models to recognize handwritten Bengali characters.
- For Averaging, two configurations of CNNs (Convolutional Neural Networks) and two configurations of SVMs (Support Vector Machines) were used for the first Ensemble model
- For Voting, kNN, Decision Tree and Random Forest classifiers were used as constituents for the respective Ensemble model.

![image](https://github.com/Chief-boy-117/Bengali-Handwriting-Using-EL/assets/67178769/08aee550-80d3-4425-8c0c-863550e455cc)

**Implementation Details**
* A dataset containing 50 Bengali-handwritten characters, with 240 variations for training and 60 for testing, were for training the prediction models
* Models used during this research:
  1. CNN – implemented using keras library with two variants (20% and 50% dropped-out results)
  2. SVM – implemented using keras library with two variants (0% and 20% dropped-out results)
  3. kNN – implemented using sklearn library with k=5
  4. Decision Tree – implemented using sklearn library with criterion=‘gini’ and max depth=45
  5. Random Forest Classifier – implemented using sklearn library with criterion=log_loss and max_depth=30
* After training (in case of CNN and SVM) and testing for optimal configurations (in case for kNN, Decision Tree and Random Forest Classifier), the CNNs and SVMs were compiled into a single averaging Ensemble model, while the rest were used for a Voting-based Ensemble model using sklearn library’s VotingClassifier function.

**Results**

From the results obtained through testing the models, the following data was gathered regarding the accuracy values of the individual models and their respective Ensemble model.

![image](https://github.com/Chief-boy-117/Bengali-Handwriting-Using-EL/assets/67178769/fb3837a0-27d5-4067-b7db-dd4c8f79468b)

![image](https://github.com/Chief-boy-117/Bengali-Handwriting-Using-EL/assets/67178769/111b6fae-a1d8-4faa-95e2-3350c7318a6d)

**Inference**
- From the first table depicting data from CNN and SVM, we can see that Ensemble Learning has the best accuracy when compared against its constituent models as well as the highest validation accuracy. 
- The results obtained from the remaining classifiers (kNN, Decision Tree and Random Forest) show considerably poorer performance, a side effect of having to flatten images.
- We can see the benefits of using Ensemble Learning algorithms for Bengali Handwriting detection. It has managed to outperform its constituent models while marginally increasing the loss values, a trade-off that is well worth it.
- While this research work was able to produce satisfactory results and demonstrated the usefulness of Ensemble Learning models and its performance at detecting Bengali handwritten characters, there are still some improvements that can be made which weren’t attainable due to various restrictions like – utilizing a greater variety of image pattern recognition models and configurations, employing other modes of Ensemble Learning, like Boosting, etc.

