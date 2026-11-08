# Exploring Measurement Validity Using Multigroup Confirmatory Factor Analysis (MGCFA)

> This study compared two versions of the Childhood Trauma
> Questionnaire-SF(CTQ-SF) and investigated cross-cultural performance
> of each version

------------------------------------------------------------------------

## ⚙️ Project Type Flags

-   [ ] Exploratory Data Analysis (EDA)
-   [ ] SQL Analysis / Querying
-   [ ] Dashboard / Data Visualization
-   [ ] Data Pipeline / ETL
-   [ ] Predictive Modelling / Machine Learning
-   [ ] Data Cleaning / Wrangling
-   [x] End-to-End (multiple of the above)
-   [ ] Other: \_\_\_\_\_\_\_\_\_\_\_

------------------------------------------------------------------------

## Table of Contents

1.  [Project Overview](#1-project-overview)
2.  [Objectives](#2-objectives)
3.  [Tools](#3-tools)
4.  [Data Workflow](#4-data-workflow)
5.  [Data](#5-data)
6.  [Analysis](#6-analysis)
7.  [Key Insights](#7-key-insights)
8.  [Recommendations](#8-recommendations)
9.  [Limitations](#9-limitations)
10. [Author](#10-author)

------------------------------------------------------------------------

## 1. Project Overview

Healthcare organizations rely on patient-reported data to identify high risk groups. Maltreatment increases risk for adverse health outcomes--making the selection of a childhood maltreatment measure that accurately captures exposure and is valid across groups important. This project explored survey data
completed by undergraduate students to determine whether an alternative
version of the Childhood Trauma Questionnaire-Short Form (CTQ-SF)
outperformed the original version using multigroup confirmatory factor
analysis (MGCFA). The analysis revealed that the alternative version
outperformed the original, especially among Black students.

------------------------------------------------------------------------

## 2. Objectives

-   **Primary Objective:** Determine whether an alternative CTQ-SF model
    performs better than the original version

-   **Secondary Objective:** Explore whether the alternative CTQ-SF
    model performs better across racial groups (i.e., Black and White
    students)

------------------------------------------------------------------------

## 3. Tools

### Tools & Technologies

| Category        | Tool(s) Used               |
|-----------------|----------------------------|
| Data Storage    | SPSS(.sav) and Excel       |
| Data Processing | R: tidyverse               |
| Analysis        | R: tidyverse, lavaan       |
| Visualization   | R: tidyverse, summarytools |
| Documentation   | RMarkdown                  |

------------------------------------------------------------------------

## 4. Data Workflow

```         
Load data 
      ↓
Explore data
      ↓
Prepare data (Remove columns, Rename CTQ-SF items, Re-code demographic variables)
      ↓
Exploratory data analysis
      ↓
confirmatory factor analysis
      ↓
Poster presentation/abstract
```

------------------------------------------------------------------------

## 5. Data

### Dataset:

This project used data that is not publicly available. Data was from a
web-based study completed at a university in the Southeast. Participants
(n=1,287) completed several self-reported measures as part of the study.

### Measures:

**Maltreatment**: The CTQ-SF (Bernstein et. al., 2003) contains 28 items
and five clinical scales (i.e., emotional abuse, physical abuse, sexual
abuse, emotional neglect, and physical neglect). Three additional items
are included in a minimization-denial scale to detect under-reporting of
maltreatment. For each subscale, the total score ranges from 5 to 25.
The cumulative score on the CTQ-SF ranges from 25 to 125. Higher CTF-SF
scores indicate exposure to a greater number of childhood maltreatment
experiences. The alternative version (Gerdner & Allgulander, 2009)
shifts two items from emotional neglect to the physical neglect
subscale: “someone to take me to doctor if needed” and “knew there was
someone to take care and protect me”. The minimization-denial scale
items were excluded from analysis.

**Race**: Participants were asked to select their race and could select
from the following options: “Native American/American Indian”, “Asian”,
“Black/African American”, “Native Hawaiian/Pacific Islander”, “White”,
“Biracial/Multiracial”, and “Other”.  If participants did not select
“Black/African American” or “White/Caucasian” as their race, then they
were excluded from the analysis.

The primarily analysis included race and 25 CTQ-SF items. For this
study, 921 participants were included.

------------------------------------------------------------------------

## 6. Analysis

### Exploratory Data Analysis:

Before conducting MGCFA, I explored the dataset to better understand
participant characteristics and CTQ-SF responses.

The exploratory data analysis involved:

-   Checking missing values
-   Reviewing data types
-   Generating descriptive statistics
-   Exploring relationships between variables
-   Creating visualizations to identify potential patterns

### Multigroup Confirmatory Factor Analysis (MGCFA):

For this study, I decided to use categorical MGCFA because distribution
of scores (majority of scores on low end) indicated that there was
limited variability and should not be treated as continuous.

I followed a five-step, iterative process to determine which model
performed better based on the following fit statistics: root mean square
error of approximation (RMSEA) and comparative fit index (CFI). RMSEA
indicates improved fit if it decreases. CFI indicates improved fit if it
increases.

First, I ran a confirmatory factor analysis to test whether the model
worked for the overall sample and within each racial group. All models
ran without errors. The fit statistics provided evidence that the
alternative model performed better for the entire sample.

Second, I tested for configural invariance, or whether the factor
structure for the model were the same between Black and White
participants. Fit statistics did not indicate there factor structure was
different.

Third, I tested for metric invariance by restricting the loadings and
making them equal between groups. Metric invariance indicates whether
there are differences in how items cluster together. Fit statistics did
not provide evidence for differences between the two groups.

Fourth, I tested for scalar invariance, which provides evidence of
differences in the means of the latent variables. For example, does one
group have a significantly higher mean for physical abuse. Fit
statistics suggested that there was no difference in latent variable
means.

Finally, I tested for error/variance invariance. Fit statistics did not
provide evidence of differences in the variability in responses between
the two groups.

I repeated these steps to test the performance of the alternative
version. Results provided evidence that there were not significant
differences between groups for the alternative version.

------------------------------------------------------------------------

## 7. Key Insights

**Insight 1**: The alternative CTQ-SF version outperformed the original
version. This suggests that the alternative model may be a better way to
understand experiences of maltreatment among adults.

**Insight 2**: The improvement in performance was driven by performance
among Black participants suggesting that using the alternative version
of the CTQ-SF may be a more valid measure across demographic groups.

------------------------------------------------------------------------

## 8. Recommendations

| Priority | Recommendation | Based On | Suggested Owner |
|------------------|------------------|------------------|-------------------|
| High | Conduct additional studies investigating the performance of the alternative CTQ-SF model with different demographic groups | Insight 1 & 2-performance of alternative CTQ-SF | Researchers |
| Medium | Investigate predictive validity of health outcomes comparing the alternative and original CTQ-SF versions | Insight 1 & 2-performance of alternative CTQ-SF | Researchers |

------------------------------------------------------------------------

## 9. Limitations

### Limitations

-   Study only compared two racial groups
-   The sample was mostly female
-   Limited distribution of responses to CTQ-SF items

------------------------------------------------------------------------

## 10. Author

**Davena -** Health Researcher \| Research Data Analyst \| Clinician

-   🔗 [LinkedIn](https://www.linkedin.com/in/davenamgbeokwere/)
-   💼 [Portfolio](https://github.com/davenalcsw)

------------------------------------------------------------------------
