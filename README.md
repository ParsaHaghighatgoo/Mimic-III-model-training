# Mimic-III-model-training

End-to-end notebooks and materials for **training machine-learning models on the MIMIC-III critical care database**, with a focus on **data loading/exploration** and **a sepsis-related modeling workflow**.

> **Important**: MIMIC-III is a controlled-access dataset. You must have approved PhysioNet access and follow the Data Use Agreement (DUA) to run the data-dependent parts of this project. :contentReference[oaicite:0]{index=0}

---

## What’s inside

This repository is organized primarily as **Jupyter notebooks** (and supporting documents) that walk through:

- Opening and exploring MIMIC-III data (schema familiarity, cohort extraction, feature prep)
- A sepsis-oriented modeling pipeline (feature creation → model training → evaluation)
- A written report folder and background reading materials (papers + idea notes)

### Repository structure

- `dataOpening/`  
  Notebooks/scripts for loading MIMIC-III data and early exploration/cleaning.
- `sepsis/`  
  Notebooks/scripts for sepsis-related feature engineering and model training.
- `report/`  
  Report material, figures, and writeups.
- `Application of Machine Learning Techniques in.pdf`  
  Background reading (paper)
- `Applying an Improved Stacking Ensemble Model to Predict the.pdf`  
  Background reading (paper)
- `Ideas.docx`  
  Notes/ideas and planning

> Folder names reflect the workflow stages; open the notebooks in order to follow the pipeline.

---

## Requirements

This project is notebook-first. Typical requirements:

- Python 3.9+ (3.10 recommended)
- JupyterLab / Notebook
- Common ML stack: `numpy`, `pandas`, `scikit-learn`, `matplotlib`
- (Optional) `xgboost` / `lightgbm` depending on the models used in notebooks
- Database connectivity (one of the following):
  - Local **PostgreSQL** loaded with MIMIC-III, or
  - Pre-extracted CSVs/parquets created from your own MIMIC-III environment

If you already have a `requirements.txt`/`environment.yml`, prefer that. Otherwise you can start with:

```bash
pip install jupyter pandas numpy scikit-learn matplotlib
