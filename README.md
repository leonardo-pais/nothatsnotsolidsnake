# 🐍 No, That's Not Solid Snake

![Python](https://img.shields.io/badge/python-3.11-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green)
![GitHub Repo Size](https://img.shields.io/github/repo-size/leonardo-pais/nothatsnotsolidsnake)

A meme-powered machine learning project that answers one simple question:

**“Is this Solid Snake?”**

Inspired by the classic Metal Gear meme, this project trains a computer vision model to identify whether an image contains Solid Snake or not.  
If it’s him, the model proudly says: **“Yes! That is Solid Snake!”**  
Otherwise: **“No! That is not Solid Snake!”**

---

<p align="center">
  <img src="media/no-that-is-not-solid-snake-mgs2.gif" alt="Demo" width="400"/>
</p>

---

## 📖 Project Overview
- **Type of problem**: Binary Image Classification  
- **Classes**:
  - `solid_snake` → images of Solid Snake  
  - `not_solid_snake` → everything else (Big Boss, Venom Snake, Old Snake, Raiden, random characters, etc.)

- Follows **CRISP-DM methodology**:
  1. Business Understanding → turn a meme into a classifier
  2. Data Understanding → collect Solid Snake vs. not Solid Snake images
  3. Data Preparation → resize, normalize, augment images
  4. Modeling → transfer learning with sigmoid output
  5. Evaluation → check accuracy, precision, recall, F1-score
  6. Deployment → API or web demo

---

## 📂 Dataset

**Note:** The full dataset is **not included** due to copyright restrictions.  
You can download images manually or from fan wikis and organize them as follows:

```
dataset/
├── train/
│   ├── solid_snake/
│   └── not_solid_snake/
├── val/
│   ├── solid_snake/
│   └── not_solid_snake/
└── test/
    ├── solid_snake/
    └── not_solid_snake/
```

---

## ⚙️ Installation

This project uses [uv](https://github.com/astral-sh/uv) for package management.

```bash
# Clone the repository
git clone https://github.com/your-username/no-thats-not-solid-snake.git
cd no-thats-not-solid-snake

# Install dependencies
uv install
```

---

## 🚀 Usage

### Training
```bash
uv run python src/train.py
```

### Inference
```python
from src.predict import predict_snake

result = predict_snake("example.jpg")
if result:
    print("Yes, that's Solid Snake.")
else:
    print("No, that's not Solid Snake.")
```

---

## 📊 Evaluation Metrics
- **Accuracy** → general performance  
- **Precision** → of all times it said “Solid Snake,” how many were true?  
- **Recall** → of all actual Solid Snake images, how many did it detect?  
- **F1-score** → balance between precision and recall  

---

## 🗂️ Repository Structure

```
nothatsnotsolidsnake/
├── README.md
├── pyproject.toml
├── .gitignore
├── media/                   # demo gif or images for README
├── models/                  # trained models
│   └── solid_snake_classifier.pt
├── src/                     # source code
│   ├── data_preprocessing.py
│   ├── train.py
│   └── predict.py
└── notebooks/               # exploration notebooks
```

---

## 🎮 Future Ideas
- Extend to multiclass classification: identify each version of Snake (Solid, Naked, Old, Venom, etc.)  
- Build a meme-generator web app  
- Deploy as a Discord bot for fans  

---

## 🐍 Acknowledgements
- Inspired by the *“No, that’s not Solid Snake”* meme  
- Metal Gear Solid and its characters belong to **Konami**. This project is purely for fun and educational purposes.
