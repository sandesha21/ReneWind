# ReneWind Predictive Maintenance

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)](https://tensorflow.org/)
[![Keras](https://img.shields.io/badge/Keras-2.x-red.svg)](https://keras.io/)
[![Pandas](https://img.shields.io/badge/Pandas-1.x-150458.svg)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-1.x-013243.svg)](https://numpy.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.x-F7931E.svg)](https://scikit-learn.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.x-11557c.svg)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-0.x-3776ab.svg)](https://seaborn.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Machine Learning](https://img.shields.io/badge/ML-Predictive%20Maintenance-brightgreen.svg)]()
[![Industry](https://img.shields.io/badge/Industry-Renewable%20Energy-success.svg)]()
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen.svg)]()
[![Neural Networks](https://img.shields.io/badge/Deep%20Learning-Neural%20Networks-purple.svg)]()
[![Data Science](https://img.shields.io/badge/Data%20Science-Analytics-blue.svg)]()

## 🏷️ Keywords & Topics

**Primary Keywords:** Data Science • Machine Learning • Predictive Maintenance • Python • Wind Energy Analytics  
**Technical Stack:** TensorFlow/Keras • Pandas • Scikit-Learn • Neural Networks • Data Preprocessing • Jupyter Notebook  
**Business Focus:** Predictive Analytics • Cost Optimization • Failure Detection • Maintenance Scheduling • Operational Efficiency  
**Industry:** Renewable Energy • Wind Power • Industrial IoT • Sensor Analytics • Energy Production • Sustainability  

**Project Type:** Predictive Analytics & Deep Learning | Industry: Renewable Energy | Focus: Maintenance Cost Optimization

## Overview  
This project focuses on predictive maintenance for wind turbines using sensor data analytics for ReneWind, a company working on improving wind energy production machinery using machine learning. By predicting generator failures before they occur, the solution aims to minimize maintenance costs, reduce downtime, and improve operational efficiency through proactive maintenance scheduling.

## 🎯 Key Achievements
- Developed neural network models for early failure detection
- Achieved proactive maintenance scheduling capabilities
- Reduced potential downtime through predictive analytics

## Objective  
Build various classification models to identify potential turbine generator failures based on sensor data, enabling proactive maintenance scheduling. The goal is to minimize overall maintenance costs by:

- **Reducing False Negatives:** Avoiding missed failures that lead to costly generator replacements
- **Optimizing Cost Structure:** Balancing inspection costs (FP) < repair costs (TP) < replacement costs (FN)
- **Maximizing Recall:** Ensuring high detection rate for actual failures

*Cost Hierarchy: Inspection < Repair < Replacement*

## 📊 Dataset  
- **Source:** ReneWind company sensor data (ciphered/anonymized version)
- **Training Set:** 20,000 observations  
- **Test Set:** 5,000 observations
- **Features:** 40 predictor variables (transformed sensor data)
  - Environmental factors (temperature, humidity, wind speed)  
  - Turbine component metrics (gearbox, tower, blades, brake sensors)
- **Target:** Binary failure status (`1` = Failure, `0` = No Failure)
- **Data Confidentiality:** Original sensor data transformed to protect proprietary information

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
   ```bash
   git clone <repository-url>
   cd ReneWind-Predictive-Maintenance
   ```
2. Install required dependencies
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn tensorflow jupyter
   ```
3. Open `ReneWind_Maintenance_Predictive_Neural_Network.ipynb` in Jupyter Notebook
4. Run all cells to reproduce the analysis

### File Structure
```
├── ReneWind_Maintenance_Predictive_Neural_Network.ipynb  # Main analysis notebook
├── Train.csv                                            # Training dataset (20k records)
├── Test.csv                                             # Test dataset (5k records)
├── PROJECT_REQUIREMENTS.md                              # Detailed business context & objectives
└── README.md                                            # This file
```

## 🛠️ Tech Stack  
- **Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, TensorFlow/Keras  
- **Tools:** Jupyter Notebook / Google Colab  

---

## 👨‍💻 Author  
**Sandesh S. Badwaik**  
- [LinkedIn](https://www.linkedin.com/in/sbadwaik/)

## 📋 Additional Resources

- [PROJECT_REQUIREMENTS.md](PROJECT_REQUIREMENTS.md) - Detailed business context, cost structure, and technical specifications

---

🌟 **If you found this project helpful, please give it a ⭐!**

*This project demonstrates machine learning applications in renewable energy maintenance optimization for ReneWind's predictive maintenance initiative.*

