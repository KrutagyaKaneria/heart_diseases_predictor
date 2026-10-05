# Heart Disease Prediction App

This project is a Streamlit web application that predicts whether a person is at low or high risk of heart disease based on medical and lifestyle input values.

## Project Overview

The app loads a trained K-Nearest Neighbors (KNN) model, a saved scaler, and the expected feature columns used during training. It then accepts patient information from the user and predicts the outcome.

### Example prediction categories

- Low Risk of Heart Disease
- High Risk of Heart Disease

## Features

The interface collects information such as:

- Age
- Sex
- Chest pain type
- Resting blood pressure
- Cholesterol
- Fasting blood sugar
- Resting ECG
- Max heart rate
- Exercise-induced angina
- Oldpeak
- ST slope

## Project Files

- `app.py` – Streamlit application code and prediction logic
- `KNN_heart.pkl` – serialized trained model
- `scaler.pkl` – saved StandardScaler used for preprocessing
- `columns.pkl` – expected input columns in the correct order
- `heart.csv` – dataset used to build the model
- `requirements.txt` – required Python packages

## Requirements

- Python 3.9+
- Streamlit
- pandas
- scikit-learn
- joblib

## Local Setup

1. Open a terminal inside the project folder.
2. Create a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

3. Install the required packages:

```bash
pip install -r requirements.txt
```

4. Run the app:

```bash
streamlit run app.py
```

The app should open in the browser at:

```text
http://localhost:8501
```

## Deployment on Streamlit Community Cloud

To deploy this app in Streamlit Community Cloud:

1. Push this project to a GitHub repository.
2. Go to Streamlit Cloud.
3. Click “New app”.
4. Select your repository and branch.
5. Set the main file path to `app.py`.
6. Click Deploy.

## Important Note

The app may show a scikit-learn version warning if the model was trained with a different version of scikit-learn than the one installed in the environment. In most cases, the app still runs, but if compatibility issues appear, retraining the model with the same environment version is recommended.

## License

This project is intended for educational and demonstration use.
