# AI/ML Security Threats

## Key Concepts

- Building Blocks of AI
- LLMs
- AI Security Threats
- Defensive AI

### Important Terms

- **Artificial Intelligence** : A machine or somputer system that is able to carry out tasks that would otherwise require human reasoning, comprehension, problem-solving, or creativity
  
- **Machine Learning** : A subfield of AI that refers to a computer's ability to learn from data without being given instructions and is comparable to how the human brain learns

- **Supervised Learning** : Relies on labeled data to train models for classification or regression tasks

- **Unsupevised Learning** : Works with unlabeled data to discover hidden patterns, often using clustering, association, or dimensionality reduction techniques

- **Semi-Supervised Learning** : combines elements of both, using a small portion of labeled data to guide the learning process

- **Reinforced Learning** : Mimics human learning by reqarding correct decisions and penalizing mistakes, allowing an agent o refine its actions over time to achieve the best outcome

- **Large Language Models (LLM)** : are advanced DL models built on neural networks, specifically transformers, designed to understand and generate human-like text
  
### How It Works

- ML follows a structured lifecycle to ensure the reliable development and deployment of models
  - Defining the problem
  - Collect, Clean, Prepare Data
  - Train model(s) using selected algorithms
  - Evaluate and Tune for optimization

- ML Algorithms consists of 3 key concepts:
  - A Decision Process
  - An Error Function
  - Model Optimization Process

- Deep Learning (DL) is concerned with receiving data as input and producing some kind of prediction or classification as output
  - The important advantage over ML is that DL does not need data to be labelled and as such doesn't require human interaction; in that way it is self-learning

- LLM's are first trained in a "pre-training" phase, where they process vast amounts of text
  - LLM's use billions of parameters that function like puzzle pieces, enabling them to understand and generate human-like planguage when assessed together

### Examples

A few examples of things that can be done to secure AI include:

- **Secure AI Models**
  - One method of preventing unauthorized access to AI models is by enforcing strict controls over who can interact with them
    - The use of RBAC and MFA can help restrict access and add an extra layer of security to AI systems

- **Privacy Protection**
  - Training data should be trates as any other sensitive data and encrypted

- **Implementation of AI Security Standards**
  - Incorporating recognized security standards throughout the development, deployment, and maintenance stages means organizations can proactively address potential risks
    - Following the best practices ensures you are adopoting AI in a secure way, minimizing exposure to cyber threats

- **Model Monitoring**
  - Monitoring should also detect unexpected behaviour, biases, or anomalies that may indicate a security attack

#### Vulnerabilities in AI Models

- **Prompt Injection**
  - Prompt Injection occurs when the original instructions provided to the model are overridden, often for malicious purposes such as disclosing more information than it should, or generating harmful content

- **Data Poisoning**
  - This is when an attacker manipulates the training data/corpus used to train an AI model so its generated output is incorrect or biased

- **Model Theft**
  - Model Theft occurs when an attacker gains unauthorized access to an AI model. From there the attacker could potentially steak the intellectual property that lies within and even use it for malicious purposes

- **Privacy Leakage**
  - This refers to the possibility of an AI model inadvertently revealing sensitive information about the data it was training on, even if the data was supposed to be kept confidential

- **Model Drift**
  - Model Drift refers to the potential for a Model's performance to dirft over time due to changes in the data or the environment surrounding it

### Tools / Commands
  
- **Transformer Neural Networks** (introduced by Google in 2017) revolutionized LLMs by enabling parallel text processing instead of sequential word-by-word analysis
  - This allowed models to assign 'attention' to keywords which improved contextual understanding

- **MITRE ATLAS (Adversarial Threat Landscape for Artificial-Intelligence Systems)** is a knowledge base of adversarial tactics and techniques targeting machine learning systems
  - Modelled on the ATT&CK framework, it documents real-world and research-backed attacks across the AI attack lifecycle
  