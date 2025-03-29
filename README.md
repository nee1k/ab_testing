## **1. Descriptive Statistics**

### **A. Measures of Central Tendency**

- **Mean (Arithmetic Average):**  
  - **Formula:**  
    $$\bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i$$  
  - **Notes:**  
    - Sensitive to extreme values (outliers).  
    - Best used when data are symmetric.
  - **Example:**  
    - For data \([2, 4, 6, 8]\),  
      $$\bar{x} = \frac{2+4+6+8}{4} = 5$$

- **Median:**  
  - **Definition:**  
    - The middle value when data are arranged in order.  
    - For an even number of observations, it is the average of the two middle numbers.
  - **Usage:**  
    - More robust than the mean in skewed distributions.
  - **Example:**  
    - For data \([1, 3, 7, 9]\),  
      Median = $$\frac{3+7}{2} = 5$$

- **Mode:**  
  - **Definition:**  
    - The most frequently occurring value(s) in the dataset.
  - **Usage:**  
    - Particularly useful for categorical data.

---

### **B. Measures of Dispersion**

- **Range:**  
  - **Formula:**  
    $$\text{Range} = \text{Max} - \text{Min}$$  
  - **Usage:**  
    - Provides a quick indication of spread; however, it is sensitive to outliers.

- **Variance:**  
  - **Population Variance:**  
    $$\sigma^2 = \frac{1}{N} \sum_{i=1}^{N} (x_i - \mu)^2$$  
  - **Sample Variance:**  
    $$s^2 = \frac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2$$  
  - **Interpretation:**  
    - A larger variance indicates that data points are more spread out.

- **Standard Deviation:**  
  - **Definition:**  
    - The square root of the variance.
  - **Formula:**  
    $$s = \sqrt{s^2}$$  
  - **Usage:**  
    - Measures the average deviation from the mean in the same units as the data.

- **Interquartile Range (IQR):**  
  - **Definition:**  
    - Difference between the third quartile (Q3) and the first quartile (Q1):  
      $$IQR = Q3 - Q1$$  
  - **Usage:**  
    - Focuses on the middle 50% of data; minimizes the impact of outliers.

---

### **C. Data Visualization Techniques**

- **Histograms:**  
  - **Purpose:**  
    - Display the frequency distribution of a continuous variable.
  - **Interpretation:**  
    - Visualizes skewness, modality, and outliers.
  
- **Box Plots (Box-and-Whisker):**  
  - **Purpose:**  
    - Summarize the median, quartiles, and potential outliers.
  - **Interpretation:**  
    - Helps identify symmetry, skewness, and detect outliers.
  
- **Scatter Plots:**  
  - **Purpose:**  
    - Assess relationships between two quantitative variables.
  - **Usage:**  
    - Identify trends, clusters, and potential outliers.
  
- **Bar Charts:**  
  - **Purpose:**  
    - Present frequency counts for categorical data.

---

## **2. Probability Fundamentals**

### **A. Basic Probability**

- **Definition:**  
  - The likelihood of an event is calculated as:  
    $$P(E) = \frac{\text{Number of favorable outcomes}}{\text{Total number of outcomes}}$$

---

### **B. Rules of Probability**

- **Addition Rule:**  
  - For mutually exclusive events:  
    $$P(A \cup B) = P(A) + P(B)$$  
  - For non-mutually exclusive events (subtracting the overlap):  
    $$P(A \cup B) = P(A) + P(B) - P(A \cap B)$$

- **Multiplication Rule:**  
  - For independent events:  
    $$P(A \cap B) = P(A) \times P(B)$$  
  - For dependent events (using conditional probability):  
    $$P(A \cap B) = P(A) \times P(B|A)$$

---

### **C. Conditional Probability and Bayes’ Theorem**

- **Conditional Probability:**  
  - **Formula:**  
    $$P(A|B) = \frac{P(A \cap B)}{P(B)}$$  
  - **Interpretation:**  
    - The probability of \(A\) occurring given that \(B\) has occurred.

