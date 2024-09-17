# Global-Ecommerce-Retail-Trends-Analysis

## Overview

This project involves analyzing global e-commerce trends and their impact on traditional retail. The analysis includes data preprocessing, outlier detection, Principal Component Analysis (PCA), Customer Lifetime Value (CLV) calculation, and a What-if analysis to simulate the effect of different pricing strategies.

## Files Included

1. **Datasets:**
   - `1.csv`, `2.csv`, `3.csv`: Raw e-commerce and retail datasets containing information about sales, customer transactions, and more.
   - `tashi.csv`: A combined and preprocessed dataset that merges `1.csv`, `2.csv`, and `3.csv`.
   - `pca_transformed_data.csv`: Dataset after applying PCA for dimensionality reduction.

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
- **Visualizations:** 
  - Scatter plot of the first two principal components.
  - Heatmap and boxplots to visualize PCA results.

### 3. Customer Lifetime Value (CLV)
- **CLV Calculation:** CLV was calculated for each customer based on average purchase value, purchase frequency, and retention rate.
- **CLV Visualization:** 
  - Boxplots and violin plots were used to visualize CLV across different customer segments.
  - A heatmap of average CLV across customer segments was generated.

### 4. What-If Analysis
- **Price Change Simulations:** The effect of different price changes on CLV was simulated by modifying the `UnitPrice` variable. The results were visualized using line plots and histograms.
- **Visualization of Impact:** Line plots and heatmaps were created to illustrate the impact of different `UnitPrice` multipliers on CLV and total sales.

## Running the Notebook

1. Open the Jupyter notebook `22i-2041_Tashfeen_D_A1.ipynb` in any Jupyter environment (e.g., JupyterLab, Google Colab).
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

## License

This project is licensed under [Your Preferred License].
