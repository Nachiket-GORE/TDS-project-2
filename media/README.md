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
- **Cluster Centers**: [[-0.06434370795764555, -0.08610627532926161, -0.17106239959567054], [-1.4439319768746028, -1.2683177907764138, -0.7004899986932008], [1.176547904849255, 1.0840497493094705, 0.8099159619324358]]
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

## Overview of the Data

The analyzed dataset comprises **2,652** records and **8** columns, with data types including timestamps, categorical data, and quantitative metrics. The primary columns are as follows:

- `date`: representing date and time (datetime64[ns])
- `language`: categorical data indicating the language (object)
- `type`: categorical data describing the type (object)
- `title`: categorical data for titles (object)
- `by`: categorical data representing the author (object)
- `overall`: numeric rating (float64)
- `quality`: numeric quality assessment (float64)
- `repeatability`: numeric measure of repeatability (float64)

The dataset contains **99 missing values** in the `date` column, while all other columns are complete.

### Numeric Summary

The numeric columns yield the following insights:

- **Date**:
  - The dataset spans from **June 18, 2005** to **November 15, 2024**.
  - The median date (50th percentile) is **December 3, 2013**.
  
- **Overall Ratings**:
  - Mean overall rating is approximately **3.05** on a scale likely ranging from **1.0 to 5.0**, indicating that most items receive moderate ratings.
  - Ratings predominantly cluster around **3.0**, with a standard deviation of **0.76**, suggesting some variability but concentrated responses.

- **Quality Ratings**:
  - Mean quality rating is roughly **3.21**.
  - Similar to overall ratings, the majority fall between **3.0** and **4.0**, indicating a trend toward moderate to high quality.
  - A standard deviation of **0.80** indicates variability in the quality ratings.

- **Repeatability**:
  - Mean repeatability is approximately **1.49**, indicating that most items are repeated at least once (most commonly rated **1**).
  - The standard deviation of **0.60** shows some variation in repeatability measures.

## Key Findings

1. **Missing Values**: The dataset contains a significant number of missing dates (99 entries), which may impact temporal analysis and trend evaluations. Further investigation is necessary to understand the reasons for these absences and how to address them effectively.

2. **Rating Distribution**: The overall and quality ratings are concentrated primarily around the values of **3** and **4**,
```

## Conclusion
The analysis provides a deep understanding of the dataset. Key findings include:

- The dataset has several missing values, which were appropriately handled during preprocessing.
- Three clusters were identified through K-Means clustering, which offer a meaningful segmentation of the data.
- Visualizations helped in identifying relationships between variables and the distribution of data across clusters.

Future improvements could involve experimenting with other clustering techniques or analyzing additional features in the dataset.

