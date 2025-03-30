## 1. Measures of Central Tendency (Describes where the data is centered)

### Mean (Average)

Used to find the average value in a dataset. Sensitive to outliers.
**Formula:** \(\bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i\)\
**Example:** Average number of reels viewed per user daily\
\([3, 5, 7, 4, 6]\) → Mean = 5

### Median

The middle value when data is sorted. More robust than the mean for skewed data.\
**Example:** Median messages sent per user per day\
\([2, 6, 8, 9, 15]\) → Median = 8

### Mode

Identifies the most frequent value(s) in the dataset. Best for categorical data.\
**Example:** Most used emoji in comments\
\([2, 3, 3, 5, 6]\) → Mode = 3

---

## 2. Measures of Dispersion (Describes variability)

### Range

Difference between maximum and minimum values.\
**Formula:** \(\text{Range} = \max(x) - \min(x)\)\
**Example:** Session durations: \([5, 10, 15]\) → 10

### Variance

Average squared deviation from the mean. Higher variance = more spread.\
**Formula:** \(s^2 = \frac{1}{n - 1} \sum (x_i - \bar{x})^2\)\
**Example:** Variance in ad impressions

### Standard Deviation

Square root of variance; same unit as data.\
**Formula:** \(s = \sqrt{s^2}\)\
**Example:** Std dev in Story watch time

### Interquartile Range (IQR)

Range of middle 50% of data; reduces impact of outliers.\
**Formula:** \(IQR = Q3 - Q1\)\
**Example:** IQR of daily post interactions

---

## 3. Probability (Quantifies uncertainty)

### Basic Probability

Chance of an event occurring.\
**Formula:** \(P(E) = \frac{\text{Favorable outcomes}}{\text{Total outcomes}}\)\
**Example:** P(click on ad) = 40/200 = 0.2

### Conditional Probability

Probability of A given B has occurred.\
**Formula:** \(P(A|B) = \frac{P(A \cap B)}{P(B)}\)\
**Example:** P(share | like) = 30/50 = 0.6

### Bayes’ Theorem

Update probability of A based on evidence B.\
**Formula:** \(P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}\)\
**Example:** P(becoming creator | uploads multiple reels)

---

## 4. Distributions (Shape and Type of Data)

Distributions help us understand how data is spread or clustered. They are generally categorized as **discrete** or **continuous**, depending on whether the values the variable can take are countable or uncountable.

---

### Discrete Distributions

Discrete distributions model variables that take on **countable** values. These are often used for metrics such as number of clicks, comments, purchases, or app sessions.

#### Binomial Distribution

Models the number of successes in a fixed number of **independent** trials, each with two outcomes (success/failure).

**Formula:** \(P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}\)

**Example:** Estimating the probability of a user clicking on an ad 3 times out of 5 shown.

---

#### Poisson Distribution

Models the number of events occurring in a **fixed interval** of time or space when events happen independently.

**Formula:** \(P(X=k) = \frac{\lambda^k e^{-\lambda}}{k!}\)

**Example:** Understanding rate of incoming messages per second in Messenger.

---

### Continuous Distributions

Continuous distributions model variables that can take on **any value within a range**. These are used for metrics such as time on site, revenue per user, or session duration.

#### Normal Distribution

A symmetric, bell-shaped curve where values are distributed evenly around the mean. Commonly used due to the Central Limit Theorem.

**Formula:** \(f(x) = \frac{1}{\sqrt{2\pi\sigma^2}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}\)

**Example:** Modeling the distribution of time spent per session across users.

---

#### Exponential Distribution

Used to model the time between **independent events** that occur at a constant average rate.

**Formula:** \(f(x; \lambda) = \lambda e^{-\lambda x},\ x \geq 0\)

**Example:** Modeling time between video plays on Facebook Watch.

---

#### Uniform Distribution

Assumes all values in a given range are **equally likely** to occur.

**Formula:** \(f(x) = \frac{1}{b-a},\ a \leq x \leq b\)

**Example:** Random time within an hour when a notification is sent


---

## 5. Hypothesis Testing (Statistical significance)

### Null Hypothesis (H₀)

Assumes no effect or change exists.\
**Example:** No change in DAU after feature launch

### Alternative Hypothesis (H₁)

Assumes there is a meaningful effect/change.

### P-value

Probability of observing results at least as extreme assuming H₀ is true.\
**Rule:** Reject H₀ if \(p < \alpha\)

### Test Statistic

Measures standardized difference between groups.\
**Formula:** \(t = \frac{\bar{x}_1 - \bar{x}_2}{\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}\)\
**Example:** Compare post frequency by age group

---

## 6. Regression (Modeling relationships)

### Linear Regression

Models relationship between dependent and one independent variable.\
**Formula:** \(Y = \beta_0 + \beta_1 X + \epsilon\)\
**Example:** Predict comments from post views

### Multiple Regression

Models dependent variable with multiple predictors.\
**Formula:** \(Y = \beta_0 + \beta_1 X_1 + ... + \beta_k X_k + \epsilon\)\
**Example:** Predict ad revenue from age, device, clicks

### Logistic Regression

Used for binary outcome predictions.\
**Formula:** \(\log \left( \frac{p}{1-p} \right) = \beta_0 + \beta_1 X\)\
**Example:** P(user makes in-app purchase)

---

## 7. A/B Testing (Experimentation & inference)

### Confidence Interval

Range in which population parameter likely falls.\
**Formula:** \(\bar{x} \pm t_{\alpha/2, n-1} \cdot \frac{s}{\sqrt{n}}\)\
**Example:** CI for post likes after UI change

### Statistical Power

Probability of detecting a true effect (\(1 - \beta\)).\
**Example:** Detect 5% lift in story taps

False positive
False negative

---

## 8. Additional Topics

### Chi-Square Test

Used for categorical data independence.\
**Example:** Independence of reaction type vs. region

### ANOVA

Compares means across 3+ groups.\
**Example:** Compare time spent across device types

### Interaction Effects

Checks whether combined variable effects differ.\
**Example:** Impact of ad frequency by age group

### Multicollinearity

Occurs when predictors are highly correlated.\
**Definition:** Use VIF to detect.\
**Example:** Session time & screen count

### Time Series Analysis

Analysis of trends over time.\
**Example:** DAU trend after policy update

### Randomized Controlled Trials (RCTs)

Gold standard for causal inference.\
**Example:** Rollout of new Explore page

### Asymmetric Experiments

Different test/control sizes for efficient experimentation.\
**Example:** Holdout of 6% users from PYMK update

