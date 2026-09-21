# Heart Disease Prediction App

A machine learning project that predicts the likelihood of heart disease using various patient health indicators. This project uses a trained K-Nearest Neighbors (KNN) model and a Streamlit web app for interactive prediction.

## Overview

Heart disease is one of the leading causes of death worldwide. Early detection can help reduce risks and improve patient outcomes. This project uses health data such as age, chest pain type, blood pressure, cholesterol, blood sugar, ECG readings, heart rate, and other indicators to classify whether a person is at high or low risk of heart disease.

The app provides a simple interface where users can enter medical values and instantly receive a prediction based on the trained model.

## Project Goals

- Predict heart disease risk using patient health information
- Build a user-friendly interface with Streamlit
- Demonstrate practical use of machine learning in healthcare
- Showcase end-to-end ML workflow: data preprocessing, model training, and deployment

## Features

- Interactive user input form for health parameters
- Real-time heart disease prediction
- Model trained using healthcare dataset
- Data preprocessing and scaling for machine learning
- Easy-to-use Streamlit web application

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Joblib
- Streamlit

## Dataset

The project uses a heart disease dataset containing features such as:

- Age
- Sex
- Chest Pain Type
- Resting Blood Pressure
- Cholesterol
- Fasting Blood Sugar
- Resting ECG
- Max Heart Rate
- Exercise-Induced Angina
- Oldpeak (ST Depression)
- ST Slope

## Model

A K-Nearest Neighbors (KNN) classifier is used for prediction. The model is trained on the dataset, saved using `joblib`, and loaded in the Streamlit app for inference.

## Project Structure

```bash
Heart Stroke Prediction/
│
├── app.py                     # Streamlit application
├── heart.csv                 # Dataset
├── HeartdiseaseFinal.ipynb   # Notebook for analysis and model training
├── Knn_heart_model.pkl       # Trained ML model
├── heart_scaler.pkl          # Saved scaler
├── heart_columns.pkl         # Expected input columns
├── README.md                 # Project documentation
└── requirements.txt          # (optional if added later)
```

## Installation

1. Clone the repository:

```bash
git clone https://github.com/sunnydubeydeoria/heart-disease-prediction.git
cd heart-disease-prediction
```

2. Create a virtual environment (optional but recommended):

```bash
python -m venv venv
venv\Scripts\activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

If a `requirements.txt` file is not available, install the required packages manually:

```bash
pip install streamlit pandas numpy scikit-learn joblib
```

## Run the App

```bash
streamlit run app.py
```

Then open the local URL shown in the terminal in your browser.

## How It Works

1. User enters health-related values in the web interface.
2. The app converts the inputs into a DataFrame.
3. Missing columns are filled with zeros to match the trained model input.
4. The scaler transforms the features.
5. The KNN model predicts whether the patient is at low or high risk.
6. The result is displayed on the app interface.

## Example of Input Features

- Age: 45
- Sex: M
- Chest Pain Type: ATA
- Resting Blood Pressure: 130
- Cholesterol: 220
- Fasting Blood Sugar: 0
- Resting ECG: Normal
- Max Heart Rate: 150
- Exercise-Induced Angina: N
- Oldpeak: 1.5
- ST Slope: Flat

## Output

The app displays one of the following results:

- High Risk of Heart Disease
- Low Risk of Heart Disease

## Future Improvements

- Add more advanced models such as Random Forest, XGBoost, or Logistic Regression
- Include patient history and lifestyle features
- Improve model accuracy with feature selection and hyperparameter tuning
- Add visual charts and risk explanations for better usability
- Deploy the application using Streamlit Cloud or Heroku

## License

This project is open-source and available for educational and personal use.

## Author

Sunny

## GitHub Upload Note

To upload this project on GitHub:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/sunnydubeydeoria/heart-disease-prediction.git
git push -u origin main
```

## Conclusion

This project demonstrates how machine learning can be applied to solve real-world healthcare problems. It highlights the importance of predictive analytics in early risk assessment and shows how data science can contribute to medical decision support systems.
