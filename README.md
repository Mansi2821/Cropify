# Cropify
# 🌾 Crop Yield Predictor

This project is a **Flask web application** that predicts crop yield (production) based on user inputs such as state, district, year, crop type, and area under cultivation. It uses a **Decision Tree Regressor** trained on real crop production data.

---

## 🚀 Features

- Predicts expected crop production (in metric tons)
- Accepts user input through a simple web form
- Displays prediction results interactively
- Trained on preprocessed agricultural data
- Supports a wide range of Indian states, districts, and crops

---

## 📂 Project Structure

├── app.py # Flask application (main web interface)
├── ml.py # Model training and preprocessing script
├── crop_production.csv # Raw dataset
├── preprocessor.pkl # Saved preprocessor object (used in app.py)
├── yield_model.pkl # Trained ML model
├── templates/
│ ├── main.html # Main page template
│ └── about.html # About page

---

## 🧠 How it Works

- The `ml.py` script loads and cleans the dataset, performs preprocessing (one-hot encoding, scaling), and trains a `DecisionTreeRegressor`.
- The model and the preprocessor are saved as `.pkl` files.
- The `app.py` script loads these saved files and uses them to make predictions based on form input.

---

## 🏃‍♀️ Getting Started

### 🔧 Prerequisites

- Python 3.7+
- Flask
- NumPy
- Pandas
- scikit-learn
- Matplotlib / Seaborn (optional, for analysis)

### 📦 Installation

1. Clone the repository or download the files.
2. Install dependencies:
pip install -r requirements.txt
Run the app:
python app.py
Open http://127.0.0.1:5000/ in your browser.

📊 Dataset
File: crop_production.csv

Columns: State_Name, District_Name, Crop_Year, Crop, Area, Production

Source: Indian government agricultural statistics

📌 Notes
Make sure the .pkl files (model and preprocessor) are in the same directory as app.py, or update their paths accordingly.

Predictions are made only for the values the model was trained on — ensure the inputs match existing categories.
