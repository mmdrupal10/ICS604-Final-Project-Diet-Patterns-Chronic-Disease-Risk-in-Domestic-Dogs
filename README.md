# Diet Patterns, Food Safety, and Chronic Disease Risk in Domestic Dogs

**ICS604 – Applied Data Science | Final Project**
**Author:** Maritza Medina | **Semester:** Spring 2026

---

## Project Overview

This project investigates whether diet type (conventional meat-based, raw/home-prepared, or vegan) is associated with chronic disease prevalence in domestic dogs. Using a large, publicly available survey dataset from Knight et al. (2022), the analysis spans five research questions — from unadjusted prevalence comparisons to adjusted logistic regression and machine learning-based predictive modeling — and concludes with an exploratory look at FDA pet food recall trends.

**Key findings:**
- Commercial-fed dogs have significantly higher rates of GI issues, obesity, mobility problems, and dental disease compared to raw or vegan-fed dogs (unadjusted).
- After controlling for age, diet type does not significantly predict cancer risk — age is the dominant predictor.
- Random Forest feature importance confirms that age, veterinary visit frequency, and medication use are the strongest predictors of chronic disease status.

---

## Repository Structure

```
.
├── ICS604_Final_Project_Medina.ipynb   # Main analysis notebook (with outputs)
├── ICS604_Final_Report_Medina.pdf        # Written report (3–4 pages)
├── requirements.txt                      # Python dependencies
└── README.md                             # This file
```

> **Note:** The dataset (`canine_health_results.xlsx`) is downloaded automatically from the public OSF repository (https://osf.io/nbepu) when you run the notebook. No manual data download is required.

---

## Environment Setup

### Option A — Google Colab (Recommended)

1. Open the notebook in Google Colab by uploading `ICS604_Final_Project_Medina.ipynb` or clicking the Colab badge if available.
2. Run **Step 0** (the first code cell) — all required libraries are pre-installed in Colab.
3. Run all cells from top to bottom using **Runtime → Run all**.

> **Important:** The first cell in the notebook mounts Google Drive. If you are running in Colab, you will be prompted to authorize access. If you are running locally, skip or delete that cell.

### Option B — Local Jupyter Environment

1. **Clone the repository:**
   ```bash
   git clone https://github.com/mmdrupal10/ICS604-Final-Project-Diet-Patterns-Chronic-Disease-Risk-in-Domestic-Dogs.git
   cd ics604-final-project
   ```

2. **Create a virtual environment (optional but recommended):**
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Launch Jupyter and open the notebook:**
   ```bash
   jupyter notebook ICS604_Final_Project_Medina.ipynb
   ```

5. **Run all cells** from top to bottom. The dataset will be downloaded automatically in Step 1.

---

## Running the Notebook

The notebook is organized into clearly labeled steps. Run them **in order from top to bottom**:

| Step | Description |
|---|---|
| **Step 0** | Install and import all libraries |
| **Step 1** | Download dataset from OSF and load into pandas |
| **Step 2** | Data cleaning and preprocessing (rename columns, binarize disease indicators, create diet groups) |
| **Step 3** | Exploratory Data Analysis (EDA) — sample composition, three-way diet comparison, disease heatmap |
| **Step 4** | **RQ1** — Unadjusted chi-square tests across all diseases and diet groups |
| **Step 5** | **RQ2** — Commercial vs. Non-commercial prevalence comparison |
| **Step 6** | **RQ3** — Adjusted logistic regression for cancer (with odds ratio table and forest plot) |
| **Step 7** | **RQ4** — Decision Tree and Random Forest predictive models with feature importance |
| **Step 8** | **RQ5** — Exploratory FDA pet food recall trends (secondary analysis) |
| **Step 9** | Summary of key findings |
| **Step 10** | Limitations |
| **References** | Full citation list |

**Expected runtime:** approximately 2–4 minutes on a standard machine or Colab instance.

---

## Dependencies

See `requirements.txt` for the full list. Core packages:

| Package | Version | Purpose |
|---|---|---|
| pandas | ≥ 2.0 | Data manipulation |
| numpy | ≥ 1.24 | Numerical operations |
| matplotlib | ≥ 3.7 | Visualization |
| seaborn | ≥ 0.12 | Statistical visualization |
| scipy | ≥ 1.10 | Chi-square and proportion tests |
| statsmodels | ≥ 0.14 | Logistic regression |
| scikit-learn | ≥ 1.3 | Decision Tree, Random Forest, metrics |
| openpyxl | ≥ 3.1 | Reading Excel files |

---

## Dataset

**Source:** Knight A, Huang E, Rai N, Brown H (2022). *Vegan versus meat-based dog food: Guardian-reported indicators of health.* PLOS ONE 17(4): e0265662.
https://doi.org/10.1371/journal.pone.0265662

**Repository:** https://osf.io/nbepu (public, no login required)

**File downloaded:** `Canine health results.xlsx` (sheet: `All`)

The dataset is downloaded automatically by the notebook. If the download fails, you can manually download the file from the OSF link above and place it in the same directory as the notebook with the filename `canine_health_results.xlsx`.

---

## Reproducing the Results

All figures, tables, and metrics reported in the written report (`ICS604_Final_Report_Medina.pdf`) are generated directly by the notebook. Running all cells from top to bottom will reproduce every result. Key outputs include:

- Three-way disease prevalence bar charts and heatmap (Step 3)
- Chi-square significance table for RQ1 (Step 4)
- Commercial vs. Non-commercial prevalence comparison table (Step 5)
- Odds ratio forest plot for cancer (Step 6)
- Decision Tree visualization and Random Forest feature importance plot (Step 7)
- FDA recall trend line chart and stacked bar chart (Step 8)

---

## website
https://caninediet-desease.manus.space

## References

1. Knight A et al. (2022). PLOS ONE. https://doi.org/10.1371/journal.pone.0265662
2. Barrett-Jolley R, German AJ (2024). PLOS ONE. https://doi.org/10.1371/journal.pone.0280173
3. FDA CVM Recalls & Withdrawals. https://www.fda.gov/animal-veterinary/safety-health/recalls-withdrawals
4. AVMA Raw Pet Foods Policy. https://www.avma.org/resources-tools/avma-policies/raw-or-undercooked-animal-source-protein-companion-animal-diets
