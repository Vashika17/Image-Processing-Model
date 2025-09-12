# Gear Match Detection using Siamese Network

This project implements a **Siamese Neural Network** to detect whether a 3D printed gear matches its original CAD design.  
It uses a *contrastive loss* approach to learn feature embeddings for a **fixed CAD reference image** and **multiple printed gear images**, classifying them as **match** or **non-match** based on their visual similarity.

---

## 📌 Project Overview
- **Goal**: Verify if a printed gear visually matches a given CAD model image.  
- **Approach**:
  - A **ResNet-18** backbone (pretrained on ImageNet) is used as a feature extractor.
  - The network takes a pair of images (CAD vs. printed) and outputs embeddings.
  - The contrastive loss minimizes the distance between embeddings of *matching* pairs and maximizes it for *non-matching* pairs.
- **Output**: During inference, a distance score between the CAD and printed image embeddings determines whether they match.

---

## 📂 Directory Structure
