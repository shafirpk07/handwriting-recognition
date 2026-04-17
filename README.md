# Automated Handwriting Recognition System ✍️

> CNN-based model for digitizing handwritten text with 90% accuracy

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)](https://tensorflow.org)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](#)

---

## Overview

This project uses a **Convolutional Neural Network (CNN)** to automatically recognize and digitize handwritten inputs from images. It converts handwritten text into machine-readable digital text with **90% accuracy**, reducing manual data entry time significantly.

---

## Features

- 🧠 **CNN-based recognition** — trained on handwritten character and word datasets
- 📸 **Image input** — accepts scanned or photographed handwriting
- 📝 **Text output** — returns clean, digitized text
- 🖥️ **Web interface** — simple HTML/CSS frontend for image upload and result display
- 📈 **90% accuracy** on benchmark validation sets

---

## Tech Stack

| Component | Technology |
|---|---|
| Deep Learning Model | TensorFlow / Keras |
| Language | Python 3.10+ |
| Frontend | HTML, CSS |
| Image Processing | NumPy, OpenCV |

---

## Installation

```bash
git clone https://github.com/shafirpk07/handwriting-recognition.git
cd handwriting-recognition
pip install -r requirements.txt
```

---

## Usage

```bash
# Train the model (or use pre-trained weights)
python train.py

# Run prediction on an image
python predict.py --image sample_handwriting.png
```

**Output:**
```
Detected Text: "The quick brown fox jumps over the lazy dog"
Confidence: 91.2%
```

---

## Model Architecture

```
Input Image (28x28 or 128x32)
    │
    ▼
Conv2D (32 filters, 3x3) → ReLU → MaxPooling
    │
    ▼
Conv2D (64 filters, 3x3) → ReLU → MaxPooling
    │
    ▼
Flatten → Dense (128) → Dropout (0.5)
    │
    ▼
Dense (num_classes) → Softmax
    │
    ▼
Predicted Character / Word
```

---

## Project Structure

```
handwriting-recognition/
├── train.py              # Model training script
├── predict.py            # Inference on new images
├── model/
│   ├── cnn_model.py      # CNN architecture definition
│   └── weights/          # Saved model weights
├── data/
│   └── preprocess.py     # Image preprocessing utilities
├── templates/
│   └── index.html        # Web upload interface
├── static/
│   └── style.css         # Frontend styling
├── requirements.txt
└── README.md
```

---

## Results

| Metric | Score |
|---|---|
| Training Accuracy | 93.4% |
| Validation Accuracy | 90.1% |
| Test Accuracy | 90.0% |

---

## Author

**Shafir PK** — Data Analyst & ML Enthusiast
📧 pkshafir07@gmail.com · [LinkedIn](https://linkedin.com/in/shafir-pk-540284278)
