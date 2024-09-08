# Volume_Pip_Correlation
Trading Volume and Average Pip Movement Analysis
Introduction
This project explores the relationship between trading volume and average pip movements across different market sessions. The analysis employs various statistical and similarity metrics to understand how trading volume influences price movements in financial markets. Key metrics analyzed include Pearson correlation, Spearman's rank correlation, Kendall’s Tau, Cosine Similarity, Euclidean Distance, and Manhattan Distance.

Project Workflow
1. Data Preparation
The initial step involves collecting and preparing data for analysis. For this research:

Data Source: Historical price and volume data were fetched using the yfinance library, which retrieves data directly from Yahoo Finance.
Data Cleaning: The dataset was cleaned by removing any rows with zero volume or missing data to ensure the analysis is based on valid entries.
Session Classification: A custom function was created to classify each time entry into corresponding market sessions (e.g., Asian, London, NYC) based on the time of day.
2. Exploratory Data Analysis (EDA)
The next step is to perform an EDA to understand the data and identify any patterns or trends:

Volume Analysis: The dataset was filtered to include only periods where the trading volume was higher than the mean volume. This helps focus on significant market activities.
Average Pip Calculation: The average pip movement for each session was calculated using the difference between the average high and low prices.
3. Visualization
Visualizations were created to represent the data and metrics more intuitively:

Bar Charts: Using seaborn and matplotlib, bar charts were plotted to visualize the count of high-volume periods across different market sessions and the corresponding average pip moves.
Dual-Axis Plots: A dual-axis plot was used to simultaneously visualize the volume count and average pip move for each market session, providing a comprehensive view of their relationship.
4. Correlation and Similarity Analysis
To assess the relationships between trading volume and average pip movement, several statistical and similarity metrics were computed:

Pearson Correlation: Measures the linear relationship between Count (trading volume) and Average_Pip (pip movement). A value of 0.90 indicates a strong positive linear correlation.

Spearman's Rank Correlation: Captures monotonic relationships. With a correlation of 0.90, it confirms a strong positive relationship even if it isn't strictly linear.

Kendall’s Tau: This metric measures ordinal association strength between the variables. A value of 0.80 indicates a strong correlation based on ranking order.

Cosine Similarity: Assesses the similarity in directional patterns between volume and price movement vectors. A value of 0.99 indicates almost identical directional movement patterns.

Euclidean Distance: Provides the straight-line distance between Count and Average_Pip, measuring absolute differences.

Manhattan Distance: Computes the grid-like distance between the two variables, giving insight into the total deviation across all data points.

5. Results Interpretation
Each metric helps us understand the relationship between trading volume and pip movements in different ways:

Strong Positive Correlations: Both Pearson and Spearman correlations highlight a strong relationship, suggesting that as trading volume increases, pip movements also tend to increase.

Pattern Alignment: The high cosine similarity value shows that the changes in trading volume and pip movements are nearly identical in direction.

Distance Measures: The Euclidean and Manhattan distances provide an understanding of how far apart the volume and pip movements are in absolute terms, indicating significant deviations despite strong correlations.

6. Conclusion
This analysis demonstrates a robust and consistent relationship between trading volume and price movement across different market sessions. The findings could be useful for traders and analysts to predict price movements based on observed trading volumes. By leveraging various statistical and similarity metrics, the study provides a comprehensive understanding of how these two variables interact in financial markets.

How to Run the Analysis
Install the Required Libraries:

bash
Copy code
pip install pandas matplotlib seaborn yfinance scipy scikit-learn
Run the Data Preparation and Analysis Scripts:

Execute the Python script to fetch data, clean it, classify sessions, and compute metrics.
Generate Visualizations:

The script will produce visualizations using matplotlib and seaborn for a better understanding of the relationships.
Future Work
Incorporate More Advanced Metrics: Consider using Jaccard similarity or Mutual Information for a more nuanced analysis.
Extend Analysis to Other Assets: Expand the analysis to include multiple assets and compare their behaviors.
Apply Machine Learning Models: Utilize predictive models to forecast price movements based on trading volume and other features.
