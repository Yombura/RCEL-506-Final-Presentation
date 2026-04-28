# Executive Summary: NASA Turbofan RUL Prediction
**Course:** RCEL 506: Applied Statistics & Data Science for Engineering Leaders

## 1. Business Problem
Unscheduled maintenance in the aviation industry leads to significant operational disruptions, high costs, and potential safety risks. Traditional maintenance strategies are often **reactive** (fixing after failure) or **scheduled** (replacing parts regardless of actual wear). 

The specific engineering challenge for this project is to accurately predict the **Total Life Capacity (Max Cycles)** of turbofan engines. By forecasting the specific "retirement age" of an engine based on its current health fingerprint, operators can derive the **Remaining Useful Life (RUL)** more reliably, optimizing maintenance schedules and maximizing asset utilization.

## 2. Proposed Solution
This project implements a predictive maintenance model using the **NASA C-MAPSS (Commercial Modular Aero-Propulsion System Simulation)** dataset. 

* **Forecasting Goal:** Unlike traditional models that predict a decaying RUL value directly, this model predicts the **Max Number of Cycles** the engine will achieve. 
* **Calculation:** $RUL = Predicted\ Max\ Cycles - Current\ Cycle$.
* **Approach:** A **Random Forest Regressor** ensemble model was selected to capture complex, non-linear relationships across 21 multivariate sensor channels.
* **Benchmark:** The model was evaluated against a naive mean-cycle baseline ($RMSE: 46.11$), with the machine learning approach providing a **60% improvement** in accuracy ($RMSE: 18.23$).

## 3. Data Source & Feature Engineering
The analysis uses the **FD001 dataset**:
* **Sensors:** 21 sensor measurements per cycle.
* **Refinement:** Non-variant sensors ($s1, s5, s10, s16, s18, s19$) were removed to reduce noise and improve model focus on critical failure drivers like Turbine Temperature ($s4$) and Static Pressure ($s11$).

## 4. Instructions to Execute Code

### Prerequisites
Python 3.8+ with: `pandas`, `numpy`, `matplotlib`, `scikit-learn`, and `streamlit`.

### Setup
1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/](https://github.com/)[your-username]/[your-repo-name].git
    cd [your-repo-name]
    ```
    
2.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

### Execution
1.  **Run the Analysis:** Open the Jupyter Notebook to view the end-to-end pipeline, from the **Radar Chart** EDA to the **Feature Importance** analysis.
2.  **Dashboard:**
    ```bash
    streamlit run app.py
    ```

---
*Developed for the RCEL 506 curriculum at Rice University.*
"""

with open('README.md', 'w') as f:
    f.write(readme_content)
