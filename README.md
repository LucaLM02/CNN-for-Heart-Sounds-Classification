# Heart Sound Classification with 1D CNN

This project implements a **1D Convolutional Neural Network (CNN)** in Python to classify heart sounds (phonocardiograms, PCGs) as **healthy** or **unhealthy**, supporting early detection of cardiovascular diseases.

---

## 🔎 Background
- Cardiovascular diseases are a leading cause of death worldwide.  
- Heart sound auscultation is widely used in clinical practice, but accurate interpretation requires expertise.  
- CNNs can automatically learn relevant acoustic patterns, improving robustness and generalization in classification tasks.  

---

## 📂 Dataset
We used the **2016 PhysioNet/CinC Challenge dataset**, which contains **3,240 heart sound recordings** from healthy and pathological patients across diverse clinical and non-clinical settings.  
- Recording duration: **5–120 seconds**  
- Labels: **Healthy** / **Unhealthy**

---

## ⚙️ Preprocessing
To improve performance, the following steps were applied:
- **Filtering**  
- **Downsampling**  
- **Normalization**  
- **Segmentation**  

---

## 🏗️ Model
- **1D CNN architecture** designed for sequential acoustic signals.  
- **Grouped Loss** strategy to:  
  - Reduce sensitivity to noisy/ambiguous segments  
  - Align predictions with recording-level labels  
  - Improve generalization across patients  

---

## 📊 Evaluation
Metrics used:
- **Accuracy**  
- **AUC (Area Under ROC Curve)**  
- **Precision, Recall, F1-score**  

Best configuration:  
- **Filtered data, no artificial noise**  
- **F1-score: 0.97**, showing strong and reliable performance  

Noise injection experiments confirmed the importance of preprocessing, with filtering yielding the most robust results.

---

## ✅ Conclusion
- Preprocessing is crucial for classification accuracy and robustness.  
- Filtering significantly improves resilience against noise.  
- The best-performing model achieved an **F1-score of 0.97**.  
