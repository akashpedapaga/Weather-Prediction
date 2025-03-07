# Weather Prediction System

## Overview

The **Weather Prediction System** is a machine learning-based approach to forecast weather conditions based on historical weather data. This project utilizes data scraping, preprocessing, and predictive modeling techniques to analyze various weather attributes such as temperature, humidity, wind speed, and atmospheric pressure.

## Features

- **Data Scraping**: Collects weather data from online sources using web scraping.
- **Data Preprocessing**: Cleans, normalizes, and transforms raw weather data.
- **Machine Learning Models**: Implements classification techniques to predict weather conditions.
- **Data Visualization**: Provides insights into weather trends using graphs and tables.
- **Automated Workflow**: Integrates data collection, preprocessing, and prediction into a single pipeline.

## Project Structure

```
Weather-Prediction/
│── data/                      # Raw and processed datasets
│── scripts/                   # Python scripts for scraping and preprocessing
│   │── scrape_data.py         # Scrapes weather data from web sources
│   │── preprocess_data.py     # Cleans and preprocesses the data
│   │── temp.py                # Alternative preprocessing script
│── models/                    # Machine learning models
│── notebooks/                 # Jupyter notebooks for analysis
│── README.md                  # Project documentation
│── requirements.txt           # Dependencies and libraries
```

## Data Collection

The **scrape\_data.py** script collects weather data from **Wunderground** for multiple years. The dataset includes:

- **Temperature** (°C)
- **Heat Index**
- **Dew Point**
- **Humidity**
- **Pressure**
- **Visibility**
- **Wind Speed & Direction**
- **Precipitation**
- **Weather Conditions**

## Data Preprocessing

The **preprocess\_data.py** script performs the following tasks:

1. **Converts units** (removes °C, %, hPa, km, etc.).
2. **Handles missing values** by removing or replacing them.
3. **Scales numerical variables** using min-max normalization.
4. **Encodes categorical variables** (e.g., one-hot encoding for wind direction).
5. **Creates a target variable** for predicting rainfall (0: No rain, 1: Rain).
6. **Saves the processed data** as `train.csv` for model training.

## Machine Learning Model

The project experiments with different classification algorithms, including:

- **Naïve Bayes**
- **Decision Tree (J48)**
- **Random Forest**
- **Support Vector Machines (SVM)**
- **Neural Networks**

The best-performing model is the **J48 Decision Tree**, which achieved high accuracy on the dataset.

## How to Run the Project

### 1. Install Dependencies

Ensure you have Python installed, then run:

```bash
pip install -r requirements.txt
```

### 2. Run Data Scraping

```bash
python scripts/scrape_data.py
```

### 3. Preprocess Data

```bash
python scripts/preprocess_data.py
```

### 4. Train and Test Model (Jupyter Notebook)

Open and execute `DMT Proj.ipynb` to train and evaluate the model.

## Results

- The J48 Decision Tree classifier showed the highest accuracy.
- Data preprocessing improved model performance significantly.
- Feature engineering (removing unnecessary attributes) enhanced classification accuracy.

## Future Improvements

- Implement **deep learning** models for improved accuracy.
- Use **real-time data** for continuous prediction.
- Deploy a **web-based interface** to visualize weather forecasts.

## Contributors

- **Akash Babu Pedapaga**
- **M. Eswar Kumar**
- **N. Gopi Krishna**

## License

This project is open-source and licensed under the MIT License.

