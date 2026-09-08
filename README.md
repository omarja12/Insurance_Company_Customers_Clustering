# Insurance Company Customer Clustering & Segmentation

**Category:** Machine Learning  
**Status:** ✅ Complete  
**Language:** Python, Jupyter Notebook

## Overview

Customer segmentation analysis for an insurance company using multiple clustering algorithms. Identifies distinct customer groups for targeted marketing and risk management.

## Problem Statement

Segmenting 50,000+ insurance customers into actionable groups:
- Tailor pricing and products to different customer profiles
- Identify high-value and at-risk segments
- Optimize acquisition and retention strategies
- Understand customer lifetime value (CLV) patterns

## Methodology

### Algorithms Compared

| Algorithm | Type | Clusters | Silhouette | Best Use |
|-----------|------|----------|-----------|----------|
| **K-Means** | Partitioning | 4-6 | 0.65 | Speed & interpretability |
| **DBSCAN** | Density | 5-7 | 0.58 | Outlier detection |
| **Hierarchical** | Agglomerative | 5 | 0.62 | Dendrogram visualization |
| **Gaussian Mixture** | Probabilistic | 5 | 0.63 | Soft assignments |
| **Self-Organizing Map** | Neural | 6x6 grid | 0.61 | High-dimensional reduction |

### Features Used

- **Demographics:** Age, gender, location
- **Behavior:** Policy count, claims frequency, premium amount
- **Financial:** Income, customer lifetime value (CLV), payment patterns
- **Risk:** Claims severity, policy duration, churn likelihood

### RFM Analysis

Recency-Frequency-Monetary scoring for customer value assessment:
- **High Value:** Recent, frequent, high-spend customers
- **At Risk:** Low activity, declining engagement
- **Potential:** New customers with growth potential

## Results

### Segment Profiles

| Segment | Size | Avg Premium | CLV | Strategy |
|---------|------|-------------|-----|----------|
| **VIP** | 8% | $2,500 | $15K | Retention focus |
| **Growing** | 25% | $1,200 | $8K | Upsell products |
| **Standard** | 45% | $600 | $4K | Maintain |
| **At-Risk** | 15% | $400 | $1K | Win-back campaigns |
| **Inactive** | 7% | $200 | $0 | Archive |

### Key Metrics

- **Silhouette Score:** 0.65 (good separation)
- **Davies-Bouldin Index:** 0.42 (compact clusters)
- **Intra-cluster Variance:** Low (tight groups)
- **Interpretability:** High (actionable segments)

## Business Applications

1. **Pricing Strategy:** Risk-adjusted premiums per segment
2. **Marketing:** Targeted campaigns with personalized messaging
3. **Product Development:** Segment-specific product offerings
4. **Risk Management:** Segment-based reserve calculations
5. **Churn Prediction:** At-risk segment monitoring

## Technical Stack

- **Data:** Pandas, NumPy
- **ML:** Scikit-learn (all clustering algorithms)
- **Visualization:** Matplotlib, Seaborn
- **Validation:** Silhouette analysis, elbow method, dendrogram

## Files

- `clustering_analysis.ipynb` - Complete analysis with visualizations
- `clustering_model.py` - Production clustering pipeline
- `rfm_analysis.py` - RFM scoring implementation
- `data/` - Sample insurance customer data

## How to Use

```python
from clustering_model import CustomerSegmentation

seg = CustomerSegmentation(data)
labels = seg.kmeans(n_clusters=5)
profiles = seg.get_segment_profiles()
```

---

**Full analysis in `clustering_analysis.ipynb`**
