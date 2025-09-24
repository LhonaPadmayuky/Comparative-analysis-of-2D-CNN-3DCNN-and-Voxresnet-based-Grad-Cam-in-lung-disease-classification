# 🫁 Lung Disease Classification using 2D CNN, 3D CNN & 3D VoxResNet with Grad-CAM

This project presents a **comparative analysis** of deep learning models for lung disease classification using CT scan images.  
It explores **2D CNN, 3D CNN, and 3D VoxResNet** architectures, and integrates **Explainable AI (Grad-CAM)** for interpretability.

---

## 📂 Dataset
- CT scan images categorized into:
  - **Normal**
  - **Community Acquired Pneumonia (CAP)**
  - **COVID-19**
  - **Adenocarcinoma**
  - **Squamous Cell Carcinoma**
  - **Large Cell Carcinoma**

Dataset size after preprocessing & augmentation: **13,440 CT slices**

### Sample Images
<img width="1052" height="521" alt="image" src="https://github.com/user-attachments/assets/d925fdcc-38a6-4569-88ac-e2e5a51c189b" />


---

## 🏗️ System Architecture
<img width="1000" height="501" alt="image" src="https://github.com/user-attachments/assets/556b7a6f-c454-4bb1-b4f0-4706cfc9b14d" />

---

## ⚙️ Methodology
### 1. Data Preprocessing
- Resized to **256x256**
- Augmentation: rotation, flipping, contrast, noise
- Synthetic slice generation for balancing
<img width="997" height="547" alt="image" src="https://github.com/user-attachments/assets/fb84bb66-e293-4151-81fe-fb2919373d91" />


### 2. Model Architectures
- **2D CNN** – classifies single CT slices  
<img width="935" height="374" alt="image" src="https://github.com/user-attachments/assets/7f74926d-73fc-4630-8d40-98e1d8d64798" />


- **3D CNN** – captures volumetric spatial features  
<img width="729" height="301" alt="image" src="https://github.com/user-attachments/assets/19b654a4-ace0-463c-b138-9564b422b9e5" />


- **3D VoxResNet** – deeper residual network for volumetric learning  
<img width="894" height="694" alt="image" src="https://github.com/user-attachments/assets/d718076d-3edb-422a-8d29-d4126850e2a9" />

---

## 🔍 Explainable AI (XAI)
To enhance transparency, **Grad-CAM** was applied to highlight critical lung regions influencing predictions.

### Example Visualizations
- Stage 1 (Normal / CAP / COVID-19 / Cancer)  
<img width="563" height="470" alt="image" src="https://github.com/user-attachments/assets/9d3529d4-99c0-48a7-9d9a-584823e41368" />
<img width="663" height="478" alt="image" src="https://github.com/user-attachments/assets/70959d4c-dcc5-4a1d-a376-314325a2ae04" />



- Stage 2 (Cancer Subtypes)  
<img width="485" height="764" alt="image" src="https://github.com/user-attachments/assets/892044d9-0192-45c5-9299-270de11d16c1" />


---

## 📊 Results
| Model          | Stage 1 Accuracy | Stage 2 Accuracy |
|----------------|-----------------|-----------------|
| 2D CNN         | 70%             | 60%             |
| 3D CNN         | 75%             | 61%             |
| 3D VoxResNet   | **79%**         | **82%**         |

### Charts
<img width="403" height="672" alt="image" src="https://github.com/user-attachments/assets/16389306-3642-42ad-9b11-3eb3ea14b9c6" />

<img width="492" height="708" alt="image" src="https://github.com/user-attachments/assets/03f3a125-ba98-4f26-bcc4-0bf6e6e1d292" />


---

## 📌 Key Findings
- **3D VoxResNet** achieved the highest accuracy for both stages.
- **Grad-CAM visualizations** improved interpretability for clinical use.
- Augmentation & synthetic slices improved data balance.

---

## 🚀 Installation & Usage
```bash
# Clone repository
git clone https://github.com/your-username/lung-disease-classification.git
cd lung-disease-classification

# Install dependencies
pip install -r requirements.txt

# Run training
python train.py

# Run testing
python test.py
