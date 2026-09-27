# Customer Profile Identification via PCA and k-Means

This repository contains an exploratory data analysis and unsupervised machine learning pipeline applied to the YPS dataset focused on identifying distinct behavioral profiles.

---

## Introduction

* Implemented Principal Component Analysis (PCA) on the YPS dataset to extract 5 dominant behavioral dimensions, mapping orthogonal eigenvectors to maximize feature interpretability.
* Segmented profiles into 4 distinct target clusters using k-Means; evaluated clustering quality and internal cohesion via detailed Silhouette Score analysis across sub-segments.

--- 

## Algorithm Overview

1. **Preprocessing & Encoding:** 
    Handled missing values, applied **Ordinal Encoder** to ordered categorical features, and rescaled numerical features using **MinMaxScaler** to preserve the relative structure within the $[0, 1]$.

2. **Variance & PCA Analysis:** 
    Evaluated feature variances before and after scaling and analyzed cumulative explained variance curves to assess the impact of features.

3. **Dimensionality Reduction & Interpretation:** 
    Extracted $m=5$ principal components to capture key behavioral traits, interpreted through component loadings.

4. **k-Means Clustering & Silhouette Analysis:** 
    Determined the optimal number of clusters ($k = 4$) using Silhouette Score evaluations ($k \in [3, 10]$), visualizing score graphs and interpreting cluster centroids via principal components.

5. **External & Internal Evaluations:** 
    Evaluated clusters externally using demographic labels (*Gender* and *Weight*) and internally via Silhouette scores to measure cohesion.

