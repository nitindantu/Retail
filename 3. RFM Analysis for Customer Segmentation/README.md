# Segmentation based on RFM Score
RFM segmentation model is very insightful and a powerful tool to understand your customer.
We first compute our customer’s individual recency, frequency, and monetary value, then their separate r_score, f_score, and m_score, and finally an aggregated rfm-score. We also keep the elementwise rfm-scores.
Now, depending on the business requirements we can divide the customer base in whichever way we want. However, for simplicity, we are going to divide our customer base into 3 segments based on the aggregated rfm-score and assign a loyalty badge (Platinum, Gold, Silver):
Segment 1 (Platinum): first 33%
Segment 2 (Gold): 33% — 66%
Segment 3 (Silver): last 33%

![image](https://github.com/nitindantu/Retail/assets/41870240/f1e7cf26-85f3-4d2b-b9f5-35902cb7a12c)

we observe the recency-vs-monetary and recency-vs-frequency charts, a clear contrast can be observed between our Platinum and Silver customers. It looks like Platinum customers tend to shop more frequently and spend more than others (which is great). And perhaps Silver customers likely to have lost interest in shopping with us. They shop less often and spend less (which is not so great). But, the Gold customers are in the middle and looks like there has been more activity among the Gold customers recently.

So, the takeaway from the analysis can be that we need to think about how we can continue satisfying our Platinum customers to continue shopping with us. And we also might have to think about how we can influence our Gold customers to increase engagement with us. And it might be too late to pursue those Silver users.

