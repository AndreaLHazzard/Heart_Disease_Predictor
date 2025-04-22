# Heart_Disease_Predictor
 Project 4

Cori Esposito, Andrea Hazzard, Sebastian Lopez, Brandon Schaeffer

## Objective
Predict the probability of heart disease using patient demographic and clinical data

## Dataset
The UCI Heart Disease dataset was used. The dataset contained 298 rows of data and 7 columns. Data was fairly evenly split between those with no disease and those with heart disease

The dataset is popular for training and evaluating classification models in machine learning — especially for predicting the presence of heart disease.

## Technologies
* Python
* Scikit-learn
* Keras
* PostgreSQL

## Models
* Logistic Regression
* Random Forest
* Neural Network

## Data Preprocessing
Data was imported and cleaned using python.

Cleaning including renaming columns to be user friendly including identifying and renaming the target column.

Features were scaled using StandardScaler

Data was split into 80% training 20% testing.

## Results for Logistic Regression and Random Forest

Logistic Regression Classification Report:
               precision    recall  f1-score   support

           0       0.77      0.72      0.74        32
           1       0.70      0.75      0.72        28

    accuracy                           0.73        60
   macro avg       0.73      0.73      0.73        60
weighted avg       0.74      0.73      0.73        60

ROC AUC: 0.8415178571428571

### Random Forest

Random Forest Classification Report:
               precision    recall  f1-score   support

           0       0.73      0.69      0.71        32
           1       0.67      0.71      0.69        28

    accuracy                           0.70        60
   macro avg       0.70      0.70      0.70        60
weighted avg       0.70      0.70      0.70        60

ROC AUC: 0.8470982142857143

## Neural Network

### Neural Network Architecture
Input layer (32 neurons)
2 hidden layers (16 and 8 neurons): 20% dropout
Activation: ReLU + Sigmoid

The 20% dropout was used to correct overfitting in early trials.

### Neural Network Results
Epoch 100/100
8/8 ━━━━━━━━━━━━━━━━━━━━ 0s 13ms/step - accuracy: 0.9363 - loss: 0.1912 - val_accuracy: 0.7833 - val_loss: 0.7474
2/2 ━━━━━━━━━━━━━━━━━━━━ 0s 28ms/step - accuracy: 0.8035 - loss: 0.6908
Neural Network Test Accuracy: 0.78

# Conclusions
## Factors that ae good indicators of heart disease:
* Age
* Sex
* Chest pain type (more on this later)
* Resting EKG results
* Maximum heart rate achieved during exercise
* Exercised induced angina

## Unexpected Results
The dataset showed that those showing no chest pain symptoms had a higher likelihood of having heart disease. Upon further research, it was noted that their condition may go unnotices longer and they do not seek care until more serious issues arise.

As a result, asymptomatic doesn't mean health.
