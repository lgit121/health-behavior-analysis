# Health Behavior Analytics Project

Understanding lifestyle behaviors and their association with health outcomes is an important step toward evidence-based public health decision-making. This project explores health survey data to identify behavioral patterns, evaluate factors associated with hypertension risk, and generate actionable insights through statistical analysis.

## Project Overview
### Dataset
This project utilized the China Health and Nutrition Survey (CHNS) dataset, which contains demographic information, dietary habits, lifestyle behaviors, physical activity, and health conditions of urban residents.

The dataset served as the foundation for investigating how different lifestyle factors contribute to health outcomes and for identifying behavioral patterns among different population groups.

### Project Objectives
The Health Behavior Analytics project aims to gain actionable insights into resident behavior and lifestyle patterns within the context of the health survey dataset. The primary objective of this project was to understand how lifestyle behaviors are associated with physical health outcomes.

### Exploration Questions
This project aimed to answer several key questions:

- Which lifestyle factors are most closely associated with hypertension risk?
- Can multiple dietary indicators be combined into a meaningful health behavior score?
- Are there distinct behavioral groups among urban residents?
- What insights can statistical analysis provide for understanding population health?

### Tools and Technologies
The project utilized the following tools and analytical methods:

- **Python:** Data preprocessing and exploratory analysis.
- **SPSS:** Statistical modeling, hypothesis testing, and clustering analysis.
- **Excel:** Initial data organization and preprocessing.

Together, these tools enabled a complete analytical workflow from data preparation to statistical modeling and interpretation.

## Approach
1. Collected and prepared the CHNS health survey dataset using Python and Excel, performing data cleaning, missing value handling, and variable transformation to obtain an analysis-ready dataset.
2. Built a dietary behavior scoring framework using Principal Component Analysis (PCA), reducing multiple dietary indicators into a comprehensive health behavior score for subsequent statistical analysis.
3. Performed descriptive statistical analysis and visualization on the comprehensive dietary scores, generating summary statistics and distribution plots to evaluate the overall dietary behavior of urban residents.
4. Applied Pearson correlation analysis to examine relationships between health indicators and identify variables for further modeling.
5. Developed a Binary Logistic Regression model to evaluate the associations between demographic characteristics, lifestyle behaviors, and hypertension risk, producing interpretable risk estimates for each factor.
6. Performed K-means clustering to segment residents into different behavioral groups based on lifestyle characteristics, generating user profiles with distinct health behavior patterns and corresponding health recommendations for each group.

## Results
**Diet Quality Analysis：**
The analysis combined nine dietary indicators into a single composite score, providing an overall measure of residents' diet quality. The score distribution showed that dietary quality was generally low and tightly concentrated, with an average score of **0.3599**, indicating considerable room for improvement.

The category-level analysis revealed that dairy consumption was the weakest aspect of residents' diets (average score **0.097**), while vegetable intake (**0.720**) and limiting fried food (**0.927**) performed relatively well. Rather than reflecting poor performance across every category, the results suggest that residents' diets were **imbalanced**, with several specific nutritional gaps.

**Lifestyle Behavior Analysis：**
The correlation analysis explored how demographic characteristics relate to lifestyle behaviors and dietary habits.

Several clear patterns emerged. Smoking behavior showed a strong association with gender (**r = 0.567**), while drinking years were negatively associated with both birth year (**r = -0.573**) and education level (**r = -0.176**), suggesting that younger and more educated residents generally reported fewer years of drinking.

The composite diet score was also positively associated with gender, marital status, and education level, indicating that women, married residents, and individuals with higher education tended to maintain healthier dietary habits.
These findings describe behavioral patterns within the dataset rather than causal relationships.

**Hypertension Risk Analysis：**
The model was statistically significant (**χ² = 224.461, p < 0.001**), indicating that the selected variables effectively distinguished hypertension status within the sample.

Among all predictors, **BMI** was the strongest risk factor (**Exp(B) = 2.495**), meaning that a one-unit increase in standardized BMI was associated with approximately **2.5 times** higher odds of hypertension. Occupation (**Exp(B) = 1.218**) and average daily exercise duration (**Exp(B) = 1.213**) also showed significant associations.

One interesting finding was the positive relationship between exercise time and hypertension. Rather than interpreting this as a direct causal effect, I examined the probability curves and observed greater uncertainty at higher exercise durations. This suggests that the relationship may be influenced by factors such as sample characteristics or reverse causality, highlighting the importance of validating statistical results before drawing conclusions.

**Resident Segmentation：**
Residents were grouped into seven behavioral profiles according to their drinking habits, exercise patterns, dietary quality, gender, and occupation.

Instead of simply identifying clusters, the analysis translated each segment into practical lifestyle recommendations. For example, one cluster consisted primarily of male technology workers with high alcohol consumption, limited exercise, and relatively poor diet quality. For this group, reducing alcohol intake, increasing regular physical activity, and improving dietary balance were identified as the highest-priority recommendations.

Other clusters represented groups such as female unemployed residents, male farmers, factory workers, and commercial service workers, each with distinct behavioral characteristics and corresponding health recommendations.

This segmentation demonstrates how behavioral data can be transformed into interpretable user profiles that support more targeted interventions.
