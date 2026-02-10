# 🧠 SemEval 2025 Task 9 – Food Hazard Detection (JU-NLP)

## 🚀 Project Overview
This repository contains our official submission to **SemEval 2025 – Task 9: Food Hazard Detection**, developed by the **JU-NLP** team.  
The project applies **Transformer-based NLP models** to automatically detect **food-related hazards and affected products** from unstructured text such as regulatory reports, scientific articles, and food safety documents.

Participation in SemEval demonstrates applied research capability, competitive benchmarking, and real-world NLP problem solving.

📄 **Paper:** *JU-NLP at SemEval-2025 Task 9: Innovative Computational Methods for Food Hazard Detection*  
🏆 **Final Rank:** **25th place** in both sub-tasks

---

## 🏆 Task Description
**Competition:** SemEval 2025  
**Task:** Task 9 – The Food Hazard Detection Challenge  
**Domain:** Natural Language Processing (NLP)

### 🔹 SubTask 1 – Food Hazard & Product Classification
- Predict **hazard categories** and **product categories**
- Multi-class text classification problem

### 🔹 SubTask 2 – Hazard & Product Detection
- Identify the **exact hazard** and **affected product**
- Requires fine-grained semantic understanding

Challenges include **domain-specific terminology**, **data imbalance**, and **noisy real-world text**.

---

## 📊 Dataset Description
- **Training samples:** 5,082  
- **Additional samples:** 997  
- **Data sources:**
  - Regulatory and safety reports
  - Scientific literature
  - Public and social data

The dataset supports prediction of:
- Hazard categories
- Product categories
- Specific hazards
- Specific products

**Preprocessing steps:**
- Tokenization
- Stop-word removal
- Text normalization
- Label encoding

---

## 🧠 Methodology & System Architecture
We adopt a **Transformer-based deep learning approach** using **BERT (bert-base-uncased)**.

### 🔹 Modeling Strategy
Separate BERT classifiers are fine-tuned for:
- Hazard category prediction
- Product category prediction
- Hazard detection
- Product detection

Independent fine-tuning reduces task interference and improves category-specific learning.

### 🔹 Training Configuration
- Tokenizer: BERT tokenizer (Hugging Face)
- Optimizer: AdamW
- Loss Function: Cross-Entropy Loss
- Batch Size: 8
- Epochs: 3
- Learning Rate Scheduler: Linear (no warm-up)
- Frameworks: PyTorch, Hugging Face Transformers

GPU acceleration was used during training.

---

## 📈 Results & Performance

### ✅ SubTask 1 – Classification
- **Overall Accuracy:** 84%
- **Macro F1-Score:** 0.62

Strong performance on major classes:
- **Biological hazards:** F1 = 0.91
- **Allergens:** F1 = 0.88
- **Meat, egg & dairy products:** F1 = 0.89

Lower performance on rare classes due to data imbalance.

---

### ⚠️ SubTask 2 – Detection
- **Test Accuracy:** 0.23
- **F1-Score:** 0.04

This task proved challenging due to:
- Overlapping hazard mentions
- Fine-grained entity boundaries
- Limited labeled samples

---

## 📁 Project Structure
