# Death_Penalty_Impact_Case_study

# Overview

This project investigates the causal relationship between the suspension of the death penalty and homicide rates in the United States. Using the 1972 Supreme Court decision Furman v. Georgia as a "natural experiment," I analyzed whether states that were forced to suspend the death penalty saw a statistically significant increase in murder rates in the following year (1973).

# Key Findings
Statistical Result: A permutation test (A/B test) yielded a p-value of approximately 0.26.

Conclusion: We fail to reject the null hypothesis. The data suggests that the temporary abolition of the death penalty did not have a statistically significant immediate impact on murder rates.

### Technologies Used
* Python 3.x

* Pandas & NumPy: For efficient data manipulation and vectorization.

* Seaborn & Matplotlib: For exploratory data analysis (EDA) and visualizing null distributions.

* Jupyter Notebook: For interactive development and reporting.

# Methodology
1. Exploratory Data Analysis (EDA)
Before testing, I visualized the distributions of murder rates for states with and without the death penalty using Boxplots. This revealed the spread, median, and potential outliers in the data.

2. A/B Testing (Permutation Test)
Instead of relying on standard parametric tests (like t-tests) which assume normality, I implemented a robust non-parametric permutation test:

Test Statistic: The difference in mean murder rates between the "No Death Penalty" group (1973) and the "Death Penalty" group (1971).

Simulation: I ran 10,000 simulations where the year labels were randomly shuffled to construct a "Null Distribution."

Optimization: The simulation loop was optimized using Python list compressions and NumPy arrays for performance.

# Results
Visualizing the Null Distribution
The histogram below shows the distribution of differences in means we would expect purely by chance. The red dashed line represents our observed statistic from the real world.(See from the code file)

* Observed Difference: +0.61
* P-Value: 0.26

Since the observed difference falls well within the typical range of random chance (p > 0.05), the result is not statistically significant.