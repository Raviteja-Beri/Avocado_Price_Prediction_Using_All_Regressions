# 🥑 Avocado Price Prediction Using Machine Learning

Welcome to the **Avocado Price Prediction** project! This repository showcases a comprehensive machine learning solution to predict avocado prices using a variety of regression algorithms. With an interactive Flask web app, users can input avocado features and get real-time price predictions. Whether you're a data enthusiast or a recruiter looking for a polished ML project, this repository demonstrates skills in data preprocessing, model training, evaluation, and web development.

---

## 🌟 Project Highlights

- **Multiple Regression Models**: Implements 13 regression algorithms, including Linear Regression, Random Forest, XGBoost, and Neural Networks, to predict avocado prices.
- **Interactive Web App**: A Flask-based interface allows users to select a model, input features, and view predictions, showcasing full-stack development skills.
- **Comprehensive Evaluation**: Models are evaluated using Mean Absolute Error (MAE), Mean Squared Error (MSE), and R² score, with results saved for analysis.
- **Reusable Artifacts**: Trained models, label encoders, and feature names are saved as `.pkl` files for seamless integration with the web app.
- **Real-World Dataset**: Uses a Kaggle-sourced avocado dataset with features like volume, type, region, and year.

---

## 📂 Repository Structure

- `main.py`: Trains regression models, preprocesses data, and saves models and artifacts.
- `app.py`: Runs the Flask web app for interactive predictions and model evaluation.
- `data/avocado.csv`: Dataset containing avocado price and feature data.
- `templates/`: HTML templates for the Flask app (`index.html`, `results.html`, `model.html`).
- `*.pkl`: Saved models (e.g., `LinearRegression.pkl`, `RandomForest.pkl`), label encoders, and feature names.
- `Avocado_model_evaluation_results.csv`: Model performance metrics.
- `requirements.txt`: Lists project dependencies.

---

## 🚀 Getting Started

Follow these steps to set up and run the project locally. The instructions are designed to be straightforward for recruiters, developers, or anyone exploring the project.

### 📦 Prerequisites

Ensure you have the following installed:
- **Python 3.8+**: Download from [python.org](https://www.python.org/downloads/).
- **Git**: Install from [git-scm.com](https://git-scm.com/downloads).

### 🛠️ Step 1: Clone the Repository

Clone the project to your local machine:

```bash
git clone https://github.com/Raviteja-Beri/Avocado_Price_Prediction_Using_All_Regressions.git
cd Avocado_Price_Prediction_Using_All_Regressions
cd Avocado-Price-Prediction
```

### 📚 Step 2: Install Dependencies
Install the required Python libraries using the provided requirements.txt:
```bash
pip install -r requirements.txt
```
Note: If `requirements.txt` is not present, install the following manually:
```bash
pip install numpy pandas scikit-learn lightgbm xgboost joblib flask
```
### 🏋️‍♂️ Step 4: Train the Models (Optional)
Take the dataset and Train the regression models and generate artifacts (models, encoders, etc.):
```bash
python main.py
```
**This step**:

1. Preprocesses the dataset.
2. Trains 13 regression models.
3. Saves models `.pkl` files, encoders, feature names, and evaluation results (Avocado_model_evaluation_results.csv).
* Note: Skip this step if the `.pkl` files and `Avocado_model_evaluation_results.csv` are already present.
  
### 🌐 Step 5: Run the Flask Web App
Launch the Flask app to interact with the models:
```bash
python app.py
```
The app will start at http://127.0.0.1:5000.
Open this URL in your browser to:
* Select a model and input features (e.g., Total Volume, type, region, year).
* View predicted avocado prices.
* Check model performance metrics (MAE, MSE, R²).

#### 💡 How It Works
**1. Data Preprocessing**:
* Loads the avocado dataset and removes irrelevant columns.
* Encodes categorical features (type, region) using LabelEncoder.
* Splits data into training and test sets (80/20).
  
**2. Model Training**:
* Trains 13 regression models, from Linear Regression to XGBoost.
* Evaluates models using MAE, MSE, and R², saving results for comparison.
  
**3. Web Interface**:
* The Flask app loads saved models and artifacts.
* Users input features via a form, select a model, and get predictions.
* A separate page displays model performance metrics.

### 📊 Model Performance
The project evaluates models using:

* `Mean Absolute Error (MAE)`: Measures average prediction error.
* `Mean Squared Error (MSE)`: Penalizes larger errors more heavily.
* `R² Score`: Indicates how well the model explains the variance.
* Results are saved in `Avocado_model_evaluation_results.csv` and viewable via the Flask app.

### 🛠️ Technologies Used
* **Python**: Core programming language.
* **Machine Learning**: `scikit-learn`, `lightgbm`, `xgboost` for regression models.
* **Data Processing**: `pandas`, `numpy` for preprocessing and analysis.
* **Web Development**: `Flask` for the interactive web app.
* **Serialization**: `joblib` for saving models and encoders.
  
### 🔧 Troubleshooting
* **Dataset Not Found**: Ensure `avocado.csv` is in data/. Update the path in `main.py` if needed.
* **Module Not Found**: Install missing libraries using `pip install <library>`.
* **Flask App Fails**: Verify all `.pkl` files and `Avocado_model_evaluation_results.csv` are present.
* **Port Conflict**: If port 5000 is in use, change the port in `app.py` (e.g., app.run(debug=True, port=5001)).

## Thank You
