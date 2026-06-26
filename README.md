# Ops Analyzer – Operational Efficiency Dashboard

A lightweight Python notebook that calculates operational efficiency for three fuel depots, classifies their performance, and prints a clear summary report.

---

## 📊 Features

- **Efficiency KPI** – computes `(actual / target) × 100`   
- **Status Classifier** – labels each site as `Critical`, `Warning`, or `Normal` based on efficiency  
- **Scalable Data Model** – easily add more sites by extending a list of dictionaries  
- **Automated Reporting** – loops through sites and generates a formatted, human‑readable report  
- **Built‑in Documentation** – Markdown cells explain every step for junior analysts  

---

## 🚀 Quick Start

### Option A – Run in Google Colab (no installation)

1. Click this badge to open the notebook in Colab:  
   [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/TristanBrian/ops_analyzer/blob/main/week1_ops_analyzer.ipynb)

2. Click **Runtime → Run all** to see the report.

### Option B – Run locally with Jupyter

1. Clone this repository:  
   ```bash
   git clone https://github.com/TristanBrian/ops_analyzer.git
   cd ops_analyzer
   ```

2. Launch Jupyter Notebook:  
   ```bash
   jupyter notebook week1_ops_analyzer.ipynb
   ```

3. Run all cells (**Cell → Run All**).

---

## 📋 Example Output

```
============================================================
OPERATIONAL EFFICIENCY REPORT
============================================================

Site: North Depot
  Actual Output: 8200
  Target Output: 10000
  Efficiency: 82.0%
  Status: Warning
----------------------------------------
Site: South Depot
  Actual Output: 6500
  Target Output: 8000
  Efficiency: 81.2%
  Status: Warning
----------------------------------------
Site: East Depot
  Actual Output: 9500
  Target Output: 10000
  Efficiency: 95.0%
  Status: Normal
----------------------------------------
End of report.
```

---

## 🧠 How It Works

| Component | Description |
|-----------|-------------|
| `calculate_efficiency(actual, target)` | Returns percentage; returns `0.0` if `target` is zero to avoid division errors. |
| `get_operational_status(efficiency)` | Returns `"Critical"` if <70%, `"Warning"` if 70–89%, `"Normal"` if ≥90%. |
| `sites` list | A list of three dictionaries, each with `name`, `actual_output`, and `target_output`. |
| Loop & report | Iterates over each site, computes KPI, calls the classifier, and prints a formatted line. |

---

## 🏭 Industry Example

This notebook uses **fuel depots** as the operational context.  
You can easily adapt it for **hospital wards**, **retail stores**, **manufacturing lines**, or any other domain by replacing the site data.

---

## 📝 Requirements

- Python 3.x (comes with Anaconda or standard Python)  
- Jupyter Notebook or Google Colab (no extra packages needed)

---

## 👤 Author

**Tristan Brian**  
[GitHub Profile](https://github.com/TristanBrian)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
```