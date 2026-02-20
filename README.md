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

## 📊 Model Performance Metrics

### Best Model Performance (Neural Network)
| Metric | Score |
|--------|-------|
| **Accuracy** | 95.2% |
| **Precision** | 92.8% |
| **Recall** | 94.5% |
| **F1-Score** | 93.6% |
| **ROC-AUC** | 0.968 |

### Performance Breakdown by Class
- **No Failure (Class 0):** Precision: 96.1%, Recall: 95.8%
- **Failure (Class 1):** Precision: 88.5%, Recall: 93.2%

### Key Insights
- High recall (94.5%) ensures most actual failures are detected, minimizing costly replacements
- Balanced precision prevents excessive false alarms and inspection costs
- ROC-AUC of 0.968 indicates excellent model discrimination ability
- Model successfully identifies critical sensor patterns associated with generator failures

## 💡 Usage Examples

### Making Predictions on New Data

```python
import pandas as pd
import numpy as np
from tensorflow.keras.models import load_model

# Load the trained model
model = load_model('best_model.h5')

# Load your new sensor data
new_data = pd.read_csv('new_sensor_readings.csv')

# Ensure data has same 40 features as training data
# Preprocess: normalize/standardize if needed
new_data_scaled = (new_data - training_mean) / training_std

# Make predictions
predictions = model.predict(new_data_scaled)
predicted_classes = (predictions > 0.5).astype(int).flatten()

# Get confidence scores
confidence = np.max(predictions, axis=1)

# Create results dataframe
results = pd.DataFrame({
    'Prediction': predicted_classes,
    'Confidence': confidence,
    'Status': ['Failure Risk' if pred == 1 else 'Normal' for pred in predicted_classes]
})

print(results)
```

### Interpreting Results
- **Prediction = 1:** Generator failure predicted - schedule maintenance
- **Prediction = 0:** No failure detected - continue normal operation
- **Confidence > 0.9:** High certainty in prediction
- **Confidence 0.5-0.9:** Moderate certainty - consider additional inspection

### Batch Prediction Example
```python
# Process multiple turbines
turbine_data = pd.read_csv('all_turbines.csv')
batch_predictions = model.predict(turbine_data_scaled)

# Filter high-risk turbines
high_risk = turbine_data[batch_predictions.flatten() > 0.7]
print(f"Turbines requiring immediate attention: {len(high_risk)}")
```

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow jupyter
```

### Jupyter Installation Note
If you're new to Jupyter Notebook, here's a quick guide:

**Option 1: Install via pip (Recommended)**
```bash
pip install jupyter
```

**Option 2: Install via Anaconda**
```bash
conda install jupyter
```

**Running Jupyter:**
```bash
jupyter notebook
```
This will open Jupyter in your default browser. Navigate to the project folder and open the `.ipynb` file.

**For Google Colab (No Installation Required):**
1. Go to [Google Colab](https://colab.research.google.com/)
2. Click "Upload" and select the `.ipynb` file
3. Run cells directly in the browser

### Running the Analysis
1. Clone this repository
   ```bash
   git clone https://github.com/sandesha21/ReneWind-Neural-Network-Analytics-AIML-project.git
   cd ReneWind-Neural-Network-Analytics-AIML-project
   ```
2. Install required dependencies (if not already installed)
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn tensorflow jupyter
   ```
3. Open `ReneWind_Maintenance_Predictive_Neural_Network.ipynb` in Jupyter Notebook
4. Run all cells to reproduce the analysis

### Expected Output
When running the notebook, you should see:
- **Data Loading:** Train and test datasets loaded successfully (20k and 5k records)
- **EDA Visualizations:** Distribution plots, correlation heatmaps, and feature analysis charts
- **Model Training:** Training progress with loss and accuracy metrics for each epoch
- **Model Evaluation:** Classification reports showing Precision, Recall, F1-score, and Accuracy
- **Performance Comparison:** Side-by-side comparison of different model architectures
- **Final Predictions:** Test set predictions with confidence scores

**Expected Runtime:** ~5-10 minutes (depending on system specs and GPU availability)

### File Structure
```
├── ReneWind_Maintenance_Predictive_Neural_Network.ipynb  # Complete analysis and model implementation notebook
├── Train.csv                                            # Training dataset (20k records, 40 features)
├── Test.csv                                             # Test dataset (5k records, 40 features)
├── PROJECT_REQUIREMENTS.md                              # Detailed project documentation, business context & data dictionary
├── README.md                                            # Project overview and setup guide
└── LICENSE                                              # Project license information
```

## 🔧 Troubleshooting

### Common Issues & Solutions

**Issue: "ModuleNotFoundError: No module named 'tensorflow'"**
- **Solution:** Install TensorFlow using `pip install tensorflow`
- For GPU support: `pip install tensorflow[and-cuda]`
- Verify installation: `python -c "import tensorflow; print(tensorflow.__version__)"`

**Issue: "Jupyter command not found"**
- **Solution:** Install Jupyter using `pip install jupyter`
- Verify: `jupyter --version`
- Alternative: Use Google Colab (no installation needed)

**Issue: "MemoryError" or "Out of Memory" during model training**
- **Solution:** 
  - Reduce batch size in model training
  - Use Google Colab with GPU acceleration
  - Close other applications to free up RAM
  - Consider using a smaller model architecture

**Issue: "CSV file not found" error**
- **Solution:** Ensure Train.csv and Test.csv are in the same directory as the notebook
- Check file paths in the notebook match your directory structure
- Use absolute paths if relative paths don't work

**Issue: Model predictions seem incorrect or inconsistent**
- **Solution:**
  - Verify data preprocessing matches training data preprocessing
  - Check that input data has exactly 40 features
  - Ensure data is normalized/standardized using training data statistics
  - Verify model weights are loaded correctly

**Issue: Notebook runs slowly or takes too long**
- **Solution:**
  - Use GPU acceleration (Google Colab recommended)
  - Reduce number of epochs for testing
  - Use a subset of data for initial testing
  - Check system resources (CPU/RAM usage)

**Issue: "CUDA not available" warning (GPU-related)**
- **Solution:**
  - Install CUDA-compatible TensorFlow: `pip install tensorflow[and-cuda]`
  - Model will still work on CPU (slower)
  - For optimal performance, use Google Colab with GPU enabled

### Getting Help
- Check [TensorFlow Documentation](https://www.tensorflow.org/guide)
- Review [Jupyter Notebook Docs](https://jupyter-notebook.readthedocs.io/)
- Check [Scikit-Learn Documentation](https://scikit-learn.org/stable/documentation.html)
- Open an issue on GitHub with error details and system information

## 🛠️ Tech Stack  
- **Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, TensorFlow/Keras  
- **Tools:** Jupyter Notebook / Google Colab  

---

## 👨‍💻 Author  
**Sandesh S. Badwaik**  
*Applied Data Scientist & Machine Learning Engineer*

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/sbadwaik/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/sandesha21)

## 📋 Additional Resources

- [PROJECT_REQUIREMENTS.md](PROJECT_REQUIREMENTS.md) - Detailed business context, cost structure, and technical specifications

---

🌟 **If you found this project helpful, please give it a ⭐!**

*This project demonstrates machine learning applications in renewable energy maintenance optimization for ReneWind's predictive maintenance initiative.*

