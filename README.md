# Student Performance Predictor

## Project Overview

The Student Performance Predictor is a Machine Learning web application that predicts a student's math score based on academic and demographic features such as:

* Gender
* Race/Ethnicity
* Parental Level of Education
* Lunch Type
* Test Preparation Course
* Reading Score
* Writing Score

This project demonstrates a complete end-to-end machine learning pipeline including data preprocessing, model training, evaluation, and deployment using Flask.

---

## Problem Statement

Educational institutions often need to identify students who may require additional academic support. This project builds a regression model that predicts student performance using historical academic data.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-Learn
* Flask
* HTML/CSS
* Pickle

---

## Project Structure

```
Student-Performance-Predictor/
│
├── artifacts/
│   ├── model.pkl
│   └── preprocessor.pkl
│
├── src/
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   │
│   ├── pipeline/
│   │   └── predict_pipeline.py
│   │
│   ├── exception.py
│   └── utils.py
│
├── templates/
│   └── index.html
│
├── app.py
├── requirements.txt
└── README.md
```

---

## Machine Learning Pipeline

### 1. Data Ingestion

* Reads the dataset (CSV file)
* Splits data into training and testing sets

### 2. Data Transformation

* Handles categorical encoding using OneHotEncoder
* Scales numerical features
* Creates preprocessing pipeline

### 3. Model Training

* Trains multiple regression models
* Selects the best model based on R² score
* Saves the trained model and preprocessor as `.pkl` files

### 4. Prediction Pipeline

* Loads the trained model
* Accepts user input from the web form
* Returns the predicted math score

---

## Models Used

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor
* Gradient Boosting Regressor

The best-performing model is automatically selected based on evaluation metrics.

---

## Running the Application

### Create Virtual Environment

```bash
conda create -p venv python=3.10 -y
conda activate venv
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run the Application

```bash
python app.py
```

Open your browser and go to:

```
http://127.0.0.1:5000/
```

---

## Example Prediction

Input:

* Reading Score = 70
* Writing Score = 75
* Test Preparation Course = Completed

Output:

```
Predicted Math Score: 72.4
```

---

## Key Learnings

* Building an end-to-end ML pipeline
* Modular coding structure
* Exception handling in production-level code
* Model serialization using pickle
* Integrating Flask with machine learning models

---

## Future Improvements

* Add model performance dashboard
* Deploy the application to cloud platforms
* Add database integration
* Implement user authentication

---

## Author

Sai Sushanth Sailla


