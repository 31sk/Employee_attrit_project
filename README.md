Employee Attrition Prediction

📌 Project Overview

Employee attrition (turnover) is a significant cost for organizations. This project utilizes a synthetic dataset of 15,000 employees to identify key drivers of attrition and build a predictive model. We use a Random Forest Classifier to estimate the likelihood of an employee leaving based on factors like job satisfaction, income, overtime, and work-life balance.

📊 Dataset Description

The dataset consists of 15,000 records with 18 features, including:

Demographics: Age, Gender, Marital Status.

Professional: Department, Job Role, Monthly Income, Years at Company.

Behavioral: Job Satisfaction, Environment Satisfaction, Overtime, Distance From Home.

Target: Attrition (Yes/No).

The dataset was synthetically generated with a current attrition rate of 24.4%.

🛠️ Tech Stack

Data Processing: Pandas, NumPy

Visualization: Matplotlib, Seaborn

Machine Learning: Scikit-Learn (Random Forest, Logistic Regression)

Model Deployment: Joblib (for model serialization)

🚀 Project Workflow

1. Data Generation & Cleaning
Synthetic data created using numpy.random with realistic distributions (e.g., lognormal for income, exponential for tenure).

Verified a clean dataset with 0 missing values.

2. Feature Engineering
Label Encoding: Converted Overtime to binary (0/1).

One-Hot Encoding: Categorical variables like Department, JobRole, and EducationField were expanded into dummy variables.

Scaling: Features were normalized using StandardScaler to ensure optimal performance.

3. Model Training
   
Split: 80% Training / 20% Testing (stratified split to maintain attrition ratio).

Algorithm: Random Forest Classifier.

Results: The model generates risk categories (High, Medium, Low) based on attrition probability.

📈 Insights

The model identified several risk factors that increase the probability of attrition:

Overtime: Significantly increases risk.

Low Income: Employees earning < 3000 are at higher risk.

Distance: Commutes over 20 miles correlate with higher turnover.

Promotion Stagnation: Lack of promotion in 5+ years increases attrition likelihood.

Risk Breakdown by Department
Department	Total Employees	High Risk Count	Avg Risk %
Human Resources	1,623	306	18.9%
Research & Dev	8,380	1,630	19.5%
Sales	4,997	997	20.0%
(Data based on model predictions)	

📦 Saved Artifacts

The following files are generated for deployment:

rf_model.pkl: The trained Random Forest model.

scaler.pkl: The fitted StandardScaler object.

feature_names.pkl: List of features used during training.

💻 How to Run

Clone the repository:

git clone https://github.com/yourusername/employee-attrition.git

Install dependencies:


pip install pandas numpy scikit-learn seaborn matplotlib joblib

Run the notebook:

jupyter notebook employee_attrition.ipynb
