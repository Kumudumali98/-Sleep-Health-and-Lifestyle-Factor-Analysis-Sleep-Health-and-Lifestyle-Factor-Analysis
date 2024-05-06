Factor Analysis Report for "Sleep Health and Lifestyle" Dataset
===============================================================

S/18/827 - J Kumudumali Sandaleka

2024/04/08

Introduction
============

Factor analysis (FA) is a fundamental statistical technique used for modelling observed variables and their covariance structure in terms of a smaller number of underlying unobservable (latent) "factors". These factors aim to explain the underlying structure or patterns within a dataset by identifying common variance among observed variables.

In this study, the "Sleep Health and Lifestyle" dataset is used to conduct factor analysis. This dataset comprises various variables related to sleeping and lifestyle. By applying factor analysis, my objective is to reduce the dimensionality of the dataset while retaining meaningful information. This process facilitates the interpretation and the understanding of the underlying factors influencing sleep and lifestyle.

Methodology
===========

The methodology section encompasses rigorous data preprocessing, exploratory factor analysis (EFA), and confirmatory factor analysis (CFA), ensuring a comprehensive understanding of latent factors and their relationships within the "Sleep Health and Lifestyle" dataset.

Dataset Description
-------------------

The "Sleep Health and Lifestyle" dataset consists of 400 row and 13 columns, covering a range of variables including,

1.  Person ID: An identifier for each individual.
    
2.  Gender: The gender of the person (Male/Female).
    
3.  Age: The age of the person in years.
    
4.  Occupation: The occupation or profession of the person.
    
5.  Sleep Duration (hours): The number of hours the person sleeps per day.
    
6.  Quality of Sleep (scale: 1-10): A subjective rating of the quality of sleep.
    
7.  Physical Activity Level (minutes/day): The number of minutes the person engages in physical activity daily.
    
8.  Stress Level (scale: 1-10): A subjective rating of the stress level experienced by the person, ranging from 1 to 10.
    
9.  BMI Category: The BMI category of the person (e.g., Underweight, Normal, Overweight).
    
10.  Blood Pressure (systolic/diastolic): The blood pressure measurement of the person.
    
11.  Heart Rate (bpm): The resting heart rate of the person in beats per minute.
    
12.  Daily Steps: The number of steps the person takes per day.
    
13.  Sleep Disorder: The presence or absence of a sleep disorder in the person (None, Insomnia, Sleep Apnea).
    

Factor Analysis
---------------

### Data Preprocessing

Before conducting factor analysis, the dataset was thoroughly preprocessed to ensure its integrity and suitability. This required addressing duplicate entries and missing values in addition to standardizing the data to reduce inconsistencies caused by disparate units of measurement.In this stage I observed that there are no outliers in this dataset.

### Exploratory Factor Analysis (EFA)

The preliminary stage of the analysis focused on determining the optimal number of factors to extract from the dataset. Various techniques were employed for this purpose, including Jolliffe’s Method and the scree plot, which aimed to identify factors explaining 80% of the variance. EFA began with an initial factor analysis using Principal Component Analysis (PCA) or Maximum Likelihood Estimation (MLE) to establish loadings for each selected factor. To enhance interpretability, rotation techniques were applied.Finally, factor loading, commonalities, and uniqueness were interpreted for more understanding.

### Confirmatory Factor Analysis (CFA)

Following the exploratory phase, CFA was used to determine how well the hypothesized model fit the observed data. This involved defining the correlations between the factors and the observed variables and evaluating the fit of the model using a variety of fit indices, such as the Tucker-Lewis Index (TLI), Comparative Fit Index (CFI), Root Mean Square Error of Approximation (RMSEA), and chi-square test. These indices validate the underlying factor structure by showing how well the suggested model fits the observed data.

In conclusion, the methodology included comprehensive data preprocessing, suitability assessment, exploratory factor analysis for factor extraction, and confirmatory factor analysis to validate the proposed model. These steps contribute to a thorough understanding of the dataset’s latent factors and their relationships with observed variables.

Results and Discussion
======================

In this section, we present the results of our analysis, beginning with an exploration of the basic assumptions underlying the factor analysis. We conducted Exploratory Factor Analysis (EFA) to identify underlying latent factors within the dataset, employing varimax rotation to enhance interpretability. The results of EFA provided insights into the structure of the data and potential underlying constructs. Following EFA, Confirmatory Factor Analysis (CFA) was performed to validate the factor structure identified in EFA.

Checking the basic assumptions
------------------------------

