# 🧠 CSET419 – Introduction to Generative AI

## 📘 Lab 9: Sequence Generation using LSTM and Transformer

---

## 🎯 Objective

The objective of this lab is to understand how generative models can be applied to sequential data such as text, time-series, or language sequences.
We design and implement models capable of learning patterns from sequences and generating new sequences.

---

## 📚 Learning Outcomes

After completing this lab, we are able to:

* Understand sequential data and its characteristics
* Learn how generative models perform sequence prediction
* Implement sequence-based models using LSTM and Transformer
* Train models to generate new sequences
* Evaluate the quality of generated outputs

---

## 🧠 Introduction

Sequential data refers to data where the **order of elements matters**. Examples include text, speech, and time-series data.

Generative models for sequences learn patterns in such data and generate new sequences by predicting the next element based on previous inputs.

Mathematically, this is modeled as:

P(wₜ | w₁, w₂, ..., wₜ₋₁)

---

## ⚙️ Methodology

---

### 🔹 Component–I: LSTM Based Sequence Generation

#### 📌 Steps Performed

1. **Data Preprocessing**

   * Loaded text dataset
   * Cleaned and split into sentences

2. **Tokenization**

   * Converted words into numerical indices using Keras Tokenizer

3. **Sequence Creation**

   * Generated input-output pairs for next-word prediction

4. **Padding**

   * Ensured uniform sequence length using pre-padding

5. **Model Architecture**

   * Embedding Layer
   * LSTM Layer
   * Dense Output Layer with Softmax

6. **Training**

   * Loss: Sparse Categorical Crossentropy
   * Optimizer: Adam

7. **Text Generation**

   * Generated sequences using seed input and iterative prediction

---

#### 🧠 Key Concept

LSTM improves over RNN by using gates to handle long-term dependencies and avoid vanishing gradient problems.

---

### 🔹 Component–II: Transformer Based Sequence Generation

#### 📌 Steps Performed

1. **Tokenization**

   * Same dataset and tokenizer used

2. **Positional Encoding**

   * Added positional information to embeddings

3. **Transformer Architecture**

   * Multi-Head Self Attention
   * Feed Forward Network
   * Layer Normalization

4. **Training**

   * Same objective: next word prediction

5. **Sequence Generation**

   * Generated text using trained Transformer model

---

#### 🧠 Key Concept

Transformers use **self-attention mechanisms** to capture relationships between all words in a sequence simultaneously, enabling better context understanding.

---

## 🔍 Results

### ✅ LSTM Generated Output

Example:
machine learning models learn patterns from data

### ✅ Transformer Generated Output

Example:
deep learning improves sequence modeling performance

---

## 📊 Comparison

| Feature               | LSTM       | Transformer |
| --------------------- | ---------- | ----------- |
| Memory Handling       | Sequential | Parallel    |
| Long Dependencies     | Good       | Excellent   |
| Speed                 | Slower     | Faster      |
| Context Understanding | Limited    | Global      |

---

## 🧠 Key Insights

* Sequential data requires models that can capture context and order
* LSTM handles long-term dependencies better than RNN
* Transformers outperform LSTM using attention mechanisms
* Embeddings convert words into meaningful vector representations

---

## ⚠️ Challenges

* Limited dataset leads to less diverse text generation
* Training time for neural models
* Overfitting on small datasets

---

## 🚀 Applications

* Language Modeling
* Chatbots and Virtual Assistants
* Speech Recognition
* Time-Series Forecasting
* Music Generation

---

## 📌 Conclusion

In this lab, we implemented sequence generation using both LSTM and Transformer architectures.
We observed that while LSTM captures sequential dependencies effectively, Transformers provide superior performance due to attention mechanisms and parallel processing.

---

## 🛠️ Technologies Used

* Python
* TensorFlow / Keras
* NumPy

---

## 🎤 Viva Summary

* Sequential data depends on order and context
* Generative models predict the next token
* LSTM uses gates to retain memory
* Transformer uses attention for global context

---

## ⭐ Author

Govind
B.Tech CSE – Bennett University
