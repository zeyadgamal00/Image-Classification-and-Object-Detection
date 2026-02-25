# 🔍 DetectaX
### **Fine-Grained Object Classification & Object Recognition Web Application**  
**“Upload. Detect. Classify. Explore.”**

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-Live-red)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Active-success.svg)

---

**DetectaX** is a comprehensive computer vision platform designed for high-precision object detection, real-time tracking, and specialized vehicle analysis. By combining state-of-the-art deep learning architectures with a user-friendly **Streamlit web interface**, DetectaX provides a seamless "Detection-as-a-Service" experience for both general-purpose and industry-specific use cases.

---

## 🚀 Key Features

* **Unified Web Platform:** A dedicated [Streamlit interface](https://github.com/omaryasser3060/DEPI_Project_App-Streamlit-interface) for uploading images or videos and visualizing results directly in your browser.
* **General Object Detection:** Real-time identification of 80+ object categories optimized for low-latency processing.
* **Specialized Car Classification:** A fine-tuned Car Classification model designed to go beyond basic detection, classifying vehicles by make, model, or category with high accuracy.
* **Multi-Object Tracking:** Maintain unique IDs for objects across video frames for consistent monitoring and counting.
---

## 🧰 Tech Stack

| Category | Technologies |
|---------|--------------|
| **Frontend** | Streamlit |
| **Deep Learning** | MobileNetV2 (Image Classification), YOLO 12X (Object Detection) |
| **Computer Vision** | OpenCV |
| **Core Python Libraries** | NumPy, Pandas, Pillow |
| **Model Serving / Utils** | TensorFlow & PyTorch |
| **Deployment** | Local machine or Azure |

---

## ⭐ Features

### **🟦 Image Classification**
- Predicts **car make**
- Predicts **car model**
- Predicts **manufacturing year**
- Fine-grained classification powered by ResNet50
- Trained using CUHK-CompCars dataset  
- Supports JPG, PNG uploads

### **🟥 Object Recognition (YOLO 12X)**
- Detects multiple objects in an image  
- Draws bounding boxes with labels & confidence  
- Fast inference  
- High-accuracy detection for real-world scenes

  
### 💻 Technical Interface (Streamlit)

The platform is powered by a Streamlit frontend, making advanced AI accessible without writing code:
-  **Upload:** Drag and drop images or video files.
-  **Toggle:** Switch between general object detection and specialized automotive classification.
-  **Visualize:** Real-time bounding boxes, confidence scores, and class labels.
-  **Export:** Download processed results and analytics.
---

## Model Details

### **ResNet50 — Car Classification**
- Pretrained on ImageNet  
- Fine-tuned on CUHK-CompCars  
- Excellent at capturing **fine-grained automotive features**  
- Predicts: **Make → Model → Year**

### **YOLO 12X — Object Recognition**
- Cutting-edge YOLO variant  
- Optimized for high-speed detection  
- Generates precise bounding boxes and class names  

---

## Installation & Usage

Follow these steps to run the project locally:

---

### **1. Clone the Repository**

```bash
git clone https://github.com/your-username/compcars-vision-app.git
cd compcars-vision-app
```

### **2. Create a Virtual Environment**

Windows:
```bash
python -m venv venv
venv\Scripts\activate
```


Mac/Linux:
```bash
python3 -m venv venv
source venv/bin/activate
```
### **3. Install Dependencies**
```bash
pip install -r requirements.txt
```

### **4️. Run the Streamlit App**
```bash
streamlit run app.py
```

## Directory Structure
- Below is a standard directory layout for a Streamlit ML project:

```bash
G:.
¦   .gitignore
¦   DEPI Project Proposal.pdf
¦   Microsoft Machine Learning Project - Round3.pdf
¦   output.txt
¦   Project Presentation.pptx
¦   Project Presentation1.pptx
¦   Project_Structure.txt
¦   README.md
¦   
+---.vscode
¦       settings.json
¦       
+---Classification Model [NEW]
+---Classification Model [OBSOLETE]
¦   ¦   best_model.h5
¦   ¦   cifar10_model.h5
¦   ¦   cifar10_model.keras
¦   ¦   cifar10_model_final_improved.keras
¦   ¦   Classification Model_notebook_converted.py
¦   ¦   classification.ipynb
¦   ¦   ImageClassification.py
¦   ¦   
¦   +---New Nov 15
¦           best_model_phase1.h5
¦           cifar10_model_final_mlflow.keras
¦           cifar10_model_phase1.keras
¦           
+---DEPI_Project_App
¦   ¦   api_client.py
¦   ¦   Home.css
¦   ¦   Home.py
¦   ¦   requirements.txt
¦   ¦   
¦   +---assets
¦   ¦   ¦   global.css
¦   ¦   ¦   
¦   ¦   +---icons
¦   ¦   ¦       brain_icon_blue.svg
¦   ¦   ¦       clf_icon_blue.svg
¦   ¦   ¦       target_icon.svg
¦   ¦   ¦       target_icon_blue.svg
¦   ¦   ¦       
¦   ¦   +---icons redun
¦   ¦   ¦       brain_icon_blue.svg
¦   ¦   ¦       clf_icon_blue.svg
¦   ¦   ¦       target_icon_blue.svg
¦   ¦   ¦       
¦   ¦   +---team_images
¦   ¦           Abdelrahman Kamal Elkhabery.png
¦   ¦           Basel Mohamed Mostafa.png
¦   ¦           Mohamed Hamada Farghali.jpg
¦   ¦           Omar Yasser Sayed.png
¦   ¦           Zeyad Gamal Mohamed.jpg
¦   ¦           Ziad Ahmed Samir.png
¦   ¦           
¦   +---footer
¦   ¦       footer.css
¦   ¦       footer.py
¦   ¦       
¦   +---navbar
¦   ¦       navbar.css
¦   ¦       navbar.py
¦   ¦       
¦   +---pages
¦   ¦       1_Image_Classification.py
¦   ¦       2_Object_Detection.py
¦   ¦       
¦   +---utils
¦           helpers.py
¦           preprocessing.py
¦           visualization.py
¦           
+---MLflow [OBSOLETE]
¦   ¦   mlflow.db
¦   ¦   model_registry.py
¦   ¦   requirments.txt
¦   ¦   tracking_setup.py
¦   ¦   train_classification_mlflow.py
¦   ¦   
¦   +---mlruns
¦   ¦   +---3
¦   ¦       +---a00c2fe554214d10b129a3c61969e92c
¦   ¦       ¦   +---artifacts
¦   ¦       ¦           cifar10_model_phase1.keras
¦   ¦       ¦           
¦   ¦       +---d698b168da4f4072bd7a5fa0ba9db668
¦   ¦       ¦   +---artifacts
¦   ¦       ¦           cifar10_model_phase1.keras
¦   ¦       ¦           class_names.txt
¦   ¦       ¦           training_history.png
¦   ¦       ¦           
¦   ¦       +---e4de11a5b34a46faa6fbe0c4e98063b8
¦   ¦       ¦   +---artifacts
¦   ¦       ¦           class_names.txt
¦   ¦       ¦           training_history.png
¦   ¦       ¦           
¦   ¦       +---f6cd3ae6570347059a9f3e3bdfdf4fca
¦   ¦           +---artifacts
¦   ¦                   cifar10_model_final_mlflow.keras
¦   ¦                   confusion_matrix_final.png
¦   ¦                   sample_predictions_final.png
¦   ¦                   
¦   +---phase1_artifacts
¦   ¦       class_names.txt
¦   ¦       training_history.png
¦   ¦       
¦   +---phase2_artifacts
¦           class_names.txt
¦           training_history.png
¦       
¦           
¦           
+---Object Detection Model
¦       object_detection_model.ipynb
¦       README.md
¦       
+---Project Images
    +---NEW
    +---OLD [OBSOLETE]
            Classification Model Full Classification Report.png
            Classification Prediction (Notebook).png
            Classification Training Code 1.png
            Classification Training Code 2.png
            Classification Training Code 3.png
            CLS_CM.png
            confusion_matrix_final.png
            MLflow Artifacts.png
            MLflow Image 1.png
            MLflow Image 2.png
            MLflow Model Description and parameters logged.png
            MLflow Model Metrics.png
            Model Summary.png
            Model Training (20 Epochs) (Notebook).png
            sample_predictions_final.png
```

## Results & Performance
1. Classification (ResNet50)
- Accuracy: e.g., 91.3%
- Top-5 Accuracy: e.g., 97.8%
- Confusion Matrix:


2. Object Detection (YOLO 12X)
- mAP50: e.g., 88.6%
- Inference Speed: e.g., 12 ms/image

Detection Examples:

![Detection Example 1](path/to/detection_example_1.jpg)
![Detection Example 2](path/to/detection_example_2.jpg)

## License

This project is released under the MIT License.
See the LICENSE file for details.

## Acknowledgements
- DEPI (Digital Egypt Pioneers Initiative)
- CUHK CompCars dataset.
- Streamlit community.
- YOLO open-source contributors.
- ResNet authors.
