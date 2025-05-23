# ✈️ Flight Delay Prediction 
This project uses a Random Forest Classifier to predict whether a flight will be delayed based on historical flight data and user inputs. It allows users to visualize the likelihood of delay for the next 7 days between a given origin and destination airport.

## 📊 Project Overview
Model Used: Random Forest Classifier

### Accuracy:

Initial: ~60%

After Tuning: ~79%

Evaluation Metrics: Accuracy, Precision, Recall, ROC-AUC Score, Confusion Matrix

### Input Features:

Year, Quarter, Month, DayofMonth, DayOfWeek

One-hot encoded: Origin, Dest

## 🛠️ Key Features
Handles missing values

Supports multiple airports

One-hot encoding of categorical features

Cross-validation with 5 folds

Delay prediction for the next 7 days

Matplotlib visualization of delay probabilities

Threshold-based interpretation (> 50% = likely delay)

## 📁 Dataset
File: flight_delay_predict.csv

Includes columns like is_delay, Year, Quarter, Month, DayofMonth, DayOfWeek, Origin, Dest

## ⚙️ How It Works
### Data Preprocessing

Check and remove missing values

One-hot encode categorical columns (Origin, Dest)

Feature selection and train-test split

### Model Training

Train a Random Forest Classifier

Apply 5-fold cross-validation

### Evaluate using:

Accuracy

ROC-AUC Score

Precision & Recall

Confusion Matrix

### User Interface Functionality

Input: Departure date, Origin, Destination

Output: Probability of delay

Visualizes delay probabilities for the next 7 days using Matplotlib

## 🧠 Prediction Functions
predict_delay(departure_date, origin, destination)
Predicts the probability of delay for a given date and route.

predict_delay_next_7_days(start_date, origin, destination)
Predicts and plots delay probabilities for the next 7 days starting from a given date.

# 📌 Sample Usage
predict_delay_next_7_days('21/02/2025', 'CLT', 'PHX')
predict_delay_next_7_days('21/02/2025', 'LAX', 'SFO')

# 🚀 Future Improvements
Include weather and carrier-specific data

Build a web interface using Flask or Streamlit

Implement real-time data streaming for live updates

Expand to more airports

# 📝 Dependencies
pandas

numpy

matplotlib

sklearn

datetime
