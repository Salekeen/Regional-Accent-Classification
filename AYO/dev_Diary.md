# Visualization
- t-SNE for the whole dataset visualization. Gotta normalize the whole dataset before!

---
# Model Building

## Random Forest:
First I wanna implement Random forest. As there's no need for preprocessing the data, this should be done quite easily.

Three things I wanna accomplish with this model:
- Find Most important features and sort them
- Make *learning* and *validation* curve to diagonize bias-variance tradeoff. Based on this, two approach should be taken:
  1. Bagging (DT as base claffier)
  2. Boosting (XGBoost)
- Plot the trees to get better understanding of the model

Now I'm gonna lay down the basic structure of the model building:
1. Make train,test split
2. Build the model with default parameters
   - Note down train accuracy 
   - Note down test accuracy
3. Hyperparameter tuning:
   - Initialize params-grid
   - Initialize skf (stratifiedK-Fold) to set it as our CV (Cross validator)
   - Do GridSearchCV with params-space and CV and then fit to the data
   - List:
     - best parameters
     - best score 
     - best estimator
   - **Test the best estimator against test set to find its accuracy**
4. Plot **Validation Curve** for some of the hyperparameters to find out whether the estimator is overfitting or underfitting for some hyperparameter values.
5. Plot **Learning Curve** to find out whether we have a bian or variance problem. This is the most important step of model debugging! Note to myself: Be patient here!
6. According to the problem, improve the model!

## Update: March 25

- Build ExtraTreesClassifier to reduce variance!





