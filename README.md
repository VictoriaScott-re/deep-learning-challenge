# Alphabet Soup Charity - Deep Learning Challenge

## Overview of the Analysis

The purpose of this project was to develop a **binary classifier** using a deep learning model to predict whether applicants funded by Alphabet Soup will be successful in their ventures. By analyzing the data and optimizing the model, we aimed to achieve a target accuracy of 75%.

---

## Results

**Dataset Preview** (`images/dataset_preview.png`): 
   - A screenshot of the dataset after dropping the `EIN` and `NAME` columns. 
   - This shows the remaining features that were used for training.

### Data Preprocessing

- **Target Variable**: 
  - `IS_SUCCESSFUL` — This binary variable indicates whether the money was used effectively.
  
- **Features**: 
  - `APPLICATION_TYPE`, `AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `INCOME_AMT`, `ASK_AMT`, `SPECIAL_CONSIDERATIONS`, and `STATUS`.

- **Removed Variables**: 
  - `EIN` and `NAME` — These columns were not beneficial to the prediction task and were dropped during preprocessing.

**Data Preprocessing** (`images/data_preprocessing.png`):
   - A screenshot showing part of the preprocessing step where categorical variables were encoded with `pd.get_dummies()` and the dataset split into features and target arrays.
---

### Compiling, Training, and Evaluating the Model

- **Neurons, Layers, and Activation Functions**:
  - A variety of models were attempted, ranging from 2 to 3 hidden layers with varying neuron counts between 25 and 100.
  - Activation functions included both `relu` (Rectified Linear Unit) and `tanh` to explore non-linearities in the data.

- **Were You Able to Achieve the Target Model Performance?**
  - Despite multiple optimization attempts, the target accuracy of 75% was not achieved. The highest accuracy obtained was **72.99%** in the combined model.

- **Steps Taken to Increase Model Performance**:
  - Increased the number of neurons and layers to capture more complex patterns in the data.
  - Tried different activation functions (`relu` and `tanh`).
  - Added `Dropout` layers to reduce overfitting.
  - Adjusted the number of epochs and batch size for more extensive training.
  - Experimented with feature engineering and used scaling and binning to optimize the input data.

**Model Summary** (`images/model_summary.png`):
   - A screenshot of the model summary displaying the architecture of the final combined model (neurons, layers, and activation functions).

**Training Output** (`images/training_output.png`):
   - A screenshot showing the training output, including loss and accuracy at the final epoch.

**Evaluation Output** (`images/evaluation_output.png`):
   - A screenshot of the model evaluation on the test data, showing the final loss and accuracy.

---

## Summary

While the deep learning model was not able to meet the 75% target accuracy, it performed consistently around **72-73%** across various optimization attempts. For future improvements, I recommend exploring other machine learning models like **Gradient Boosting**, **XGBoost**, or **LightGBM**, which are often well-suited for tabular data and may achieve better performance.


