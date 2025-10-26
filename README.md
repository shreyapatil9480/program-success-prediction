# Business Analytics Program Success Analysis

This repository contains a **synthetic yet realistic project** that demonstrates an end‑to‑end analytics workflow.  It is designed to showcase skills relevant to roles such as **business analyst**, **program manager**, and **data analyst**.

## Overview

Many organisations run complex programmes and projects.  Evaluating which initiatives are likely to succeed — and understanding the drivers behind that success — can help decision‑makers allocate resources more effectively.  To illustrate this process, a synthetic dataset was generated describing **50** programmes with the following fields:

| Column                     | Description                                                   |
|---------------------------|---------------------------------------------------------------|
| **Budget_Million**        | Total programme budget in millions of currency units          |
| **Duration_Months**       | Programme duration in months                                   |
| **Team_Size**             | Number of people involved in the programme                     |
| **Complexity**            | Categorical indicator of complexity (Low, Medium, High)        |
| **Region**                | Geographic region (North, South, East, West)                   |
| **Stakeholder_Satisfaction** | Satisfaction rating on a 1‑5 scale                         |
| **Success**               | Binary outcome (1 for success, 0 for failure)                  |
| **ROI_Million**           | Return on investment in millions of currency units             |

The `Success` variable was derived using a logistic function of the other features with added randomness to mirror real‑world uncertainty.  The `ROI_Million` column scales with both budget and success to simulate increased returns for more successful programmes.

## Project Structure

```
.
├── data/
│   └── synthetic_project_data.csv   # Synthetic dataset (CSV)
├── analysis_notebook.ipynb          # Jupyter Notebook with EDA and models
├── requirements.txt                 # Python dependencies
└── README.md                        # Project description and instructions
```

### Data

The dataset lives in the `data/` directory.  Because it is synthetically generated there are **no privacy concerns**.  Feel free to open the CSV file in Excel or any text editor to explore.

### Notebook

The notebook walks through the following steps:

1. **Load and inspect the data** — display a few rows and compute summary statistics.
2. **Visualise distributions** — generate histograms and counts for key variables.
3. **Build predictive models** — start with a simple logistic regression using numeric features, then move to a more complex random forest model that includes categorical variables via one‑hot encoding.
4. **Evaluate and interpret** — assess model accuracy, review classification reports, and discuss next steps.

The modelling workflow demonstrates increasing difficulty: from basic exploratory analysis through to more sophisticated machine learning.  This progression shows how you might approach real data in stages.

## Getting Started

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/your‑repository.git
   cd your‑repository
   ```

2. **Create and activate a virtual environment (optional but recommended)**

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run the notebook**

   You can open `analysis_notebook.ipynb` in Jupyter Notebook, JupyterLab, or VS Code.  Make sure the kernel has the dependencies listed in `requirements.txt`.

## Next Steps

This project is intentionally open‑ended.  Here are a few ideas for extending it:

- **Hyperparameter tuning** using grid search or randomised search to improve model performance.
- **Feature engineering**, such as calculating budget per team member or complexity‑adjusted durations.
- **Regression modelling** to predict continuous outcomes like ROI or satisfaction instead of binary success.
- **Interactive dashboards** built with Plotly Dash, Streamlit or PowerBI to share insights with non‑technical stakeholders.

Feel free to fork this repository and tailor it to specific industries or questions that align with your career goals.  Demonstrating that you can take a problem from data ingestion through to interpretation is a valuable signal to prospective employers.
