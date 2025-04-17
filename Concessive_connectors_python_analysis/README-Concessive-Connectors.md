# 🔍 Cross-linguistic Corpus Analysis of Concessive Connectors

This project investigates the use of concessive discourse markers — specifically **"néanmoins"** and **"toutefois"** in French, and **"nevertheless"** and **"nonetheless"** in English — across various genres. It combines **corpus linguistics**, **translation analysis**, and **NLP tools** to assess their usage frequency, contextual behavior, and translation tendencies.

---

## 🎯 Objective

To compare the use and translation of concessive connectors across French and English corpora, using a combination of **quantitative** and **qualitative** analysis.

---

## 📚 Corpus

- Multilingual, genre-diverse texts (literature, journalism, legal writing, social media)
- Sources: Google Books, online press, tweets, legal texts
- Divided by language (FR/EN) and genre

---

## 🧰 Methodology

1. **Corpus Collection**
   - Texts scraped and saved as `.txt`
   - Sorted into genre folders per language

2. **Preprocessing**
   - Cleaning via Regex (removal of special characters and URLs)
   - Language detection via `langdetect`
   - Sentence segmentation and tokenization using **SpaCy**

3. **Connector Extraction**
   - Lemmatization and part-of-speech tagging
   - Frequency counts per genre and language
   - Contextual analysis with **word clouds** and **collocations**

4. **Translation Analysis**
   - Used **Google Translate API** to translate sentences with connectors
   - Categorized results into:
     - ✅ Direct translation
     - ❌ Omission
     - 🔁 Substitution (none observed)
   - Quantified and visualized outcomes

5. **Visualization**
   - Plotted frequencies, co-occurrences, and contextual differences using **Seaborn** and **Matplotlib**

---

## 📊 Key Results

- **French connectors** ("néanmoins", "toutefois") appeared more frequently than their English counterparts.
- Genres like **literature and legal writing** showed a higher frequency of concessive markers.
- English favored simpler forms like "however" or "but", while French leaned toward **stylistic variation**.
- Most Google Translate results were:
  - 48.7% direct matches
  - 51.3% omissions
  - 0% substitutions (literal bias)

---

## 🧠 Interpretation

- **Concessive connectors are genre-sensitive**: prevalent in formal or academic settings, rare in social media.
- **Language-specific stylistic preferences**:
  - French emphasizes logical structure through connectives
  - English allows more implicit relations
- **Automatic translations** often omit markers, especially in informal texts — this raises questions about fidelity and register awareness in MT tools.

---

## 📂 Files

| File | Description |
|------|-------------|
| `Projet1_linguistique_corpus.ipynb` | Main notebook for extraction, analysis & visualization |
| `Rapport projet linguistique de corpus.pdf` | Full academic report (in French) |

---

## 🛠️ Tools & Libraries

- Python
- SpaCy
- Pandas
- LangDetect
- Google Translate API
- Matplotlib & Seaborn

---

## 👩‍💻 Author

**Chloé Petridis**  
Master 2 Langue & Informatique – Sorbonne Université  
Linguistic Corpus Analysis Project, 2025