- **Bayes’ Theorem:**  
  - **Formula:**  
    $$P(A|B) = \frac{P(B|A) \times P(A)}{P(B)}$$  
  - **Usage:**  
    - Fundamental for updating beliefs with new data; commonly used in medical testing, spam filtering, and more.

---

### **D. Random Variables and Their Distributions**

- **Types:**  
  - **Discrete:** Takes countable values (e.g., number of successes).  
  - **Continuous:** Takes any value within an interval (e.g., weight, height).

- **Probability Mass Function (PMF) for Discrete Variables:**  
  - Provides the probability that a discrete random variable is exactly equal to a particular value.
  
- **Probability Density Function (PDF) for Continuous Variables:**  
  - Describes the likelihood of a continuous random variable falling within a particular range.  
  - **Note:**  
    - The probability at any single point is zero; integrate over an interval to obtain probabilities.

- **Cumulative Distribution Function (CDF):**  
  - **Definition:**  
    $$F(x) = P(X \leq x)$$  
  - **Usage:**  
    - Provides the cumulative probability up to a value \(x\).

---

## **3. Probability Distributions**

### **A. Discrete Distributions**

- **Binomial Distribution:**  
  - **Scenario:**  
    - \(n\) independent trials, each with a probability \(p\) of success.
  - **Probability Function:**  
    $$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}$$  
  - **Applications:**  
    - Quality control, survey responses, and more.

- **Poisson Distribution:**  
  - **Scenario:**  
    - Models the number of events in a fixed interval with a constant rate.
  - **Probability Function:**  
    $$P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}$$  
  - **Usage:**  
    - Modeling rare events, e.g., number of emails received per hour.

- **Geometric Distribution:**  
  - **Scenario:**  
    - Models the number of trials until the first success.
  - **Probability Function:**  
    $$P(X = k) = (1-p)^{k-1} p$$  
  - **Usage:**  
    - Reliability testing, survival analysis.

---

### **B. Continuous Distributions**

- **Normal Distribution:**  
  - **Characteristics:**  
    - Bell-shaped and symmetric about the mean.
  - **Probability Density Function (PDF):**  
    $$f(x) = \frac{1}{\sqrt{2\pi\sigma^2}} \exp\left(-\frac{(x-\mu)^2}{2\sigma^2}\right)$$  
  - **Central Limit Theorem (CLT):**  
    - States that the sampling distribution of the mean tends toward normality as sample size increases, regardless of the population distribution.
  
- **Exponential Distribution:**  
  - **Scenario:**  
    - Often used to model the time between independent events.
  - **PDF:**  
    $$f(x; \lambda) = \lambda e^{-\lambda x}, \quad x \geq 0$$
  
- **Uniform Distribution:**  
  - **Definition:**  
    - All outcomes in the interval \([a, b]\) are equally likely.
  - **PDF:**  
    $$f(x) = \frac{1}{b-a}, \quad a \leq x \leq b$$

---

## **4. Inferential Statistics**

### **A. Sampling and Sampling Distributions**

- **Random Sampling:**  
  - Ensures each member of the population has an equal chance of selection.
- **Central Limit Theorem (CLT):**  
  - **Implication:**  
    - For a sufficiently large sample size, the sampling distribution of the sample mean is approximately normally distributed regardless of the shape of the population.
- **Law of Large Numbers:**  
  - States that as the number of observations increases, the sample mean converges to the expected value.

---

### **B. Estimation Techniques**

- **Point Estimation:**  
  - Provides a single best guess of an unknown population parameter (e.g., using the sample mean to estimate the population mean).

- **Interval Estimation:**  
  - **Confidence Intervals:**  
    - **General Form for a Mean:**  
      $$\bar{x} \pm t_{\alpha/2,\,n-1}\frac{s}{\sqrt{n}}$$  
    - **Interpretation:**  
      - There is a specified level of confidence (often 95%) that the interval contains the true population parameter.

- **Standard Error (SE):**  
  - **Definition:**  
    - The standard deviation of the sampling distribution:  
      $$SE = \frac{s}{\sqrt{n}}$$

