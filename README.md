# Understanding Transformers and Hugging Face

## Overview

This repository contains the implementation and documentation for the assignment **"Understanding Transformers and Hugging Face"**. The project explores the Transformer architecture, analyzes a Hugging Face model card, and demonstrates practical applications using Hugging Face AutoClasses for text summarization and language translation.

---

## Assignment Objectives

The primary objectives of this project are:

- Understand the fundamentals of Natural Language Processing (NLP)
- Explore the limitations of RNNs and LSTMs
- Learn why Transformers were introduced
- Study the Transformer architecture in detail
- Analyze a Hugging Face Transformer model card
- Implement Text Summarization using Hugging Face AutoClasses
- Implement Language Translation using Hugging Face AutoClasses
- Evaluate model outputs and document observations

---

## Topics Covered

### 1. Introduction to NLP

- What is Natural Language Processing (NLP)?
- Applications of NLP
- Limitations of RNNs
- Limitations of LSTMs
- Why Transformers were introduced
- Significance of the *Attention Is All You Need* paper

### 2. Transformer Architecture

- Input Embeddings
- Positional Encoding
- Self-Attention Mechanism
- Query, Key, and Value
- Multi-Head Attention
- Feed Forward Networks (FFN)
- Residual Connections
- Layer Normalization
- Encoder Architecture
- Decoder Architecture

### 3. Hugging Face Model Card Analysis

Selected Model:

```text
facebook/bart-large-cnn
```

Analysis includes:

- Model Name
- Architecture
- Intended Use Cases
- Training Data
- Evaluation Metrics
- Limitations and Biases
- License Information

### 4. Practical Implementation

#### Task 1: Text Summarization

Model Used:

```text
facebook/bart-large-cnn
```

Implemented using:

```python
AutoTokenizer
AutoModelForSeq2SeqLM
```

#### Task 2: Language Translation

Model Used:

```text
Helsinki-NLP/opus-mt-en-fr
```

Implemented using:

```python
AutoTokenizer
AutoModelForSeq2SeqLM
```

---

## Technologies Used

- Python
- Google Colab
- Hugging Face Transformers
- PyTorch
- LangChain (Optional Integration)
- GitHub

---

## Project Structure

```text
Understanding-Transformers-HuggingFace/
│
├── README.md
├── transformers_assignment.ipynb
├── screenshots/
│   ├── summarization_output.png
│   ├── translation_output.png
│   └── architecture_diagram.png
│
└── requirements.txt
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/Understanding-Transformers-HuggingFace.git
```

Navigate to the project folder:

```bash
cd Understanding-Transformers-HuggingFace
```

Install dependencies:

```bash
pip install transformers
pip install torch
pip install sentencepiece
pip install accelerate
pip install langchain
pip install langchain-community
pip install huggingface_hub
```

---

## Text Summarization Example

```python
from transformers import AutoTokenizer, AutoModelForSeq2SeqLM

model_name = "facebook/bart-large-cnn"

tokenizer = AutoTokenizer.from_pretrained(model_name)
model = AutoModelForSeq2SeqLM.from_pretrained(model_name)
```

Sample Input:

```text
Artificial Intelligence is transforming industries across the globe.
```

Sample Output:

```text
Artificial Intelligence is transforming industries by improving efficiency and decision-making.
```

---

## Language Translation Example

```python
from transformers import AutoTokenizer, AutoModelForSeq2SeqLM

model_name = "Helsinki-NLP/opus-mt-en-fr"

tokenizer = AutoTokenizer.from_pretrained(model_name)
model = AutoModelForSeq2SeqLM.from_pretrained(model_name)
```

Sample Input:

```text
Artificial Intelligence is changing the world.
```

Sample Output:

```text
L'intelligence artificielle change le monde.
```

---

## Results and Observations

| Task | Input | Output | Observation |
|--------|--------|---------|------------|
| Summarization | Long AI Paragraph | Short Summary | Main idea preserved |
| Translation | English Sentence | French Sentence | Accurate translation |

### Strengths

- Easy implementation using AutoClasses
- High-quality pretrained models
- Strong performance on NLP tasks
- Minimal training required

### Limitations

- May hallucinate information
- Performance depends on training data
- Domain-specific limitations
- Computationally intensive for large models

---

## References

1. Vaswani et al. (2017) – *Attention Is All You Need*
2. Hugging Face Transformers Documentation
3. Hugging Face Model Card – facebook/bart-large-cnn
4. Hugging Face Model Card – Helsinki-NLP/opus-mt-en-fr
5. LangChain Documentation
6. CNN/DailyMail Dataset Documentation

---

## Author

**Vamsi Krishna**

---

## Acknowledgement

This assignment was completed as part of the curriculum tasks assigned by **Innomatics Research Labs**.

The objective of this assignment was to gain a deeper understanding of Transformer architecture and practical implementation using the Hugging Face ecosystem.
