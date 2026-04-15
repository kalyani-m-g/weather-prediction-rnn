# 🌦️ Weather Prediction using RNN

## 📌 Project Overview

This project predicts future weather conditions using a Recurrent Neural Network (RNN) trained on historical weather data. Since weather patterns are sequential and depend on previous days, RNN is well suited for time-series forecasting.

The model uses past weather observations such as temperature, rainfall, sunshine, and cloud cover to predict the next day’s mean temperature.

---

## 🎯 Objective

To build a deep learning model that learns weather trends from historical data and forecasts future temperature values accurately.

---

## 📂 Dataset Used

Dataset: **London Weather Dataset**

Features used in training:

* Mean Temperature
* Minimum Temperature
* Maximum Temperature
* Precipitation
* Cloud Cover
* Sunshine Duration

Missing values were handled before training.

---

## ⚙️ The Process

### 1. Data Preprocessing

* Loaded historical weather dataset using Pandas.
* Selected relevant numerical weather features.
* Removed / filled missing values.
* Sorted data chronologically.
* Applied MinMaxScaler normalization to improve model learning.

### 2. Sequence Creation

Weather is time-dependent, so previous days were used to predict the next day.

* Used past **7 days** data as input sequence.
* Predicted the **8th day mean temperature**.

### 3. Train-Test Split

* 80% data used for training
* 20% data used for testing

### 4. Tensor Conversion

Data converted into PyTorch tensors and loaded using DataLoader for batch training.

---

## 🧠 Model Architecture

The model was built using PyTorch.

### Architecture:

* Input Layer: 6 weather features
* RNN Layer: 64 hidden units
* Activation: tanh (default RNN activation)
* Fully Connected Dense Layer: 1 neuron
* Output: Predicted next day mean temperature

### Loss Function

* Mean Squared Error (MSE)

### Optimizer

* Adam Optimizer

### Training Configuration

* Epochs: 25
* Batch Size: 32
* Learning Rate: 0.001

---

## 📈 Results

The model successfully learned temperature trends from historical weather data.

### Evaluation Metrics

* Mean Squared Error (MSE)
* Mean Absolute Error (MAE)

### Output Visualizations

* Actual vs Predicted Temperature Graph
* Training Loss Curve

The predicted values followed the real trend closely, showing that the RNN captured temporal weather patterns effectively.

---

## 🚀 How to Run

```bash
pip install pandas numpy matplotlib scikit-learn torch
```

Run the notebook or Python script and upload the dataset when prompted.

---

## 📌 Future Improvements

* Replace Simple RNN with LSTM or GRU
* Predict multiple future days
* Add humidity / wind speed features
* Deploy as Streamlit web app

---

## 👩‍💻 Author

Kalyani
