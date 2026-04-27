# RCEL-506-Capstone-Project

# Remaining Useful Life (RUL) Prediction for NASA Turbofan Engines 🚀

## 1. Business Problem
Unscheduled maintenance in the aviation industry leads to significant operational disruptions, high costs, and potential safety risks. Traditional maintenance strategies are often **reactive** (post failure) or **scheduled** (replacing parts regardless of actual wear).

The specific engineering challenge for this project is to accurately predict the **Remaining Useful Life (RUL)** of turbofan engines. By identifying the exact point when an engine transitions from a "healthy" state to a "degraded" state, operators can optimize maintenance schedules, minimize downtime, and maximize asset utilization.

## 2. Proposed Solution
This project implements a predictive maintenance model using a **NASA C-MAPSS (Commercial Modular Aero-Propulsion System Simulation)** dataset on the Kaggle website.

* **Approach:** A **Random Forest Regressor** ensemble model was selected to capture complex, non-linear relationships across 21 multivariate sensor channels (temperatures, pressures, and speeds).
* **Target Variable:** Remaining Useful Life (RUL), defined as the number of operational cycles remaining before system failure.
* **Benchmark:** The model was evaluated against a baseline mean-cycle prediction ($RMSE: 46.11$), with the machine learning approach providing a more granular and actionable forecasting tool for engineering leads.

## 3. Data Source
The analysis uses the **FD001 dataset**, which includes:
* 100 engine units running until failure.
* 3 operational settings and 21 sensor measurements per cycle.
* Time-series degradation patterns under sea-level conditions.

## 4. Instructions to Execute Code

### Prerequisites
Ensure you have Python 3.8+ installed. You will need the following libraries:
`pandas`, `numpy`, `matplotlib`, `scikit-learn`, and `streamlit` (if running the dashboard).

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
1.  **Run the Analysis Notebook:**
    Open the `.ipynb` file in Jupyter or Google Colab to view the data preprocessing, exploratory data analysis (EDA), and model training steps.
2.  **Launch the Streamlit App:**
    To view the interactive results and visualizations:
    ```bash
    streamlit run app.py
    ```

---
*Developed as part of the RCEL 506 curriculum at Rice University.*
"""

with open('README-Executive-Summary.md', 'w') as f:
    f.write(readme_content)
