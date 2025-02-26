# TATA-STEEL-MACHINE-FAILURE-PREDICTION-MACHINE-LEARNING-MODEL
 
## **Project Overview**  
This project focuses on **predictive maintenance** for industrial machines, helping businesses reduce unexpected failures, minimize downtime, and optimize maintenance schedules. The goal is to develop a **machine learning model** that predicts machine failures based on sensor data, allowing industries to shift from reactive maintenance to a data-driven predictive approach.  

## **Business Problem**  
Unexpected machine failures result in costly downtime and production losses. Predictive maintenance enables businesses to **forecast failures in advance** by analyzing real-time sensor data. By implementing an AI-driven approach, companies can reduce maintenance costs and enhance operational efficiency.  

## **Dataset**  
The dataset contains various machine sensor readings and operational parameters:  

- **Air temperature [K]** – Ambient temperature in Kelvin  
- **Process temperature [K]** – Internal machine temperature  
- **Rotational speed [rpm]** – Speed of machine rotation in revolutions per minute  
- **Torque [Nm]** – Torque applied to the machine  
- **Tool wear [min]** – Duration for which the tool has been used  
- **Machine failure** – Binary label indicating failure occurrence (1) or not (0)  
- **Failure Types (TWF, HDF, PWF, OSF, RNF)** – Different types of failures observed  

## **Key Steps in the Project**  

### **1. Data Exploration & Visualization**  
- Identified missing values, duplicates, and outliers.  
- Used **boxplots, violin plots, scatter plots, and correlation heatmaps** to analyze sensor data.  
- Visualized failure patterns across machine types.  

### **2. Feature Engineering & Data Preprocessing**  
- **Handling Missing Values:**  
  - Used **mean/median imputation** to fill missing values in numerical columns.  
- **Outlier Treatment:**  
  - Applied **Interquartile Range (IQR)** method to detect and cap extreme values.  
- **Categorical Encoding:**  
  - Used **one-hot encoding** for categorical machine types.  
- **Feature Scaling:**  
  - Applied **MinMaxScaler** to normalize numerical features for better model performance.  

### **3. Model Training & Evaluation**  
- **Machine Learning Models Used:**  
  - **XGBoost** – High-performance gradient boosting model  
  - **LightGBM** – Optimized for speed and efficiency  
  - **Random Forest** – Robust ensemble learning algorithm  
- **Performance Metrics Used:**  
  - Accuracy  
  - Precision, Recall, and F1-score  
  - ROC-AUC Score for classification quality  

### **4. Hypothesis Testing**  
- Conducted **t-tests and ANOVA** to validate the impact of different parameters on machine failure.  
- Example Findings:  
  - Machines with **higher tool wear** are significantly more likely to fail.  
  - **Process temperature differences** impact failure rates.  

### **5. Business Recommendations**  
- **Real-time monitoring** should be implemented for sensor anomalies.  
- **Predictive maintenance scheduling** is more effective than fixed-time maintenance.  
- Machines with **higher torque and tool wear values** should be prioritized for early maintenance.  

## **Results & Conclusion**  
- The **XGBoost model** performed the best, achieving high accuracy in predicting failures.  
- Predictive analytics can **reduce downtime and maintenance costs** by proactively identifying faulty machines.  
- Businesses can implement this **ML-powered approach for real-time failure detection**.  

## **Technologies Used**  
- **Programming Language:** Python  
- **Libraries:** Pandas, NumPy, Scikit-learn, XGBoost, LightGBM, Matplotlib, Seaborn  
- **Machine Learning Algorithms:** XGBoost, LightGBM, Random Forest  
- **Deployment (Optional):** Flask/FastAPI for API deployment  

## **How to Use the Project**  
1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/Predictive-Maintenance-ML.git
   cd Predictive-Maintenance-ML
   ```
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook to explore the dataset and train models.  

## **Future Scope**  
- Deploy the model using a **real-time dashboard** for monitoring machine health.  
- Improve feature engineering to enhance model accuracy.  
- Incorporate **deep learning models** for complex failure pattern detection.  
