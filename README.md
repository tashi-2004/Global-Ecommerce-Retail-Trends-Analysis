# Global-Ecommerce-Retail-Trends-Analysis

## Overview

This project involves analyzing global e-commerce trends and their impact on traditional retail. The analysis includes data preprocessing, outlier detection, Principal Component Analysis (PCA), Customer Lifetime Value (CLV) calculation, and a What-if analysis to simulate the effect of different pricing strategies.

## Files Included

1. **Datasets:**
   - `1.csv`, `2.csv`, `3.csv`: Raw e-commerce and retail datasets containing information about sales, customer transactions, and more.
   - `tashi.csv`: A combined and preprocessed dataset that merges `1.csv`, `2.csv`, and `3.csv`. [Download](https://mega.nz/folder/GRMlHbzB#RNCqR2Wn1MwV6UkK4i-8dQ)
   - `pca_transformed_data.csv`: Dataset after applying PCA for dimensionality reduction. [Download](https://mega.nz/folder/GRMlHbzB#RNCqR2Wn1MwV6UkK4i-8dQ)


2. **Reports:**
   - `report.pdf`: A comprehensive report detailing the analysis, visualizations, and insights.
   - `Pre-Processing_Insights.pdf`: A detailed document explaining the preprocessing steps taken, including outlier detection and handling missing values.

3. **Notebook:**
   - `code.ipynb`: Jupyter notebook containing Python code for data preprocessing, PCA, CLV calculation, and visualizations.

## Project Steps

### 1. Data Preprocessing
- **Data Integration:** Datasets `1.csv`, `2.csv`, and `3.csv` are combined into a single dataset `tashi.csv`.
- **Handling Missing Values:** Missing values in numerical columns were filled using the mean of each column.
- **Outlier Detection and Removal:** Outliers were detected using the Z-score method with a threshold of 2.5. These outliers were removed from the dataset.
- **Normalization:** Numerical columns were normalized using `MinMaxScaler`.
- **Label Encoding:** Categorical columns were label encoded using `LabelEncoder`.
- **Feature Creation:** 
  - `Total_Sales`: Calculated by multiplying `UnitPrice` and `Quantity`.
  - `Discount_Effectiveness`: Ratio of `discount_amount` to `Total_Sales`.
  - `Sales_per_Customer`: Sum of total sales per customer.

### 2. Dimensionality Reduction with PCA
- **Principal Component Analysis (PCA):** Applied to the normalized dataset to reduce dimensionality while retaining 80% of the variance.
  
     <img width="1000" alt="pcaaaa" src="https://github.com/user-attachments/assets/9bd6672d-39b0-4ebe-80b6-abd7517fde98">
- **Visualizations:** 
  - Scatter plot of the first two principal components.
    <img width="1016" alt="2" src="https://github.com/user-attachments/assets/45bb81f4-3343-4c1c-960f-c7492e1c534e">

  - Heatmap and boxplots to visualize PCA results.
    <img width="946" alt="23" src="https://github.com/user-attachments/assets/a683e71a-0ab3-42da-b911-5c7ab226095b">
    <img width="1022" alt="22" src="https://github.com/user-attachments/assets/760a4c63-d1af-4cb3-b055-9ac0ca06c857">

### 3. Customer Lifetime Value (CLV)
- **CLV Calculation:** CLV was calculated for each customer based on average purchase value, purchase frequency, and retention rate.
- **CLV Visualization:** 
  - Boxplots and violin plots were used to visualize CLV across different customer segments.
    <img width="1011" alt="image" src="https://github.com/user-attachments/assets/1aec4759-4764-46ec-9f15-c7c779683401">

  - A heatmap of average CLV across customer segments was generated.
    <img width="942" alt="223" src="https://github.com/user-attachments/assets/808cb868-9f09-431a-88d6-0377fe9cd303">

### 4. What-If Analysis
- **Price Change Simulations:** The effect of different price changes on CLV was simulated by modifying the `UnitPrice` variable. The results were visualized using line plots and histograms.
- **Visualization of Impact:** Line plots and heatmaps were created to illustrate the impact of different `UnitPrice` multipliers on CLV and total sales.
    <img width="1200" alt="Screenshot 2024-09-18 013304" src="https://github.com/user-attachments/assets/6d17c7c4-16c3-420f-be94-47c9119c576a">

## Running the Notebook

1. Open the Jupyter notebook `code.ipynb` in any Jupyter environment (e.g., JupyterLab, Google Colab).
2. Run the code cells in sequence to preprocess the data, apply PCA, calculate CLV, and generate the visualizations.

### Dataset Files:

- Ensure that `1.csv`, `2.csv`, and `3.csv` are available in the working directory.
- The notebook generates `tashi.csv` and `pca_transformed_data.csv` as outputs.

## Key Insights

- **Dimensionality Reduction:** PCA effectively reduced the dataset dimensions while preserving most of the data's variance.
- **CLV Segmentation:** Customer Lifetime Value was calculated and segmented, highlighting differences in customer value across groups.
- **Impact of Price Changes:** The What-if analysis demonstrated how changes in `UnitPrice` affect CLV, providing insights into potential pricing strategies.

## Visualizations

- **Scatter Plot of Principal Components:** Highlights clusters or separations in the dataset after applying PCA.
- **Boxplot of CLV Segments:** Showcases the distribution of CLV across different customer segments.
- **Violin Plot of CLV Segments:** Visualizes the density of CLV values across segments.
- **Heatmaps:** Used to display the relationship between CLV, total sales, and `UnitPrice` changes.
- **Histograms:** Demonstrate the frequency of CLV values for various price multipliers in the What-if analysis.

## Contact

For any questions or suggestions, feel free to contact at [abbasitashfeen7@gmail.com]
