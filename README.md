💳 Fraud Detection System (Flask + ML)

This project is a Machine Learning–powered Fraud Detection System that identifies fraudulent financial transactions using a Random Forest model. It provides both the model training pipeline and a Flask web app for real-time predictions.

📂 Project Structure

model.py – Trains the Random Forest model on transaction data (ML_Data2.0.csv), performs feature scaling, and saves both the trained model (model.pkl) and scaler (scaler.pkl) using pickle.

app.py – Flask-based web application that loads the saved model and scaler, accepts user inputs (transaction details), and predicts whether the transaction is Fraudulent 🚨 or Legitimate ✅.

zidio_project2.ipynb – Jupyter Notebook used for data exploration, preprocessing, and experimentation before finalizing the ML pipeline.

⚙️ How it Works

Data Preprocessing

Features: type, amount, oldbalanceOrg, newbalanceOrig

Target: isFraud (1 = Fraudulent, 0 = Legitimate)

Standardization applied via StandardScaler.

Model Training (model.py)

Uses RandomForestClassifier for classification.

Saves model and scaler for later inference.

Web Application (app.py)

User inputs transaction details (amount, balance, type).

Transaction type is encoded numerically.

Data is scaled and passed into the trained ML model.

Prediction result is displayed in the browser.

🚀 Run the Project
# Train the model
python model.py  

# Start Flask app
python app.py

🔮 Future Improvements

Add more features (e.g., destination balances, time-based features).

Enhance UI/UX for the web app.

Deploy on cloud (Heroku/AWS/Streamlit).
