# Plastic Type Classification 🛍️♻️

This project uses **MobileNetV2 (CNN)** for feature extraction and **LightGBM** for classification to identify different types of plastic materials.  
The dataset contains images of various plastic types like **PET, PP, PS, PE, PC, Others**.

---

## 📂 Dataset
The dataset folder structure in Google Drive:
Plastic types/
│── PET/
│── PP/
│── PS/
│── PE/
│── PC/
│── Others/

Example image added in repo: `image_101.jpg`

---

## ⚙️ Requirements
- Python 3.8+
- TensorFlow / Keras
- LightGBM
- scikit-learn
- NumPy

Install dependencies:

pip install tensorflow lightgbm scikit-learn numpy
🚀 Training the Model

Run the following steps in Google Colab:

Mount Google Drive

Load dataset from Plastic types/

Extract features using MobileNetV2

Train LightGBM classifier

Evaluate accuracy

🖼️ Predicting New Image

To test with a new image:

test_img = "/content/drive/MyDrive/Plastic types/image_101.jpg"
features = extract_features(test_img).reshape(1, -1)
prediction = np.argmax(model.predict(features), axis=1)
print("Predicted class:", classes[prediction[0]])

📊 Results

Feature extractor: MobileNetV2

Classifier: LightGBM

Evaluation Metric: Accuracy

🔮 Future Scope

Expand dataset with more plastic types

Deploy as a web app for real-time classification

Optimize for edge devices (Raspberry Pi, Arduino, etc.)


