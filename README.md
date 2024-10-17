# [Clustering and Time Series Analysis Project](https://medium.com/@sujay1829/clustering-and-time-series-analysis-with-r-a-deep-dive-into-two-case-studies-88b29799b985)

This project is divided into two main analyses:
1. **Clustering Analysis**: A project analyzing land mines data using various clustering techniques.
2. **Time Series Analysis**: A project focused on forecasting oil sales using time series models.

Each section provides in-depth analysis and insights into real-world datasets, using R for statistical computing and visualization.

## 1. Clustering Analysis

### Overview
This analysis applies unsupervised learning techniques to the **Land Mines Dataset** to identify natural groupings or clusters. The dataset consists of features representing different attributes of land mines, and the goal is to discover distinct clusters based on these attributes.

### Methodology
- **Data Preprocessing**: The dataset was cleaned and preprocessed, with features standardized to ensure meaningful distance metrics.
- **Clustering Techniques**: Several algorithms were applied to group the data:
  - **K-Means Clustering**: Identifies `k` distinct clusters by minimizing the within-cluster variance.
  - **Hierarchical Clustering**: Builds a hierarchy of clusters using an agglomerative approach, visualized via dendrograms.
  - **DBSCAN**: Density-based clustering method used to find clusters of varying shapes.
- **Evaluation**: The optimal number of clusters was chosen using the **Elbow Method** and **Silhouette Scores**.

#### Visualizations:
The following plots are used to visualize the clustering results:

![Clustering Plot](https://github.com/jayshrivastava0/Clustering-and-Time-Series-Analysis-Project/blob/main/Clustering%20Analysis/images/newplot%20(1).png)

*Figure 1: Visualization of the clusters formed using K-Means.*

![Elbow Plot (WCSS vs Number of Clusters)](https://github.com/jayshrivastava0/Clustering-and-Time-Series-Analysis-Project/blob/main/Clustering%20Analysis/images/newplot%20(2).png)

*Figure 2: Elbow plot showing the Within-Cluster Sum of Squares (WCSS) vs the number of clusters. This helps determine the optimal number of clusters.*

### Findings
The analysis revealed distinct groups within the dataset, each corresponding to different types of land mines based on their features.

### Files
- `Project 1 - Rmd.Rmd`: Contains the R code and methodology used for the clustering analysis.
- `Project-1---Rmd.html`: An HTML report generated from the R markdown file, detailing the analysis.
- `Project 1 - Report.pdf`: A PDF summary of the clustering project, including key results and visualizations.
- `mine_data.xlsx`: The dataset used in the clustering analysis.

## 2. Time Series Analysis

### Overview
The goal of this project was to analyze and forecast **oil sales** using time series data. The dataset contained historical oil sales data, and the objective was to build predictive models to forecast future sales.

### Methodology
- **Data Exploration**: Key patterns in the dataset were explored, including trend, seasonality, and autocorrelation. **ACF** and **PACF** plots were used to understand lag relationships.
  
  ![Original Data Plot with Missing Values](https://github.com/jayshrivastava0/Clustering-and-Time-Series-Analysis-Project/blob/main/Time%20Series%20Analysis/images/newplot%20(3).png)

  *Figure 3: Plot of the original oil sales data, highlighting missing values.*

- **Data Imputation**: Missing values were handled using imputation strategies. Below is a plot of the data after imputation.
  
  ![Imputed Data Plot using "up" strategy in R](https://github.com/jayshrivastava0/Clustering-and-Time-Series-Analysis-Project/blob/main/Time%20Series%20Analysis/images/newplot%20(4).png)

  *Figure 4: Data plot after imputation using the "up" strategy in R.*

- **Modeling**: Several time series models were implemented:
  - **ARIMA (AutoRegressive Integrated Moving Average)**: A statistical model used for forecasting time series data by combining autoregressive, moving average, and differencing techniques.
  - **Exponential Smoothing (ETS)**: Captures level, trend, and seasonal components in the data.
  
  ![ETS and Holt-Winters Method formula and explanation](https://github.com/jayshrivastava0/Clustering-and-Time-Series-Analysis-Project/blob/main/Time%20Series%20Analysis/images/Screenshot%202024-10-16%20192328.png)

  *Figure 5: Explanation of the ETS and Holt-Winters methods used for forecasting.*

- **Forecasting**: Forecasts were generated using ARIMA and ETS models.
  
  ![Forecasts with ARIMA(0,1,0)](https://github.com/jayshrivastava0/Clustering-and-Time-Series-Analysis-Project/blob/main/Time%20Series%20Analysis/images/Screenshot%202024-10-16%20192403.png)

  *Figure 6: Forecasts generated using ARIMA (0,1,0).*
  
  ![Forecasts with ETS(A,N,N)](https://github.com/jayshrivastava0/Clustering-and-Time-Series-Analysis-Project/blob/main/Time%20Series%20Analysis/images/Screenshot%202024-10-16%20192435.png)

  *Figure 7: Forecasts generated using ETS (A,N,N).*

### Findings
The models successfully captured the trend and seasonal components of the oil sales data, providing accurate short-term forecasts.

### Files
- `Project 2 - RMD.Rmd`: Contains the R code for the time series analysis, including data exploration, modeling, and forecasting.
- `Project-2---RMD.html`: An HTML report generated from the R markdown file, providing a detailed walkthrough of the time series analysis.
- `oil.csv`: The dataset used for time series analysis.

## How to Use
1. **Clone the repository**: Download the project files to your local machine.
2. **Open the R markdown files**: Use RStudio or any compatible editor to view and run the R markdown files (`.Rmd`).
3. **View the reports**: You can directly view the HTML and PDF reports for each analysis to see the detailed results and visualizations.

## Technology Stack
- **R**: The analysis was performed using the R programming language, leveraging its powerful libraries for data manipulation and visualization.
- **R Libraries**:
  - `ggplot2` for data visualization.
  - `dplyr` for data manipulation.
  - `cluster`, `factoextra`, and `dbscan` for clustering algorithms.
  - `forecast`, `tseries`, and `stats` for time series modeling.
- **Datasets**: The project utilizes `.csv` and `.xlsx` datasets for analysis.

## License
This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.
