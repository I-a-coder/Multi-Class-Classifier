# 🧠 Multi-Task Human Attribute Classification  
**Assignment 3B – R**

**Author:** Sadia Shafeeq  
**Roll No:** BSAI23009  

---

## 📌 Project Overview

This project implements a **multi-task deep learning model** to predict multiple human attributes from a single image.  
Instead of training separate models for each task, a **shared ResNet backbone** is used to jointly learn:

- Gender  
- Upper Body Clothing Color  
- Lower Body Clothing Color  

Multi-task learning improves efficiency by sharing visual features across related tasks.

---

## 🎯 Tasks & Classes

### 1️⃣ Gender Classification
- Male  
- Female  
- N/V (Not Visible)

### 2️⃣ Upper Body Clothing Color
- Black  
- White  
- Gray  
- Brown  
- Green  
- Blue  
- Pink  
- N/V (Not Visible)

### 3️⃣ Lower Body Clothing Color
- Black  
- White  
- Gray  
- Brown  
- Green  
- Blue  
- N/V (Not Visible)

---

## 🗂 Dataset Description

- The dataset consists of cropped images of individuals.
- Labels are provided via a CSV file.
- Each image has three labels:
  - Gender
  - Upper clothing color
  - Lower clothing color
- Class imbalance exists, especially in clothing color categories.

---

## 🏗 Model Architecture

- **Backbone:** ResNet (Transfer Learning)
- **Shared Feature Extractor**
- **Three Classification Heads:**
  - Gender Head
  - Upper Color Head
  - Lower Color Head
- **Loss Function:** Categorical Cross-Entropy (per task)
- **Total Loss:** Sum of all task losses
- **Optimizer:** Adam
- **Learning Rate:** 0.001

---

## 📈 Training Details

- Multi-task training performed over multiple epochs
- Stable convergence observed
- Gradual improvement in accuracy for all tasks
- Training curves include:
  - Total Loss
  - Gender Accuracy
  - Upper Color Accuracy
  - Lower Color Accuracy

---

## 📊 Evaluation Metrics

Performance is evaluated using **Weighted Average F1-Score**, which accounts for class imbalance.

### 🔹 Final Results

- **Gender:** 0.7980  
- **Upper Clothing Color:** 0.6995  
- **Lower Clothing Color:** 0.6553  

---

## 🧪 Key Observations

- Gender classification achieved the highest performance
- Clothing color prediction is more challenging due to visual variability
- Multi-task learning successfully balances performance across all tasks

---

## 🚀 Future Improvements

- Class rebalancing techniques
- Stronger data augmentation
- Fine-tuning deeper backbone layers
- Experimenting with attention mechanisms

---

## 📄 Report

A detailed project report is included in the repository:
