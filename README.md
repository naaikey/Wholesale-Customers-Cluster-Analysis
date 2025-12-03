# Wholesale Customers Dataset - Cluster Analysis

**Author:** Nikhilesh Kumar  
**Email:** nikhileshkumar97@gmail.com

---

## Overview

This project analyzes a wholesale customer dataset to identify distinct customer segments based on their annual spending patterns across various product categories. The primary goal is to describe the variation in different customer types to equip the distributor with actionable insights for optimizing delivery services, inventory management, and business strategies.

---

## The Dataset

The dataset contains data on various customers' annual spending amounts (reported in monetary units) for the following product categories:

- **Fresh:** Fruits, vegetables, etc.
- **Milk:** Milk products.
- **Grocery:** Grocery items.
- **Frozen:** Frozen goods.
- **Detergents_Paper:** Detergents and paper products.
- **Delicassen:** Meats, cheeses, etc.
- **Channel:** Sales channel (e.g., Retail, Horeca).
- **Region:** Customer region (e.g., Lisbon, Oporto).

---

## Analysis Approach

The project follows a structured unsupervised learning workflow to segment the customers:

### Data Preprocessing
- **Feature Scaling:** A natural logarithm transformation was applied to normalize skewed spending distributions.
- **Outlier Detection:** Outliers were detected and removed to ensure robust analysis.

### Dimensionality Reduction
- **Principal Component Analysis (PCA):** PCA was applied to the preprocessed data to reduce dimensionality and reveal underlying spending patterns. The first two dimensions captured the most significant variance.

### Clustering
- **Gaussian Mixture Model (GMM):** GMM was employed for clustering.
- **Model Selection:** A silhouette score analysis indicated that two distinct customer segments provided the optimal clustering structure (Silhouette Score: ~0.42).

---

## Key Findings: Customer Segments

The analysis identified two primary customer segments with distinct behaviors:

### Cluster 0: "Staple Goods Bulk Purchasers"
- **Spending Profile:** Significantly higher annual spending on Milk, Grocery, and Detergents_Paper. Spending on Fresh and Frozen products is comparatively lower.
- **Demographics:** Predominantly composed of Channel 2 (Horeca) customers (Hotels/Restaurants/Cafes), with a strong presence in Region 3 (Lisbon) and Region 1 (Oporto).
- **Interpretation:** These likely represent large establishments such as hotels, restaurants, or supermarkets requiring a steady supply of staple and cleaning goods.

### Cluster 1: "Fresh & Frozen Specialists"
- **Spending Profile:** Distinguished by significantly higher spending on Fresh and Frozen products. Expenditure on Milk, Grocery, and Detergents_Paper is considerably lower.
- **Demographics:** Primarily consists of Channel 1 (Retail) customers, also concentrated in Region 3 (Lisbon) and Region 1 (Oporto).
- **Interpretation:** This segment likely includes specialized food stores, markets, or smaller retail outlets focusing on fresh produce and frozen items.

---

## Business Implications & Recommendations

The identification of these segments allows the distributor to move away from a "one-size-fits-all" strategy:

- **Tailored Marketing:** Develop targeted campaigns (e.g., bulk discounts on staples for Cluster 0 vs. emphasis on freshness/quality for Cluster 1).
- **Optimized Inventory:** Align stock levels with the specific high-demand categories of each cluster.
- **Differentiated Logistics:** Customize delivery schedules and vehicles (e.g., temperature-controlled transport for Cluster 1, larger volume trucks for Cluster 0) to improve efficiency.
- **Strategic Growth:** Focus acquisition efforts on businesses that align with the most profitable segments.

---

## Future Work

Potential extensions to this analysis include:
- **Time-Series Analysis:** Using historical data to predict future demand and seasonal fluctuations (e.g., ARIMA, Prophet).
- **Advanced Clustering:** Applying DBSCAN to handle noise better or Hierarchical Clustering for a dendrogram view of segmentation.
- **Churn Prediction:** Building classification models to identify customers at risk of leaving.
- **Association Rule Mining:** Analyzing purchase baskets (e.g., Apriori algorithm) to uncover cross-selling opportunities.

---
