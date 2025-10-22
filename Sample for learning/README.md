# 🧠 My Personal Note about Active Learning in Machine Learning

## 🔹 Definition
**Active learning** is a machine learning technique where the model itself chooses which data points it wants to learn from.  
Instead of training on a large, fully labeled dataset, the model *interactively queries* an **oracle** (usually a human annotator) to label only the most informative or uncertain examples.

This helps the model reach high performance with **less labeled data**, which is especially useful when labeling is expensive or time-consuming.

---

## 🔹 Why It’s Used
Labeling large datasets is costly — think of tagging thousands of images or medical scans.  
Active learning reduces this burden by letting the algorithm decide **which samples will provide the most useful information** if labeled.

---

## 🔹 How It Works
1. Start with a small labeled dataset and a large pool of unlabeled data.  
2. Train a model on the labeled data.  
3. Select the most uncertain or informative samples from the unlabeled pool (using a query strategy).  
4. Ask a human or system to label those samples.  
5. Add the newly labeled samples to the training set.  
6. Repeat until performance is satisfactory or the labeling budget is used up.

---

## 🔹 Common Query Strategies
- **Uncertainty Sampling:** Choose data where the model is least confident (e.g., predictions near 50% probability).  
- **Query-by-Committee:** Use multiple models and select samples they disagree on.  
- **Expected Model Change:** Pick samples that would most change the model if labeled.  
- **Expected Error Reduction:** Pick samples that would most reduce future prediction error.

---

## 🔹 Benefits
- 💰 Reduces labeling costs  
- ⚡ Speeds up learning  
- 🎯 Focuses annotation on the most valuable data points  

---

## 🔹 Reference Article
- [Active Learning (Wikipedia)](https://en.wikipedia.org/wiki/Active_learning_(machine_learning))  
- [Label Propagation digits: Active learning (example notebooks)](https://scikit-learn.org/stable/auto_examples/semi_supervised/plot_label_propagation_digits_active_learning.html)  
- [“Active Learning Literature Survey” by Burr Settles (University of Wisconsin–Madison, 2009)](https://burrsettles.com/pub/settles.activelearning.pdf)  
- [A Gentle Introduction to Active Learning — Medium](https://arindam-dey.medium.com/a-gentle-introduction-to-active-learning-e983b9d175cb)  

---

📘 *Active learning helps create efficient, cost-effective ML systems by teaching models to ask for the most useful data — just like curious humans do!*
