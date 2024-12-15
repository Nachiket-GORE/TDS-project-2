# Automated Dataset Analysis

# Dataset Analysis Summary

## Overview of the Data

The dataset consists of **2,363 rows** and **11 columns**, capturing various societal and economic indicators for different countries over a range of years (from 2005 to 2023). The dataset includes the following columns:

- **Country name**: The name of the country.
- **Year**: The year of the data entry.
- **Life Ladder**: A measure of subjective well-being or happiness.
- **Log GDP per capita**: A logarithmic transformation of a country�s GDP per capita, which serves as an economic metric.
- **Social support**: A measure reflecting the strength of social relationships.
- **Healthy life expectancy at birth**: An estimate of the average number of years a newborn is expected to live in good health.
- **Freedom to make life choices**: A score reflecting the perceived level of freedom experienced by individuals in making life choices.
- **Generosity**: A measure indicating the level of giving behavior among citizens.
- **Perceptions of corruption**: A score reflecting how corrupt the citizens perceive their government to be.
- **Positive affect**: A measure of positive feelings and emotional health.
- **Negative affect**: A measure of negative feelings and emotional health.

### Data Quality Assessment

- **Missing Values**: The dataset appears to be clean with **no missing values** across any of the columns.
- **Column Types**: The dataset includes object and float types, with the majority being numeric indicators (float64).

## Key Findings

### Descriptive Statistics

1. **Year**:
   - Mean Year: **2014.76**
   - Range: **2005 - 2023**
   - Standard Deviation: **5.06** indicates a diverse range of years represented.

2. **Life Ladder**:
   - Mean Score: **5.48**
   - Min/Max: Ranges from **1.281** to **8.019**, indicating varying happiness levels among different countries.

3. **Log GDP per capita**:
   - Mean: **9.40**
   - Range: From **5.527** to **11.676**, showcasing diverse economic conditions across countries.

4. **Social Support**:
   - Mean Score: **0.81**
   - Range: From **0.228** to **0.987**, suggesting significant differences in social support systems in different countries.

5.

## Summary of Dataset
```
{'total_rows': 2363, 'total_columns': 11, 'column_types': {'Country name': 'object', 'year': 'float64', 'Life Ladder': 'float64', 'Log GDP per capita': 'float64', 'Social support': 'float64', 'Healthy life expectancy at birth': 'float64', 'Freedom to make life choices': 'float64', 'Generosity': 'float64', 'Perceptions of corruption': 'float64', 'Positive affect': 'float64', 'Negative affect': 'float64'}, 'missing_values': {'Country name': 0, 'year': 0, 'Life Ladder': 0, 'Log GDP per capita': 0, 'Social support': 0, 'Healthy life expectancy at birth': 0, 'Freedom to make life choices': 0, 'Generosity': 0, 'Perceptions of corruption': 0, 'Positive affect': 0, 'Negative affect': 0}, 'numeric_summary': {'year': {'count': 2363.0, 'mean': 2014.7638595006347, 'std': 5.059436468192795, 'min': 2005.0, '25%': 2011.0, '50%': 2015.0, '75%': 2019.0, 'max': 2023.0}, 'Life Ladder': {'count': 2363.0, 'mean': 5.483565806178587, 'std': 1.1255215132391925, 'min': 1.281, '25%': 4.647, '50%': 5.449, '75%': 6.3235, 'max': 8.019}, 'Log GDP per capita': {'count': 2363.0, 'mean': 9.400895471857808, 'std': 1.1452751661753888, 'min': 5.527, '25%': 8.52, '50%': 9.503, '75%': 10.382, 'max': 11.676}, 'Social support': {'count': 2363.0, 'mean': 0.8095076174354633, 'std': 0.1208920386005142, 'min': 0.228, '25%': 0.744, '50%': 0.8345, '75%': 0.904, 'max': 0.987}, 'Healthy life expectancy at birth': {'count': 2363.0, 'mean': 63.44710325856962, 'std': 6.756315797293225, 'min': 6.72, '25%': 59.545, '50%': 65.1, '75%': 68.4, 'max': 74.6}, 'Freedom to make life choices': {'count': 2363.0, 'mean': 0.7505975454930174, 'std': 0.13831425560919758, 'min': 0.228, '25%': 0.662, '50%': 0.771, '75%': 0.861, 'max': 0.985}, 'Generosity': {'count': 2363.0, 'mean': -0.000659754549301734, 'std': 0.15864720823860773, 'min': -0.34, '25%': -0.108, '50%': -0.022, '75%': 0.088, 'max': 0.7}, 'Perceptions of corruption': {'count': 2363.0, 'mean': 0.7468554803216251, 'std': 0.18032105258484032, 'min': 0.035, '25%': 0.696, '50%': 0.7985, '75%': 0.864, 'max': 0.983}, 'Positive affect': {'count': 2363.0, 'mean': 0.6519949217096911, 'std': 0.10570446303305296, 'min': 0.179, '25%': 0.573, '50%': 0.663, '75%': 0.7364999999999999, 'max': 0.884}, 'Negative affect': {'count': 2363.0, 'mean': 0.2730753279729158, 'std': 0.08684027838928515, 'min': 0.083, '25%': 0.209, '50%': 0.262, '75%': 0.326, 'max': 0.705}}}
```

## Clustering Analysis Results
```
{'inertia': 14635.997146158657, 'cluster_centers': [[0.0664523904697957, 1.322799239964082, 1.1473655500974262, 0.9214456493119507, 0.9256603349491285, 1.0592758193403473, 0.9871318717869703, -1.5416886783207255, 0.8060696592923025, -0.6978735962260308], [0.008726237108870728, 0.2886000805428054, 0.349250813879037, 0.4246885911677729, 0.39256835767788106, 0.06700341010474575, -0.3489389007563439, 0.3515516125375219, 0.12450517084398358, -0.117858065035101], [-0.0421385012153896, -0.9912344271186891, -0.9910138327263128, -0.9871915899709945, -0.9465176096907767, -0.5760570824417155, 0.008932586502320917, 0.2426450712740218, -0.5358909013248582, 0.4773125302979255]]}
```

