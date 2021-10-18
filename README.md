### Hey! I'm Andrew. Welcome to my [Github] 👋

## RFM Customer Segmentation in Python and Data Visualization in Tableau

- 📊 Data visualization is my forte. See my [Tableau] page! 
- 🚀 Most of what you see here is Tableau, Python, and Figma
- 🧠 I'm interested in how our social climate and media trends influence marketing needs
- ⛳ A nice quote: "If it's worth doing, it's worth doing well"

This readme includes various screenshots, but you can see the actual [dashboard] here.
![](Dashboard_Screenshots/central_overview.png)

## Approach
1. The dataset required basic data cleaning and restructuring via Python. RFM modeling was done by manually assigning customer loyalty groups to various combinations of R/F/M values ranked from 1-4 (4 being the highest).
2. The dashboard was designed in Figma and built in Tableau. It includes the aforementioned loyalty groups as well as a visualization detailing k-means clustering.
3. Insights were derived from various graphs in the dashboard and noted in both the **data insights** section of this readme, and the tooltips within the dashboard's sidebar.

## Customer Segmentation and RFM Modeling

The dashboard displays a scatter plot of k-means clusters at the level of Customer-ID. K-means aside, we've also used a segmentation model to categorize our customers into various "loyalty" segments.

| Loyalty | Requirement | Score e.g. | Description |
| :--------- | :--------- | :--------- | :--------- |
| **Platinum** | All scores = 4 | 444 | highest-scoring, most loyal customers
| **Gold** | All scores >= 3 | 333, 344 | very loyal, second only to Platinum
| **Silver** | Moderate R/F/M | 133, 324 | represents the dependable majority
| **New** | High R; Low M | 411, 431 | made their first purchase recently, or their first purchase in a very long time
| **High-Spend** | High M; Low R/F | 113, 214 | top 25% of sales, large purchases but very infrequent, not considered loyal
| **Churn Risk** | Moderate M/F; Low R | 122, 133 | no recent purchases, at risk of defecting to competition
| **Churning** | Low R/F/M | 111, 112 | lowest RFM values, likely receptive to competitor-focused targeting

![](Dashboard_Screenshots/loyalty_groups.png)



## Data Insights

**High-Spend Corporate Tech**

Initially, it was assumed that many High-Spend customers were one-off bargain-shoppers. 
After reviewing our data, we arrived at a different conclusion. 

- The average discount of High-Spend customers was well below the mean: 13.88% < 15.75%. 

- It was more than just promotions that attracted these customers.

- High-Spend customers strongly preferred Corporate and Consumer Tech products over other categories and segments. Corporate customers likely came became one-time purchasers when outfitting their properties with our products. This knowledge will give us the precision to target these customers more successfully.
![](Dashboard_Screenshots/kpi_grid.png)


**Grouping and Clustering**

- These graphs aim to give perspective to the varying loyalty groups as we compare and contrast them. 
Similar to RFM scores, clusters are graded on an increasing scale from 1-4..

- Silver and Gold are the most influential groups with regards to total profit.
Platinum and High-Spend are the most valuable per customer.

- K-means clustering displays the variance within groups and where they overlap. 

- Parts of High-Spend, Silver and Churn Risk all belong to Cluster 3 (hover to see tooltip) - our model interprets each group to be statistically similar to a certain degree. With proper targeting, Silver is a group we'd aim to grow and maintain. A future comparison will ideally show the "fringe" customers of High-Spend and Churn Risk to have ultimately moved into the Silver group. 

![](Dashboard_Screenshots/kmeans_clustering.png)
![](Dashboard_Screenshots/highspend_cust.png)

![](Dashboard_Screenshots/rfm_matrix.png)
![](Dashboard_Screenshots/rfm_scoring_key.png)
![](Dashboard_Screenshots/sales_distribution.png)
![](Dashboard_Screenshots/segment_details.png)
![](Dashboard_Screenshots/ternary_graph.png)








</details>

[Tableau]: https://public.tableau.com/app/profile/andrew.bruening
[Github]: https://github.com/andrewbruening 
[dashboard]: https://public.tableau.com/app/profile/andrew.bruening/viz/SampleSuperstoreRFMCustomerSegmentation/CentralDB