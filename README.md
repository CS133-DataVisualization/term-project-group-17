# Medicaid Drug Utilization Analysis (2025)

## Team Members
- Aaditya Deshmukh  
- Nyi Wai Yan Tun  
- Sana Al Hamimidi  

---

## Project Overview

This project analyzes the 2025 Medicaid State Drug Utilization Dataset to uncover patterns in drug prescriptions, spending, and distribution across U.S. states.

We explore key questions such as:
- What are the most prescribed drugs by volume?
- Which drugs cost the government the most money?
- How are prescriptions distributed across states?
- How do high-cost drugs compare to high-volume drugs?
- Can we predict high vs low coverage using machine learning?

The goal is to combine data visualization and machine learning to generate actionable insights.

---

## Dataset Information

- Source: Medicaid.gov  
- Link: https://download.medicaid.gov/data/sdud-2025-updated-dec2025.csv  
- Size: ~2.6 million rows  

### Key Features:
- State
- Product Name
- Units Reimbursed
- Number of Prescriptions
- Total Amount Reimbursed
- Medicaid Amount Reimbursed

Note: Some values are suppressed or missing and were filtered during preprocessing.

---

## Data Cleaning & Preparation

Steps performed:
- Removed suppressed (Suppression Used == True) rows  
- Dropped missing/null values in key columns  
- Converted numeric columns to appropriate formats  
- Aggregated data by drug and state  
- Created derived features (e.g., spending buckets, volume categories)

---

## Machine Learning Model

### Task: Binary Classification

We built a model to classify drugs into:
- High Coverage
- Low/Medium Coverage

### Model Used:
- Decision Tree Classifier
- Logistic Regression
- Random Forest

### Best Results:
- Accuracy: ~95%  
- F1 Score: ~0.97  
- F1 (Low Coverage): ~0.81  

### Key Insight:
The model performs well overall but highlights class imbalance, with lower performance on minority classes.

---

## How to Run

### 1. Clone the Repository
```bash
git clone https://github.com/your-repo-link.git
cd your-repo-name
```

### 2. Install Dependencies
```bash
pip install pandas matplotlib seaborn plotly scikit-learn
```

### 3. Run the Notebook
```bash
jupyter notebook
```
*Note this can be done through Google Colab as well. 

Open the .ipnyb files and run them. 

## Github Structure

├── Extra Outside Analysis/

│   └── (additional exploration for analysis)

├── Models/

│   └── (machine learning models and related code)

├── Project Assignments/

│   └── (main notebooks, analysis, and required project assignments)

├── FinalReport/

└── README.md
