# 🚨 CCTV Anomaly Detection & Intelligent Surveillance

A deep learning-based **video anomaly detection system** designed for intelligent CCTV surveillance. The model analyzes video sequences and identifies abnormal activities such as **Arson, Fighting, Shoplifting, and Vandalism**, along with normal activities.

The project uses **MobileNetV2 for spatial feature extraction** and **LSTM for learning temporal patterns across video frames**.

---

## 🎯 Project Objective

Traditional CCTV surveillance requires continuous human monitoring, which can be time-consuming and difficult to scale.

This project aims to automatically analyze CCTV video sequences and classify them into different activity categories using a combination of **Convolutional Neural Networks (CNN)** and **Recurrent Neural Networks (RNN/LSTM)**.

---

## 🧠 Model Architecture

```text
Input CCTV Video
       ↓
Video Frame Extraction
       ↓
Frame Preprocessing
       ↓
MobileNetV2
(Spatial Feature Extraction)
       ↓
TimeDistributed CNN
       ↓
LSTM
(Temporal Feature Learning)
       ↓
Dense Layer
       ↓
Softmax
       ↓
Activity Classification
```

### Why MobileNetV2?

MobileNetV2 is a lightweight CNN architecture that efficiently extracts visual features from individual video frames while requiring fewer computational resources compared with heavier CNN architectures.

### Why LSTM?

CCTV activities occur over a sequence of frames rather than a single image.

LSTM learns the **temporal relationship between consecutive frames**, helping the model distinguish activities based on how they evolve over time.

---

## 📂 Dataset

The project uses the **UCF-Crime dataset**, a large-scale video dataset for real-world anomaly detection in surveillance videos.

The dataset contains different types of anomalous and normal activities.

For this implementation, the model focuses on selected categories:

* 🔥 Arson
* 🥊 Fighting
* 🛍️ Shoplifting
* 💥 Vandalism
* ✅ Normal

---

## 🛠️ Technologies Used

* Python
* TensorFlow / Keras
* OpenCV
* NumPy
* Pandas
* Matplotlib
* Scikit-learn
* MobileNetV2
* LSTM
* CNN
* Deep Learning

---

## 🔄 Data Preprocessing

The video data is processed before being given to the model.

### Steps

1. Read CCTV videos using OpenCV.
2. Extract frames from videos.
3. Resize frames to the required input size.
4. Normalize pixel values.
5. Create frame sequences.
6. Assign activity labels.
7. Split the data into training and testing sets.

---

## 🧪 Training

The model learns both:

**Spatial information**

> What is happening in an individual frame?

**Temporal information**

> How does the activity change across multiple frames?

The extracted frame-level features are passed to the LSTM network, which learns temporal patterns and performs the final activity classification.

### Loss Function

```text
Categorical Cross-Entropy
```

### Optimizer

```text
Adam
```

### Output Layer

```text
Softmax
```

---

## 📊 Model Evaluation

The model can be evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

These metrics help measure how effectively the model identifies different surveillance activities.

---

## 📈 Results

Add your actual results here after training:

```text
Accuracy  : XX%
Precision : XX%
Recall    : XX%
F1-Score  : XX%
```

### Confusion Matrix

Add your generated confusion matrix image here:

```markdown
![Confusion Matrix](images/confusion_matrix.png)
```

---

## 🖼️ Sample Predictions

You can add sample prediction screenshots/results here.

```markdown
![Sample Prediction](images/sample_prediction.png)
```

Example:

```text
Input Video
     ↓
Model Prediction
     ↓
Fighting
```

---

## 📁 Project Structure

```text
cctv-anomaly-detection/
│
├── dataset/
│
├── notebooks/
│   └── cctv_anomaly_detection.ipynb
│
├── models/
│   └── model.h5
│
├── images/
│   ├── confusion_matrix.png
│   └── sample_prediction.png
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/ShivaniYadav354/cctv-anomaly-detection.git
```

### 2. Navigate to the project

```bash
cd cctv-anomaly-detection
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Open the notebook

```text
notebooks/cctv_anomaly_detection.ipynb
```

Run the notebook cells sequentially.

---

## 📦 Requirements

Example dependencies:

```text
tensorflow
opencv-python
numpy
pandas
matplotlib
scikit-learn
Pillow
```

---

## 🔮 Future Improvements

* Real-time CCTV video detection
* More anomaly categories
* Real-time alert generation
* Integration with IP cameras
* Model optimization for edge devices
* Improved performance on long video sequences
* Deployment using FastAPI
* Docker-based deployment

---

## 💡 Key Learning Outcomes

Through this project, I worked with:

* Video-based deep learning
* CNN-based feature extraction
* MobileNetV2
* LSTM-based temporal modeling
* Video preprocessing using OpenCV
* Multi-class classification
* Model evaluation
* Anomaly detection in surveillance videos

---

## 👩‍💻 Author
**Shivani Yadav**

### Connect
* GitHub: [ShivaniYadav354](https://github.com/ShivaniYadav354)

---

## ⭐ Project Highlights

```text
✔ Video-based anomaly detection
✔ MobileNetV2 spatial feature extraction
✔ LSTM temporal sequence learning
✔ UCF-Crime dataset
✔ Multi-class activity classification
✔ Precision / Recall / F1 evaluation
✔ Deep Learning + Computer Vision
```
