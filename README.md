# Smart Traffic Signal Simulation using Modelling & Machine Learning

---

## Objective
The objective of this project is to generate synthetic data using computer simulation and apply multiple Machine Learning models to determine the most accurate predictor for traffic waiting time.

---

## Simulation Tool
**SimPy** – A lightweight Python-based discrete-event simulation library used to model real-world systems such as traffic flow, queues, and resource allocation.

---

## Project Workflow

### Step 1 – Tool Selection
SimPy was selected due to its ease of integration with Python and its capability to generate simulation-based synthetic datasets efficiently.

---

### Step 2 – Installation & Exploration
All required libraries were installed using `pip` in Google Colab and small test simulations were executed to understand the working of SimPy.

---

### Step 3 – Parameter Study

| Parameter | Lower Bound | Upper Bound |
|-----------|-------------|-------------|
| Vehicle Arrival Rate | 5 | 40 |
| Green Signal Time | 20 | 90 |
| Red Signal Time | 20 | 90 |
| Number of Lanes | 1 | 4 |
| Simulation Duration | 60 | 300 |

These parameters influence congestion level, waiting time, and overall traffic efficiency.

---

### Step 4 – Random Parameter Generation
Random values between the lower and upper bounds were generated using **NumPy** for every simulation run.

---

### Step 5 – 1000 Simulations
A total of **1000 simulation runs** were executed.  
The generated dataset was stored in:

simulation_data.csv

---

### Step 6 – Machine Learning Model Comparison
Multiple regression models were trained and evaluated using performance metrics to identify the best performing model.

---

## Machine Learning Models Used

- Linear Regression  
- Decision Tree Regressor  
- Random Forest Regressor  
- K-Nearest Neighbors Regressor  
- Support Vector Regressor  
- Gradient Boosting Regressor  

---

## Evaluation Metrics

- **R² Score** – Measures prediction accuracy  
- **MAE (Mean Absolute Error)** – Measures average prediction error  
- **RMSE (Root Mean Squared Error)** – Penalizes large prediction errors  

---

## Results
<img width="760" height="208" alt="image" src="https://github.com/user-attachments/assets/ff6d9abb-3b7b-43b1-b3ec-800bb81e7086" />

The best model according to this was Linear Regression.
---

### Best Model Selection – TOPSIS Method
To ensure fair comparison across multiple metrics, the **TOPSIS (Technique for Order Preference by Similarity to Ideal Solution)** method was manually implemented.

The model with **Rank 1** in topsis_results.csv is considered the most accurate and balanced predictor.

---

## Graphical Analysis

### Model vs R² Score
<img width="993" height="615" alt="image" src="https://github.com/user-attachments/assets/2f9f6871-a0a0-4db7-8604-b45c0054335a" />

### Model vs MAE
<img width="986" height="613" alt="image" src="https://github.com/user-attachments/assets/b86129ad-237f-4a4d-9b24-bed514e66dc0" />

### Model vs RMSE
<img width="986" height="617" alt="image" src="https://github.com/user-attachments/assets/868f9066-62d7-4e9d-9cff-e0a60697bb3f" />

---

## Conclusion
This project demonstrates how simulation-generated synthetic datasets can effectively be used to train and evaluate Machine Learning models.  
By combining **Simulation + Machine Learning + TOPSIS multi-criteria decision making**, the most suitable predictive model for traffic waiting time was successfully identified.

---

## Files Included

- `traffic_signal_simulation.ipynb` – Complete notebook  
- `simulation_data.csv` – Generated synthetic dataset  
- `model_results.csv` – ML evaluation results  
- `topsis_results.csv` – TOPSIS ranking results  
- `README.md` – Project documentation  

---

## How to Run

1. Open the notebook in **Google Colab**
2. Install required libraries
3. Run all cells sequentially
4. CSV files and graphs will be generated automatically
