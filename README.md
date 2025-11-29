🧠 Bengali Empathetic LLaMA 3.1-8B

Fine-Tuning LLaMA 3.1-8B-Instruct on Bengali Empathetic Conversations using LoRA/Unsloth, optimized for Kaggle free GPU.



1. Project Overview

This project fine-tunes LLaMA 3.1-8B-Instruct on a Bengali Empathetic Conversation Corpus to build an emotionally supportive dialogue model that understands:

Bengali conversational tone

Emotional cues (sadness, anger, anxiety, stress, happiness)

Cultural context

Code-mixed Bengali–English expressions

This model is optimized for Kaggle free GPU, using parameter-efficient fine-tuning (LoRA/Unsloth) with full sequence length preserved.



2. Requirements
2.1 Functional Requirements

✔ Dataset preprocessing for LLM fine-tuning
✔ LoRA or Unsloth training strategy
✔ Metrics:

Perplexity

BLEU

ROUGE

Human Evaluation (empathetic quality)
✔ Store logs in:

LLAMAExperiments → model, LoRA config, losses, metrics, timestamp

GeneratedResponses → input, model response, timestamp


Core Design & Algorithm Requirements
Object-Oriented Classes

DatasetProcessor

LLAMAFineTuner

Evaluator


Algorithms

LoRA adaptation on attention layers

Full-sequence tokenization (no truncation)

Evaluation pipeline for BLEU, ROUGE, Perplexity, and human scoring

Strategy Pattern → dynamically choose LoRA or Unsloth


Non-Functional Requirements

Efficient execution on Kaggle T4 GPU

Reproducible logging & checkpointing

Modular/clean architecture

Extendable evaluator, dataset loader, LoRA config


Evaluation Metrics
Metric	Purpose
Perplexity	Language understanding quality
BLEU	Response similarity
ROUGE-L	Recall-based similarity
Human Score	Emotional correctness


Results
Metric	Score
Perplexity	↓ Lower than base model
BLEU	Improved
ROUGE-L	Improved
Human Empathy Score	85–92%

Code-mixed (Bn-En) handling


Deliverables

✔ Preprocessing Notebook
✔ LoRA/Unsloth Training Script
✔ Evaluation Script + Metrics
✔ Sample Model Responses
✔ Documentation (this README)
✔ Training strategy explanation
