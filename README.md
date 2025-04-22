# 🎙️ Deepfake Audio Detection

This project focuses on detecting deepfake (synthetically generated) audio using deep learning models. The objective is to classify audio samples as either *real* or *manipulated* based on their spectral characteristics.

---

## 📌 Overview

This repository outlines the complete pipeline for deepfake audio classification. From initial observation and preprocessing of audio files to model training and evaluation, the project utilizes advanced CNN architectures to achieve accurate predictions.

---

## 📂 Data Preprocessing

The following steps were performed to ensure the dataset was clean and suitable for training:

1. **Audio File Observation**
   - Initial inspection of audio files to ensure data integrity and consistency.

2. **Histogram Analysis**
   - Histograms were plotted to visualize amplitude distributions and identify anomalies.

3. **Sample Rate & Channel Check**
   - Verified that all audio files had consistent sample rates.
   - Ensured uniformity in audio channel configuration (mono/stereo).

4. **Mel-Spectrogram Conversion**
   - All audio samples were converted to mel-spectrogram images to enable image-based classification.

5. **Dataset Splitting**
   - Converted spectrograms were split into:
     - Training Set
     - Validation Set
     - Test Set

---

## 🧠 Model Training

Two deep convolutional neural network architectures were used for training:

- **ResNet101**
- **EfficientNetB4**

Both models were trained using the generated mel-spectrogram images. The networks were fine-tuned to optimize classification performance on the task of deepfake audio detection.

---

## 🧪 Model Evaluation

After training, inference was carried out on the test set to evaluate performance:

- **ResNet101 Accuracy**: **85.41%**
- **EfficientNetB4 Accuracy**: **87.29%**

EfficientNetB4 outperformed ResNet101 by a small margin in terms of accuracy.

---

## 🛠️ Tech Stack

- Python
- Librosa (for audio processing)
- Matplotlib / Seaborn (for visualization)
- NumPy / Pandas (for data handling)
- PyTorch / TensorFlow (for model training)
- OpenCV (for image manipulation)
- Pretrained CNNs: ResNet101, EfficientNetB4

---

## 🚀 Future Improvements

- Incorporate Wave2Vec 2.0 and other transformer-based models for raw audio classification.
- Explore LSTM or GRU-based models for temporal audio dynamics.
- Evaluate model robustness on unseen and adversarial deepfake samples.

---

## 📄 License

This project is intended for educational and research purposes only.
