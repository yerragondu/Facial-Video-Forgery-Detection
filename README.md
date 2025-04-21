# Facial Video Forgery Detection using MesoNet

This project implements a deep learning pipeline for detecting facial video forgeries, specifically focusing on **DeepFake** and **Face2Face** manipulation techniques. It utilizes the lightweight and efficient **MesoNet** architecture to classify whether a given facial image is real or forged.

The system can operate as a complete pipeline: from **video frame extraction**, through **face detection**, to **classification** using pretrained models.

---

## 📁 Project Structure

```
.
├── test_images/           # Contains test images for evaluation
├── weights/               # Pretrained MesoNet weights for DeepFake (_DF) and Face2Face (_F2F)
├── LICENSE                # Project license (Apache-2.0)
├── README.md              # This README file
├── classifiers.py         # Defines MesoNet models and classification logic
├── example.py             # Example script for running classification
├── pipeline.py            # End-to-end pipeline with face detection and classification
├── test.py                # Script for testing model performance
```

---

## 🔧 Requirements

> Python 3.5 is recommended for compatibility with original Keras versions.

Install dependencies:

```bash
pip install numpy==1.14.2 keras==2.1.5 imageio face_recognition
```

Ensure **FFMPEG** is installed on your system for video processing.

---

## ▶️ How to Run

### 1. Using Pretrained Models (Recommended)

- DeepFake model: `Meso4_DF`
- Face2Face model: `Meso4_F2F`

```bash
python example.py --model weights/Meso4_DF.h5 --input test_images/
```

Or use the full pipeline with face detection:

```bash
python pipeline.py --video input_video.mp4 --model weights/Meso4_F2F.h5
```

> Note: You can switch between models by replacing the `.h5` file accordingly.

---

## 🧪 Dataset

The project is trained on **aligned face datasets**, split into:

| Set        | Forged Images | Real Images |
|------------|---------------|-------------|
| Training   | 5,111         | 7,250       |
| Validation | 2,889         | 4,259       |

- Training set size: ~150 MB  
- Validation set size: ~50 MB  

**📩 Dataset Access:**  
The dataset is not publicly hosted but **can be made available upon request** for academic and research purposes. Please contact the project maintainer or raise an issue in the repository to request access.

---

## 🧠 Pretrained Weights

You can find pretrained models inside the `weights/` folder:

- `Meso4_DF.h5` – trained for DeepFake detection
- `Meso4_F2F.h5` – trained for Face2Face detection

These models are ready to use and achieve high classification accuracy on aligned face images.

---

## 📄 License

This project is licensed under the **MIT License**.

---



