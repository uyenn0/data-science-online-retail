# Data Science Project: Online retail Industry

## Topic

K-Means Clustering for Customer Segmentation for a online-retail company

Context : The company is a UK-based, solely online retail company, and the data ranges from 01/12/2009 to 09/12/2011. The company focuses on selling special occasions gifts, and a good chunk of their customers are wholesalers


## Skills Applied:
- EDA: Retain 77% of cleaned data and applicable data for clustering, while using the other 23% data for outlier analysis, thus maintained most data for the company
- Feature Engineering: Construct
    1. MonetaryValue: How much a customer has spent, across the sum of their orders
    2. Frequency: Use InvoiceDate to count how many times they have placed an order
    3. Recency: Use InvoiceDate to check the last time a customer placed their purchase

  These three features, once combined, helped with paiting a clear image of different types of customers within this company.

- K-Means Clustering: Identified 4 groups of customers

- Outliers Detection: identified overlapped customers in their Spending Capacity, and their Frequency of Purchase

## Insights

**1.**  **4285 unqiue customes** out of **406309** cleaned entries.

**2.** Identified 3 groups in need for immediate attention, and compatible marketing/attracting campagain: 

    - DELIGHT: Customers with high spending capacity and high frequency, and have interacted with the company recently.
    
        >> VIP Customers who drive the major impact within the company's financial growth, should be introduced with tailored services, can reward them with exclusive offers.
        
    - RE-ENGAGE: Customers who have not interacted with the company very recently, low in spending and low freq, but second highest number of customers within this group.
        
        >> Conduct: Investigation to see if any specific product the company has stopped selling that these customers may have bought, as this might be the reason the company loses these customers.

    - ENGAGE: Largest group of customers (~30%), also have low spending capacity and low frequency behaviours

        >> Also need investigation to see why this is the case

    
**3.** Using K-Means clustering, there are 4 significant group of customers that the company should focus their Marketing Campaigns upon, ideally in a strategic way tailoring to their purchase behaviours.


- Group 1 (Blue cluster): **"Retain"**

  - Characteristics: Relatively spent high amount of money, and spent very regularly, but those purchases are not always recent

  - Action: Encourage them to be active again with the client, i.e go in depth into what section of goods they have bought, has the client got rid of such items, or any other reasons that could have impacted their purchase
 
- Group 2 (Orange cluster): **"Engage"**
 
  - Characteristics: These are customers who interacted with the brand very recently, hence explaining their fairly low level spending , also have low frequency (mostly 1 or 2 times).

  - Action: Run more ad campaigns to remind them of the brand, send out mails or text messages asking for their feedbacks, etc.

- Group 3 (Green cluster): **"Reward"**
 
  - Characteristics: These customers are loyal to the brand, spent the highest amount and spent very regularly, but have not interacted with the brand recently.

  - Action: Should start rewarding scheme immediately to draw back their attention, as these are the customers who drive the big part of the company financial growth.
    
        Could also run customer in-depth analysis to see why they have stopped purchasing recently

- Group 4 (Red cluster): **"Re-engage"**
 
  - Characteristics: This group has the pattern of : low spending, low frequency, and have not purchased recently.

  - Action: Start running marketing ads to gain their attention, but could consider cutting this group to save cost. 



| Results |
|:-------------------------:|
|<img width="1604" alt="screen" src="assets/Cluster - kmeans.png">|

#### Why K-Means Clustering
Relied on randomly initialsed centroids, K-Means Clustering method looks for the stationary states of centroids where each distance vectors of points within the cluster, to its centroid, is minimised, while that of other centroids, is maximised

To: further confirm the number of clusters, i.e 4 cluster in this context, 'silhouette scores' are computed to compare the level of overlapping of clusters, between choosing 4, or 5 clusters. If the level of overlapping is high, clusters are not really distinct from each other, thus not creating a clear characteristic of customers behaviours.
