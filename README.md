# 🧠 AutoEncoders for Dimensionality Reduction & Feature Learning
![Made with Python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)
![TensorFlow/Keras](https://img.shields.io/badge/Framework-TensorFlow%2FKeras-blue)
![AutoEncoder](https://img.shields.io/badge/Model-AutoEncoder-green)
![Dataset](https://img.shields.io/badge/Dataset-MNIST-orange)
![Task](https://img.shields.io/badge/Task-Dimensionality%20Reduction-yellowgreen)
![Notebook](https://img.shields.io/badge/Notebook-Jupyter-yellow)
![License](https://img.shields.io/badge/License-MIT-green)


This project demonstrates how AutoEncoders can be used for **dimensionality reduction**, **data visualization**, and **hidden feature extraction** using neural networks. It compresses and reconstructs images from the MNIST dataset to reveal underlying patterns in data.

---

## 🔍 Objective

AutoEncoders are neural networks that aim to learn a compressed representation of the input data (encoding) and reconstruct the input back from this representation (decoding). They are powerful tools for:
- Dimensionality reduction
- Visualization of data in lower dimensions
- Revealing hidden relationships between features

---

## 🧰 Project Highlights

- **Architecture**:
  - **Encoder**: Stack of `Dense` layers followed by a `Flatten` layer, gradually reducing the number of neurons from 400 down to 25.
  - **Decoder**: Mirror architecture of the encoder using `Dense` layers and a final `Reshape` layer to reconstruct the input.
  - **Symmetry**: Input and output layer sizes are equal (important for AutoEncoders).

- **Loss & Activation**:
  - `Sigmoid` activation is used in the output layer.
  - `binary_crossentropy` is used as the loss function because we are comparing the input image with the reconstructed output (pixel-level).

- **Dataset**:
  - MNIST dataset containing grayscale handwritten digits (0–9).
  - The focus is not on classification but on learning data representation.

---

## 📊 Model Summary

| Layer Type | Neurons / Shape | Role |
|------------|------------------|------|
| Input Layer | 784 (28x28) | Flattened image input |
| Encoder | 400 → ... → 25 | Dimensionality reduction |
| Decoder | 25 → ... → 784 | Reconstruction |
| Output Layer | 784 | Image reconstruction (same size as input) |

---

## 💡 Key Insights

- AutoEncoders can effectively compress high-dimensional input data while retaining important features.
- The learned compressed representation (25 neurons) can be used for visualization or clustering.
- Hidden layers in the middle of the network act as a bottleneck to capture key patterns.

---

## 🧪 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/AutoEncoder-Project.git
   cd AutoEncoder-Project


---

## 🔮 Future Work

- Implement denoising AutoEncoders
- Visualize latent space using PCA or t-SNE
- Explore convolutional AutoEncoders for image data

---

## 📚 References

- [Understanding AutoEncoders - Deeplizard](https://deeplizard.com/)
- [MNIST Dataset](http://yann.lecun.com/exdb/mnist/)

---