---

## **5. Hypothesis Testing**

### **A. Framework and Key Concepts**

- **Null Hypothesis (\(H_0\)) vs. Alternative Hypothesis (\(H_1\)):**  
  - **\(H_0\):** Assumes no effect or difference.  
  - **\(H_1\):** Suggests that there is an effect or difference.
- **Errors in Testing:**  
  - **Type I Error (\(\alpha\)):** Incorrectly rejecting a true \(H_0\).  
  - **Type II Error (\(\beta\)):** Failing to reject a false \(H_0\).
- **Power of a Test:**  
  - \(1 - \beta\); the probability of correctly rejecting a false \(H_0\).

---

### **B. Test Statistics and Decision Making**

- **P-Value:**  
  - The probability of obtaining test results at least as extreme as those observed, assuming \(H_0\) is true.
- **Decision Rule:**  
  - Compare the p-value to the significance level (\(\alpha\)) to decide whether to reject \(H_0\).

---

### **C. Common Hypothesis Tests**

- **t-Tests:**  
  - **One-Sample t-Test:**  
    - Tests whether the sample mean differs significantly from a known value.
  - **Independent t-Test:**  
    - Compares the means of two independent groups.
  - **Paired t-Test:**  
    - Compares means from the same group at different times or under different conditions.
  
- **Chi-Square Test:**  
  - **Goodness-of-Fit Test:**  
    - Determines if the observed frequency distribution differs from the expected distribution.
  - **Test for Independence:**  
    - Assesses whether two categorical variables are independent.
  
- **Analysis of Variance (ANOVA):**  
  - **Purpose:**  
    - Compares means across three or more groups.
  - **F-Statistic:**  
    - The ratio of the variance between group means to the variance within groups.
  
- **Non-Parametric Tests:**  
  - **Examples:**  
    - Mann-Whitney U Test, Kruskal-Wallis Test, Spearman’s Rank Correlation.  
  - **Usage:**  
    - Applied when data do not meet the assumptions required for parametric tests.

---

## **6. Regression Analysis**

### **A. Linear Regression**

- **Simple Linear Regression:**  
  - **Model:**  
    $$Y = \beta_0 + \beta_1 X + \epsilon$$  
  - **Assumptions:**  
    - **Linearity:** The relationship between \(X\) and \(Y\) is linear.  
    - **Independence:** Observations are independent.  
    - **Homoscedasticity:** Constant variance of the residuals.  
    - **Normality:** Residuals are normally distributed.
  - **Interpretation:**  
    - \(\beta_1\) indicates the change in \(Y\) for a one-unit change in \(X\).

- **Multiple Linear Regression:**  
  - **Model:**  
    $$Y = \beta_0 + \beta_1 X_1 + \beta_2 X_2 + \ldots + \beta_k X_k + \epsilon$$  
  - **Interpretation:**  
    - Each \(\beta_i\) measures the effect of a one-unit change in \(X_i\) on \(Y\) while holding other predictors constant.

- **Model Evaluation Metrics:**  
  - **R-squared (\(R^2\)):**  
    - Proportion of variance in the dependent variable explained by the independent variables.
  - **Adjusted \(R^2\):**  
    - Adjusts \(R^2\) for the number of predictors.

---

### **B. Model Diagnostics and Improvement**

- **Residual Analysis:**  
  - Plot residuals to detect non-linearity, heteroscedasticity, or outliers.
- **Multicollinearity:**  
  - **Variance Inflation Factor (VIF):**  
    - A VIF value above 10 may indicate problematic multicollinearity.
- **Model Selection Criteria:**  
  - **AIC (Akaike Information Criterion)** and **BIC (Bayesian Information Criterion):**  
    - Compare models while penalizing for complexity.

---

### **C. Extensions and Specialized Regression**

- **Logistic Regression:**  
  - **Model for Binary Outcomes:**  
    $$\log\left(\frac{p}{1-p}\right) = \beta_0 + \beta_1 X_1 + \ldots + \beta_k X_k$$  
  - **Interpretation:**  
    - Coefficients represent the change in the log-odds of the outcome for a one-unit change in the predictor.
  
