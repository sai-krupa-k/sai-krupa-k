# Data Dictionary - Folate Anaemia Classification

This document provides detailed descriptions of all variables included in the folate anaemia classification dataset. The data is designed to support machine learning models for predicting folate deficiency anaemia based on clinical and lifestyle factors.

## Variable Definitions

**Participant ID**
- Unique identifier for each research participant in the study. Used for data linkage and tracking while maintaining participant anonymity.

**Age**
- Patient age in years at the time of data collection. Age affects folate metabolism, absorption, and nutritional requirements.

**Haematocrit percentage**
- The proportion of blood volume occupied by red blood cells, expressed as a percentage. Low haematocrit values indicate anaemia and reduced oxygen-carrying capacity.

**Haemoglobin concentration**
- The concentration of haemoglobin protein in blood, measured in grams per deciliter. Primary biomarker for diagnosing anaemia and assessing oxygen transport capacity.

**Red blood cell (erythrocyte) distribution width**
- A measure of the variation in size of red blood cells (RDW). Elevated RDW suggests mixed cell populations and can indicate various types of anaemia including folate deficiency.

**Body mass index (BMI)**
- Weight-to-height ratio calculated as kg/m², indicating nutritional status. BMI affects nutrient absorption and can reflect overall dietary quality related to folate intake.

**Cooked vegetable intake**
- Frequency or quantity of cooked vegetable consumption. Cooked vegetables are important sources of bioavailable folate, though cooking can reduce folate content.

**Salad / raw vegetable intake**
- Frequency or quantity of raw vegetable and salad consumption. Raw vegetables retain higher folate content compared to cooked preparations.

**Fresh fruit intake**
- Frequency or quantity of fresh fruit consumption. Citrus fruits and other fresh fruits are significant dietary sources of natural folate.

**Dried fruit intake**
- Frequency or quantity of dried fruit consumption. Concentrated source of nutrients including folate, though processing may affect bioavailability.

**Oily fish intake**
- Frequency or quantity of oily fish consumption. Rich source of B-vitamins including B12, which works synergistically with folate in DNA synthesis.

**Processed meat intake**
- Frequency or quantity of processed meat consumption. Generally low in folate and may contain compounds that interfere with folate metabolism.

**Lamb/mutton intake**
- Frequency or quantity of lamb or mutton consumption. Meat products provide some B-vitamins but are not significant sources of folate.

**Never eat**
- Indicator for dietary restrictions or foods never consumed. May represent vegetarian/vegan status or specific food avoidances affecting nutrient intake.

**Sugar**
- Sugar consumption frequency or quantity. High sugar intake may displace nutrient-dense foods and affect overall dietary quality related to folate intake.

**Anaemia**
- Binary outcome variable (0/1) indicating the presence or absence of anaemia. Primary endpoint for classification models predicting anaemia risk based on clinical and lifestyle factors.

**Sex_Female**
- Binary indicator variable (0/1) representing female participants. Gender influences folate requirements, particularly during reproductive years.

**Sex_Male**
- Binary indicator variable (0/1) representing male participants. Complementary to Sex_Female for complete gender representation.

## Data Usage Notes

This dataset combines laboratory biomarkers, anthropometric measurements, and detailed dietary intake variables to provide a comprehensive view of factors influencing anaemia development. The combination of haematological parameters with lifestyle factors enables robust prediction modeling for clinical decision support.
