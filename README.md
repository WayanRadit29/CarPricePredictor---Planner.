# CarPricePredictor---Planner

**CarPricePredictor---Planner** is an end-to-end solution that:  
1. **Predicts used car prices** via a linear regression model (~95 % R²), and  
2. **Plans optimal production** to maximize profit under weight, efficiency, and capacity constraints.

---

## 🚀 Project Overview

1. **Price Prediction**  
   - Load and clean the provided `CarPrice_Assignment.csv` dataset  
   - Engineer features (vehicle age, engine specs, fuel type, etc.)  
   - Train a scikit-learn Linear Regression model in Jupyter  
   - Achieve ~95 % R² on a held-out test set  

2. **Production Planning**  
   - Use predicted unit prices and key specs (curb weight, MPG)  
   - Define constraints: total plant capacity, aggregate weight, minimum fuel efficiency  
   - Formulate and solve a linear program (SciPy `linprog`)  
   - Output the optimal mix of models and the projected maximum profit

## 📁 Repository Structure
├── CarPrice_Assignment.csv # Raw used-car dataset
├── car-price-prediction.ipynb # Notebook: EDA, modeling, evaluation
├── ProductionOptimizer.py # Script: linear program solver for production
└── README.md # This documentation


---

## 📊 Data Description

- **CarPrice_Assignment.csv** (~2 000 records)  
  Features include make, model, year, engine size, horsepower, mileage, and sale price.

---

## 🔧 Price Prediction

Open `car-price-prediction.ipynb` to:

1. Load, clean, and encode the data  
2. Visualize distributions and correlations  
3. Create derived features (e.g., `age = current_year − model_year`)  
4. Split into training/test sets  
5. Train and evaluate a Linear Regression model  
6. Report metrics: R², MAE, RMSE  

> **Result**: ~95 % variance explained on test set.

---

## ⚙️ Production Planning

Run:

```bash
python ProductionOptimizer.py

