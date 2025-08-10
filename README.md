# Facial Expression Recognition using Weighted Graphs and LSTMs

This repository contains an end-to-end **video-level facial expression recognition** (FER) system.  
It detects facial landmarks from videos using **MediaPipe Face Mesh**, constructs **weighted graphs** from selected landmark pairs, and models temporal variations in edge weights using an **LSTM network** to classify emotions.

The implementation is modular and can be adapted to any labeled video dataset.  
No dataset is included here due to size and licensing; instructions are provided for preparing your own.

---

## How It Works

1. **Landmark Detection**  
   Extracts 468 facial landmarks per frame using MediaPipe Face Mesh.

2. **Graph Construction**  
   Connects specific landmark pairs to form edges; weights are Euclidean distances.

3. **Feature Extraction**  
   Captures temporal changes in edge weights across frames.

4. **LSTM Classification**  
   Uses sequential features to predict the emotion at the video level.

---

## Notes
Dataset must be prepared separately; see data/README.md for instructions.
Large model weights (>100MB) should be hosted externally (GitHub Releases, Hugging Face, etc.).
This project is intended for research and learning, not optimized production deployment.
