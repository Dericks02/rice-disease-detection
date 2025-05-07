# rice-disease-detection
*Developed By Jones*

# 🌾 Rice Plant Disease Detection & Fertilizer Suggestion Using Hybrid Model (CNN, ViT)

This project leverages deep learning techniques, specifically **Convolutional Neural Networks (CNN)** and **Vision Transformers (ViT)**, to detect diseases in rice plant leaves from images. A **hybrid model** combines the strengths of CNN and ViT to improve accuracy. Based on the detected disease, the system also suggests appropriate fertilizers to enhance crop health.

## 🔍 Features

- Upload rice plant leaf images through a web interface
- Disease prediction using:
  - CNN Model
  - Vision Transformer (ViT) Model
  - Hybrid Model (CNN + ViT)
- Confidence scores for each model's prediction
- Fertilizer suggestions based on the detected disease
- Real-time results displayed in the browser

---

## 📁 Folder Structure

```
project/
│
├── static/
│   └── images/              # Uploaded images
├── templates/
│   └── index.html           # Frontend HTML template
├── config.py                # Configuration file with paths, class names, etc.
├── app.py                   # Main Flask application
├── models/                  # Trained CNN, ViT, and Hybrid models (optional location)
└── README.md                # Project documentation
```

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/rice-disease-hybrid-model.git
cd rice-disease-hybrid-model
```

### 2. Install Requirements

```bash
pip install -r requirements.txt
```

> Make sure you have Python 3.7 or higher and TensorFlow installed.

### 3. Add Configuration (`config.py`)

Create a `config.py` file with the following structure:

```python
CONFIG = {
    'model_paths': {
        'cnn': 'models/cnn_model.h5',
        'vit': 'models/vit_model.h5',
        'hybrid': 'models/hybrid_model.h5'
    },
    'img_size': 224,
    'classes': ['Bacterial Blight', 'Blast', 'Brown Spot', 'Healthy'],  # Example classes
    'fertilizer_suggestions': {
        'Bacterial Blight': 'Use potassium-based fertilizer.',
        'Blast': 'Apply nitrogen-rich fertilizer.',
        'Brown Spot': 'Use phosphorus-rich fertilizer.',
        'Healthy': 'No treatment needed.'
    }
}
```

### 4. Run the Application

```bash
python app.py
```

Visit `http://127.0.0.1:5000` in your browser.

---

## 🧠 Models Used

- **CNN**: Standard convolutional layers for spatial feature extraction.
- **ViT**: Vision Transformer for capturing long-range dependencies in image data.
- **Hybrid**: Ensemble or merged architecture combining CNN and ViT outputs.

---

## 🧪 Example Output

- **Input**: Image of a rice leaf
- **CNN Prediction**: Blast (95.32%)
- **ViT Prediction**: Blast (94.10%)
- **Hybrid Prediction**: Blast (97.85%)
- **Fertilizer Suggestion**: Apply nitrogen-rich fertilizer.

---

## 📌 TODO / Improvements

- Add support for more plant types
- Optimize model performance for mobile devices
- Deploy to cloud (GCP/AWS/Azure)
- Add multilingual support for farmers

---

## 🧑‍💻 Authors

- **Dericks Josen J**  
  Final Year B.Tech Student – CSE  
  Reg. No: URK21CO1004

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).