- **Polynomial Regression:**  
  - Incorporates polynomial terms (e.g., \(X^2, X^3\)) to model non-linear relationships.
- **Interaction Effects:**  
  - Evaluates if the effect of one predictor on the outcome depends on the level of another predictor.

---

## **7. Advanced Topics and Specialized Methods**

### **A. Non-Parametric Methods**

- **Rationale:**  
  - Used when data do not meet the assumptions of normality or homoscedasticity.
- **Examples:**  
  - **Mann-Whitney U Test:**  
    - Compares differences between two independent groups without assuming normality.
  - **Kruskal-Wallis Test:**  
    - Non-parametric alternative to ANOVA for comparing more than two groups.
  - **Spearman’s Rank Correlation:**  
    - Measures the strength and direction of association based on rank order.

---

### **B. Time Series Analysis**

- **Components of Time Series Data:**  
  - **Trend:**  
    - The long-term progression of the series.
  - **Seasonality:**  
    - Regular, periodic fluctuations.
  - **Cyclicality:**  
    - Non-fixed, long-term oscillations.
- **Common Models:**  
  - **ARIMA Models (AutoRegressive Integrated Moving Average):**  
    - Combines autoregressive (AR), differencing (I), and moving average (MA) components.  
    - **Notation:** ARIMA(\(p, d, q\)), where \(p\) is the order of the AR term, \(d\) is the degree of differencing, and \(q\) is the order of the MA term.
  - **Exponential Smoothing:**  
    - Methods such as Holt-Winters for forecasting data with trends and seasonality.

---

### **C. Bayesian Statistics**

- **Key Concepts:**  
  - **Prior Distribution:**  
    - Represents initial beliefs before observing data.
  - **Likelihood:**  
    - The probability of the observed data given a parameter.
  - **Posterior Distribution:**  
    - Updated beliefs after incorporating the data.  
    - **Formula:**  
      $$P(\theta|X) \propto P(X|\theta) \times P(\theta)$$
- **Computational Methods:**  
  - **Markov Chain Monte Carlo (MCMC):**  
    - Algorithms (e.g., Gibbs sampling, Metropolis-Hastings) to approximate complex posterior distributions.

---

### **D. Experimental Design**

- **Randomized Controlled Trials (RCTs):**  
  - The gold standard for causal inference; random assignment minimizes confounding factors.
- **Factorial Design:**  
  - Evaluates the effect of two or more factors simultaneously, including their interaction effects.
- **Blocking and Stratification:**  
  - Techniques to reduce variability by grouping similar subjects before randomization.
- **ANOVA in Design:**  
  - Used to test for significant differences among group means in experimental settings.

---

## **8. Core Concepts and Terminology**

### **A. Degrees of Freedom (df)**

- **Definition:**  
  - The number of independent pieces of information available for estimating parameters.  
  - **Example:**  
    - For sample variance calculation, \(df = n - 1\).

### **B. Overfitting vs. Underfitting**

- **Overfitting:**  
  - A model that fits the training data too closely, capturing noise and failing to generalize to new data.
- **Underfitting:**  
  - A model that is too simple and fails to capture the underlying patterns in the data.
- **Validation Techniques:**  
  - Methods like k-fold cross-validation help assess model performance on unseen data.

### **C. Correlation vs. Causation**

- **Correlation:**  
  - A statistical measure indicating the extent to which two variables fluctuate together.
- **Causation:**  
  - Implies that one variable directly affects another; establishing causation typically requires controlled experiments or advanced statistical methods.

### **D. Confidence and Credibility Intervals**

- **Confidence Intervals (Frequentist):**  
  - Provide a range within which the true parameter is expected to lie with a certain probability (e.g., 95% confidence).
- **Credibility Intervals (Bayesian):**  
  - Derived from the posterior distribution, reflecting the degree of belief that the parameter lies within the interval.

---
