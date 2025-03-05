# A/B Testing: Comparing Bidding Methods for Conversion Rates

## Project Description

Facebook recently introduced a new bidding strategy called "average bidding" as an alternative to the existing "maximum bidding" method. One of our clients, bombabomba.com, has decided to test this new feature. They aim to determine whether average bidding results in higher conversions compared to maximum bidding by conducting an A/B test.

The A/B test has been running for one month, and bombabomba.com expects an analysis of the results. The primary success metric for bombabomba.com is **Purchase**, making it the key focus for statistical testing.

## Dataset Description

This dataset contains website information for a company, including the number of ads viewed, clicks made, and revenue generated from purchases. It consists of two separate datasets: one for the **Control Group** (using **Maximum Bidding**) and another for the **Test Group** (using **Average Bidding**). These datasets are stored in different sheets of the **ab_testing.xlsx** file.

### Variables:
- **Impression**: Number of ad views.
- **Click**: Number of clicks on the displayed ads.
- **Purchase**: Number of products purchased after clicking an ad.
- **Earning**: Revenue generated from purchased products.

## Project Tasks

### Task 1: Preparing and Analyzing the Data
1. Load the dataset **ab_testing.xlsx** and assign control and test group data to separate variables.
2. Analyze the data for both control and test groups.
3. Merge the control and test datasets using the **concat** method for further analysis.

### Task 2: Defining the A/B Test Hypothesis
1. Define the hypothesis:
   - **H0**: The mean purchase values for the two groups are equal.
   - **H1**: The mean purchase values for the two groups are different.
2. Analyze the purchase averages for the control and test groups.

### Task 3: Conducting the Hypothesis Test

#### A/B Testing (Independent Two-Sample T-Test)
1. Before conducting the hypothesis test, check for assumptions:
   - **Normality Assumption** (Shapiro-Wilk test)
   - **Homogeneity of Variance** (Levene’s test)
   - **Decision Criteria**:
     - **H0**: Normal distribution assumption holds.
     - **H1**: Normal distribution assumption does not hold.
     - If **p < 0.05**, reject H0; otherwise, fail to reject H0.
2. Based on the normality and variance homogeneity results, choose the appropriate test:
   - If assumptions hold, use an **Independent Two-Sample T-Test**.
   - If assumptions do not hold, use a **Mann-Whitney U Test**.
3. Interpret the p-value to determine whether there is a statistically significant difference between the control and test group purchase averages.

### Task 4: Analyzing the Results
1. Specify which statistical test was used and justify the choice.
2. Based on the test results, provide recommendations to the client regarding the effectiveness of **average bidding** compared to **maximum bidding**.

## Conclusion
This project evaluates the effectiveness of Facebook's **average bidding** strategy compared to **maximum bidding** using an A/B test. By conducting statistical analyses, we determine whether there is a significant difference in conversion rates between the two methods. The results help bombabomba.com make data-driven decisions to optimize their bidding strategy and maximize revenue.

