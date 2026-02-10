# 🧠 SemEval 2025 Task 9 – Food Hazard Detection (JU-NLP)

## 🚀 Project Overview
This repository presents our official **SemEval 2025 Task 9** system submission: **Food Hazard Detection**, developed under the **JU-NLP** team. The project focuses on applying **Transformer-based NLP models** to automatically detect **food-related hazards and affected products** from unstructured textual data such as regulatory reports, scientific articles, and public safety documents.

SemEval is a globally respected NLP evaluation campaign, and participation demonstrates applied research skills, competitive benchmarking, and real-world problem solving. This project highlights my hands-on experience with **NLP, deep learning, and transformer fine-tuning** on a domain-specific task.

📄 **Paper:** *JU-NLP at SemEval-2025 Task 9: Innovative Computational Methods for Food Hazard Detection*  
🏆 **Final Rank:** 25th place in both sub-tasks

---

## 🏆 Task Description
**Competition:** SemEval 2025 – Task 9  
**Task Name:** The Food Hazard Detection Challenge  
**Problem Domain:** Natural Language Processing (NLP)

The task consists of two sub-tasks:

### 🔹 SubTask 1 – Food Hazard & Product Classification
- Predict **hazard categories** and **product categories** from incident titles and descriptions
- Multi-class text classification problem

### 🔹 SubTask 2 – Hazard & Product Detection
- Identify the **exact hazard** and **affected product** mentioned in text
- Fine-grained semantic understanding and entity-level prediction

The challenge emphasizes robust modeling under **data imbalance**, **domain-specific terminology**, and **real-world noisy text**.

---

## 📊 Dataset Description
- **Training Samples:** 5,082
- **Additional Samples:** 997
- **Sources:**
  - Regulatory reports
  - Scientific literature
  - Social media and public safety data

The dataset supports structured prediction for:
- Hazard categories
- Product categories
- Specific hazards
- Specific products

Preprocessing includes:
- Tokenization
- Stop-word removal
- Text normalization
- Label encoding for multi-class learning

---

## 🧠 System Architecture & Methodology

We adopt a **Transformer-based deep learning approach** using **BERT (bert-base-uncased)** for multi-label and multi-task text classification.

### 🔹 Modeling Strategy
- Separate BERT-based classifiers for:
  - Hazard category prediction
  - Product category prediction
  - Hazard detection
  - Product detection
- Each model fine-tuned independently to reduce inter-task interference

### 🔹 Training Details
- Tokenizer: Hugging Face BERT tokenizer
- Optimizer: AdamW
- Loss Function: Cross-Entropy Loss
- Batch Size: 8
- Epochs: 3
- Learning Rate Scheduler: Linear scheduler (no warm-up)
- Frameworks: PyTorch, Hugging Face Transformers

GPU acceleration was used to improve training efficiency and scalability.

---

## 📈 Results & Performance

### ✅ SubTask 1 – Classification Performance
- **Overall Accuracy:** 84%
- **Macro F1-Score:** 0.62
- Strong performance on well-represented classes:
  - Biological hazards: **F1 = 0.91**
  - Allergens: **F1 = 0.88**
  - Meat, egg & dairy products: **F1 = 0.89**

Performance drops were observed for underrepresented classes due to data imbalance.

### ⚠️ SubTask 2 – Detection Performance
- **Test Accuracy:** 0.23
- **F1-Score:** 0.04

This sub-task proved significantly more challenging due to:
- Overlapping hazard mentions
- Fine-grained entity identification
- Limited labeled examples

---

## 📁 Project Structure
```
├── data/               # Training, validation, and test datasets
├── notebooks/          # EDA and experimentation
├── src/                # Training and inference scripts
├── models/             # Fine-tuned BERT checkpoints
├── results/            # Predictions and evaluation reports
├── requirements.txt    # Project dependencies
└── README.md           # Project documentation
```

---

## ⚙️ How to Run
```bash
# Clone the repository
git clone https://github.com/your-username/semeval-2025-task9-food-hazard.git
cd semeval-2025-task9-food-hazard

# Install dependencies
pip install -r requirements.txt

# Train models
python src/train.py

# Run inference
python src/predict.py
```

---

## 📌 Key Learnings
- Practical experience with **Transformer fine-tuning**
- Handling **imbalanced, real-world NLP datasets**
- Building **modular ML pipelines** for research tasks
- Evaluating systems using **SemEval benchmark metrics**

---

## ⚠️ Limitations
- Dependency on general-purpose pre-trained BERT
- High computational cost
- Limited generalization for rare classes
- Sequential fine-tuning does not exploit task interdependencies

---

## 🔮 Future Work
- Domain-specific or multilingual pre-training
- Data augmentation (SMOTE, GAN-based synthesis)
- Multi-task learning frameworks
- Lightweight transformer models for real-time deployment
- Improved interpretability for regulatory use cases

---

## 🎯 Why This Project Matters
This project demonstrates my ability to:
- Work on **international NLP competitions**
- Translate research ideas into **working ML systems**
- Handle **end-to-end NLP pipelines**
- Communicate results clearly through **research papers & code**

Relevant roles:
- **Data Scientist**
- **NLP Engineer**
- **Machine Learning Engineer**

---

## 👤 Author
**Hara Ju**  
Data Analyst | Aspiring Data Scientist | NLP & ML Research Enthusiast

🔗 GitHub: This repository  
🔗 LinkedIn: *(add your profile link)*

---

⭐ If you are a recruiter or researcher and find this project interesting, feel free to ⭐ star the repository or reach out!
