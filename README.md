# A/B Testing Using Python: Summary and Code Walkthrough

## Overview
![unnamed](https://github.com/user-attachments/assets/37645c90-9b98-4702-9dca-48873edb05ba)

A/B testing is a method used to compare two variants (A and B) to determine which performs better based on certain metrics. 
The general steps in conducting A/B testing are as follows:

1. **Define Hypothesis**: Propose a change (e.g., changing button color) to improve a metric.
2. **Randomly Assign Users**: Split users into two groups — a control group (A) and a treatment group (B).
3. **Measure Metrics**: Track conversion rates or key metrics for both groups.
4. **Statistical Testing**: Use statistical tests (e.g., t-test, Z-test) to determine if observed differences are statistically significant.

At this stage of Analysis within the NoteBook, steps 1 and 2 above are complete i.e. the Control and treatment groups have been assigned, hypotheses are set, and data collection is complete. Users have interacted with their respective pages, and conversions (yes or no) have been recorded. Now, we analyze this data to determine if the new page significantly affects conversion rates compared to the old page. Below are the steps carried out:

## Data Cleaning and Preprocessing

### Step 1: Data Exploration
* Check for duplicates (e.g., the same user interacting with control and treatment groups).
* Ensure correct alignment between groups and pages (i.e., no control group user should see the new page or vice versa).

### Step 2: Handling Data Misalignment
* These rows are dropped.

### Step 3: Handle Duplicates
* Duplicate entries are removed, keeping only the first occurrence of each user.

## Analysis and Visualization
### Step 4: Power Analysis and Sample Size Calculation
* Performing power analysis to ensure that the sample size is sufficient for detecting meaningful differences.

### Step 5: Conversion Rate Calculation and Visualization
* Calculate Conversion rates for both groups are calculated and visualize them.

### Step 6: Z-Test for Statistical Significance
* The Z-test is performed to determine if the difference in conversion rates between the two groups is statistically significant.   * Note: A p-value less than 0.05 suggests a significant difference.

## Interpretation of Results
* In this analysis, the p-value was 0.582, which is greater than 0.05, indicating that the difference in conversion rates between the control and treatment groups is not statistically significant.

## Conclusion
* Since the p-value exceeds 0.05, we fail to reject the null hypothesis and conclude that there is no significant difference between the conversion rates of the old page and the new page. Thus, the recommendation is to continue using the old page.
