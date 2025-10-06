# ReneWind Predictive Maintenance

## Overview  
This project focuses on predictive maintenance for wind turbines using sensor data analytics. By predicting generator failures before they occur, the solution aims to help renewable energy companies minimize maintenance costs, reduce downtime, and improve operational efficiency.

## Objective  
The primary goal was to build machine learning models capable of identifying potential turbine generator failures based on environmental and sensor data. Accurate failure prediction allows for proactive maintenance scheduling, significantly lowering replacement costs and increasing system reliability.

## Dataset  
- **Source:** Provided as part of the project coursework  
- **Size:** ~20,000 training records, ~5,000 test records  
- **Key Features:**  
  - Environmental variables (temperature, humidity, wind speed)  
  - Turbine component metrics (gearbox, tower, blade sensors)  
- **Target:** Failure Status (`1` = Failure, `0` = No Failure)

## Workflow  
1. **Data Preprocessing** – Cleaned, standardized, and prepared sensor data for model training.  
2. **Exploratory Data Analysis (EDA)** – Explored feature distributions and identified critical signals correlated with failures.  
3. **Model Development** – Built multiple classification models, including neural networks, and experimented with techniques like dropout, optimizers, deeper layers, and class weighting.  
4. **Evaluation & Insights** – Compared model performances and selected the best approach for failure prediction.

## Results & Key Insights  
- Built a robust predictive model capable of early failure detection to support proactive maintenance.  
- Reduced potential downtime and costly replacements by enabling scheduled component repairs.  
- Provided actionable insights into key sensor variables influencing turbine reliability.

## Tech Stack  
- **Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, TensorFlow/Keras  
- **Tools:** Jupyter Notebook / Google Colab  

## Author  
**Sandesh S. Badwaik**  
- [LinkedIn](https://www.linkedin.com/in/sbadwaik/)
