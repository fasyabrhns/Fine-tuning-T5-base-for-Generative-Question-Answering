# Fine-tuning T5 for Question Answering

## 👥 Team Information

**Course:** Deep Learning  
**Institution:** Telkom University  

| Name | NIM |
| :--- | :--- |
| **Fasya Burhanis Syauqi** | 1103223054 |
| **Muhammad Muhammad Farhan** | [ISI NIM DISINI] |

---

## 🎯 Purpose

This repository contains the implementation of **Task 2: Question Answering (QA)**.

The objective is to fine-tune a pre-trained **T5 (Text-to-Text Transfer Transformer)** model to perform extractive question answering. Given a context paragraph and a question, the model learns to generate the correct answer span from the text.

## 🔍 Project Overview

### The Task: Question Answering
We utilize the **SQuAD (Stanford Question Answering Dataset)**, a reading comprehension dataset consisting of questions posed by crowdworkers on a set of Wikipedia articles.

### The Model: Google T5-base
* **Architecture:** Encoder-Decoder Transformer (Seq2Seq).
* **Approach:** We treat Question Answering as a text-generation problem, where the input is `question: <question> context: <context>` and the output is the `<answer>`.

### The Dataset: SQuAD
* **Input:** A passage of text (Context) and a specific Question.
* **Output:** The precise segment of text that answers the question.

---

## 📊 Technical Approach

### Model Configuration
* **Base Model:** `google/t5-base` (or `t5-small` depending on resource).
* **Tokenizer:** T5 Tokenizer (SentencePiece).
* **Framework:** PyTorch & Hugging Face Transformers.

### Training Configuration
* **Batch Size:** 16
* **Learning Rate:** 2e-5
* **Epochs:** 3
* **Optimizer:** AdamW

---

## 📁 Repository Structure

```text
.
├── notebooks/
│   └── task_2_deep_learning.ipynb    # Main Jupyter Notebook for QA Training
├── reports/                          # Training logs and metrics
├── requirements.txt                  # Python dependencies
└── README.md                         # Project documentation
