---

# **Annotation Guidelines for Developer Comment Analysis**

This document describes the annotation procedure used for labeling developer comments from community forum threads. It is intended for student annotators and for researchers who wish to understand or reproduce our labeling process.

---

## **1. Overview of Annotation Process**

The goal of annotation is to assign each comment:

1. **An Overall Sentiment**
2. **An Extended Emotion Label**
3. **Additional Notes (Optional)**
4. **Perceived Preference** (SO / ChatGPT / None)
5. **Content-Type Tags** (Use-case advice, critique, technical details, etc.)

This labeling scheme is adapted from a standard tree-based emotional taxonomy used in prior work, but simplified into broader usable categories for technical discussions. We collapsed the original multi-level hierarchy into **two columns**:
(1) A **Primary Sentiment Category**
(2) A set of **Associated Emotions**, including extensions drawn from our own dataset.

Annotations were performed by three computer science undergraduates with >3 years of coding experience. The first author jointly annotated the first 100 comments with them. The rest (900 comments) were independently annotated by all annotators, followed by majority voting. Fleiss’ Kappa = **0.723**.

---

## **2. Primary Sentiment Categories**

Annotators must classify each comment into one of the following:

* **Positive**
* **Negative**
* **Neutral**
* **Mixed**
* **Not Clear**

*Note:*
“Neutral” and “neutral” were merged.
Mixed sentiments were used when opposing emotions co-occurred.

---

## **3. Extended Emotion Labels**

Extended labels allow more fine-grained understanding of what the user expresses.
Annotators may assign multiple emotions if present (e.g., *“Frustration + Caution”*).

Below is the **merged and cleaned** emotional taxonomy used in our project.
It merges:

* Canonical emotion groups from the reference study
* All additional emotions found in your 269 unique dataset labels
* Removal of duplicates, spelling inconsistencies, combinations, and long descriptive strings
* Collapsing of multi-word hybrid expressions into parent-level categories

---

## **4. Final Emotion Taxonomy (Collapsed Two-Column Format)**

### **Table 1. Emotion Categories**

| **Primary Category** | **Combined Emotion Labels (Merged and Cleaned)**                                                                                                                                                                                                                    |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Positive**         | Affirmation, Appreciation, Joy, Relief, Optimism, Hope, Support, Praise, Agreement, Enthusiasm, Confidence, Encouragement, Humor (positive), Surprise (positive), Enthrallment, Gratitude                                                                           |
| **Negative**         | Frustration, Caution, Skepticism, Concern, Disagreement, Criticism, Disapproval, Pessimism, Toxicity, Abuse, Rudeness, Anger, Irritation, Sarcasm, Disgust, Disappointment, Fear, Anxiety, Worry, Distress, Alarm, Confusion, Negativity toward SO or AI, Hostility |
| **Neutral**          | Clarification, Pragmatism, Technical Explanation, Informative, Balanced, Analytical, Descriptive, Factual, Recommendation, Use-case Context                                                                                                                         |
| **Mixed**            | Any combination of the above, e.g., “Frustration + Joy”, “Caution + Appreciation”, “Relief + Concern”, “Sarcasm + Humor”, etc. Annotators should mark the dominant emotions but preserve multiple labels.                                                           |
| **Not Clear**        | Used when the comment is too short, ambiguous, off-topic, or uninterpretable.                                                                                                                                                                                       |

---

### **Notes on Merging**

1. Many dataset labels combined emotion strings (e.g., *“Frustration, Caution, Pragmatism”*).
   These were treated as **Multi-Emotion Labels** but mapped to the parent categories above.

2. Variants like *“Frustation”*, *“frustration, cautious”*, *“frustration, critical”*, etc. were merged into **Frustration** or **Frustration + Caution**.

3. Negative tones such as *“Abusive”, “Toxic”, “Rude”, “Judgmental”, “Dismissive”* were grouped under **Toxicity/Abuse** unless clarifying context required a secondary label.

4. Long descriptive “sentiment essays” from your dataset were abstracted into core categories (e.g., skepticism, caution, frustration, appreciation).

---

## **5. Additional Notes (Optional Field)**

Annotators also assigned secondary meta-labels capturing content or interaction type:

### **Common Additional Notes**

* Use-case Advice
* Technical Details
* Critique (of ChatGPT, SO, both)
* Negative Experience of SO Community
* Insensitive or Abusive Behavior
* Policy or Moderation Discussion
* Detailed Analysis
* Clarification Request
* Recommendation or Suggestion

These were tagged **only when explicitly present** in the comment.

---

## **6. Preference Labeling**

Each comment was also marked for expressed preference:

* **Prefers ChatGPT**
* **Prefers Stack Overflow**
* **No clear preference**
* **Balanced view**

Annotators used explicit linguistic cues (“ChatGPT is better for…”, “SO answers are more reliable…”, etc.).

---

## **7. Annotation Instructions for Students**

1. **Read the entire comment carefully.**
   Understand whether the user is expressing a reaction, an evaluation, or simply giving technical information.

2. **Assign the Overall Sentiment**
   Look at the general tone:

   * Positive
   * Negative
   * Neutral
   * Mixed
   * Not clear

3. **Assign Extended Emotions**
   Pick the closest parent categories from Table 1.
   Multiple tags are allowed.

4. **Add Additional Notes** (Optional)
   Use only if explicit in the comment.

5. **Assign Preference** if the comment compares SO and ChatGPT.

6. **Avoid overthinking labels.**
   The goal is consistent categorization, not psychological diagnosis.

---

## **8. Example Annotation**

| Comment                                                     | Overall Sentiment | Extended Emotions    | Additional Notes  | Preference          |
| ----------------------------------------------------------- | ----------------- | -------------------- | ----------------- | ------------------- |
| “ChatGPT is fast but often wrong. I trust SO answers more.” | Mixed             | Frustration, Caution | None              | Prefers SO          |
| “Thanks! This worked perfectly.”                            | Positive          | Joy, Appreciation    | None              | None                |
| “Your example is missing imports. This won’t run.”          | Negative          | Frustration          | Technical details | None                |
| “Both sources have value depending on the task.”            | Neutral           | Balanced, Pragmatic  | None              | No clear preference |

---
