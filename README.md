# StrokeRiskPredictor-
AI-powered stroke risk prediction web app using XGBoost with SHAP-based explainability and personalized health &amp; diet recommendations. Built with Flask and deployed on Render.

Here's a detailed README template for your project on GitHub:



# Stroke Risk Prediction Model

This project is aimed at predicting the risk of stroke using machine learning techniques. The model evaluates various health parameters such as age, sex, BMI, cholesterol levels, hypertension, and more to determine the likelihood of a person experiencing a stroke. The primary goal is to provide insights into stroke risk and offer personalized recommendations for lifestyle changes based on the prediction results.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Model Training](#model-training)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

This project implements a **stroke risk prediction model** using the **XGBoost** algorithm. The model is trained using a dataset that includes various health-related features such as:
- Age
- Sex
- Hypertension
- Heart Disease
- Average Glucose Levels
- BMI
- Smoking Status
- Previous Stroke

The goal is to predict the likelihood of a stroke occurring, with the following output:
- **Risk Percentage**: The likelihood of having a stroke.
- **Risk Level**: Categorized into **Low**, **Medium**, or **High** risk.
- **Personalized Recommendations**: Tailored health advice based on the risk level, including lifestyle suggestions and food recommendations.

## Features

- **Stroke Risk Prediction**: Predicts the probability of stroke for an individual based on input health data.
- **Personalized Recommendations**: Suggests health practices and food plans based on predicted risk.
- **Data Preprocessing**: Categorical variables are handled, and missing data is imputed before model training.
- **Model Explainability**: Uses SHAP (SHapley Additive exPlanations) to interpret and explain the model's predictions.

## Installation

### Prerequisites

1. **Python 3.7+**: Ensure that you have Python installed on your system. If not, download and install it from the official Python website.
2. **pip**: Python's package installer for installing dependencies.

### Steps to Install

1. Clone the repository:

```bash
git clone https://github.com/yourusername/repositoryname.git
cd repositoryname
```

2. Create a virtual environment:

```bash
python3 -m venv venv
```

3. Activate the virtual environment:
   - On Windows:

   ```bash
   .\venv\Scripts\activate
   ```

   - On macOS/Linux:

   ```bash
   source venv/bin/activate
   ```

4. Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Usage

### Running the Model

1. Navigate to the project directory.
2. Use the provided Flask app to input health data via a web interface.
3. The app will output a stroke risk prediction and personalized recommendations.

Run the Flask application:

```bash
python app.py
```

Visit the application in your browser at `http://127.0.0.1:5000/`.

### Inputs

- **Age**: The age of the individual.
- **Sex**: The gender of the individual (Male/Female).
- **BMI**: The Body Mass Index of the individual.
- **Cholesterol**: Cholesterol level, categorized as low, normal, or high.
- **Hypertension**: Whether the individual has hypertension (Yes/No).
- **Atrial Fibrillation**: Presence of irregular heartbeat (Yes/No).
- **Smoking**: Whether the individual smokes (Yes/No).
- **Previous Stroke**: Whether the individual has had a stroke before (Yes/No).

### Output

- **Risk Percentage**: The probability of stroke.
- **Risk Level**: Categorized as low, medium, or high.
- **Personalized Recommendations**: Including lifestyle and dietary suggestions.

## Model Training

The model is based on **XGBoost**, which is a powerful gradient boosting algorithm. The training process involves the following steps:
- Data Preprocessing: Handle missing values, encode categorical variables, and scale the data.
- Model Tuning: Hyperparameters are optimized using techniques like **GridSearchCV**.
- Model Evaluation: The model is evaluated using metrics such as **accuracy**, **AUC**, and **F1 score**.

### Hyperparameters Tuned:
- Learning rate
- Max depth
- Number of estimators
- Subsample ratio

## Contributing

Contributions to this project are welcome! Feel free to fork the repository, make improvements, and create pull requests.

### How to Contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a new Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

