# 🧪 Cancer Cell Detection using Deep Learning

This project provides a **complete pipeline** for **Cancer Cell Detection** using **Deep Learning (CNN)**.
It includes:

1. **Model Training Script** → Trains a CNN model on cancer cell datasets and saves it as `Cancer_detection_model.h5`.
2. **GUI Application (Tkinter)** → A simple interface to upload images and classify them as **Healthy** or **Leukemia/Lymphoma subtypes**.

---

## 🚀 Features

* Train a **Convolutional Neural Network (CNN)** on custom datasets.
* Evaluate the model with validation and test sets.
* Save the trained model (`.h5` format).
* User-friendly **Tkinter GUI** for predictions.
* Upload images and get predictions with confidence scores.

---

## 🛠️ Tech Stack

* **Python 3.x**
* **TensorFlow / Keras**
* **Tkinter** (for GUI)
* **Pillow (PIL)** (for image processing)
* **NumPy, Pandas, Matplotlib** (for data handling and visualization)

---

## 📂 Project Structure

```
📁 Cancer-Cell-Detection
│── train_model.py              # Training script (model training & saving)
│── cancer_gui.py               # Tkinter GUI application
│── Cancer_detection_model.h5   # Pre-trained model (generated after training)
│── requirements.txt            # Dependencies
│── README.md                   # Documentation
```

---

## ⚙️ Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/Cancer-Cell-Detection.git
   cd Cancer-Cell-Detection
   ```

2. Install dependencies:

   ```bash
   pip install -r req.txt
   ```

---

## 📦 req.txt

```
tensorflow
numpy
pandas
matplotlib
pillow
```

*(Tkinter comes pre-installed with Python, no need to install separately)*

---

## 🧬 Dataset

The dataset should be structured as:

```
📁 dataset
│── 📁 train
│   │── 📁 Healthy
│   │── 📁 Leukemia_I
│   │── 📁 Leukemia_II
│   │── 📁 Leukemia_III
│   │── 📁 Chronic_Lymphocytic_Leukemia
│   │── 📁 Follicular_Lymphoma
│   │── 📁 Mantle_Cell_Lymphoma
│
│── 📁 val
│   │── same subfolders as train
│
│── 📁 test
│   │── same subfolders as train
```

---

## 🏋️ Model Training

To train the CNN model, run:

```bash
python train_model.py
```

This will:

* Load the dataset (`train`, `val`, `test` folders).
* Train the CNN model for **32 epochs**.
* Save the trained model as `Cancer_detection_model.h5`.

---

## ▶️ GUI Usage

Once the model is trained (or if you already have `Cancer_detection_model.h5`), run the GUI:

```bash
python cancer_gui.py
```

Steps:

1. Click **📁 Upload Image**.
2. Select an image (`.jpg`, `.png`, `.jpeg`).
3. The model will display:

   * **Predicted Class**
   * **Accuracy (%)**

---

## 📊 Model Architecture

* Input: `180 x 180` images
* Layers:

  * Rescaling (Normalization)
  * Conv2D (16 → 32 → 64 filters) + MaxPooling
  * Flatten + Dropout
  * Dense (128)
  * Output: Softmax over number of classes

---




