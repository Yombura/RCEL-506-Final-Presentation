# 🚀 NASA Turbofan RUL Predictor: Predictive Maintenance Strategy
**RCEL 506: Applied Statistics & Data Science for Engineering Leaders**

### 🎯 Business Problem
In the aviation industry, unplanned engine maintenance is a primary driver of operational costs and safety risks. Traditional maintenance strategies often rely on:
1. **Run-to-failure:** High risk of catastrophic failure and flight cancellations.
2. **Fixed-interval maintenance:** High cost due to replacing components that still have useful life remaining.

**The Challenge:** How can we use real-time sensor data to predict the **Remaining Useful Life (RUL)** of a turbofan engine to transition from reactive to proactive maintenance?

### 💡 Proposed Solution
We developed a **Predictive Maintenance Model** using a Regularized Random Forest Regressor. By analyzing degradation patterns across multiple sensors, the model provides an objective estimate of when an engine will reach its failure point.

* **Benchmark Improvement:** Our solution reduced the Root Mean Square Error (RMSE) from a naive baseline of **43.82** to **31.76** (a 27.5% improvement).
* **Safety Buffer:** The model achieves a Mean Absolute Error (MAE) of **24.94 cycles**, providing a reliable window for scheduling maintenance before failure occurs.

### 📊 Data Source & Feature Engineering
* **Data Source:** The **NASA C-MAPSS FD001 Dataset**, which simulates turbofan engine degradation under sea-level conditions.
* **Preprocessing:** Removed 7 non-variant sensors (S1, S5, S10, S16, S18, S19, S21) that provided no physical degradation signal.
* **Feature Engineering (Rolling Averages):** Implemented a **10-cycle grouped rolling average** for all sensor inputs. This acts as a low-pass filter to remove stochastic sensor noise, allowing the model to focus on the underlying physical wear-and-tear (the "Health Signal").

### 📈 Final Performance Summary
| Metric | Naive Baseline (Fleet Mean) | Engineered Solution | Improvement |
| :--- | :--- | :--- | :--- |
| **RMSE** | 43.82 | **31.76** | **-27.5% Error** |
| **MAE** | 38.00 | **24.94** | **-34.3% Error** |
| **R-Squared ($R^2$)** | 0.00 | **0.48** | **Statistically Valid Signal** |

### 💻 Instructions to Execute Code
To replicate this analysis, follow these steps:

1. **Prepare Environment:**
   Ensure you have Python installed with the following libraries:
   pip install `pandas`, `numpy`, `matplotlib`, `scikit-learn`, `seaborn`

2. **Download Data:**
   Ensure the NASA files train_FD001.txt and test_FD001.txt are located in the same directory as the notebook.

3. **Run Analysis:**
Open the file `Yucabeth_Ombura_RCEL_506_Project-2.ipynb` in a Jupyter environment or Google Colab.

4. **Navigation:**
   * **EDA Section:** Exploratory charts (Radar charts, Sensor trends, Histograms).
   * **Baseline Section:** Calculation of the naive fleet-mean benchmark.
   * **Modeling Section:** Feature engineering (rolling averages) and Random Forest training.
   * **Evaluation Section:** Comparison of model performance vs. the baseline.

---
*Developed for the RCEL 506 curriculum at Rice University.*
