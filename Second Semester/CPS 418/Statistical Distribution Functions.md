
---

### 🔍 **Unit 5: Statistical Distribution Functions – Summary**

#### 📌 **1. What You’ll Learn (ILOs)**

* Understand what statistics and statistical distributions are
* Calculate **mean, median, mode, range, standard deviation**
* Explain **normal distribution**, **z-scores**, **percentiles**, and **skewness**
* Visualize data with **bar graphs**, **histograms**, and **pie charts**

---

#### 📊 **2. Key Concepts**

* **Statistics**: The science of collecting, analyzing, and interpreting data.
* **Statistical Distribution**: Shows how often each outcome appears (e.g., how many A's, B's, etc. in test scores).

---

#### 🧮 **3. Measures of Central Tendency**

* **Mean**: Average of data
* **Median**: Middle value (or average of middle two)
* **Mode**: Most frequent value

#### 📐 **4. Measures of Variation**

* **Range**: Difference between max and min
* **Standard Deviation**: How far each value is from the mean (on average)

---

#### 📊 **5. Visualizing Data**

* **Bar Graph**: Compares different values
* **Double Bar Graph**: Compares two groups (e.g., boys vs. girls)
* **Histogram**: Shows frequency within intervals
* **Pie Chart**: Shows proportions as parts of a circle

---

#### 🔢 **6. Types of Distributions**

* **Discrete**: Countable outcomes (like number of children)
* **Continuous**: Infinite possibilities within a range (like height)

---

#### 🔔 **7. Normal Distribution**

* **Bell-shaped curve**; most values around the mean
* Defined by:

  * Mean (µ) = center
  * Standard Deviation (ζ) = spread
* Formula:

  $$
  Y = \frac{1}{ζ \sqrt{2π}} e^{-\frac{(x - µ)^2}{2ζ^2}}
  $$

---

#### 🧮 **8. Standard Normal Distribution**

* A special case: mean = 0, SD = 1
* Convert any normal variable X to z-score:

  $$
  z = \frac{X - µ}{ζ}
  $$

---

#### 📈 **9. Real-World Applications**

* Convert scores/data to **z-scores**
* Use **z-tables** to find probabilities
* Examples: Ada's test score, lifespan of a lightbulb

---

#### ↩️ **10. Skewness**

* **Right Skew (Positive)**: Long tail to the right
* **Left Skew (Negative)**: Long tail to the left
* **Pearson’s Skewness**:

  * 1st coefficient: $(\text{Mean} - \text{Mode}) / SD$
  * 2nd coefficient: $3(\text{Mean} - \text{Median}) / SD$

---

#### 🎯 **11. Percentiles**

* A **percentile** tells you what percent of the data is below a given value
  (e.g., 80th percentile = better than 80% of scores)

---

#### 🎲 **12. Discrete Probabilities**

* Example: 5 A’s, 2 B’s out of 10 →
  P(A or B) = (5+2)/10 = 0.7

---

#### 📉 **13. Probability & Normal Curve**

* Area under curve = 1
* Probability of *exact* value = 0
* Probabilities found as area *under* the curve between ranges

---

#### ✅ **Self-Assessment Highlights**

* Understand how and why we convert to **z-scores**
* Differentiate **discrete vs. continuous**
* Calculate skewness using given data
* Practice computing mode, median, and mean deviation


---
**Binomial Probability Formula**, which gives the probability of getting exactly $r$ successes in $n$ independent Bernoulli trials, where each trial has a success probability of $p$. The formal expression is:

$$
P(X = r) = \binom{n}{r} p^r (1 - p)^{n - r}
$$

### Where:

* $P(X = r)$ is the probability of getting exactly $r$ successes,
* $\binom{n}{r}$ is the **binomial coefficient**: $\frac{n!}{r!(n - r)!}$,
* $p$ is the probability of success on a single trial,
* $(1 - p)$ is the probability of failure on a single trial,
* $n$ is the number of trials,
* $r$ is the number of successful trials.

### Example:

If you flip a fair coin (so $p = 0.5$) 5 times ($n = 5$), the probability of getting exactly 3 heads ($r = 3$) is:

$$
P(X = 3) = \binom{5}{3} (0.5)^3 (1 - 0.5)^{5 - 3} = 10 \cdot (0.125) \cdot (0.25) = 0.3125
$$

---
The **Poisson distribution** models the probability of a given number of events occurring in a fixed interval of time or space, assuming these events happen independently and at a constant average rate.

### **Poisson Probability Formula:**

$$
P(X = r) = \frac{\lambda^r e^{-\lambda}}{r!}
$$

### Where:

* $P(X = r)$ is the probability of observing exactly $r$ events,
* $\lambda$ is the average number of events in the given time/space interval (called the **rate parameter**),
* $e$ is the base of the natural logarithm (approximately 2.71828),
* $r$ is the number of occurrences (a non-negative integer: $r = 0, 1, 2, \dots$),
* $r!$ is the factorial of $r$.

---

### **When to Use Poisson Distribution:**

Use Poisson when:

* Events occur independently,
* Events occur at a constant average rate,
* Two events cannot occur at the exact same time,
* You're counting **how many events** occur in a given interval (not just success/failure).

---

### **Example:**

If a call center receives an average of $\lambda = 4$ calls per hour, the probability of receiving exactly 2 calls in an hour is:

$$
P(X = 2) = \frac{4^2 e^{-4}}{2!} = \frac{16 \cdot e^{-4}}{2} \approx \frac{16 \cdot 0.0183}{2} \approx 0.1465
$$

