# FER2013 — Facial Expression Recognition

<div align="center">
  
![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

</div>

This project focuses on **facial expression recognition** using the **FER2013 dataset**. The goal is to build a deep learning model that can classify human facial expressions into seven emotion categories, enabling applications in sentiment analysis, human-computer interaction, and social robotics.

##  Sample Images from Dataset

![Dataset Samples](dataset_samples.png)

##  Class Distribution

![Class Distribution](Class%20distribution.png)

## 📁 Project Structure

```
fer2013/
├── train/                      # Training images organized by emotion
├── test/                       # Testing images organized by emotion
├── Fer2013 Dataset.py          # Script to convert images to pixel values + labels
├── emotion_recognition.py      # Main script for training the deep learning model
├── compressed_data.csv.gz      # Processed dataset in CSV format
├── fer2013_arrays.npz          # Preprocessed data arrays
├── dataset_samples.png         # Sample images from the dataset
├── Class distribution.png      # Visualization of class balance
├── training curves.png         # Training and validation loss/accuracy curves
├── Confusion Matrix.png        # Model performance evaluation
├── Sample predictions.png      # Example predictions on test images
└── README.md
```

##  Dataset

The **FER2013 dataset** contains thousands of facial images categorized into **seven emotions**:

| Emotion | Label |
|---------|-------|
| 😊 Happiness | 0 |
| 😢 Sadness | 1 |
| 😠 Anger | 2 |
| 😨 Fear | 3 |
| 😲 Surprise | 4 |
| 🤢 Disgust | 5 |
| 😐 Neutral | 6 |

The dataset is already split into **training** and **testing** sets for easy model evaluation.

##  Preprocessing

A custom Python script (`Fer2013 Dataset.py`) is used to:
1. Convert images into **pixel values** (numerical representation)
2. Assign a **numerical label** to each image based on its emotion category
3. Store the processed data in a **CSV file** (`compressed_data.csv.gz`) for streamlined training

##  Model Training

The `emotion_recognition.py` script loads the preprocessed data and trains a **deep learning model** (Convolutional Neural Network) to classify facial expressions.

### Training Progress

![Training Curves](training%20curves.png)

### Model Performance

![Confusion Matrix](Confusion%20Matrix.png)

### Sample Predictions

![Sample Predictions](Sample%20predictions.png)

##  Applications

This project demonstrates how AI can be applied in:

* **Sentiment analysis** — Understanding customer or user emotions from facial cues
* **Human-computer interaction** — Enabling more intuitive and responsive interfaces
* **Social robotics** — Helping robots perceive and react to human emotional states

##  Requirements

- Python 3.x
- Libraries: `numpy`, `pandas`, `tensorflow`/`keras`, `matplotlib`, `seaborn`, `opencv-python` (or `PIL`)

You can install dependencies using:
```bash
pip install numpy pandas tensorflow matplotlib seaborn opencv-python
```

##  Results

The model achieves promising performance on the test set, with the confusion matrix and sample predictions demonstrating its capability to differentiate between the seven emotion classes with good accuracy.

##  How to Use

1. **Clone the repository:**
   ```bash
   git clone https://github.com/EngReem85/fer2013.git
   cd fer2013
   ```

2. **Run preprocessing** (if needed) to generate the CSV from raw images:
   ```bash
   python "Fer2013 Dataset.py"
   ```

3. **Train the model:**
   ```bash
   python emotion_recognition.py
   ```

4. **Evaluate performance** using the generated plots:
   - `training curves.png` — Check training progress
   - `Confusion Matrix.png` — See per-class performance
   - `Sample predictions.png` — View test results


##  Author

**Reem Algethami** — [EngReem85](https://github.com/EngReem85)

---

<div align="center">
  
### ⭐ If you find this project useful, please give it a star! ⭐

</div>

---

