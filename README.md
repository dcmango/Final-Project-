SQL Query Runtime Prediction  
=============================

Author: Chong Deng  
Course: CS 210 - Data Management in Data Science  
Semester: Summer 2025  
Project Type: Individual  
GitHub Repo: [Insert GitHub Link]  

Overview  
--------
This project aims to predict the runtime of SQL queries based on their structure and complexity using machine learning models. The goal is to help developers understand and optimize queries before executing them, by providing real-time predictions of execution time and performance class (Fast, Moderate, Slow).

Key Features  
------------
- SQL query structure analysis using keyword features  
- Predict query runtime using regression  
- Classify runtime performance category using classification  
- Feature visualization and insights  
- Streamlit-based user interface for demonstration

Tools & Libraries Used  
-----------------------
- Python 3.12  
- pandas  
- numpy  
- sqlparse  
- scikit-learn  
- matplotlib  
- seaborn  
- streamlit  

Project Structure  
-----------------
- sql_runtime_predictor.ipynb: Jupyter Notebook with full implementation  
- streamlit_app.py: Streamlit UI for runtime prediction  
- data/: Folder containing synthetic SQL query dataset  
- models/: Trained ML models (regression and classification) saved with joblib  
- screenshots/: Output images used in report and demo  
- README.txt: This file  

How It Works  
------------
1. **Data Generation**:  
   A synthetic dataset of SQL queries is created with simulated runtime values and performance class labels (Fast, Moderate, Slow).

2. **Feature Engineering**:  
   Each query is parsed using `sqlparse`, and keyword frequencies (e.g., SELECT, WHERE, JOIN) are extracted as features.

3. **Model Training**:  
   - `RandomForestRegressor` is used to predict numerical runtime.  
   - `RandomForestClassifier` is used to classify the runtime category.

4. **Model Evaluation**:  
   - Regression evaluated using RMSE and R² score.  
   - Classification evaluated using precision, recall, and F1-score.

5. **Streamlit Deployment**:  
   A Streamlit app takes user-input SQL queries, processes them into keyword features, and returns both predicted runtime and performance category.

Instructions to Run  
-------------------
To run the Jupyter Notebook (analysis and training):
jupyter notebook sql_runtime_predictor.ipynb

To run the Streamlit app (for demo use):
streamlit run streamlit_app.py

📦 **Python Libraries Required (install manually if needed):**
- pandas  
- numpy  
- sqlparse  
- scikit-learn  
- matplotlib  
- seaborn  
- streamlit  

Sample Predictions  
------------------
Example 1:
- Input Query:  
  SELECT name FROM employees WHERE department = 'HR';  
- Predicted Runtime: 0.6 seconds  
- Predicted Class: Fast  

Example 2:
- Input Query:  
  SELECT department, COUNT(*) FROM employees GROUP BY department HAVING COUNT(*) > 5;  
- Predicted Runtime: 2.3 seconds  
- Predicted Class: Moderate  

Example 3:
- Input Query:  
  SELECT e.name, d.name FROM employees e JOIN departments d ON e.dept_id = d.id;  
- Predicted Runtime: 3.9 seconds  
- Predicted Class: Slow  

Screenshots  
-----------

   <img width="800" height="500" alt="sql_keyword_freq" src="https://github.com/user-attachments/assets/fbece971-884f-4a62-b4ff-00aeac1c372f" />

   <img width="800" height="500" alt="complexity_vs_runtime" src="https://github.com/user-attachments/assets/06467c40-6f27-4e16-88e6-a2401d862c60" />

   <img width="218" height="66" alt="截屏2025-07-15 上午5 45 28" src="https://github.com/user-attachments/assets/4f6b4b30-7118-434a-bce5-4bc2b5f5c904" />

   <img width="450" height="169" alt="截屏2025-07-15 上午5 45 35" src="https://github.com/user-attachments/assets/ee1bf3f3-a96e-4801-83ab-15e4d8464b6b" />

   <img width="914" height="854" alt="截屏2025-07-15 上午5 32 59" src="https://github.com/user-attachments/assets/e219bac7-dae4-4446-947e-ba4369c97349" />
 

Demo Video  
----------
Google Drive Link: [Insert Demo Video Link]

Contact  
-------

E-mail: dcmang1016@gmail.com 
