# Network Traffic Data Analysis

A Python-based data analysis project focused on exploring and comparing normal and attack network traffic using statistical analysis and data visualization.

## Project Overview

This project analyzes a network intrusion detection dataset containing network flow records labeled as Normal Traffic and Attack traffic. The analysis focuses on understanding the dataset, cleaning and preparing the data, exploring important traffic features, visualizing patterns, and testing whether there is a statistically significant difference between the two traffic classes.

## Objectives

- Understand the structure of the network traffic dataset
- Select relevant network traffic features
- Remove missing values and duplicate records
- Rename traffic labels for easier interpretation
- Calculate descriptive statistics
- Analyze correlations between numerical features
- Visualize traffic patterns
- Remove outliers using the IQR method
- Compare Normal Traffic and Attack traffic
- Perform hypothesis testing on Flow Duration

## Technologies Used

- Python
- Pandas
- Matplotlib
- Seaborn
- SciPy
- Jupyter Notebook
- Statistical Analysis

## Dataset

The dataset used in this project is:

`ids.csv`

It contains network flow information such as:

- Destination Port
- Flow Duration
- Total Forward Packets
- Total Backward Packets
- Packet Length Mean
- Flow Bytes/s
- Flow Packets/s
- Active Mean
- Idle Mean
- Label

The original traffic labels were renamed from:

- `BENIGN` → `Normal Traffic`
- `Infiltration` → `Attack`

## Data Preparation

The dataset was prepared by:

- Selecting the required columns
- Checking data types
- Removing missing values
- Removing duplicate records
- Renaming traffic labels
- Keeping numerical features ready for statistical analysis

## Data Analysis

Descriptive statistics were calculated for selected variables including:

- Flow Duration
- Packet Length Mean

The analysis included:

- Sum
- Mean
- Standard deviation
- Skewness
- Kurtosis

Correlation analysis was also performed across numerical variables.

A correlation heatmap was created using Seaborn to identify strong relationships between network traffic features.

The strongest correlations were mainly found between packet-size-related features.

## Data Exploration

Several visualizations were created to compare Normal Traffic and Attack traffic, including:

- Bar chart for traffic class frequency
- Pie chart for average Flow Duration
- Pie chart for average Packet Length Mean
- Correlation heatmap
- Boxplot for Forward Packet Length Mean

The dataset showed more Normal Traffic records than Attack records.

## Outlier Removal

Outliers from `Fwd Packet Length Mean` were removed using the Interquartile Range (IQR) method before creating the final boxplot.

This made the comparison between Normal Traffic and Attack traffic easier to interpret.

## Hypothesis Testing

An independent statistical t-test was performed to determine whether there was a significant difference in mean Flow Duration between Normal Traffic and Attack traffic.

### Null Hypothesis

There is no significant difference in mean Flow Duration between Normal Traffic and Attack traffic.

### Alternative Hypothesis

There is a significant difference in mean Flow Duration between Normal Traffic and Attack traffic.

The resulting p-value was less than `0.05`, so the null hypothesis was rejected.

This indicates that there is a statistically significant difference in mean Flow Duration between Normal Traffic and Attack traffic.

## Project Files

- `24046876 Code.ipynb` - Jupyter Notebook containing the complete analysis
- `ids.csv` - Network traffic dataset
- `24046876_SantoshShrestha(1).pdf` - Coursework report containing explanation, analysis, screenshots, and results

## How to Run

1. Download or clone the repository.
2. Make sure Python and Jupyter Notebook are installed.
3. Install the required libraries:

```bash
pip install pandas matplotlib seaborn scipy
Keep ids.csv in the same directory as the notebook.
Open the notebook:
jupyter notebook
Open 24046876 Code.ipynb.
Run the cells from top to bottom.
Conclusion

The project successfully cleaned, explored, and analyzed the network traffic dataset. The analysis identified relationships between important traffic features and showed measurable differences between Normal Traffic and Attack traffic.

The hypothesis test also showed that Flow Duration differs significantly between the two traffic classes, suggesting that it may be a useful feature for future intrusion detection or classification tasks.

Author

Santosh Shrestha
