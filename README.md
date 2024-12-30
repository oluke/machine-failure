# Model Prediction for Machine Failure ⚙️💻

## Project Background

Machine failures are a common challenge in the manufacturing industry, leading to unexpected downtime and increased costs. Understanding and predicting machine failures is critical for improving operational efficiency and reducing expenses. With advancements in predictive maintenance, leveraging data-driven models can significantly aid in early detection and prevention of such failures.

This project focuses on developing a machine failure prediction model to assist companies in minimizing unplanned maintenance costs and optimizing their production processes. By analyzing key machine parameters, the model aims to identify potential failures before they occur, enabling better planning and resource allocation.

---

## Problem Statement

A reputable spare parts company, planning to expand, has encountered frequent machine failures. These issues result in:

- Increased operational costs due to unplanned maintenance.
- Challenges in meeting production schedules.

This project aims to:

1. Understand the primary causes of machine failures.
2. Evaluate costs associated with these failures.
3. Identify opportunities for cost savings through predictive maintenance.

---

## Goals

- **Identify Key Factors**: Determine the main contributors to machine failures.
- **Reduce Costs**: Highlight cost-saving opportunities by mitigating failures.
- **Optimize Operations**: Enhance reliability and operational efficiency through predictive modeling.

---

## Dataset

The dataset used for this project is the **AI4I 2020 Predictive Maintenance Dataset**, sourced from the UCI Machine Learning Repository.

### Data Overview:
- **Rows**: 10,000
- **Columns**: 14

### Data Dictionary:
- **UDI**: Unique identifier for each record.
- **Product ID**: Specific product identifier (e.g., L, M, H).
- **Type**: Product type (Low, Medium, High).
- **Air Temperature**: Ambient air temperature (K).
- **Process Temperature**: Process temperature (K).
- **Rotational Speed**: Machine's rotational speed (rpm).
- **Torque**: Torque exerted by the machine (Nm).
- **Tool Wear**: Tool usage duration (minutes).
- **Machine Failure**: Failure type (Tool Wear, Heat Dissipation, Power, Overstrain, Random).

For detailed dataset information, visit: [AI4I Predictive Maintenance Dataset](https://archive.ics.uci.edu/ml/datasets/AI4I+2020+Predictive+Maintenance+Dataset).

---

## Data Preprocessing

1. **Data Quality Check**:
   - No missing or duplicate values identified.

2. **Feature Engineering**:
   - Created a new feature `Power` from the product of `Torque` and `Rotational Speed`.
   - Categorical encoding for `Type`.

3. **Outlier Handling**:
   - Addressed outliers in `Rotational Speed`, `Torque`, and `Power` using Box-Cox transformation.

4. **Dataset Splitting**:
   - Training data: 75%.
   - Testing data: 25%.

5. **Standardization**:
   - Applied robust scaling for numerical features.

---

## Modeling and Evaluation

The XGBoost algorithm was selected as the final model due to its stable performance metrics.

### Performance:
- **Training F1-Score**: 99.84%
- **Testing F1-Score**: 78.83%

The model demonstrated significant cost-saving potential, reducing expenses by 3.33 times compared to traditional methods.

---

## Feature Importance

Top 5 contributing factors:
1. **Rotational Speed**
2. **Torque**
3. **Tool Wear**
4. **Power**
5. **Product Type H**

---

## Recommendations

1. **Routine Maintenance**:
   - Implement regular maintenance schedules based on predictive insights.

2. **Early Failure Detection**:
   - Monitor critical parameters to identify early signs of machine failures.

3. **Supplier Collaboration**:
   - Partner with high-quality spare parts suppliers to enhance machine reliability.

---

## Thank You 🙏

Explore more:
- [Dashboard](https://bit.ly/Dashboard_The_Game_Changers)
- [Code Repository](https://bit.ly/Coding_The_Game_Changers)

