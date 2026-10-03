# Clustering an Insurance Company's Customers

A 2022 coursework notebook that segments the customers of an insurance company with several clustering methods.

**This repository is archived.** The notebook is kept unchanged as a dated record of the original work. It has known defects (listed below).

## What the notebook does

It clusters customers described by demographic and value variables (for example age, income, customer lifetime value and years as a customer). The data has 10,296 rows, and 6,592 remain after outlier removal. The methods are K-Means, hierarchical clustering, a Gaussian mixture model, a self-organising map (50 x 50) and DBSCAN. DBSCAN found a single cluster. The best silhouette score is 0.218.

## Known issues

- The silhouette plots are shifted by one value of k, so the chosen k does not match the plotted peak.
- The cluster R-squared values include the label column, and for the SOM also the best-matching-unit index. This inflates them.
- The t-SNE plots were fitted with the cluster label as a feature, so the separation they show is circular.
- The number of outliers printed in the notebook (258) does not match the number of rows actually dropped (3,393).
- The notebook was written against 2022 library versions and may not run unchanged today.

Earlier versions of this README described results (for example 50,000 customers and higher silhouette scores) that the notebook does not produce. This README replaces them.