### Sampling adequacy

The Kaiser-Meyer-Olkin (KMO) measure of sampling adequacy is a better measure of factor-ability. The minimum acceptable value is 0.50.

                        Kaiser-Meyer-Olkin factor adequacy
                        Call: KMO(r = standardized_data)
                        Overall MSA =  0.76
                        MSA for each item = 
                        age         sleep_duration    quality_of_sleep     stress_level     bmi_category 
                        0.77             0.85             0.71             0.73             0.83 
                        systolic_bp      diastolic_bp    heart_rate        sleep_disorder 
                        0.71             0.72             0.81             0.79 

Initially, the KMO analysis for the "Sleep Health and Lifestyle" dataset yielded an overall Measure of Sampling Adequacy (MSA) of 0.59, which suggests marginal adequacy. After removing the variables with low MSA values, a second KMO analysis was conducted, resulting in a substantially improved overall MSA of 0.76. This indicates a higher level of sampling adequacy, suggesting that the remaining variables are more suitable for factor analysis.

### Significance of the multiple correlations

This evaluates whether or not the variables intercorrelate at all, by evaluating the observed correlation matrix against an “identity matrix”.

                        R was not square, finding R from data
                        $chisq             $p.value         $df
                        [1] 3709.504          0              36

The p-value of 0 indicates that the observed correlation matrix significantly differs from an identity matrix, as it is less than the conventional significance level of 0.05. Therefore, we reject the null hypothesis, suggesting that there are correlations among the variables in the dataset.

Explanatory Factor Analysis (EFA)
---------------------------------

The Explanatory Factor Analysis (EFA) section delves into determining the appropriate number of factors to extract and estimating factor model parameters, revealing insights into underlying constructs within the dataset.

### Determining the Number of Factors to Extract

After checking basic assumptions, we need to clarify that how many components or factors that we are going to extract. For this purposes, we can use some methods or criterion:

1.  **Eigenvalues / Variances**
    
    Based on the Jolliffe‘s method, it appears that the first two factors contribute significantly to the variance, with eigenvalues above 0.7. First three factors explains approximately 86.91% of the total variance, suggesting that they capture a substantial portion of the variability in the dataset.
    
