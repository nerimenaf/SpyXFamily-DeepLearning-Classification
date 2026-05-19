# 🧠 Spy x Family Character Classification using Transfer Learning

Deep Learning Practical Exam Project  
Implemented using **TensorFlow** and **Keras** in Google Colab.

---

## 📌 Project Objective

The objective of this project is to implement an image classification model using **Transfer Learning** to classify anime characters from *Spy x Family*:

- 🕵️ Loid Forger  
- 👧 Anya Forger  
- 🗡️ Yor Forger  

The project compares different fine-tuning strategies and evaluates their performance.

---

## 📂 Dataset

Images were collected using an automated image downloader.

- ~120 images per class
- 3 classes
- Train / Validation split: 80% / 20%

Data augmentation techniques were applied to improve generalization.

---

## 🛠 Model Architecture

Pretrained model used:

✅ **MobileNetV2** (ImageNet weights)  
✅ `include_top=False`  
✅ Custom classification head  

Final layers:

- GlobalAveragePooling2D
- Dropout
- Dense (128, ReLU)
- Dropout
- Dense (3, Softmax)

---

## 🔄 Training Approaches Compared

### 1️⃣ Frozen Model (Feature Extraction)
- Base model frozen
- Only classifier trained

### 2️⃣ Partial Fine-Tuning
- Last 20 layers unfrozen

### 3️⃣ Full Fine-Tuning
- All layers trainable

---

## 📊 Results Comparison

| Approach | Validation Accuracy |
|-----------|---------------------|
| Frozen Model | ~80% |
| Partial Fine-Tuning | ~83% |
| Full Fine-Tuning | ~84% |

✅ **Best Model: Full Fine-Tuning**

Full fine-tuning achieved the highest validation accuracy and best adaptation to the dataset.

---

## 📈 Techniques Used

- ✅ Transfer Learning
- ✅ Data Augmentation
- ✅ EarlyStopping
- ✅ ReduceLROnPlateau
- ✅ Confusion Matrix
- ✅ Webcam Real-Time Testing
- ✅ Confidence Threshold for Unknown Detection

---

## 📷 Real-Time Camera Testing

The trained model was tested using the computer webcam in Google Colab.  
A confidence threshold was implemented to detect unknown inputs.

---

## 🚀 How to Run

1. Open the notebook in Google Colab
2. Mount Google Drive (if loading saved model)
3. Run all cells

---

## 📚 Technologies Used

- Python
- TensorFlow
- Keras
- Google Colab
- OpenCV
- Scikit-learn
- Matplotlib
- Seaborn

---

## 🎓 Conclusion

Transfer learning with MobileNetV2 proved effective for small datasets.  
Full fine-tuning provided the best performance by allowing deeper adaptation of pretrained features.

---

## 👨‍💻 Author

Deep Learning Practical Exam Project  
2026
