# Student Success Prediction

This project aims to predict the success of students based of various features using different machine learning models. This dataset used in this project is StudentsPerformance.csv found from [Kaggle](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams/data), which includes information about student demographics, parent education levels, lunch types, preparation courses, and scores in math, reading, and writing. 

## Data Preperation

1. Load the Dataset: Reading the CSV file into a DataFrame.
2. Check for Missing Values: Ensure there are no missing values with .isnull.sum()
3. Encode Categorical Variables: Use one-hot coding for categorical variables.
4. Normalize Numerical Variables: Standardize numerical features.
5. Create Target Variable: Define 'success' as a student having an average socre of above 70.
6. Split the Data: Split the data into training and testing sets.

## Model Training
- Neural Network model is defined with a structure of an Input Layer, two Hidden Layers, and an Output layer. The model is compiled using 'binary_crossentropy' loss and 'adam' optimizer, and trained for 100 epochs.
- A Random Forest Regressor model is trained to compare preformance with the neural network model.

## Evaluation
The Neural Network model is evaluated based on Loss (2.43153e-04)and Accuracy (1.00) and the Random Forest model is evaluated based on Mean Squared Error (0.0) and R-Squared Score (1.0). Due to both models achieving perfect accuracy on the test set, there is potential for overfitted data or data leakage.
