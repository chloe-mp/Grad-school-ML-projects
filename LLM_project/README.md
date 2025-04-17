# LLM-powered Innovation Chatbot

This project implements a chatbot capable of understanding user queries about recent technological innovations using a combination of NLP, large language models (LLMs), and a structured innovation knowledge base.

---

## 💡 Objective

The goal is to build an intelligent assistant that can:

- **Understand natural language questions** in French
- **Detect user intentions** (e.g., ask, compare, explain)
- **Extract key information** (slots) like topics or categories
- **Provide relevant responses** based on a curated innovation database or generate responses using a fine-tuned LLM

---

## 🧠 Architecture

The chatbot is designed using a **Hierarchical Task Analysis (HTA)** framework, where user interactions are broken down into tasks and subtasks such as:

- Intent recognition
- Slot extraction
- Context handling
- Response generation

Each component is modular and responds to specific subtasks, enabling clear separation of concerns and easier scaling.

---

## 🧩 Project Components

### 1. **Dialogue Manager (`Gestionnaire_de_dialogue.py`)**

This is the core of the system. It handles:

- **Intent detection** using keywords and expressions from a structured lexicon (`lexique.json`)
- **Slot filling**: identifying named entities (dates, concepts, categories, etc.)
- **Language detection** to support multilingual input (via `langdetect`)
- **Answer generation** either:
  - from a structured innovation file (`innovation_data.json`)
  - or using a pre-trained LLM model like `Gemma` for open-ended responses

---

### 2. **Knowledge Sources**

- `innovation_data.json`: A structured JSON file listing innovations from 2024–2025 in domains like AI, cybersecurity, cloud, quantum computing, etc.
- `chatbot_history.json`: Keeps track of user–bot conversations for context reuse
- `Corpus_dialogues_LLM`: Example dialogues for pretraining or testing intent detection

---

## 🤖 Technologies

- **Spacy**: For French NLP (tokenization, NER, lemmatization)
- **Transformers (Hugging Face)**: To load a local LLM (e.g. `gemma-2b-it`)
- **Torch**: For model inference on GPU or CPU
- **Custom intent detection system**: Based on slot-based matching and lexical rules

---

## 📊 Results and Analysis

The chatbot was tested on a variety of queries including:

- Requests for definitions (`"What is quantum computing?"`)
- Comparisons (`"What's the difference between 5G and 6G?"`)
- Contextual follow-ups (`"Tell me more about Gemini AI"`)
- History recall and confirmation detection (`"Show me my chat history"`)

The bot shows strong performance in:
- **Detecting user intentions** accurately, even with vague queries
- **Adapting responses to context**, using past inputs from `chatbot_history.json`
- **Answering fact-based questions** from structured data when available

When the LLM is used:
- The responses are **contextually rich**, sometimes even verbose or nuanced
- The **temperature and repetition penalty** settings help control creativity and redundancy

---

## 📁 Project Files

| File | Description |
|------|-------------|
| `Gestionnaire_de_dialogue.py` | Main logic (intent detection, LLM calls, slot extraction) |
| `innovation_data.json` | Structured data on recent innovations |
| `chatbot_history.json` | Logged conversations |
| `Corpus_dialogues_LLM.*` | Test and example queries |
| `lexique.json` | Intent detection rules and keywords |

---

## 📌 Use Case

This chatbot is especially suited for:

- **Educational support** in technology courses
- **Digital assistants** for innovation consultants or R&D departments
- **Language model experiments** in intent-slot NLP frameworks

---

## 📚 Example Query

> **User**: "What are the latest innovations in cybersecurity?"  
> **Bot**:  
> "Here are recent innovations:  
> - Zero Trust Security  
> - AI for cyberattack detection  
> - Next-gen firewalls using behavioral analysis.  
> Would you like more info on one of these?"

---

## 🚀 Future Improvements

- Integration with real-time news APIs
- More robust language model fine-tuning

---

Made by Chloé Petridis
