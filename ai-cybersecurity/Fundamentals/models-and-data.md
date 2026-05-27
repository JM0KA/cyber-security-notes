# AI Models and Data

## Key Concepts

- Training Dat
- Building the Model
- The Inheritence Problem
- The Black Box Problem

## Important Terms

- **Validation Set** : A portion of the training data that is held back and never used for training

- **Pruning** : Removes parameters that contribute little to predictions, shrinking model size

- **Quantisation** : Reduces numerical precision of weights (e.g., 32-bit to 8-bit floats) to cut memory and compute requirements

- **Federated Learning** : Trains the model across many decentralized devices or organizations, with each participant training locally on their own data and only sending weight updates back to a central server for aggregation

- **Pre-Trained Model** : is one that has alreadt been trained on a large, general-purpose dataset

- **Fine Tuning** : is the process of continuing to train one of these pre-trained models on a smaller, task-specific dataset

> Fine tuning changes the model's task specific behaviour, tone, and domain knowledge
> Fine tuning DOES NOT change the base model weights

## How it Works

- LLM's are first trained in a "pre-training" phase, where they process vast amounts of text
  - LLM's use billions of parameters that function like puzzle pieces, enabling them to understand and generate human-like planguage when assessed together

- Training a large language model requires a staggering amount of text; The typical pipeline draws from four buckets
  - Web Scraping
  - Licensed Datasets
  - Synthetic Data
  - Internal Corpora

 > *The most common used training dataset is **Common Crawl***

- By using *validation sets* at regular intervals, a model is able to be tested on unseen data to check whether its performance is actually generalizing or just improving on the triain examples it's seen before

> *If training accuracy keeps climbing but validation accuracy plateaus or drops, that's overfitting in real time*

- Once a model is trained, it often goes through compression steps before deployment; particularly if it needs to run efficiently on limited hardware
  - The two most common are:
    - Pruning
    - Quantisation

> *Research has shown that quantisation can silently degrade the safety mechanisms built into a model*

- When you fine-tune a pre-trianed model, you inherit everything that model already contains. This includes things you cannot see and did not choose:
  - Biases baked in during pre-trianing persist
  - Unexpected behaviours introduced by the base model's training data carry through
  - Any safety alignment built into the base models is not durable as it might appear
  
> This shows up in 3 concrete ways:
>
> - Safety Alignment Erodes
> - Specialization increases attack surface
> - Version matters, and its rarely tracked
