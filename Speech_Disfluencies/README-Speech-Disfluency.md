# 🗣️ Spontaneous Speech Transcription & Disfluency Analysis (Texan English)

This project focuses on the **phonetic, phonological, and syntactic analysis** of spontaneous speech in **Texan-accented American English**. The study aims to investigate how disfluencies (e.g., hesitations, filler words, repetitions) relate to the phonetic specificities of the Texan variety and how these features affect speech production.

---

## 🎯 Objectives

- Analyze a spoken dialogue in Texan English for disfluency patterns
- Study how disfluencies reflect **regional phonetic characteristics**
- Measure vocal features such as pitch (F0) and formants (F1, F2)
- Understand the relationship between accent, spontaneity, and syntax

---

## 🧩 Methodology

### 🔉 Corpus

- Extracted from a U.S. **radio show featuring two Texan male speakers**
- Duration: ~3 minutes of informal, spontaneous speech
- Context: Casual storytelling with emotional and humorous exchanges

---

### 🔍 Workflow Overview

1. **Audio Preprocessing**
   - Annotated with **Praat** and aligned using a `.TextGrid` file
   - Transcribed using **OpenAI’s Whisper API** and verified manually

2. **Disfluency Tagging**
   - Manual annotation of disfluencies (hesitations, filler words, pauses, etc.)
   - Classification in an Excel sheet (`Projet_1_dysfluences.xlsx`)
   - Mapped to their **syntactic position** in the utterance

3. **Lexical & Syntactic Analysis**
   - Word frequency analysis using Python
   - Qualitative review of informal and regional expressions
   - Study of contractions, ellipses, deixis, and discourse markers

4. **Phonetic Analysis**
   - Extracted pitch (F0) and formants (F1, F2)
   - Visualized with **matplotlib**
   - Evaluated vowel openness and articulatory positioning

---

## 📊 Key Findings

### 📌 Lexical & Disfluency Analysis

- High frequency of **filler words**:  
  *“you know” (7), “like” (6), “right” (5), “dude” (5), “yeah” (4), etc.*
- Disfluencies serve as **cognitive and emotional markers**, not just noise
- Indicative of **natural speech rhythm**, emotional involvement, and **Texan social identity**
- Frequent use of **regional expressions** (e.g. *“bless her heart”*) and informal grammar

### 📌 Phonetic Features

- **Pitch (F0)** ≈ 150 Hz → typical male voice, calm tone  
- **F1 (893 Hz)** → use of open vowels (e.g., /æ/)  
- **F2 (1949 Hz)** → tendency toward front vowels (/i/, /e/)  
- **Formant distribution** confirms typical Texan vowel shifts and diphthongization

### 📌 Syntactic Observations

- Frequent **sentence fragments, contractions, ellipses**
- Parataxis and simplified structures (e.g., “Riding, riding what?”)
- Use of **conjunctions** (“so”, “and”) to link ideas informally
- Dialogue reflects **high spontaneity and emotional engagement**

---

## 🧠 Interpretation

This project reveals that **disfluencies are deeply tied to identity, spontaneity, and region**. The Texan accent shows both expected phonetic patterns and rich sociolinguistic signals through vocabulary, syntax, and rhythm. Rather than being flaws, disfluencies in this context serve communicative and expressive purposes.

---

## 🧰 Tools Used

- **Praat**: phonetic annotation
- **Whisper (OpenAI)**: automatic transcription
- **Python (matplotlib, pandas)**: data analysis and visualization
- **Excel**: disfluency classification
- **TextGrid**: time-aligned annotation

---

## 📁 Files

| File | Description |
|------|-------------|
| `Code_projet_1_transcription_parole.ipynb` | Python code for analysis |
| `synthRadio201_16.TextGrid` | Time-aligned Praat annotations |

---

## 👩‍💻 Author

Chloé Petridis — Master 2 Langue & Informatique  
Sorbonne Université  
Project completed as part of the *Phonologie et traitement de la parole* course
