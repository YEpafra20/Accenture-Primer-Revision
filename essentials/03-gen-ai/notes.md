# Gen AI — Revision Notes

**Category:** Essentials · **Focus Area:** Generative Adversarial Network · **Level:** Beginner

---

## Table of Contents

1. [Introduction to Generative AI](#1-introduction-to-generative-ai)
2. [Brief History of Generative AI](#2-brief-history-of-generative-ai)
3. [Fundamentals of Machine Learning and Neural Networks](#3-fundamentals-of-machine-learning-and-neural-networks)
4. [Introduction to Generative Models](#4-introduction-to-generative-models)
5. [Variational Autoencoders (VAEs)](#5-variational-autoencoders-vaes)
6. [Generative Adversarial Networks (GANs)](#6-generative-adversarial-networks-gans)
7. [Sequence Generation with RNNs](#7-sequence-generation-with-rnns)
8. [Transformers and Attention Mechanisms](#8-transformers-and-attention-mechanisms)
9. [Generative AI in Industry and Real-World Applications](#9-generative-ai-in-industry-and-real-world-applications)

---

## 1. Introduction to Generative AI

### 1.1 Important Terms

| Term | Definition |
|---|---|
| **Artificial Intelligence (AI)** | The ability to think, learn, and be creative |
| **Machine Learning (ML)** | Allows machines to learn from data rather than explicit programming. ML algorithms detect patterns in data to make predictions or decisions |
| **Deep Learning** | Powers image recognition, language translation, and voice synthesis — technologies like self-driving cars and precise medical diagnoses |
| **Generative AI** | Creates content such as images, music, and text by learning from vast data |

### 1.2 Difference Between Gen AI and Other Types of AI

| Type | Focus |
|---|---|
| **Traditional AI** | Focuses on rule-based systems and predefined patterns |
| **Generative AI** | Creates new content based on patterns learned from data |

### 1.3 Generative AI vs Predictive AI

- **Predictive AI** — forecasts outcomes based on historical data
- **Generative AI** — creates new instances that fit the underlying distribution of the data

---

## 2. Brief History of Generative AI

**1. Generative Adversarial Nets (GAN)**

**Definition:**  
A deep learning framework where two neural networks (Generator and Discriminator) compete to generate realistic data.

### Key Points
- Introduced by **Ian Goodfellow (2014)**.
- **Generator (G):** Creates fake data from random noise.
- **Discriminator (D):** Identifies real vs fake data.
- Trained using a **Minimax (Adversarial) Game**.
- Produces highly realistic images, text, and audio.

**Flow:**
Noise → Generator → Fake Data → Discriminator → Real/Fake

---

**2. Auto-Encoding Variational Bayes (VAE)**

**Definition:**  
A probabilistic generative model that learns compressed latent representations and reconstructs the original data.

#### Key Points
- Introduced by **Diederik P. Kingma & Max Welling (2013)**.
- **Encoder:** Converts input into latent vector (z).
- **Decoder:** Reconstructs data from the latent vector.
- Uses the **Reparameterization Trick** for efficient training.
- Useful for image generation, denoising, and representation learning.

**Flow:**
Input → Encoder → Latent Space (z) → Decoder → Reconstructed Output

**3. Attention Is All You Need (Transformer)**

**Definition:**  
A deep learning architecture that uses **self-attention** instead of RNNs or CNNs to process sequential data efficiently.

### Key Points
- Introduced by **Ashish Vaswani et al. (2017)**.
- Based entirely on the **Transformer** architecture.
- Uses **Self-Attention** to understand relationships between words.
- **Multi-Head Attention** learns different contextual patterns simultaneously.
- Enables **parallel processing**, making training much faster than RNNs.

### Core Components
- **Encoder:** Understands the input sequence.
- **Decoder:** Generates the output sequence.
- **Positional Encoding:** Preserves word order.
- **Feed-Forward Network:** Refines learned representations.

**Flow:**
Input → Positional Encoding → Encoder → Multi-Head Attention → Decoder → Output

# History of Generative AI — Components & Purpose

| **Model** | **Component** | **Purpose** |
|-----------|---------------|-------------|
| **GAN (2014)** | Generator (G) | Generates realistic fake data from random noise |
|  | Discriminator (D) | Identifies whether data is real or fake |
|  | Random Noise (Z) | Starting input for the Generator |
|  | Minimax Game | Trains G and D through competition |
| **VAE (2013)** | Encoder | Converts input into a latent representation |
|  | Latent Space (Z) | Stores compressed features of the data |
|  | Decoder | Reconstructs data from the latent vector |
|  | Reparameterization Trick | Enables efficient gradient-based learning |
| **Transformer (2017)** | Self-Attention | Learns relationships between all tokens |
|  | Multi-Head Attention | Captures multiple contextual patterns simultaneously |
|  | Encoder | Builds contextual understanding of the input |
|  | Decoder | Generates the output sequence |
|  | Positional Encoding | Preserves the order of words/tokens |
|  | Feed-Forward Network | Refines feature representations after attention |

> **Memory Shortcut**
> - **GAN:** Generate → Discriminate
> - **VAE:** Encode → Compress → Decode
> - **Transformer:** Attend → Understand → Generate

## 3. Fundamentals of Machine Learning and Neural Networks

### 3.1 What is Machine Learning?

**Machine Learning** is a subset of AI where computers learn from data without being explicitly programmed.

```
Input → Process → Output (prediction)
```

### 3.2 Types of Machine Learning

| Type | Description |
|---|---|
| **Supervised Learning** | Learns from labeled data |
| **Unsupervised Learning** | Discovers patterns in unlabeled data |
| **Semi-Supervised Learning** | Utilizes both labeled and unlabeled data |
| **Reinforcement Learning** | Learns by interacting with an environment |

### 3.3 How Supervised ML Learning Works

1. Provide the machine learning algorithm categorized/labeled input and output data to learn from
2. Introduce new, unlabeled data to evaluate its classification accuracy. If not accurate, further refine the algorithm

**Types of problems suited:** Classification, Regression

### 3.4 How Unsupervised ML Learning Works

1. Provide the machine learning algorithm uncategorized/unlabeled input to see what pattern it finds
2. Observe and learn from the patterns the machine identifies

**Types of problems suited:** Clustering, Anomaly Detection

### 3.5 How Reinforcement Learning Works

1. Formulate the problem
2. Create the environment
3. Define the reward
4. Create the agent and train the agent
5. Validate the agent
6. Deploy the policy

### 3.6 Common ML Algorithms

- Linear Regression
- Logistic Regression
- Decision Trees
- Random Forest
- Support Vector Machines (SVM)
- Naive Bayes
- K-Nearest Neighbors (KNN)
- Neural Networks
- Principal Component Analysis (PCA)
- K-Means Clustering
- DBSCAN
- Hierarchical Clustering
- Gradient Boosting Machine (GBM)
- AdaBoost
- Hidden Markov Models

### 3.7 ML Model Deployment

| Stage | Description |
|---|---|
| **Data Collection** | Extract data from various sources |
| **Data Storage** | Store data in reliable storage |
| **Data Preparation** | Organize and clean data to make it usable |
| **Data Analysis** | Uncover patterns, identify trends, distributions, and segments |
| **Prototyping & Testing ML** | Interpretable simple models, A/B testing and experiments |
| **ML in Production** | Deploy, monitor, and update models in production |

### 3.8 Deep Learning

**Deep Learning** is a subset of Machine Learning in Artificial Intelligence that has networks capable of learning unsupervised from data that is unstructured or unlabeled.

**Deep learning models can be used for a variety of complex tasks:**

| Model | Use Case |
|---|---|
| Artificial Neural Network | Regression and Classification |
| Convolutional Neural Network (CNN) | Computer Vision |
| Recurrent Neural Network (RNN) | Time Series Analysis |
| Self Organizing Maps | Feature Extraction |
| Deep Boltzmann Machines | Recommendation Systems |
| Auto Encoders | Recommendation Systems |

### 3.9 Neural Network

A **neural network** is a series of algorithms that attempts to recognize underlying relationships in a set of data through a process that mimics the human brain.

---

## 4. Introduction to Generative Models

### 4.1 What are Generative Models?

**Generative Models** — algorithms that can generate new data samples from the same distribution as the training data. (**Generative Adversarial Networks (GANs)** are a popular choice.)

### 4.2 Generative vs Discriminative Models

| Model Type | Models |
|---|---|
| **Generative** | The joint probability `p(X, Y)` |
| **Discriminative** | The conditional probability `P(Y | X)` |

### 4.3 Example — Facial Recognition

- **Generative** — GANs in action, generating faces from scratch
- **Discriminative** — with CNNs, comparing your face to the stored one for an exact match

### 4.4 Probability Distributions

Act as a mathematical lens, guiding the creation of new, realistic data points in generative models.

### 4.5 What a Generative Model IS and IS NOT

Model: `Y = f(X)`

---

## 5. Variational Autoencoders (VAEs)

> Placeholder — the source notepad listed this as a section header without further detail. Add VAE architecture (encoder, latent space, decoder), the reparameterization trick, and typical use cases here once available.

---

## 6. Generative Adversarial Networks (GANs)

> Placeholder — the source notepad listed this as a section header without further detail beyond earlier mentions (GANs generating faces from scratch in the Facial Recognition example, and GANs used across Healthcare, Fashion & Design, and Finance applications in Section 9). Add the Generator vs Discriminator architecture, the adversarial training loop, and GAN variants here once available.

---

## 7. Sequence Generation with RNNs

### 7.1 RNN Fundamentals

**RNNs (Recurrent Neural Networks)** — neural networks designed for sequences. Can remember past information. Used in time series, speech, and text.

- RNNs retain information from previous inputs, making them adept at understanding sequences
- **The power of sequences:** sequences and their patterns are omnipresent in our lives — e.g., DNA, Language, Music

### 7.2 LSTM (Long Short-Term Memory)

A type of RNN architecture designed to remember long-term dependencies and combat the **vanishing gradient problem**.

### 7.3 GRU (Gated Recurrent Unit)

A simplified RNN architecture, similar to LSTM, that efficiently captures long-term dependencies with fewer parameters.

---

## 8. Transformers and Attention Mechanisms

### 8.1 Transformer Architecture

A model architecture designed for handling sequential data, consisting of an **Encoder** and a **Decoder**.

### 8.2 Attention Mechanism

A mechanism that allows the model to focus on different parts of the input data.

### 8.3 Transformers in Action

| Model | Description |
|---|---|
| **BERT** | Pre-trains on vast text. Understands context bidirectionally |
| **GPT** | Generates coherent text. Predicts subsequent words |
| **T5** | Addresses all NLP as text-to-text. Handles translation to summarization |
| **Transformer-XL** | Captures long-term dependencies. Attends to extended sequences |
| **RoBERTa** | Enhanced BERT training. Removes next-sentence prediction |
| **DistilBERT** | Lighter BERT version. Faster, yet retains accuracy |
| **CLNet** | Merges GPT and BERT strengths. Dynamic word prediction |
| **ALBERT** | Streamlined BERT. Uses parameter-sharing and factorized embedding |

---

## 9. Generative AI in Industry and Real-World Applications

### 9.1 Publishing & Media

**Tools used:** OpenAI's GPT variants for text generation

### 9.2 Healthcare

**Tools and Models:** DeepChem for molecular analysis, Generative Adversarial Networks (GANs) for generating potential drug compounds

### 9.3 Fashion & Design

**Tools:** DALL-E for image generation from textual descriptions, StyleGANs, GANs trained on fashion datasets for generating clothing designs

### 9.4 Real Estate

**Tools and Models:** NVIDIA's StyleGAN for high-quality image generation, custom models trained on interior design datasets

### 9.5 Finance & Banking

**Tools and Models:** GANs for simulating transaction data with anomalies, anomaly detection models trained on generated data to recognize patterns of fraud

### 9.6 Dynamic Game Development

**Features:**

| Feature | Description |
|---|---|
| Worlds | Diverse AI-generated landscapes |
| Characters | Designed from player inputs |
| Sound | Adapts to in-game actions |
| Difficulty | Adjusts to player skill |

**Tools:**

| Area | Tool |
|---|---|
| World | No Man's Sky engine |
| Design | NVIDIA's StyleGAN |
| Sound | OpenAI's MuseNet |
| Gameplay | Reinforcement Learning |

---

## Quick Revision Checklist

- [ ] Can define AI, ML, Deep Learning, and Generative AI in one line each
- [ ] Can differentiate Traditional AI vs Generative AI vs Predictive AI
- [ ] Can list all 4 types of Machine Learning
- [ ] Can explain the workflow for Supervised, Unsupervised, and Reinforcement Learning
- [ ] Can name at least 8 common ML algorithms
- [ ] Can list the 6 stages of ML model deployment
- [ ] Can list deep learning model types and their use cases (CNN, RNN, etc.)
- [ ] Can differentiate Generative vs Discriminative models with the facial recognition example
- [ ] Can explain what RNNs, LSTM, and GRU are used for and how they differ
- [ ] Can explain the Transformer architecture (Encoder/Decoder) and Attention Mechanism
- [ ] Can name at least 5 transformer-based models and what makes each unique
- [ ] Can name at least 4 industries using Generative AI and their associated tools
