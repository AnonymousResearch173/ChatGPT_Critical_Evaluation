---

# README: Statistical Validation of Sampling Strategy

## 📌 1. Background

We began with all Stack Overflow questions that satisfy:

* The programming language tag is **Python** or **Java**
* The accepted answer contains **≥ 15 lines of code**

The filtered dataset size:

| Language  | Total Questions |
| --------- | --------------- |
| Python    | 20,000          |
| Java      | 5,300           |
| **Total** | **25,300**      |

From this large population, a **sample of 2,000 questions** was drawn for the main study.

To verify whether this sample is representative, we compare:

* **score** (upvotes on the question)
* **code_length** (number of code lines in accepted answer)

using descriptive statistics and the **Kolmogorov–Smirnov (KS) test**.

---

## 📊 2. Python Results

### **Score**

* Population mean: **1.89**
* Sample mean: **6.45**
* Δ (%): **+242.05%**
* KS-test p-value: **0.0000**

**Interpretation:**
Sample contains significantly higher-scored Python questions.
Large difference both statistically and practically.

---

### **Code Length**

* Population mean: **34.36**
* Sample mean: **36.35**
* Δ (%): **+5.79%**
* KS-test p-value: **0.0246**

**Interpretation:**
The sample slightly over-represents longer Python code answers.
Practical difference is small.

---

## 📊 3. Java Results

### **Score**

* Population mean: **2.03**
* Sample mean: **2.28**
* Δ (%): **+12.17%**
* KS-test p-value: **0.0000**

**Interpretation:**
Distributions differ statistically, but the score deviation is small.

---

### **Code Length**

* Population mean: **41.71**
* Sample mean: **42.28**
* Δ (%): **+1.37%**
* KS-test p-value: **0.0380**

**Interpretation:**
Code-length distribution is extremely close to population.
Statistical significance due to large sample size; practical difference negligible.

---

## 🧪 4. Understanding the KS Test

The **Kolmogorov–Smirnov test** checks whether two distributions differ in shape.

* **p < 0.05** → statistically significant difference
* But with very large datasets (20k+), *tiny practical differences* can still produce significant p-values.

Thus, interpretation must combine:

* Statistical significance
* Practical effect size (Δ%)

---

## 📌 5. Is the Sample Representative?

### **Python**

* Score distribution: biased toward higher-scored posts
* Code-length distribution: close enough for practical purposes

### **Java**

* Score: slightly higher scores in sample
* Code length: very representative

### **Overall Conclusion**

The sample of **2,000 posts** is reasonably representative of the **code-length characteristics** of the 25k-post population — which is the critical metric given the ≥15-line inclusion criterion.

Scores show some upward bias (especially for Python), which should be mentioned as a mild sampling limitation.

---



---

