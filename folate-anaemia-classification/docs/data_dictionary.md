# Data Dictionary - Folate Anaemia Classification

This document provides detailed descriptions of all variables included in the folate anaemia classification dataset. The data is designed to support machine learning models for predicting folate deficiency anaemia based on clinical and lifestyle factors.

## Variable Definitions

### Demographic Variables

**patient_id**
- **Type**: String (Categorical)
- **Description**: Unique identifier for each patient record
- **Format**: Alphanumeric (e.g., P001, P002)
- **Purpose**: Primary key for data linkage and patient tracking
- **Notes**: Anonymized identifier to protect patient privacy

**age**
- **Type**: Numeric (Integer)
- **Description**: Patient age in years at time of data collection
- **Range**: 18-80 years
- **Unit**: Years
- **Clinical Relevance**: Age affects folate metabolism and absorption; elderly patients at higher risk

**gender**
- **Type**: Categorical
- **Description**: Biological sex of the patient
- **Values**: F (Female), M (Male)
- **Clinical Relevance**: Gender differences in folate requirements, especially during pregnancy and menstruation

### Laboratory Values

**hemoglobin**
- **Type**: Numeric (Float)
- **Description**: Hemoglobin concentration in blood
- **Range**: 6.0-18.0 g/dL
- **Unit**: Grams per deciliter (g/dL)
- **Normal Range**: Female: 12.0-15.5 g/dL, Male: 13.5-17.5 g/dL
- **Clinical Relevance**: Primary indicator of anaemia; low levels suggest various types of anaemia

**mcv**
- **Type**: Numeric (Float)
- **Description**: Mean Corpuscular Volume - average size of red blood cells
- **Range**: 70-110 fL
- **Unit**: Femtoliters (fL)
- **Normal Range**: 80-100 fL
- **Clinical Relevance**: Elevated MCV (>100 fL) suggests megaloblastic anaemia, often due to folate/B12 deficiency

**mch**
- **Type**: Numeric (Float)
- **Description**: Mean Corpuscular Hemoglobin - average hemoglobin content per red blood cell
- **Range**: 20-35 pg
- **Unit**: Picograms (pg)
- **Normal Range**: 27-32 pg
- **Clinical Relevance**: Helps classify anaemia type; elevated in megaloblastic anaemia

**folate_level**
- **Type**: Numeric (Float)
- **Description**: Serum folate concentration
- **Range**: 1.0-20.0 ng/mL
- **Unit**: Nanograms per milliliter (ng/mL)
- **Normal Range**: >3.0 ng/mL
- **Deficiency**: <3.0 ng/mL
- **Clinical Relevance**: Direct measure of folate status; primary predictor for folate deficiency anaemia

**vitamin_b12**
- **Type**: Numeric (Float)
- **Description**: Serum vitamin B12 concentration
- **Range**: 100-900 pg/mL
- **Unit**: Picograms per milliliter (pg/mL)
- **Normal Range**: >200 pg/mL
- **Deficiency**: <200 pg/mL
- **Clinical Relevance**: B12 deficiency can cause similar megaloblastic anaemia; important differential diagnosis

**iron_status**
- **Type**: Categorical
- **Description**: Overall iron status assessment
- **Values**: Normal, Low, High
- **Clinical Relevance**: Iron deficiency is most common cause of anaemia; helps differentiate from folate deficiency

### Lifestyle and Anthropometric Variables

**bmi**
- **Type**: Numeric (Float)
- **Description**: Body Mass Index calculated as weight(kg)/height(m)²
- **Range**: 15.0-40.0 kg/m²
- **Unit**: kg/m²
- **Categories**: Underweight (<18.5), Normal (18.5-24.9), Overweight (25.0-29.9), Obese (≥30.0)
- **Clinical Relevance**: Malnutrition affects folate absorption; obesity may indicate poor dietary quality

**alcohol_consumption**
- **Type**: Categorical
- **Description**: Self-reported alcohol consumption level
- **Values**: Low (0-1 drinks/week), Moderate (2-7 drinks/week), High (>7 drinks/week)
- **Clinical Relevance**: Alcohol interferes with folate absorption and metabolism; major risk factor

**dietary_score**
- **Type**: Numeric (Integer)
- **Description**: Composite dietary quality score based on folate-rich food consumption
- **Range**: 0-100
- **Calculation**: Based on frequency of leafy greens, fortified grains, legumes, and citrus fruits
- **Higher scores**: Better dietary folate intake
- **Clinical Relevance**: Primary modifiable risk factor for folate deficiency

### Target Variable

**anaemia_status**
- **Type**: Binary (Integer)
- **Description**: Diagnosis of folate deficiency anaemia
- **Values**: 0 (No anaemia), 1 (Folate deficiency anaemia present)
- **Diagnostic Criteria**: 
  - Hemoglobin below normal range for age/gender
  - MCV >100 fL (megaloblastic)
  - Serum folate <3.0 ng/mL
  - Normal or elevated B12 levels (to exclude B12 deficiency)
- **Clinical Relevance**: Primary outcome for prediction models

## Data Quality Notes

- All laboratory values are within physiologically plausible ranges
- Missing values are excluded from this sample dataset
- Categorical variables are consistently encoded
- Numeric variables are rounded to appropriate precision based on measurement capability

## Clinical Context

This dataset represents a subset of variables commonly used in clinical practice for diagnosing folate deficiency anaemia. The combination of laboratory markers (hemoglobin, MCV, MCH, folate, B12) with lifestyle factors (diet, alcohol, BMI) provides a comprehensive view for predictive modeling.

## Usage Recommendations

- Use folate_level and hemoglobin as primary predictive features
- Consider interaction effects between alcohol consumption and dietary score
- MCV and MCH are highly correlated; consider dimensionality reduction
- Validate model performance across different age and gender subgroups
- Consider temporal aspects if longitudinal data becomes available
