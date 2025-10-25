# Flight Price Prediction Web App

A **Flight Price Prediction** web application built using **Flask** and **CatBoost Regressor** that predicts flight ticket prices based on inputs like airline, source, destination, date and time of travel, and total stops. The app integrates a machine learning model into a web interface for real-time predictions.

---

## 🔹 Project Overview

This web app allows users to predict flight ticket prices dynamically by entering:

- **Departure Date and Time**
- **Arrival Date and Time**
- **Total Stops**
- **Airline**
- **Source City**
- **Destination City**

The backend processes these inputs, transforms them into model-compatible features, and returns the predicted price instantly.

---

## 🔹 Model Details

- **Algorithm Used:** CatBoost Regressor  
- **Training Data:** `deploy_df.csv`  
- **Features Used:**
  - Date and time features (day, month, departure hour, arrival hour, duration)
  - Total Stops
  - Airline (One-hot encoded)
  - Source & Destination (One-hot encoded)
- **Target Variable:** Flight Price (`Price`)  

The model was trained using an 80-20 split on the dataset and saved using **pickle** for deployment.

---

## 🔹 Technologies Used

- **Backend:** Flask, Python  
- **Machine Learning:** CatBoost, scikit-learn, pandas, numpy  
- **Frontend:** HTML (Flask templates)  
- **Deployment:** Local Flask server  
- **Version Control:** GitHub  

---

## 🔹 How It Works

1. User enters travel details on the web page.
2. Flask backend extracts inputs and converts date/time into numeric features.
3. Airlines, source, and destination are **one-hot encoded**.
4. Duration is calculated from departure and arrival times.
5. Features are passed to the trained CatBoost model to predict the flight price.
6. Predicted price is displayed on the web page.

---

## 🔹 Getting Started

### Prerequisites

- Python 3.x
- Flask
- scikit-learn
- pandas
- catboost
- pickle
- Flask-CORS

Install dependencies:

```bash
pip install flask pandas scikit-learn catboost flask-cors
