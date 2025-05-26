# 🧩 RepieceViT

**RepieceViT** is a Vision Transformer (ViT)-based model designed to solve the **Jigsaw Puzzle Task** on image datasets like STL-10 and CIFAR-10. The model takes a shuffled 3×3 grid of image patches (from 96×96 images) and predicts the correct position of each patch, learning spatial and semantic relationships in the image.

## 📚 Project Overview

The notebook [`repiece_ViT.ipynb`](https://github.com/DeAnd02/RepieceViT/blob/main/repiece_ViT.ipynb) contains the full pipeline:

- Splitting input images into 9 shuffled patches (32×32)
- Vision Transformer architecture for spatial reasoning
- Training the model to reconstruct the correct patch order
- Evaluation and visualization of qualitative results
- Support for datasets like STL-10 and CIFAR-10

## 🧠 Model Architecture

The model follows a simplified Vision Transformer (ViT) design adapted for jigsaw solving:

- **Patch Embedding**: Each image patch is projected to a fixed-size vector.
- **Positional Encoding**: Learnable embeddings to encode patch positions.
- **Transformer Encoder**: Multiple self-attention layers for contextual learning.
- **Prediction Head**: Fully-connected layers that output the predicted position for each patch.

## 🚀 Setup & Requirements

You can run the notebook in environments like Google Colab or locally with:

- Python 3.8+
- PyTorch
- torchvision
- matplotlib
- numpy
- tqdm

Install dependencies with:

```bash
pip install torch torchvision matplotlib numpy tqdm
