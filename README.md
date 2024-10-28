# Global-Ecommerce-Retail-Trends-Analysis

## Overview

This project involves analyzing global e-commerce trends and their impact on traditional retail. The analysis includes data preprocessing, outlier detection, Principal Component Analysis (PCA), Customer Lifetime Value (CLV) calculation, and a What-if analysis to simulate the effect of different pricing strategies.

## Files Included

1. **Datasets:**
   - `1.csv`, `2.csv`, `3.csv`: Raw e-commerce and retail datasets containing information about sales, customer transactions, and more.
   - `tashi.csv`: A combined and preprocessed dataset that merges `1.csv`, `2.csv`, and `3.csv`. [Download](https://mega.nz/folder/GRMlHbzB#RNCqR2Wn1MwV6UkK4i-8dQ)
   - `pca_transformed_data.csv`: Dataset after applying PCA for dimensionality reduction. [Download](https://mega.nz/folder/GRMlHbzB#RNCqR2Wn1MwV6UkK4i-8dQ)


2. **Reports:**
   - `Report.pdf`: A comprehensive report detailing the analysis, visualizations, and insights.
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
  
- **Visualizations:** 
  - Scatter plot of the first two principal components.
    <img width="1100" alt="1" src="https://github.com/user-attachments/assets/1134287c-f498-45f9-a74a-30c0e39a93be">

  - Heatmap and boxplots to visualize PCA results.
    <img width="1100" alt="2" src="https://github.com/user-attachments/assets/e7756edf-af5d-49d8-85ff-5932ce6c86c8">
    <img width="1100" alt="3" src="https://github.com/user-attachments/assets/a6d3c33c-536b-4a1f-81fb-e1711a3d560b">

### 3. Customer Lifetime Value (CLV)
- **CLV Calculation:** CLV was calculated for each customer based on average purchase value, purchase frequency, and retention rate.
- **CLV Visualization:** 
  - Boxplots and violin plots were used to visualize CLV across different customer segments.
    <img width="1100" alt="5" src="https://github.com/user-attachments/assets/b3cb5426-c3f0-4f88-902b-d7119fde153f">

  - A heatmap of average CLV across customer segments was generated.
    <img width="1100" alt="6" src="https://github.com/user-attachments/assets/b316849a-93ae-480f-a9dd-1163b5101cc6">
### 4. What-If Analysis
- **Price Change Simulations:** The effect of different price changes on CLV was simulated by modifying the `UnitPrice` variable. The results were visualized using line plots and histograms.
- **Visualization of Impact:** Line plots and heatmaps were created to illustrate the impact of different `UnitPrice` multipliers on CLV and total sales.
    <img width="1100" alt="8" src="https://github.com/user-attachments/assets/2e18dec6-3889-4d51-bedc-1bc9ad3ea209">
    <img width="1100" alt="9" src="https://github.com/user-attachments/assets/6461a42e-36b8-481c-bcbd-3c7990aa5c0f">
    <img width="1100" alt="10" src="https://github.com/user-attachments/assets/f8ff3bbd-5c92-447f-a474-8f3f2a169ad0">

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
