# SMS Spam Detection

This project implements an AI model to classify SMS messages as spam or legitimate using techniques like TF-IDF and various classifiers, including Naive Bayes, Logistic Regression, and Support Vector Machines (SVM).

## Table of Contents

- [Overview](#overview)
- [Technologies Used](#technologies-used)
- [Dataset](#dataset)
- [Model Training](#model-training)
- [API](#api)
- [Deployment](#deployment)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Overview

The goal of this project is to develop a machine learning model that accurately identifies spam messages in SMS data. By leveraging text feature extraction methods and classification algorithms, the model aims to provide reliable predictions on incoming messages.

## Technologies Used

- Python
- Pandas
- Scikit-learn
- Flask
- Joblib

## Dataset

The dataset used in this project is derived from a CSV file containing SMS messages labeled as 'ham' (legitimate) or 'spam'. The dataset can be found in the `sms_data` folder, and the specific file used is `spam.csv`.

## Model Training

1. **Load the Dataset**: The dataset is read into a Pandas DataFrame.
2. **Data Cleaning**: Unnecessary columns are removed, and labels are mapped to binary values (0 for ham, 1 for spam).
3. **Data Splitting**: The dataset is split into training and testing sets.
4. **TF-IDF Vectorization**: Text messages are converted into a numerical format using TF-IDF.
5. **Training Classifiers**: The following classifiers are trained and evaluated:
   - Naive Bayes
   - Logistic Regression
   - Support Vector Machine (SVM)

## API

A simple RESTful API is created using Flask, allowing users to send SMS messages and receive predictions on whether they are spam or ham.

### Endpoints

- `POST /predict`
  - **Request Body**: JSON object with a `message` key containing the SMS text.
  - **Response**: JSON object indicating whether the message is spam (`true` or `false`).

## Deployment

This project can be deployed on platforms like Heroku, AWS, or Google Cloud. Follow the deployment instructions specific to your chosen platform.

### Heroku Deployment Example

1. Install the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli).
2. Create a `requirements.txt` file listing all dependencies.
3. Create a `Procfile` with the following content:
