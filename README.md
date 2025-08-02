# 🚀 Spaceship Titanic - Passenger Transport Prediction

## 📌 Overview

The Spaceship Titanic was a luxury interstellar cruise ship that disappeared en route to TRAPPIST-1e. Our mission is to predict whether a passenger was **transported to another dimension** based on their profile and onboard behavior.

This project is inspired by a Kaggle competition and involves applying **classification models** to a fictional but structured dataset with demographic, categorical, and spending features.

## 🎯 Objective

To build a predictive machine learning model that determines the `Transported` status (True/False) of passengers using features like:
- HomePlanet
- Age
- Cabin details
- VIP status
- Onboard services usage (Spa, VRDeck, FoodCourt, etc.)


## 🧩 Dataset Features

| Column Name     | Description                                |
|------------------|--------------------------------------------|
| PassengerId      | Unique ID for each passenger               |
| HomePlanet       | Origin planet of the passenger             |
| CryoSleep        | Whether the passenger was in cryo-sleep    |
| Cabin            | Cabin number, further split into Deck/Side|
| Destination      | Final destination                         |
| Age              | Passenger’s age                            |
| VIP              | VIP status                                 |
| RoomService, FoodCourt, ShoppingMall, Spa, VRDeck | Spending amounts |
| Transported      | Target variable (True if transported)      |
| Grouped, Deck, Side, Has_expenses, Is_Embryo | Engineered features |


## 📊 Exploratory Data Analysis (EDA)

- Identified missing values in multiple features (e.g., `Cabin`, `HomePlanet`, `VIP`)
- Visualized transport rates across CryoSleep, Age bins, and Destination
- Noted high correlation between `CryoSleep`, `VIP`, and `Transported`


## 🏗️ Feature Engineering

- Extracted `Deck` and `Side` from `Cabin`
- Created `TotalSpent` from sum of onboard services
- Engineered `Has_expenses` and `Is_Embryo` as new boolean features


## 🤖 Model Development

| Model                | Accuracy Score |
|---------------------|----------------|
| Logistic Regression | 76.2%          |
| Random Forest       | **82.5%** ✅    |
| XGBoost             | 81.8%          |

**Random Forest** gave the best result on the validation set.

## 📈 Feature Importance (Random Forest)

Top predictors for being transported:
- CryoSleep
- Destination
- VIP
- Age
- RoomService, VRDeck

## 🛠️ Tools & Libraries

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn
- XGBoost


## 📁 Folder Structure

