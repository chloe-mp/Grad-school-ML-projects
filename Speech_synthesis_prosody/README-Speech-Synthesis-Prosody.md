# 🗣️ Speech Synthesis and Prosody Analysis

This project explores different methods of **text-to-speech (TTS)** synthesis, with a focus on the **prosody** (intonation, rhythm, and emphasis) of the generated speech. The aim is to evaluate how various synthesis systems reproduce natural speech dynamics, particularly in expressive contexts like poetry and storytelling.

---

## 🎯 Objectives

- Compare **neural** and **rule-based** TTS systems in terms of prosodic rendering
- Analyze the acoustic properties (F0, duration, energy) of synthesized speech
- Perform a **classification task** to evaluate how distinguishable the systems are based on prosodic features

---

## 🧩 Systems Compared

| System     | Type           | Description |
|------------|----------------|-------------|
| CoquiTTS   | Neural         | Deep learning-based TTS with expressive voice models |
| eSpeak     | Rule-based     | Lightweight multilingual speech synthesizer |
| Mbrola     | Rule-based     | Legacy system (not used in final experiments due to compatibility issues) |

> **Note**: Mbrola was initially considered but excluded due to technical issues and its obsolescence.

---

## 🧪 Methodology

1. **Synthesis**
   - Selected expressive texts (e.g., poetry, dialogue)
   - Generated audio using CoquiTTS and eSpeak
   - Exported `.wav` files for analysis

2. **Acoustic Feature Extraction**
   - Used **Librosa** to compute:
     - **Fundamental frequency (F0)** = pitch contour
     - **Duration** and **energy**
   - Saved results to `prosody_analysis_librosa.csv`

3. **Perceptual Classification**
   - Embedded audio samples using `Wav2Vec2`
   - Trained an **SVM classifier** to distinguish between TTS systems based on prosodic features

---

## 📊 Results

### 🔈 Prosody Analysis

- CoquiTTS produces **more natural pitch variation**, closer to human speech
- eSpeak has **flat intonation**, limited emphasis and emotional rendering
- Duration and energy contours are more dynamic in CoquiTTS outputs

### 🎯 Classification Task

- **SVM model** achieved high accuracy (>90%) distinguishing between the two systems
- Indicates that prosodic differences are **clearly detectable** in the acoustic signal

---

## 💡 Interpretation

This experiment shows that **neural TTS systems** (like CoquiTTS) are significantly more effective at rendering expressive and realistic prosody compared to rule-based systems.  
The acoustic analysis and classification results confirm that **prosody is a strong cue** for TTS quality and system identification.

---

## 📂 Files

| File | Description |
|------|-------------|
| `Projet_3_Montacié.ipynb` | Jupyter notebook for analysis |
| `prosody_analysis_librosa.csv` | Extracted prosodic features |
| *(Optional)* `Projet synthèse de la parole.docx` | Full report (not needed for execution) |

---

## 🧰 Tools & Libraries

- [CoquiTTS](https://github.com/coqui-ai/TTS)
- eSpeak
- Librosa
- Wav2Vec2 (Hugging Face Transformers)
- Scikit-learn (SVM)

---

## 👩‍💻 Author

Chloé Petridis — Master 2 Langue & Informatique  
Sorbonne Université — Project 3: Synthèse et analyse prosodique

