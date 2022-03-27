## Overview
This goal of the project is to perform binary classification using machine learning to classify whether a patient has diabetes or not based on the diagnostic measurements provided in the dataset. The dataset used is the Pima Indians Diabetes Database which consists of 768 female patients with certain numerical features (Glucose, BloodPressure, etc.) along with the class label.

As step 1 of this exercise, the data is first processed before being trained and tested. For the second step, we have trained a Logistic Regression classifier. As part of this exercise the model has been coded from scratch without the use of common libraries like sklearn, etc. The data is divided into train (60%), test (20%), validation (20%) and model are trained. A look into the performance metrics comprises the third step of this exercise.

As part of the next phase, the same dataset is also introduced to a neural networks model with the help of the tensorflow module from python. The model is built through multiple iterations with different hidden layers, regularization functions, etc. The comparison between multiple iterations of the results of this model is the final part of this work.

## Preprocessing
The data is read and stored as a pandas dataframe. The data has 768 rows and 9 columns. The ‘Outcome’ column is the target variable and contains two class – 0 and 1.

1. **Duplicate Check** - The data is initially checked for row level duplicates
2. **Zero values sense check** - The number of zeros in each variable is checked to check if the data is filled with too many meaningless values. Columns like Glucose, BloodPressure, SkinThickness and BMI do not make sense if they are zero.
3. **Data Standardization** - It is observed that the range of each variable is quite different from the other. This may affect the weight of the model. To tackle this, each column has to be standardized.
4. **Handling Class Imbalance** - There is a class imbalance with a higher number of 0’s than 1’s, so the data is oversampled before modelling.
5. **Train-test split** - The data is split in the ratio of 60:20:20 (Train:Test:Validation)

## Modelling
1. **Logistic Regression** - The Logistic Regression Model is coded from scratch
2. **Neural Network** - Three different variations of neural networks were built. The keras module from the tensorflow package was used to build each iteration of the model.

   1. 1 hidden layer with L2 regularization
   2. 1 hidden layer with L1 regularization
   3. 1 hidden layer and 1 dropout with L2 regularization

## Project Work
This is the code repository for my project in CSE-574 Machine Learning course.
