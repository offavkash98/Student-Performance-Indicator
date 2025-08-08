## End-to-End Machine Learning Project: Student Performance Indicator

     Project Presentation : https://drive.google.com/file/d/1VlOd5lpA2uahUHYxHAKq37sOOwJlQ7WL/view?usp=sharing

### Project Overview

This project builds a **production-ready**, end-to-end machine learning pipeline to predict student performance based on socio-demographic factors. It integrates best practices in modular **ML development**, **CI/CD deployment**, and cloud hosting on **AWS Elastic Beanstalk**.

The dataset used consists of **1000 rows and 8 columns**, including both **categorical and numerical features**, and serves as a foundation for understanding complex data handling and model building.

🎯 Goal: Predict students' test scores using features like gender, parental education, and test preparation course.

### 🔧 Tech Stack & Tools

| Category             | Tools                                                             |
| -------------------- | ----------------------------------------------------------------- |
| Language             | `Python 3.8`                                                      |
| Data Handling        | `Pandas`, `NumPy`                                                 |
| ML Models            | `Linear Regression`, `Random Forest`, `XGBoost`, `CatBoost`, etc. |
| Feature Engineering  | One-Hot Encoding, Standard Scaling                                |
| Logging & Exceptions | Custom `logger.py` and `exception.py`                             |
| Web Framework        | `Flask`                                                           |
| CI/CD                | `GitHub` → `AWS CodePipeline` → `Elastic Beanstalk`               |
| Deployment           | `AWS Elastic Beanstalk`, `.ebextensions`                          |
| Version Control      | `Git`, `GitHub`                                                   |


### 🧠 ML Workflow

📁 Data Flow

      raw.csv ──► train.csv & test.csv ──► preprocessor.pkl ──► model.pkl ──► predictions
      
### 📦 Modular Architecture

            SRC/
            ├── components/
            │   ├── data_ingestion.py
            │   ├── data_transformation.py
            │   └── model_trainer.py
            ├── pipeline/
            │   ├── train_pipeline.py
            │   └── predict_pipeline.py
            ├── logger.py
            ├── exception.py
            └── utils.py

### 🖥️ Project Structure

            ├── .ebextensions/         # AWS deployment config
            ├── artifacts/             # All generated artifacts (CSV, pickles)
            ├── logs/                  # Logging output
            ├── notebook/              # EDA and experiments
            ├── templates/             # Flask HTML templates
            ├── SRC/                   # All project source code
            ├── app.py / application.py
            ├── requirements.txt
            ├── setup.py
            └── README.md
            
###  🌐 Deployment Strategy (CI/CD)
✅ GitHub → 📦 AWS CodePipeline → 🚀 AWS Elastic Beanstalk
- Push to GitHub auto-triggers deployment
- .ebextensions/python.config sets WSGI path
- Fully managed production environment on AWS

### 📷 UI Preview

| Home Page                                                   | Prediction Output                                                   |
| ----------------------------------------------------------- | ------------------------------------------------------------------- |
| ![Home](https://via.placeholder.com/400x200?text=Home+Page) | ![Result](https://via.placeholder.com/400x200?text=Prediction+Page) |


### 🧪 How to Run Locally

         # 1. Clone Repo
         git clone https://github.com/<your-username>/student-performance-indicator.git
         cd student-performance-indicator
         
         # 2. Create Virtual Environment
         conda create -p venv python=3.8 -y
         conda activate venv
         
         # 3. Install Requirements
         pip install -r requirements.txt
         
         # 4. Run the Flask App
         python app.py  # or python application.py
         
         # 5. Open in browser
         http://127.0.0.1:5000/

### 📈 Model Highlights

| Metric                | Score                                           |
| --------------------- | ----------------------------------------------- |
| R² (Test Set)         | `0.87+`                                         |
| Best Model            | `XGBoostRegressor` (with hyperparameter tuning) |
| Preprocessing         | One-Hot Encoding + Standard Scaling             |
| Custom Logging        | Enabled                                         |
| Robust Error Handling | ✅                                              |

### 📌 Key Learnings
- ✅ End-to-end ML lifecycle
- ✅ Modular, scalable, and production-ready design
- ✅ AWS deployment & automation (CI/CD)
- ✅ Real-world implementation of Flask for ML apps

### 🤝 Connect with Me
📧 avkashkhandekar.mum.dbda@gmail.com
📞 9082698210
