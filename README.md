# 🧬 Cancer Information Assistant (FLAN-T5 + LoRA)

An educational cancer Q&A chatbot built by fine-tuning **google/flan-t5-base (220M)** using **LoRA (PEFT)**.
The assistant provides **general medical information only** and follows strict safety rules.

---

## 🚀 Features

- Educational cancer-related explanations
- Strict medical safety guardrails
- No diagnosis or treatment recommendations
- Lightweight fine-tuning with LoRA (≈1.4% trainable params)
- Interactive Gradio web interface

---

## 🧠 Model Details

- **Base Model**: `google/flan-t5-base`
- **Fine-tuning Method**: LoRA (PEFT)
- **Trainable Parameters**: ~3.5M (1.4%)
- **Frameworks**: Hugging Face Transformers, PEFT, PyTorch

---

## 📊 Dataset

- Curated cancer-related Q&A dataset
- Focused on:
  - cancer definitions
  - symptoms (educational)
  - causes & prevention
- Explicitly excludes:
  - diagnosis
  - prescriptions
  - treatment plans

---

## 🛡️ Safety Design

The assistant is explicitly instructed to:
- ❌ NOT diagnose diseases
- ❌ NOT prescribe medicines or treatments
- ✅ Encourage consulting healthcare professionals
- ✅ Provide general educational information only

A post-generation safety filter prevents misleading medical generalizations.

---

## 🧪 Evaluation Strategy

Instead of relying on validation loss, the model was evaluated using:
- Prompt-based qualitative testing
- Safety compliance tests
- Human inspection of generated responses

This reflects real-world LLM evaluation practices.

---
## sample
what are common symptoms of lung cancer?

Model Answer (Educational):
 -Common symptoms of lung cancer may include:
 -A persistent cough or changes in an existing cough
 -Shortness of breath or difficulty breathing
 -Chest pain or wheezing
 -Fatigue or weakness
 -Unexplained weight loss or loss of appetite
 -Frequent respiratory infections



## 🖥️ Demo

Run the Gradio app:

```bash
python app.py
