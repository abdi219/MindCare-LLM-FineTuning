# Mental Health Chatbot Fine Tuning

This project was completed as part of the AI/ML Engineering Internship at DevelopersHub Corporation.

---

# Project Overview

This project focuses on fine-tuning a lightweight causal language model to build a supportive mental health chatbot. The system is designed to understand emotional input from users and generate empathetic, context-aware responses without repetitive or mirrored outputs.

---

# Dataset

The dataset used is empathetic_dialogues from Hugging Face, which contains real-world human conversations labeled with emotional context.

Target structure:
Therapist response (empathetic reply to user input)

Key inputs used:
- Emotional context prompt
- User utterance

---

# Data Preprocessing

- Mapped user emotional input to model input format
- Matched user utterance with corresponding empathetic response
- Tokenized text into numerical format for model processing
- Applied padding and truncation to maintain fixed sequence length (128 tokens)
- Selected a subset of samples for faster training and experimentation

---

# Exploratory Data Analysis

- Analyzed conversation structure and emotional patterns in dataset
- Verified alignment between emotional context and response tone
- Ensured dataset consistency for causal language modeling

---

# Model Used

Pre-trained DistilGPT-2 model was used for fine-tuning.

Training configuration:
- Epochs: 2
- Batch size: 8
- Learning rate: 5e-5
- Mixed precision (fp16): enabled for GPU training

---

# Model Training

The model was trained using Hugging Face Trainer API on a T4 GPU.
Training was performed over multiple epochs to optimize response generation capability.

---

# Evaluation & Inference Improvements

- Temperature set to 0.5 for stable outputs
- Top-k sampling limited to 50 tokens
- Top-p sampling set to 0.92 probability threshold
- No-repeat n-gram size set to 2 to reduce repetition

---

# Results Interpretation

- Reduced repetition of user input in responses
- Improved contextual relevance of chatbot outputs
- Generated more stable and empathetic responses

---

# Conclusion

This project demonstrates a complete pipeline for fine-tuning a causal language model for empathetic chatbot behavior.

---

# Future improvements:

- Increase dataset size
- Train for more epochs
- Use a larger transformer modl
