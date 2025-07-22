# 🤖 Context-Aware Chatbot

This project demonstrates a **Context-Aware Chatbot** built using transformer-based language models. The chatbot can maintain context across multiple turns in a conversation, enabling more natural and coherent interactions.

---

## 📌 Objective

To build an intelligent chatbot capable of understanding and remembering previous messages in a conversation to deliver relevant and context-sensitive responses.

---

## 📁 Dataset / Input

- The chatbot does not require supervised training data by default.
- It utilizes a **pretrained transformer model** (e.g., GPT-2 or DialoGPT).
- Input consists of:
  - A sequence of user and bot messages
  - Maintained conversation history to provide contextual relevance

---

## ⚙️ Technologies & Libraries Used

- Python
- `transformers` (Hugging Face)
- `torch` (PyTorch backend)
- `nltk` (tokenization and text preprocessing)
- Jupyter Notebook

---

## 🔍 Chatbot Pipeline Overview

1. **Conversation Setup**
   - Initializes a pretrained transformer model and tokenizer
   - Defines a method for storing and updating conversation history

2. **User Interaction Loop**
   - Accepts user input
   - Appends it to context
   - Generates model output using the full conversation history

3. **Context Management**
   - History is truncated or trimmed to fit model’s token limit
   - Ensures model memory remains relevant to the latest context

4. **Response Generation**
   - Uses model’s `generate()` function with decoding strategies like:
     - Top-k sampling
     - Temperature control
     - Maximum length

---
