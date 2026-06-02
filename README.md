# AI-Powered Financial Fraud Detection & Risk Scoring System

## Overview
A machine learning system that detects fraudulent credit card transactions and assigns risk scores (Low / Medium / High). Built with MLOps best practices including experiment tracking, automated retraining, and cloud deployment.

---

## Dataset
| Detail | Info |
|--------|------|
| Source | ULB Credit Card Fraud Detection (Kaggle) |
| Size | 284,807 transactions |
| Fraud Rate | 0.17% (highly imbalanced) |

---

## Technologies
| Area | Tools |
|------|-------|
| Language | Python 3.11 |
| Machine Learning | XGBoost, scikit-learn, imbalanced-learn (SMOTE) |
| Experiment Tracking | MLflow |
| Web App | Streamlit |
| Dashboard | Power BI |
| Database | SQLite |
| Containerization | Docker |
| CI/CD | GitHub Actions |
| Version Control | Git & GitHub |

---

## Folder Structure
```
fraud-detection-mlops/
├── data/
│   ├── raw/              # Original dataset (not tracked by Git)
│   └── processed/        # Cleaned and transformed data
├── notebooks/            # Jupyter notebooks for EDA and modelling
├── app/                  # Streamlit web application
├── dashboard/            # Power BI dashboard files
│   └── screenshots/      # Dashboard screenshots
├── models/               # Trained model files (not tracked by Git)
├── docs/                 # Project documentation
├── reports/              # Analysis reports and figures
├── tests/                # Unit tests
├── requirements.txt      # Python dependencies
├── retrain.py            # Automated retraining script
└── README.md             # Project documentation
```

---

## Setup Instructions

### Step 1 — Clone the repository
```bash
git clone https://github.com/Poorrvajaa-J/fraud-detection-mlops.git
cd fraud-detection-mlops
```

### Step 2 — Create and activate virtual environment
```bash
py -3.11 -m venv venv
venv\Scripts\activate
```

### Step 3 — Install dependencies
```bash
pip install -r requirements.txt
```

### Step 4 — Download the dataset
- Go to [Kaggle Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- Download `creditcard.csv`
- Place it inside `data/raw/`

---

## Run Streamlit App
```bash
streamlit run app/streamlit_app.py
```

## Run with Docker
```bash
docker build -t fraud-detection .
docker run -p 8501:8501 fraud-detection
```

---