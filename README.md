Executive Summary:  I analyzed 119k+ Brazilian e-commerce orders in order to segment 96k+ unique customers into actionable marketing groups, helping the Brazilian firm "Olist" to optimize retention spend and identify high-value users.

Key insights from the exploratory data analysis:
- the Brazilian seller_state "SP" and the seller_city "Sao Paulo" are by far the most frequent. Sao Paulo is also the most frequent customer city, followed by Rio de Janeiro and "SP" is also the most frequent customer_state


Key insights from the RFM analysis:
- both frequency and monetary are very skewed and exhibit a heavy tails distribution. This means that in the tails of the distribution, very few customers spend a lot more than average and purchase more frequently than just once
- more than 75% of customers didn't make more than one purchase and the max number of purchases by a unique customer is 17.
- 50% of customers haven't made a purchase for 269 days or ~9 months as of October 18, 2018 (the last transaction in the data set)

Key insights from the cluster analysis:


Visualizations: 
![Alt Text](images/heatmap_relimp_segments.png)

![Alt Text](images/customersegment_pct_piechart.png)

Tables: 
[Summary Statistics on the preprocessed RFM data](tables/rfm_df_summarystats.csv)
[Summary Statistics on the 6 generated customer segments](tables/cluster_analysis.csv)



Strategic recommendations:
- a local warehouse in Sao Paulo or at least in the state "SP" makes sense logistically
- a "win-back" campaign would be in order to act on the insight that 50% of customers have been "hibernating", i.e. they haven't made a purchase in 9 months or more.
