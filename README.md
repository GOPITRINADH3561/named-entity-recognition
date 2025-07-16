# Named Entity Recognition

## 📄 Overview

This project involves performing Named Entity Recognition (NER) in three phases:

1. Manual annotation using an online NER tool  
2. Automatic entity detection using SpaCy's built-in `en_core_web_sm` pipeline  
3. Accuracy assessment comparing SpaCy's predictions against manual annotations

The goal is to evaluate how well SpaCy performs on real-world tweet data.

---

## 🗂 Data Description

- **Tweets Source:** Cleaned tweets from Kaggle (`Assignment 1 Data.xlsx`)
- **Sheet Used:** `Tweets` (assigned 300 tweets via `Roster` sheet)
- **Entities Annotated:**
  - `PERSON`
  - `NORP`
  - `ORG`
  - `GPE`
  - `LOC`
  - `DATE`
  - `MONEY`

---

## 🚦 Phase 1: Manual NER Annotation

Used the online tool: [NER Annotator](https://tecoholic.github.io/ner-annotator/)

### Steps:
- Extracted 300 assigned tweets to `Sentences.txt`
- Loaded into NER Annotator with:
  - `New Line` separator
  - `Character Level` precision
- Annotated using 7 entity types
- Exported labeled data as `annotations.json`

---

## 🧠 Phase 2: Named Entity Recognition with SpaCy

- Loaded pretrained SpaCy model: `en_core_web_sm`
- Parsed each tweet with `nlp(sentence.strip())`
- Extracted only the specified entity tags
- Stored predicted results using a counter for each entity

---

## 📊 Phase 3: Accuracy Assessment

Compared SpaCy’s predictions with manual annotations:

### Metrics Used:
- **Precision** = TP / (TP + FP)
- **Recall** = TP / (TP + FN)
- **F1 Score** = Harmonic mean of precision and recall

### Observations:
- `MONEY` tag had the **highest Precision**
- `LOC` tag had the **lowest Recall**
- `DATE` tag had the **best F1 Score**

---

## 📎 Files Included

- `Coded_solution.ipynb`: All code (data loading, SpaCy NER, and evaluation)
- `annotations.json`: Manually labeled entities in SpaCy JSON format
- `Report.pdf`: Detailed explanation of each phase and performance analysis

---

## ⚠️ Academic Integrity

> No AI tools were used to write the report. Manual annotations were done as per instructions. Coding assistance tools were used only for code debugging, not report writing.
