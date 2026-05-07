**Executive Summary**:  I analyzed 119k+ Brazilian e-commerce orders in order to segment 96k+ unique customers into actionable marketing groups, helping the Brazilian firm "Olist" to optimize retention spend and identify high-value users. First, I merged the 7 separate data sets using key columns, then I created histograms on the numeric features and top10-category-countplots for the categorical features to obtain first insights. Thereafter, I created a separate array with numerical values that represent the 3 dimensions of a Recency-Frequency-Monetary (RFM) model that is commonly used in order to segment unique customers by means of the unsupervised k-means algorithm using 6 centroids. The number of clusters was chose by applying the Elbow method. Recency describes the number of days that have passed since the last purchase compared to a reference data (Oct 18, 2018). Frequency refers to the number of purchases made and Monetary refers to the sum of price and freight value per unique customer. After running the algorithm, I analyzed the clusters and labeled them accordingly. The customer segments of interest are as follows: low value customers, loyal customers, recent users, best customers, new customers and slipping customers.

**Key insights from the exploratory data analysis**:
- the Brazilian seller_state "SP" and the seller_city "Sao Paulo" are by far the most frequent. Sao Paulo is also the most frequent customer city, followed by Rio de Janeiro and "SP" is also the most frequent customer_state


**Key insights from the RFM analysis**:
- both frequency and monetary are very skewed and exhibit a heavy tails distribution. This means that in the tails of the distribution, very few customers spend a lot more than average and purchase more frequently than just once
- more than 75% of customers didn't make more than one purchase and the max number of purchases by a unique customer is 17.
- 50% of customers haven't made a purchase for 269 days or ~9 months as of October 18, 2018 (the last transaction in the data set)

**Key insights from the cluster analysis**:
- approximately 3,000 customers (3%) fall into the "best customers" segment, which is characterized by the highest frequency values and the second highest monetary values.
- 18,000 customers (19%) can be considered "low value" from a business lens due to the fact that this segment exhibits high recency values (last purchase occured long ago) and low monetary values.
- About 22,500 customers (23%) are slipping away according to this analysis since customers in this segment tend to spend the second lowest amount of money and they tend to range in the second lowest recency value range (they purchased recently).
- 11,400 customers (12%) can be considered as loyal customers. The latter segment is characterized by the highest monetary values combined with a moderate recency.
  

**Visualizations**:   
![Alt Text](images/heatmap_relimp_segments.png)  

![Alt Text](images/countplot_customercity.png)

![Alt Text](images/customersegment_pct_piechart.png)

**Tables**:   
[Summary Statistics on the preprocessed RFM data](tables/rfm_df_summarystats.csv)  

[Summary Statistics on the 6 generated customer segments](tables/cluster_analysis.csv)



**Strategic recommendations**:
- a local warehouse in Sao Paulo or at least in the state "SP" makes sense logistically
- a "win-back" campaign would be in order to act on the insight that 50% of customers have been "hibernating", i.e. they haven't made a purchase in 9 months or more.
