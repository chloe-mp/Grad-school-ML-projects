# 🧠 Deep Learning Speech Recognition (Wav2Vec2)

This project is a modern reimplementation of a university assignment initially designed to use **HTK** (Hidden Markov Model Toolkit) for phoneme-level speech recognition.  
Instead of using HTK, I rebuilt the project using a **deep learning approach**, specifically leveraging the **Wav2Vec2** model and PyTorch-based tools for feature extraction, alignment, and classification.

---

## 🎯 Objective

To build a functional pipeline for **phoneme-level speech recognition** from raw audio using modern tools and deep learning techniques.

---

## 🚀 Why I Rebuilt It

> The original assignment relied on HTK — an outdated and difficult-to-use HMM toolkit.  
> I chose to redo the project using **Wav2Vec2**, **librosa**, and **PyTorch**, to explore a more modern, flexible, and intuitive approach to the task.

---

## 🧩 Pipeline Overview

1. **Audio Input**
   - Audio is loaded and processed using `librosa`
   - The waveform is normalized and resampled as needed

2. **Transcription with Wav2Vec2**
   - A pre-trained `facebook/wav2vec2-large-960h` model is used
   - Output: a raw text transcription
   - Transcription is converted to **phonemes** using the `phonemizer` library

3. **Phoneme Alignment**
   - A basic time alignment is generated using model logits and token timestamps
   - Each phoneme is associated with a time range in the audio

4. **Feature Extraction**
   - MFCCs are extracted with `librosa`
   - Feature statistics are computed (mean, min, max, std)

5. **Modeling (Experimental)**
   - A simple **LSTM-based model** is defined to predict phoneme sequences from MFCCs
   - A basic **HMM pipeline** using `hmmlearn` is also tested
   - Classification is done on a small number of phoneme categories

---

## 📊 Results

- **WER (Word Error Rate)**: ~15.3% — a solid result without fine-tuning
- Frequent `<UNK>` tokens suggest room for improvement in model adaptation
- MFCCs showed clear clustering by phoneme type
- The LSTM architecture is functional but not deeply optimized
- Pitch and energy analysis supported phoneme segmentation visually

---

## 🧠 Interpretation

This experiment shows that it's not only possible to replace HTK with modern deep learning tools — it's **preferable**.  
The pipeline is more flexible, more interpretable, and more in line with current research and industry practices.

---

## 📂 Files

| File | Description |
|------|-------------|
| `DL_speech_recognition.ipynb` | Full pipeline in notebook form |
| `*.wav` (not included) | Audio samples used for testing |

---

## 🧰 Tools & Libraries

- Hugging Face Transformers (`Wav2Vec2`)
- PyTorch
- librosa
- phonemizer
- hmmlearn
- matplotlib, pandas

---

## 👩‍💻 Author

Chloé Petridis  
Master 2 Langue & Informatique — Sorbonne Université  
Speech & Phonology coursework project

