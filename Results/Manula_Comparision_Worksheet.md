---

# **Manual Code Comparison Methodology

(Used for Subset Analysis of 100 Stack Overflow and ChatGPT Answers)**

This document describes the procedure we followed to manually compare a subset of code solutions taken from Stack Overflow and ChatGPT. The purpose of this analysis was to evaluate code quality and security characteristics through a structured and reproducible assessment process.

The analysis was conducted on **100 paired answers** (i.e., the accepted/most relevant Stack Overflow answer and the corresponding ChatGPT answer to the same programming question).

---

## **1. Goal of the Manual Analysis**

The main objective of this evaluation was:

* To compare code produced by human developers (Stack Overflow) and by an AI system (ChatGPT).
* To assess each solution using a consistent set of criteria related to:

  1. **Code Quality**
  2. **Security**

This manual assessment complements our static analysis (Bandit, Pylint, Semgrep, PMD) by providing an interpretive evaluation of clarity, maintainability, safety practices, and overall implementation quality.

---

## **2. Evaluation Framework**

Each pair of solutions was evaluated independently before comparison.
The assessment framework consisted of two main dimensions, each weighted equally.

---

### **A. Code Quality Assessment (50% weight)**

For each solution, we examined:

1. **Code Structure and Organization**

   * Logical flow
   * Clear separation of tasks
   * Appropriate use of language features

2. **Readability and Naming Conventions**

   * Meaningful variable and function names
   * Spacing, formatting, and adherence to style guidelines (e.g., PEP 8 for Python)

3. **Documentation and Comments**

   * Presence of explanatory comments
   * Clarity of example usage

4. **Error Handling and Robustness**

   * Presence of exception handling or input checks
   * defensive coding practices

5. **Maintainability and Complexity**

   * Avoidance of overly complex or nested logic
   * Modularity and reusability of functions

6. **Best Practice Compliance**

   * Use of recommended patterns and idioms for the language
   * Avoidance of deprecated or dangerous constructs

---

### **B. Security Assessment (50% weight)**

Each solution was examined for:

1. **Input Validation and Sanitization**

   * Checks for unsafe or malformed input
   * Appropriate type validation

2. **Use of Secure APIs and Libraries**

   * Avoiding insecure function calls
   * Proper use of safe alternatives

3. **Confidentiality and Data Handling**

   * Absence of hardcoded secrets
   * Safe handling of file paths, environment data, or sensitive information

4. **Exposure to Common Vulnerability Patterns**

   * Injection risks
   * Resource mismanagement
   * Unsafe code constructs

5. **Error Handling and Information Disclosure**

   * Avoiding overly verbose error messages
   * Prevention of sensitive data leaks

6. **General Defensive Programming**

   * Safe defaults
   * Boundary checking
   * Secure configuration choices

---

## **3. Language-Specific Guidance**

To maintain consistency across programming languages, the following principles were used:

### **Python**

* We aligned our assessment with the types of issues typically flagged by:

  * **Pylint** for code quality
  * **Bandit** for security
* Particular attention was paid to:

  * PEP 8 compliance
  * Use of context managers
  * Unsafe imports
  * Injection vulnerabilities

### **Java**

* We aligned our assessment with patterns commonly identified by:

  * **PMD** for quality
  * **Semgrep** for security
* We evaluated:

  * Class design
  * Exception handling
  * Resource management
  * Potential taint-flow weaknesses

---

## **4. Scoring Procedure**

Each solution received two scores:

* **Code Quality Score (1–10)**
* **Security Score (1–10)**

Scoring Guidelines:

* **10–8**: Excellent, follows best practices, minimal issues
* **7–5**: Reasonable, but with notable shortcomings
* **4–2**: Weak, multiple bad practices or unsafe patterns
* **1**: Very poor or fundamentally unsafe

A **weighted average** was computed:

```
weighted_score = (quality_score * 0.5) + (security_score * 0.5)
```

This produced a final combined score for each solution.

---

## **5. Comparison and Winner Determination**

Once both solutions were scored independently:

1. We calculated the **difference in weighted averages**.
2. The higher score was considered the better solution.

**Tie Criteria:**
If the final scores differed by **≤ 0.25**, or if both weighted averages were exactly equal, the pair was recorded as a tie.
In such cases, we documented the specific strengths and weaknesses of both solutions that led to a balanced outcome.

---

## **6. Documentation Format**

For each pair, we recorded:

* Detected programming language
* Stack Overflow quality and security scores
* ChatGPT quality and security scores
* Weighted averages
* Winner (Human / AI / Tie)
* An explanation summarizing:

  * Key quality characteristics
  * Security findings
  * Reasons for the final decision

This produced a structured CSV file containing the manually analyzed results.

---
* A PDF version of this document
* A sample row from the CSV (with anonymized content)

Just let me know.
