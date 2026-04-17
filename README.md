# Soil Moisture Trend Analysis & Prediction 📈

This project utilizes **Linear Regression** to analyze and predict soil moisture levels based on real-time sensor data. By applying machine learning techniques to raw hardware output, we can visualize moisture depletion trends and calculate the mathematical relationship between time and moisture percentage.

## 📝 Project Overview
The core objective is to take a time-series dataset (collected via Arduino) and fit a linear model that describes how moisture changes over time. This is critical for automated irrigation systems where predicting the "time-to-dry" is necessary.

### Key Logic:
1. **Data Preprocessing**: Loads sensor data from CSV and handles missing (NaN) values using `pandas`.
2. **Feature Engineering**: Reshapes time-series data into a format compatible with `scikit-learn`.
3. **Linear Regression**: Calculates the line of best fit using the Ordinary Least Squares method.
4. **Trend Visualization**: Generates a high-quality scatter plot with a regression line and mathematical annotations ($y = mx + c$).

## 🛠️ Technical Stack
* **Language:** Python 3.x
* **Data Handling:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn` (LinearRegression)
* **Visualization:** `matplotlib`

## 📊 Mathematical Results
The model automatically extracts:
* **Slope (m):** The rate of moisture change per second.
* **Intercept (c):** The initial moisture level at $t=0$.
* **R² Score:** The accuracy of the fit (Coefficient of Determination).

## 🚀 How to Use
1. Clone this repository.
2. Ensure your dataset is named `soil_moisture_data.csv` in the root directory.
3. Install dependencies:
   ```bash
   pip install numpy pandas scikit-learn matplotlib
