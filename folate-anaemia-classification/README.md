# Prediction of Folate Deficiency Anaemia using Machine Learning

This project applies machine learning algorithms to predict folate deficiency anaemia using clinical and lifestyle features derived from the UK Biobank. Developed as part of a research project at BMS College of Engineering.

---

## Project Highlights

- **Goal:** Early, accessible prediction of folate deficiency anaemia to aid clinicians and improve patient outcomes.
- **Dataset:** UK Biobank (no raw data provided, see [reports](./reports/) for methodology and features).
- **Tools:** Python (Pandas, Scikit-learn, PyTorch), Jupyter Notebook, Matplotlib, Power BI.

---

## Key Steps

1. **Data Preparation:**  
   - Cleaned and preprocessed 500,000+ samples.
   - Selected features include CBC metrics, demographics, diet, lifestyle.

2. **Model Development:**  
   - Compared 10+ models (Extra Trees, XGBoost, Random Forest, etc.).
   - Achieved F1-score of 0.86, ROC-AUC of 0.90 with Extra Trees.
   - Interpreted key features driving anaemia predictions.

3. **Analysis & Results:**  
   - Confusion matrices, ROC curves, feature importances in `results/`.
   - See [detailed report](./reports/FINAL_REPORT-SEE-1-1.pdf).

4. **Societal Impact:**  
   - Early detection tools can optimize resources, enable interventions, and empower patients for better future clinical management.

---

## Repository Structure

| Folder               | Contents                                                       |
|----------------------|----------------------------------------------------------------|
| `data/`              | Data loaders/sample formats/dummy data (no raw Biobank data)   |
| `notebooks/`         | Jupyter Notebooks for EDA, model building                     |
| `src/`               | Main Python scripts and utilities                             |
| `results/`           | Visualizations, confusion matrices, metrics                   |
| `reports/`           | Project reports, slide decks, documentation                   |

---

## How To Run

_Privileged data cannot be shared; code, feature engineering, and evaluation scripts are provided for demonstration._  
1. Install required packages (`requirements.txt` if available).
2. Clone/Download repo, open notebooks in Jupyter.
3. Replace `data/` with your own sample (see `data/README.md`).
4. Run and view results in `results/`.

---

## References

- [Project Reports](./reports/)
- Original data: UK Biobank (see references in report for access)

