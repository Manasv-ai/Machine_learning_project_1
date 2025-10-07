# 🎯 Student Exam Performance Prediction (Flask + Machine Learning Project)

This project is a **Machine Learning web application** built using **Flask** that predicts a student's exam performance based on demographic and educational factors such as gender, ethnicity, parental education, lunch type, and test preparation course.
It integrates a **complete ML pipeline** — from **data ingestion** and **transformation** to **model training** and **deployment**.

---

## 🚀 Features

✅ End-to-end Machine Learning project
✅ Flask-based interactive web interface
✅ Modular pipeline structure for scalability
✅ Data preprocessing with **Scikit-learn Pipelines**
✅ Prediction using trained and serialized model
✅ Easy to deploy locally or on cloud platforms

---

## 🧠 Project Architecture

```
Machine Learning Project/
│
├── app.py                          # Flask application (main entry point)
│
├── templates/
│   ├── index.html                  # Landing page
│   ├── home.html                   # Prediction form + result display
│
├── src/
│   ├── components/
│   │   ├── data_ingestion.py       # Reads raw data and splits into train/test
│   │   ├── data_transformation.py  # Handles preprocessing and scaling
│   │   ├── model_trainer.py        # Trains and saves the model
│   │
│   ├── Pipeline/
│   │   ├── predict_pipeline.py     # Loads model & performs predictions
│   │
│   ├── utils.py                    # Helper functions for model evaluation etc.
│   ├── exception.py                # Custom exception handling
│   ├── logger.py                   # Logging for debugging and monitoring
│
├── artifacts/
│   ├── data.csv                    # Raw dataset
│   ├── train.csv                   # Training data
│   ├── test.csv                    # Testing data
│   ├── model.pkl                   # Trained ML model
│   ├── preprocessor.pkl            # Data transformer (StandardScaler, encoders)
│
├── notebook/
│   ├── EDA.ipynb                   # Exploratory data analysis notebook
│   ├── Model_Training.ipynb        # Model experimentation and tuning
│
├── requirements.txt                # List of Python dependencies
└── README.md                       # Project documentation
```

---

## ⚙️ Workflow Overview

### 1. Data Ingestion

The `data_ingestion.py` component:

* Reads the dataset from the source (CSV or database)
* Splits it into **train** and **test** sets
* Stores data in the `artifacts/` directory

### 2. Data Transformation

The `data_transformation.py` component:

* Encodes categorical variables (like gender, lunch, etc.)
* Scales numerical features using **StandardScaler**
* Returns transformed train/test arrays ready for model training

### 3. Model Training

The `model_trainer.py` component:

* Trains multiple models (e.g., Linear Regression, RandomForest, XGBoost)
* Evaluates models using metrics like R², MAE, and RMSE
* Selects the best-performing model and saves it as `model.pkl`

### 4. Prediction Pipeline

The `predict_pipeline.py` component:

* Loads both the **model** and **preprocessor** from the artifacts
* Accepts user input through the web interface
* Returns the final prediction displayed on the browser

---

## 🧩 Tech Stack

| Category                  | Technology            |
| ------------------------- | --------------------- |
| **Programming Language**  | Python 3.9+           |
| **Framework**             | Flask                 |
| **Data Processing**       | Pandas, NumPy         |
| **Machine Learning**      | Scikit-learn          |
| **Web Templates**         | HTML, CSS, Jinja2     |
| **Version Control**       | Git                   |
| **Deployment (optional)** | Render / AWS / Heroku |

---

## 🧮 Input Parameters

| Feature                     | Type        | Example                 |
| --------------------------- | ----------- | ----------------------- |
| gender                      | Categorical | male / female           |
| race_ethnicity              | Categorical | group A / group B / ... |
| parental_level_of_education | Categorical | bachelor's degree       |
| lunch                       | Categorical | standard / free/reduced |
| test_preparation_course     | Categorical | none / completed        |
| reading_score               | Numerical   | 72                      |
| writing_score               | Numerical   | 70                      |

---

## 🖥️ Running the Project Locally

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/student-performance-predictor.git
cd student-performance-predictor
```

### 2️⃣ Create Virtual Environment

```bash
conda create -n myenv python=3.9 -y
conda activate myenv
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Run the Application

```bash
python app.py
```

Then open your browser and go to:

```
http://127.0.0.1:5000/
```

---

## 💡 Future Improvements

* Add a database (PostgreSQL / MongoDB) for user data storage
* Deploy on Render or AWS
* Build a React or Streamlit frontend
* Use advanced hyperparameter tuning (GridSearchCV / Optuna)
* Integrate visualization dashboards

---

## 👨‍💻 Author

**Manas Khatri**
B.Tech in Mathematics and Computing
📍 M.S. Ramaiah University of Applied Sciences
