# Proactive-Infra-Failure-detection using Isolation Forest

This project implements an **unsupervised anomaly detection model** using the **Isolation Forest algorithm** to identify infrastructure failures from system log metrics such as CPU, memory, and disk usage. The goal is to support **proactive maintenance** by detecting anomalies early and reducing incident response times.

---

##  Dataset

- **Source**: `predictive_maintenance_dataset.csv` (structured performance log data)
- **Features include**:  
  - CPU usage  
  - Memory usage  
  - Disk I/O metrics  
  - Failure status labels (used for evaluation, not model training)

---

---

##  Objectives

-  Improve failure detection **recall** compared to baseline rules
-  Reduce average **incident response time**
-  Visualize anomaly trends over time for proactive infrastructure decisions

---

##  Performance Summary

| Metric                | Isolation Forest | Baseline Rules |
|-----------------------|------------------|----------------|
| Accuracy              | 94.9%            | 99.4%          |
| Precision             | 0.87%            | 0.16%          |
| Recall                | **51.89%**       | 0.94%          |
| F1 Score              | 1.70%            | 0.27%          |
| Response Time         | **15 mins**      | 180 mins       |
| Improvement in IRT    | **+91.67%**      | —              |

---

##  Visualizations

- **Anomaly Time Series Plot**: Shows when anomalies occurred across the monitoring window  
- **Confusion Matrix Heatmap**: Visual representation of model performance  
- **Response Time Distribution**: Compares detection delay between model and manual detection

---

##  Tech Stack

- **Python 3.12**
- **Libraries**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`, `joblib`
- **Notebook**: Jupyter-compatible `.ipynb` for full model training and evaluation

---

##  Saving & Loading Model

```python
import joblib

# Save model
joblib.dump(model, 'isolation_forest_model.pkl')

# Load model
model = joblib.load('isolation_forest_model.pkl')

# 1. Clone the repository
git clone https://github.com/yourusername/infrastructure-failure-detection.git

# 2. Navigate to project directory
cd infrastructure-failure-detection

# 3. Open the notebook or run script
jupyter notebook anomaly_detection.ipynb







