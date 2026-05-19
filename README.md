# **AgroZone Analytics**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1TwLeNTdcjoGDq0FU5rb7vpjHZ3yhbBBR?usp=sharing)

**Unsupervised Agro-Zoning Based Crop Recommendation Using Soil, Yield, and Market Data**

---

## **Project Overview**

AgroZone Analytics is a **context-aware, unsupervised agro-zoning–based crop recommendation system designed as a decision-support tool**.

The system:

* Discovers agro-zones using unsupervised learning on soil and climate data  
* Uses historical crop yield and market price data to rank crops  
* Provides **Top-3 crop recommendations per season**  
* Does **not predict a single crop** or optimize profit  
* Supports an optional interactive interface in Google Colab

---

## **How to Run the Project**

This project is designed to run **entirely on Google Colab**.

### **Steps:**

1. Open the provided [Google Colab notebook](https://colab.research.google.com/drive/1TwLeNTdcjoGDq0FU5rb7vpjHZ3yhbBBR?usp=sharing).  
2. Mount Google Drive when prompted.  
3. Download datasets using the Kaggle API (instructions are included inside the notebook).  
4. Run all cells **from top to bottom** in order.  
5. (Optional) Use the interactive recommendation section at the end of the notebook to input soil and climate values.

No local setup is required.

Note : If **“Run all”** does not successfully download the datasets, please run the **Kaggle setup and dataset download cells manually** first. After the datasets are available, the remaining notebook cells can be executed normally.

---

## 

## 

## **Datasets Used**

Due to size constraints, datasets are **not included directly** in the submission ZIP.

The datasets can be accessed using the following Kaggle links:

1. **Crop Recommendation Dataset (Soil & Climate)**  
   [https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset](https://www.kaggle.com/datasets/atharvaingle/crop-recommendation-dataset)  
2. **Crop Production in India**  
   [https://www.kaggle.com/datasets/abhinand05/crop-production-in-india](https://www.kaggle.com/datasets/abhinand05/crop-production-in-india)  
3. **Agmarknet India Commodity Prices (Oct’24 – Aug’25)**  
   [https://www.kaggle.com/datasets/anishaman07/agmarknet-india-commodity-prices-oct24-aug25](https://www.kaggle.com/datasets/anishaman07/agmarknet-india-commodity-prices-oct24-aug25)

Alternatively, all datasets can be accessed via Google Drive:

---

## **Methodology Summary**

* **Unsupervised Learning:** K-Means clustering on soil and climate features  
* **Agro-Zone Discovery:** Optimal number of zones selected using Elbow Method and Silhouette Score  
* **Crop Recommendation:**  
  * Historical Yield (Production / Area)  
  * Market Price (Average Modal Price)

**Scoring Formula:**  
`Score = 0.6 × Normalized_Yield + 0.4 × Normalized_Market_Price`

*   
* **Recommendation Output:**  
  * Top-3 crops per season (Kharif, Rabi, Summer)  
  * Zone-wise, season-wise ranked recommendations

---

**Interactive Recommendation Interface (Optional)**

The Colab notebook includes an optional interactive section where users can:

* Input soil and climate values  
* Select a season  
* Identify the corresponding agro-zone  
* View precomputed crop recommendations

Important notes:

* No retraining occurs  
* No prediction is performed  
* The interface only retrieves results from the final recommendation table

---

## **Dependencies**

The following Python libraries are used:

* Python 3.x  
* numpy  
* pandas  
* scikit-learn  
* matplotlib  
* ipywidgets

All dependencies are **pre-installed in Google Colab**.

## **Folder Structure**

The submission ZIP is organized as follows:

`srujan.24bcs10339@sst.scaler.com/`  
`│`  
`├── AgroZone_Analytics/`  
`│   │`  
`│   ├── AgroZone_Analytics.ipynb`  
`│   ├── Project_Report_AgroZone_Analytics.pdf`  
`│   └── Datasets/`  
`│       ├── Crop_recommendation.csv`  
`│       ├── crop_production.csv`  
`│       └── agmarknet_india_historical_prices_2024_2025.csv`  
`├── README.md`

                 

## **Notes** 

* This project is a **decision-support system**, not a prediction model.  
* Agro-zones are discovered using unsupervised learning.  
* No accuracy, precision, recall, or supervised metrics are used.  
* Recommendations are advisory and based on historical data.