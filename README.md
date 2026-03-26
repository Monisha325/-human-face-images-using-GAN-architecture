# 🧠 Human Face Generation using GAN

## 📌 Overview

This project implements a **Generative Adversarial Network (GAN)** to generate realistic human face images using the **CelebA dataset**. The model learns facial features such as structure, texture, and patterns through adversarial training between two neural networks: Generator and Discriminator.

---

## 🚀 Features

* Generate realistic human face images
* Implemented using **PyTorch**
* Supports training on **Google Colab (GPU)**
* Handles dataset directly from **Google Drive folder**
* Saves generated images at each epoch
* Lightweight and fast training pipeline

---

## 🏗️ Project Structure

```
GAN-Face-Generation/
│
├── data/
│   └── raw/
│       └── celeba/
│           └── img_align_celeba/
│               └── faces/
│                   ├── 000001.jpg
│                   ├── 000002.jpg
│                   └── ...
│
├── outputs/
│   ├── images/
│   └── checkpoints/
│
├── GAN_Face_Generation.ipynb
└── README.md
```

---

## 📂 Dataset

* Dataset used: **CelebA (Large-scale CelebFaces Dataset)**
* Contains thousands of aligned human face images
* Images are resized and normalized before training

👉 Ensure dataset structure:

```
img_align_celeba/
   faces/
       images...
```

---

## ⚙️ Installation

Install required libraries:

```bash
pip install torch torchvision matplotlib
```

---

## ▶️ How to Run

1. Open the notebook in **Google Colab**
2. Enable GPU:

   ```
   Runtime → Change runtime type → GPU
   ```
3. Mount Google Drive:

   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```
4. Set dataset path:

   ```python
   DATA_PATH = "/content/drive/MyDrive/GAN-Face-Generation/data/raw/celeba/img_align_celeba"
   ```
5. Run all cells sequentially

---

## 🧠 Model Architecture

### Generator

* Takes random noise as input
* Uses Transposed Convolution layers
* Outputs fake human face images

### Discriminator

* Classifies images as real or fake
* Uses Convolution layers
* Outputs probability score

---

## 🔄 Training Process

1. Generate fake images from noise
2. Train discriminator on real + fake images
3. Train generator to fool discriminator
4. Repeat for multiple epochs

---

## 📈 Results

* Initial epochs: noisy images
* Mid training: partial facial features
* Final epochs: realistic human faces

Generated images are saved in:

```
outputs/images/
```

---

## ⚠️ Limitations

* Training instability
* Blurry outputs in early stages
* Requires tuning for better results

---

## 🚀 Future Improvements

* Implement **WGAN-GP** for stability
* Increase resolution (64×64 or higher)
* Use **StyleGAN** for high-quality images
* Add evaluation metrics (FID Score)

---

## 🎯 Applications

* Image synthesis
* AI-generated avatars
* Data augmentation
* Research in generative models

---

## 💡 Key Concept

> GAN consists of two networks competing with each other — one generates images, and the other evaluates them — improving both over time.

---

## 👩‍💻 Author

* Your Name

---

## ⭐ Acknowledgements

* CelebA Dataset
* PyTorch
* Google Colab

---

