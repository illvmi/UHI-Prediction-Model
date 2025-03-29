URBAN HEAT ISLAND PREDICTION MODEL 🌆🔥
This machine learning model was developed as part of the 2025 EY Open Science AI and Data Challenge to predict Urban Heat Islands (UHI) using satellite imagery, meteorological data, and machine learning techniques.

📌 Project Overview
📌 OVERVIEW
Urban Heat Islands (UHIs) occur when urban areas experience significantly higher temperatures than surrounding rural areas due to human activities and infrastructure. This project aims to:

✔ Analyze satellite and land surface temperature data to detect UHI patterns.

✔ Predict UHI intensity using a Random Forest Regression model.

✔ Provide insights to help urban planners mitigate excessive heat effects.

📂 DATASETS AND FEATURES
The model uses the following datasets:

📍 Satellite Imagery Data (Sentinel-2) → Extracts spectral bands (B01, B04, B06, B08).

🌡 Land Surface Temperature (LST) → Derived from Landsat data.

🌱 Vegetation Index (NDVI) → Calculated to assess vegetation coverage.


FEATURE ENGINEERING INCLUDES:

 NDVI_Calculated: Normalized Difference Vegetation Index (NDVI) from Sentinel-2 data.
  
 LST_Sqrt: Square root transformation of Land Surface Temperature.
 
 NDVI_LST_Ratio: Ratio of NDVI to LST for improved feature representation.


🛠️ MODEL AND TECHNIQUES USED

Random Forest Regressor (800 trees, max depth=45, fine-tuned for performance).

Cross-validation (7-fold) to improve generalization.

Winsorization to handle outliers in features.

Standardization (Z-score normalization) for feature scaling.


🚀 HOW TO RUN THE MODEL
This project was developed on Google Colab. To run it:

Open the Colab notebook: [https://colab.research.google.com/drive/1_WldUrkwkfqJzi0jd2lIugG8N3VRSNF7?usp=sharing].

Upload the dataset files: Training_data_uhi_index_2025-02-18.csv, Landsat_LST.csv, and S2_sample.tiff.

Execute the cells to preprocess data, train the model, and make predictions.

The final UHI predictions will be saved as submission.csv.

📊 PERFOMRMANCE METRICS
Metric	Training Score	Testing Score

R² Score	[0.957210434274]	[0.738015659865]

MSE	[1.12530182587693e-05]	[7.007281932012015e-05]

Mean Cross-Validation R²	[0.6905245151421614]	

📎 FILES IN THIS REPOSITORY
📂 uhi_model.ipynb → Colab notebook containing all code.
📂 Training_data_uhi_index_2025-02-18.csv → UHI training dataset.
📂 Landsat_LST.csv → LST dataset.
📂 S2_sample.tiff → Sentinel-2 satellite image file.
📂 submission.csv → Predicted UHI index results.