2.  **Scree Plot**
    
    ![scree_plot](https://github.com/Kumudumali98/Factor-Analysis-ST-405/assets/121919679/1d77f1a4-4a53-4b92-bb9d-3ffa8b0f0015)

    The scree plot shows the eigenvalues plotted against the factor number. The first three factors lie on the elbow.
    

Considering the findings of the scree plot and eigen values - variance we are positive that extracting three factors for our factor analysis of the "Sleep Health and Lifestyle" dataset is appropriate and meaningful.

### Estimate the factor model parameters

In exploratory factor analysis (EFA), begin by conducting an initial factor analysis to determine the loadings for each selected factor. Two commonly used methods are Principal Component Analysis (PCA) and Maximum Likelihood Estimation (MLE):

In this analysis, both PCA and ML methods revealed that all three factors extracted from the analysis are statistically significant. The three factors together explain around 80% of the total variance in the data and factor loadings are also closer to -1 or +1, indicating stronger relationships between variables and factors in both methods. In terms of correlation patterns, PCA identifies factor 3 solely correlated with sleeping disorder, whereas ML shows factor 3 correlated with both sleeping disorder and BMI category.

Consequently, the Maximum Likelihood method is chosen for further analysis due to its more reliable factor loadings and better representation of the relationships between variables and factors.

### Factor Rotations

Factor extraction aims to identify underlying constructs in the data, but these factors can be challenging to interpret directly. To address this issue, rotation techniques are used.

According to the results, the rotated factor loadings demonstrate notable correlations closer to 1 and -1, indicating stronger and more meaningful relationships between variables and factors. Given these findings, it is sound to continue with factors rotated using varimax rotation.

### Varimax - MLE Factor Model

![fa_variax_ml](https://github.com/Kumudumali98/Factor-Analysis-ST-405/assets/121919679/89ae5e6e-cf98-4991-ad4f-6c3330231fa0)


Based on the factor loadings provided in the table, the following improvements and factor names could be suggested:

1.  **Factor Loadings**
    
    *   Factor 1 shows strong positive correlations with Systolic Blood Pressure (0.97) and Diastolic Blood Pressure (0.95), indicating that it represents aspects related to blood pressure. Moreover, a moderate positive correlation with Age (0.65) suggests that older individuals tend to have higher blood pressure.
        
    *   Factor 2 exhibits a strong positive correlation with Quality of Sleep (0.97) and a strong negative correlation with Stress Level (-0.93), suggesting that higher levels of stress are associated with lower quality of sleep. Additionally, positive correlations with Sleep Duration (0.85) and Age (0.51) imply that older individuals with longer sleep durations experience higher quality of sleep. The negative correlation with Heart Rate (-0.69) may indicate that lower heart rates are associated with better sleep quality.
        
    *   Factor 3 is positively correlated with BMI category (0.72), indicating that it represents aspects related to body composition. Conversely, it shows a negative correlation with Sleep Disorder (-0.47), suggesting that lower scores on this factor are associated with fewer sleep disorders.
        
2.  **Communalities**
    
    Another assessment of how well this model performs can be obtained from the communalities. The model performs particularly well in explaining the variation in Quality of Sleep and Systolic Blood Pressure, while also showing relatively strong performance for variables such as Diastolic Blood Pressure, Stress Level, Sleep Duration, Age, Sleep Disorder, and BMI Category. However, the model performs less effectively for Heart Rate, explaining half of the variation.
    
3.  **Total communality value**
    
    The sum of all communality values is the total communality value = 7.261763
    
4.  **The proportion of total variation explained by the three factors**
    
    7.261763 / 9 = 0.8068625
    
    Therefore, 80.69% proportion of the total variation is explained by the three factors.
    
5.  **Uniqueness**
    
    The uniqueness of a variable represents the variance that is unique to that variable and not shared with other variables. According to this analysis, the uniqueness of Heart Rate is 0.48, which means that 48% of the variance in Heart Rate is not shared with other variables in the factor model. Conversely, Quality of Sleep and Systolic BP indicate that only 0.4% of their variance is not accounted for by other variables. It is important to note that, variables with lower uniqueness values are more important in explaining the common variance captured by the factors.
    

Confirmatory Factor Analysis (CFA)
----------------------------------

CFA is used to assess the overall measurement of a concept when there are multiple items available to measure it.

                    Test statistic                               314.838
                    Degrees of freedom                                23
                    P-value (Chi-square)                           0.000
                    
                    User Model versus Baseline Model:
                    
                    Comparative Fit Index (CFI)                    0.922
                    Tucker-Lewis Index (TLI)                       0.877
                    
                    Root Mean Square Error of Approximation:
                    
                    RMSEA                                          0.184
                    90 Percent confidence interval - lower         0.166
                    90 Percent confidence interval - upper         0.203
                    P-value H_0: RMSEA <= 0.050                    0.000
                    P-value H_0: RMSEA >= 0.080                    1.000
                    
                    Standardized Root Mean Square Residual:
                    
                    SRMR                                           0.071
                    
                    R^2 Values
                    age          quality_of_sleep     stress_level   sleep_duration     heart_rate      
                    0.675               NA            0.807            0.779              0.435             
                    systolic_bp     diastolic_bp     bmi_category   sleep_disorder 
                    0.992            0.954            0.796            0.526 
                    

### Overall Model Level Fit

Multiple methods of estimation have been developed for SEM models generally and CFA models specifically.

1.  **Model Test:**
    
    The chi-square test assesses the goodness of fit of the model. A lower p-value (close to 0) suggests that the model significantly deviates from the expected values, indicating a potential lack of fit. In this case, with a p-value of 0.000, the model significantly deviates from the expected values.
    
2.  **Root Mean Square Error of Approximation (RMSEA):**
    
    The root mean square error of approximation is a parsimony-adjusted fit index, meaning that it favours simplicity in models. Lower RMSEA values indicate better fit, with values below 0.05 typically considered good. The provided RMSEA of 0.184 suggests a moderate fit.
    
3.  **Comparative Fit Index (CFI) and Tucker-Lewis Index (TLI):**
    
    These indices assess the model fit by comparing it to a baseline model. Values closer to 1 indicate a better fit. Both CFI and TLI values are closer to 1, suggesting a reasonable fit of the model.
    
4.  **Standardized Root Mean Square Residual (SRMR):**
    
    SRMR measures the square root of the standardized difference between the sample covariances and the covariances predicted by the model. Lower values indicate a better fit. The provided SRMR of 0.071 suggests a reasonably good fit.
    

Overall, the model appears to have a reasonable fit to the data, although it may not be perfect. Further adjustments or evaluations might be necessary depending on the specific goals of the analysis.

### Equation Level Fit

The equation-level fit of the model was assessed using R\\(^2\\) values for each observed variable. The model demonstrated strong predictive power for variables such as stress level, sleep duration, systolic and diastolic blood pressure, and BMI category, with R\\(^2\\) values ranging from approximately 79.6% to nearly 99.2%. Variables like age and sleep disorder also exhibited moderate to high levels of explained variance (approximately 67.5% and 52.6% respectively). Notably, heart rate showed comparatively lower explained variance at around 43.5%. These results suggest that the model provides a generally good fit for predicting the observed variables.

### Parameter Level Fit

Factor loadings indicate the strength and direction of the relationship between latent factors and observed variables.

In Factor 1, variables like age, sleep duration, and systolic blood pressure have relatively high loadings, suggesting a strong association with the latent factor represented by Factor 1. Conversely, variables like stress level and heart rate show negative loadings, indicating an inverse relationship with Factor 1.

Factor 2 primarily captures variables related to blood pressure (systolic and diastolic), with high loadings on these variables and relatively low loadings on others.

Factor 3 is predominantly associated with BMI category and sleep disorder, with high loadings on these variables and negligible loadings on others.

                    $psi
                    factr1 factr2 factr3
                    factor1  1.000              
                    factor2 -0.120  1.000       
                    factor3 -0.361  0.795  1.000

Theta and Psi matrices represent the relationships between factors and error terms. These values indicate the strength of association and covariance between latent factors and any unexplained variance in the observed variables.

Overall, the factor loadings suggest that the model adequately captures the relationships between latent factors and observed variables, providing insights into the underlying structure of the data and informing potential model refinement. Non-significant loadings, such as those for certain variables on Factor 3, may indicate areas for model improvement, possibly through the inclusion of additional variables or modification of the structural model.

Conclusion
==========

In conclusion, the Explanatory Factor Analysis (EFA) and Confirmatory Factor Analysis (CFA) conducted on the "Sleep Health and Lifestyle" dataset have revealed three distinct factors that explain various facts about sleep health and overall well-being. Factor 1, identified as the Cardiovascular Health Factor, contains variables related to blood pressure and age, highlighting the critical role of cardiovascular health in sleep quality. Factor 2, named the Sleep Wellness Factor, includes variables associated with sleep duration, quality, and stress levels, highlighting the relationship between sleep patterns and psychological well-being. Finally, Factor 3, the Body-Mind Balance Factor, reflects variables related to body composition and sleep disorders, emphasizing the interconnection of physical and mental health with sleep quality.

These factors offer valuable insights for healthcare professionals, researchers, and policymakers looking to create specific measures to improve sleep quality and promote overall well-being. Understanding the different dimensions of sleep health and lifestyle factors allows for the development of customized solutions to address the specific needs and challenges that individuals in various populations face. Furthermore, the discovery of these factors emphasizes the importance of taking a variety of perspectives when it comes to sleep health management.

References
==========

1.  CitedDemir, Ergul. “RPubs - Intro to EFA and CFA in R.” Rpubs.com, 2022, [rpubs.com/isbell\_daniel/efa\_cfa\_intro](rpubs.com/isbell_daniel/efa_cfa_intro). Accessed 7 Apr. 2024.
    
2.  Example of Factor Analysis Method Section Reporting. Huang, Gaoping. “Exploratory Factor Analysis – Notes and R Code · Gaoping Huang’s Blog.” Gaopinghuang0.Github.io, 9 Feb. 2018, [gaopinghuang0.github.io/2018/02/09/exploratory-factor-analysis-notes-and-R-code](gaopinghuang0.github.io/2018/02/09/exploratory-factor-analysis-notes-and-R-code). Accessed 23 Nov. 2022.
    
3.  Isbell, Dan. “RPubs - MyClassNotes\_EFA\_CFA.” Rpubs.com, 17 Apr. 2021, [rpubs.com/Symrna/EFA\_CFA](rpubs.com/Symrna/EFA_CFA).
    
4.  Murphy, Phil. “RPubs - Exploratory Factor Analysis in R.” Rpubs.com, 21 Apr. 2021, [rpubs.com/pjmurphy/758265](rpubs.com/pjmurphy/758265).
    
5.  THARMALINGAM, LAKSIKA. “Sleep Health and Lifestyle Dataset.” [www.kaggle.com](www.kaggle.com), Oct. 2023, [https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset](https://www.kaggle.com/datasets/uom190346a/sleep-health-and-lifestyle-dataset).
    
