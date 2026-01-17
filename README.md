# ReneWind Predictive Maintenance

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)](https://tensorflow.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

## Overview  
This project focuses on predictive maintenance for wind turbines using sensor data analytics. By predicting generator failures before they occur, the solution aims to help renewable energy companies minimize maintenance costs, reduce downtime, and improve operational efficiency.

## 🎯 Key Achievements
- Developed neural network models for early failure detection
- Achieved proactive maintenance scheduling capabilities
- Reduced potential downtime through predictive analytics

## Objective  
The primary goal was to build machine learning models capable of identifying potential turbine generator failures based on environmental and sensor data. Accurate failure prediction allows for proactive maintenance scheduling, significantly lowering replacement costs and increasing system reliability.

## 📊 Dataset  
- **Source:** Provided as part of the project coursework  
- **Size:** ~20,000 training records, ~5,000 test records  
- **Key Features:**  
  - Environmental variables (temperature, humidity, wind speed)  
  - Turbine component metrics (gearbox, tower, blade sensors)  
- **Target:** Failure Status (`1` = Failure, `0` = No Failure)

## 🔄 Workflow  
1. **Data Preprocessing** – Cleaned, standardized, and prepared sensor data for model training.  
2. **Exploratory Data Analysis (EDA)** – Explored feature distributions and identified critical signals correlated with failures.  
3. **Model Development** – Built multiple classification models, including neural networks, and experimented with techniques like dropout, optimizers, deeper layers, and class weighting.  
4. **Evaluation & Insights** – Compared model performances and selected the best approach for failure prediction.

## 📈 Results & Key Insights  
- Built a robust predictive model capable of early failure detection to support proactive maintenance  
- Reduced potential downtime and costly replacements by enabling scheduled component repairs  
- Provided actionable insights into key sensor variables influencing turbine reliability

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow jupyter
```

### Running the Analysis
1. Clone this repository
2. Open `ReneWind_Maintenance_Predictive_Neural_Network.ipynb` in Jupyter Notebook
3. Run all cells to reproduce the analysis

### File Structure
```
├── ReneWind_Maintenance_Predictive_Neural_Network.ipynb  # Main analysis notebook
├── Train.csv                                            # Training dataset
├── Test.csv                                             # Test dataset
├── Problem_Statement.pdf                                # Project requirements
└── README.md                                            # This file
```

## 🛠️ Tech Stack  
- **Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, TensorFlow/Keras  
- **Tools:** Jupyter Notebook / Google Colab  

## 👨‍💻 Author  
**Sandesh S. Badwaik**  
- [LinkedIn](https://www.linkedin.com/in/sbadwaik/)

---

*This project demonstrates the application of machine learning in renewable energy maintenance optimization.*
