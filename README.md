# Student Success Deep Dive

This project aims to create a deep dive analysis of students based on various features using different machine learning models. This dataset used in this project is StudentsPerformance.csv found from [Kaggle](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams/data), which includes information about student demographics, parent education levels, lunch types, preparation courses, and scores in math, reading, and writing. 

## Data Preparation 

1. Load the Dataset: Reading the CSV file into a DataFrame.
2. Check for Missing Values: Ensure there are no missing values with .isnull.sum()
3. Encode Categorical Variables: Use one-hot coding for categorical variables.
4. Normalize Numerical Variables: Standardize numerical features.
5. Create Target Variable: Define 'success' as a student having an average score of above 70.
6. Split the Data: Split the data into training and testing sets.

## Model Training
- Neural Network model is defined with a structure of an Input Layer, two Hidden Layers, and an Output layer. The model is compiled using 'binary_crossentropy' loss and 'adam' optimizer, and trained for 100 epochs.
- A Random Forest Regressor model is trained to compare preformance with the neural network model.

## Evaluation
The Neural Network model is evaluated based on Loss (2.43153e-04)and Accuracy (1.00) and the Random Forest model is evaluated based on Mean Squared Error (0.0) and R-Squared Score (1.0). Due to both models achieving perfect accuracy on the test set, there is potential for overfitted data or data leakage.

## Data Analysis Using SparkSQL

By conducting a detail analysis using SparkSQL, we can better understand the various factors influencing students success and further refine our models to ensure accuracy and generalizability. 

## Results
- Students who's parents education tended to have higher average reading and writing scores, but similar scores to other students in math. On average students who's parents completed highscool or some highshool had lower average scores in all three subjects.

- Students who had reduced or free lunches had lower scores on average in all three subjects.

- Students who completed test preparation courses had higher average scores in all three subjects.

- Based on scores, female students had higher average reading and writing scores, while male students had higher average math scores.

- On Average, White Students had the highest scores overall, and Native students had the lowest average scores.


## Presentation Link
[Presentation](https://www.canva.com/design/DAGNChaWtG8/9w96h0OMf5jmJjL9ChiDjw/edit?utm_content=DAGNChaWtG8&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)
