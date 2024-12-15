# Automated Dataset Analysis

## Overview
This repository contains an analysis of the dataset **media.csv**. The following sections describe the preprocessing steps, the analysis conducted, clustering results, visualizations, and insights derived from the data.

## Dataset Summary
The dataset consists of the following structure:

### Data Overview
- Total Rows: 2652
- Total Columns: 8
### Column Data Types
```
- date: datetime64[ns]
- language: object
- type: object
- title: object
- by: object
- overall: float64
- quality: float64
- repeatability: float64
```
### Missing Values
```
- date: 99 missing values
- language: 0 missing values
- type: 0 missing values
- title: 0 missing values
- by: 0 missing values
- overall: 0 missing values
- quality: 0 missing values
- repeatability: 0 missing values
```
### Numeric Summary
```
date:
- count: 2553
- mean: 2013-12-16 21:25:27.144535808
- min: 2005-06-18 00:00:00
- 25%: 2008-03-24 00:00:00
- 50%: 2013-12-03 00:00:00
- 75%: 2019-05-24 00:00:00
- max: 2024-11-15 00:00:00
- std: nan
overall:
- count: 2652.0
- mean: 3.0475113122171944
- min: 1.0
- 25%: 3.0
- 50%: 3.0
- 75%: 3.0
- max: 5.0
- std: 0.7621797580962717
quality:
- count: 2652.0
- mean: 3.2092760180995477
- min: 1.0
- 25%: 3.0
- 50%: 3.0
- 75%: 4.0
- max: 5.0
- std: 0.7967426636666686
repeatability:
- count: 2652.0
- mean: 1.4947209653092006
- min: 1.0
- 25%: 1.0
- 50%: 1.0
- 75%: 2.0
- max: 3.0
- std: 0.598289430580212
```

## Data Preprocessing
Before performing any analysis, several preprocessing steps were conducted to clean and prepare the data:

- **Missing Values Handling**: Missing values in categorical columns were replaced with 'Unknown'. Numeric columns had missing values imputed using the median.
- **Date Parsing**: Any columns containing dates were parsed and converted into datetime objects.
- **Standardization**: Numerical data was standardized to ensure that features are on the same scale before applying clustering algorithms.

## Clustering Analysis
To uncover patterns in the data, we performed K-Means clustering on the dataset. The number of clusters was set to 3 based on prior understanding.

### Clustering Results
- **Cluster Centers**: [[-0.06434370795764555, -0.0861062753292616, -0.17106239959567054], [-1.4439319768746026, -1.2683177907764138, -0.7004899986932007], [1.1765479048492549, 1.0840497493094705, 0.8099159619324358]]
- **Inertia (Sum of Squared Distances)**: 3053.031692241744
### Cluster Distribution
The following plot shows the distribution of data points across the clusters:

![Cluster Distribution](cluster_distribution.png)

## Visualizations
The following visualizations help in understanding the data distribution and clustering results:

### Correlation Heatmap
This heatmap displays the correlation between the numerical features in the dataset.

![Correlation Heatmap](correlation_heatmap.png)

## Narrative Summary
Below is the detailed narrative generated from the dataset analysis:

### Insights
```
# Dataset Analysis Summary

## Overview

The dataset consists of 2,652 rows and 8 columns, detailing various attributes, including timestamped data, ratings, and reviews. The primary focus seems to be on evaluating different items based on their **overall** performance, **quality**, and **repeatability**, elaborated across different **languages** and **types**. The dataset features the following attributes:

- **date**: The date when the review or rating was recorded.
- **language**: The language of the review or rating.
- **type**: The type/category of the reviewed item.
- **title**: The title of the item being reviewed.
- **by**: The author or reviewer of the item.
- **overall**: A numerical rating for the item on a scale (likely 1 to 5).
- **quality**: A numerical score representing the quality of the item.
- **repeatability**: A metric assessing how often the item can be repeated or reproduced.

## Key Findings

### Data Completeness
- **Missing Values**: The dataset contains a total of 99 missing entries in the **date** column, while other columns do not feature any missing data points. This indicates a relatively high level of completeness for most attributes, making the dataset robust for analysis.

### Date Distribution
- The **date** field spans from **June 18, 2005**, to **November 15, 2024**, with a mean date around **December 16, 2013**. The interquartile range shows that most records are concentrated between **March 24, 2008** and **May 24, 2019**.

### Ratings Overview
- **Overall Ratings**:
  - Mean: **3.05**
  - Minimum: **1.0**
  - Maximum: **5.0**
  - Distribution indicates most ratings fall around **3.0**, suggesting a tendency for average satisfaction.
  
- **Quality Ratings**:
  - Mean: **3.21**
  - Minimum: **1.0**
  - Maximum: **5.0**
  - Similar to overall ratings, the distribution suggests a tendency towards moderate quality, with an inclination beyond middle ground.

- **Repeatability Ratings**:
  - Mean: **1.49**
  - Minimum: **1.0**
  - Maximum: **3.0**
  - The low average and maximum scores
```

## Conclusion
The analysis provides a deep understanding of the dataset. Key findings include:

- The dataset has several missing values, which were appropriately handled during preprocessing.
- Three clusters were identified through K-Means clustering, which offer a meaningful segmentation of the data.
- Visualizations helped in identifying relationships between variables and the distribution of data across clusters.

Future improvements could involve experimenting with other clustering techniques or analyzing additional features in the dataset.
