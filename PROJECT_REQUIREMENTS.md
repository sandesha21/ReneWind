# Project Requirements

## Business Context

Renewable energy sources play an increasingly important role in the global energy mix, as the effort to reduce the environmental impact of energy production increases.

Out of all the renewable energy alternatives, wind energy is one of the most developed technologies worldwide. The U.S. Department of Energy has put together a guide to achieving operational efficiency using predictive maintenance practices.

Predictive maintenance uses sensor information and analysis methods to measure and predict degradation and future component capability. The idea behind predictive maintenance is that failure patterns are predictable and if component failure can be predicted accurately and the component is replaced before it fails, the costs of operation and maintenance will be much lower.

The sensors fitted across different machines involved in the process of energy generation collect data related to various environmental factors (temperature, humidity, wind speed, etc.) and additional features related to various parts of the wind turbine (gearbox, tower, blades, break, etc.).

## Objective

"ReneWind" is a company working on improving the machinery/processes involved in the production of wind energy using machine learning and has collected data on generator failure of wind turbines using sensors. They have shared a ciphered version of the data, as the data collected through sensors is confidential (the type of data collected varies with companies). Data has 40 predictors, 20000 observations in the training set, and 5000 in the test set.

The objective is to build various classification models, tune them, and find the best one that will help identify failures so that the generators can be repaired before failing/breaking to reduce the overall maintenance cost.

## Cost Structure

The nature of predictions made by the classification model will translate as follows:

- **True positives (TP)** are failures correctly predicted by the model. These will result in repair costs.
- **False negatives (FN)** are real failures where there is no detection by the model. These will result in replacement costs.
- **False positives (FP)** are detections where there is no failure. These will result in inspection costs.

It is given that the cost of repairing a generator is much less than the cost of replacing it, and the cost of inspection is less than the cost of repair.

**Cost Hierarchy:** Inspection < Repair < Replacement

## Target Variable

- `1` in the target variable should be considered as "failure"
- `0` represents "No failure"

## Data Dictionary

The data provided is a transformed version of the original data which was collected using sensors.

### Files Description

- **Train.csv** - To be used for training and tuning of models
- **Test.csv** - To be used only for testing the performance of the final best model

Both datasets consist of:
- **40 predictor variables** (sensor data features)
- **1 target variable** (failure status)

### Dataset Specifications

- **Training Set:** 20,000 observations
- **Test Set:** 5,000 observations
- **Features:** 40 predictors (ciphered/anonymized sensor data)
- **Target:** Binary classification (0 = No failure, 1 = Failure)

## Success Criteria

The model should prioritize:
1. **Minimizing False Negatives** (missed failures leading to costly replacements)
2. **Optimizing overall cost** considering the cost hierarchy
3. **Achieving high recall** for failure detection
4. **Balancing precision** to avoid excessive inspection costs

## Data Quality Notes

### Missing Values & Data Integrity
- Dataset is pre-processed and cleaned; minimal missing values expected
- All 40 predictor variables are numeric (transformed sensor readings)
- No categorical variables requiring encoding
- Data is already standardized/normalized for model compatibility

### Outliers & Anomalies
- Sensor data may contain outliers due to extreme environmental conditions
- Outliers are retained as they may indicate genuine failure signals
- Statistical outlier detection should be applied cautiously to avoid removing critical failure indicators
- Class imbalance may exist (more "No Failure" than "Failure" cases) - requires handling via class weighting or resampling

### Data Characteristics
- All features are anonymized/ciphered for confidentiality
- No feature names provided; features are referenced as numeric indices
- Data is already split into training and test sets with no overlap
- No temporal ordering; observations are independent

## Model Constraints & Assumptions

### Model Limitations
- **Binary Classification Only:** Model predicts failure/no-failure; does not predict failure severity or time-to-failure
- **Sensor Data Dependency:** Predictions rely on sensor accuracy; faulty sensors will degrade model performance
- **Historical Data Bias:** Model trained on past failure patterns; may not generalize to new turbine models or environmental conditions
- **Real-time Constraints:** Model inference time should be <100ms for practical deployment

### Key Assumptions
- **Failure Patterns are Consistent:** Historical failure patterns will repeat in future data
- **Sensor Calibration:** All sensors are properly calibrated and maintained
- **Stationary Distribution:** Data distribution remains consistent over time (no concept drift)
- **Feature Independence:** Features are treated as independent; multicollinearity is acceptable
- **Balanced Cost Structure:** Cost hierarchy (Inspection < Repair < Replacement) remains constant

### Deployment Considerations
- Model requires regular retraining with new failure data
- Monitoring for model drift is essential for long-term performance
- Predictions should be reviewed by domain experts before maintenance decisions
- Model performance may degrade with new turbine models or environmental changes