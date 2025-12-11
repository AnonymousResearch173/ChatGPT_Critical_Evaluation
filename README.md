---

# Repository Overview

This repository provides the complete dataset, analysis scripts, survey material, manual evaluation guidelines, and experimental results used in our study comparing ChatGPT-generated code with accepted Stack Overflow answers across quality, security, and developer perception dimensions. The repository is organized into multiple folders, each containing specific resources and artifacts used throughout the study.

---

## Folder Structure and Description

### 1. **community/**

This directory contains all resources related to the community-driven analysis of developer discussions.

* **raw/**
  Includes raw text threads collected from Stack Overflow and Reddit that were used for community sentiment and comment analysis.

* **labeled_comments.csv**
  Contains manually labeled developer comments used for qualitative and quantitative analysis.

* **annotation_guideline.md**
  Describes the annotation scheme, labeling criteria, and the process followed to categorize community comments.

---

### 2. **technical/**

This directory contains the primary dataset of code solutions and preprocessing material used for the technical evaluation.

* **ChatGPT/**
  Contains 4,000 ChatGPT-generated answers (2,000 Python and 2,000 Java).

* **StackOverflow/**
  Contains 4,000 accepted Stack Overflow answers (2,000 Python and 2,000 Java).

* **sql_query_java.txt**
  The SQL query used to fetch Java questions and their accepted answers from Stack Overflow.

* **sql_query_python.txt**
  The SQL query used to fetch Python questions and accepted answers.

* **preprocessing.ipynb**
  Notebook containing the preprocessing pipeline applied to Stack Overflow posts before analysis.

---

### 3. **survey_details/**

Material related to the developer survey conducted as part of the study.

* **google_form_link.txt**
  Provides the URL of the survey form distributed across academic and industry participants.

* **survey_results.xlsx**
  The anonymized dataset of all survey responses, including demographic information and detailed feedback on AI tool usage.

---

### 4. **evaluation_script/**

Scripts and notebooks used to execute static analysis across languages.

* **static_analysis.ipynb**
  Notebook implementing evaluation using Bandit and Pylint for Python, and PMD and Semgrep for Java.
  Includes complete code for executing tool-based analysis at scale.

---

### 5. **sampling_test/**

Contains the documentation and experiments related to statistical sampling reliability checks.

* **README.md**
  Explains the sampling strategy, rationale, and statistical verification methodology.

* **sampling_test.ipynb**
  Notebook demonstrating the sampling experiments and validating sample representativeness.

---

### 6. **manual_subset_analysis/**

Contains the material used for the manual evaluation of a subset of code pairs.

* **manual_comparison_guideline.md**
  A structured guideline describing how manual comparisons were conducted, including evaluation criteria for code quality and security.

* **manual_subset.csv**
  The subset of question–answer pairs (both ChatGPT and Stack Overflow) that were manually analyzed using the guideline.

---

### 7. **results/**

Contains the detailed outputs from the full static analysis across all tools.

* **bandit_results/**
* **pylint_results/**
* **semgrep_results/**
* **pmd_results/**

Each folder includes tool-generated reports, aggregated findings, and structured summaries used in the technical analysis section of the study.

---

## How to Cite

If you use this dataset, evaluation scripts, or analysis guidelines in your research, please cite our accompanying paper (details to be added upon publication).

---
