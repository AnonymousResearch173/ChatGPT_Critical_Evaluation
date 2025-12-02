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

using descriptive statistics and the **KS-test**.

---

## 📊 2. Python Results

### **Score**

* Population mean: **1.89**
* Sample mean: **6.45**
* Deviation (Δ%): **+242.05%**
* KS-test p-value: **0.0000**

**Interpretation:**
The sample contains Python questions with **much higher scores** compared to the population.
The KS-test p-value near zero indicates the distributions differ significantly.

---

### **Code Length**

* Population mean: **34.36**
* Sample mean: **36.35**
* Deviation (Δ%): **+5.79%**
* KS-test p-value: **0.0246**

**Interpretation:**
Code length in the sample is only slightly higher than the population average.
KS-test p-value (~0.02) indicates a small but statistically significant difference, though practically the deviation is minor.

---

## 📊 3. Java Results

### **Score**

* Population mean: **2.03**
* Sample mean: **2.28**
* Deviation (Δ%): **+12.17%**
* KS-test p-value: **0.0000**

**Interpretation:**
Java score distribution differs between sample and population, but the **mean deviation is small** (~12%).

---

### **Code Length**

* Population mean: **41.71**
* Sample mean: **42.28**
* Deviation (Δ%): **+1.37%**
* KS-test p-value: **0.0380**

**Interpretation:**
The code-length distribution is nearly identical between sample and population.
Although the p-value indicates statistical difference, the **practical deviation is negligible**.

---

## 🧪 4. What the KS-test Tells Us

The Kolmogorov–Smirnov test measures whether two distributions differ **in shape**.

* **p < 0.05** → distributions are statistically different
* But **statistical significance ≠ practical significance**, especially with large populations

In our case:

* Python/Java **code length** distributions are very close in practice
* Python scores differ substantially
* Java scores differ mildly

Large populations (20k–25k) make even small differences statistically significant.

---

## 📌 5. Summary: Is the Sample Representative?

### **Python**

* **Score** over-represented (bias toward popular questions)
* **Code length** nearly representative

### **Java**

* **Score** slightly over-represented
* **Code length** representative

### **Overall Conclusion**

The sample is **reasonably representative** in terms of **code length**, which is central to your study (≥15 lines filter).
However, the sample tends to **favor higher-scored questions**, especially in Python, which should be noted as a mild sampling bias.

---
---
