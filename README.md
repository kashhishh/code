# Income Prediction App

This project demonstrates an end-to-end machine learning pipeline for predicting income using the Adult Income dataset (`adult_corrected.csv`). It includes data cleaning, feature engineering, model training, bias analysis, and a Flask web API for real-time predictions.

## Features
- Data cleaning and imputation of missing values using PySpark
- Categorical variable encoding (StringIndexer, OneHotEncoder)
- Numerical feature scaling (StandardScaler)
- Feature engineering (interaction terms, binary indicators)
- Model training (Logistic Regression, Random Forest)
- Bias analysis and mitigation (gender, race)
- Visualization of feature distributions and correlations
- Flask API for serving predictions

## Usage
1. **Data Preparation**: Clean and preprocess the `adult_corrected.csv` dataset using PySpark.
2. **Model Training**: Train a machine learning model (Logistic Regression or Random Forest) on the processed data.
3. **Bias Analysis**: Evaluate model bias across demographic groups and apply mitigation techniques if needed.
4. **Visualization**: Explore feature distributions and relationships using matplotlib and seaborn.
5. **Flask API**: Serve the trained model via a Flask web app for real-time predictions.

## How to Run
1. Install required packages:
   ```bash
   pip install pyspark flask flask-ngrok pandas matplotlib seaborn scikit-learn
   ```
2. Run the notebook step by step to clean data, train the model, and save it.
3. Start the Flask app:
   ```bash
   python app.py
   ```
4. Access the web interface at [http://127.0.0.1:5000](http://127.0.0.1:5000) or use the `/predict` endpoint for API calls.

## API Example
Send a POST request to `/predict` with a JSON payload containing the feature vector:
```json
{
  "features": [value1, value2, ..., valueN]
}
```
Response:
```json
{
  "predicted_income": ">50K"
}
```

## Project Structure
- `Income_prediction.ipynb`: Main notebook for data processing, modeling, and analysis
- `app.py`: Flask web application for serving predictions
- `adult_corrected.csv`: Dataset
- `README.md`: Project documentation

## Notes
- The pipeline uses PySpark for scalable data processing and modeling.
- Bias analysis is performed using group metrics and mitigation strategies.
- The Flask app can be deployed locally or with ngrok for public access.

## License
This project is for educational purposes.
