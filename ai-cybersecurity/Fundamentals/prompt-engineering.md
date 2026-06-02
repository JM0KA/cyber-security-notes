# Prompt Engineering

## Key Concepts

- LLM Fundamentals
- The Anatomy of a Prompt
- System vs User Prompts
- Advanced Prompting Techniques

## Important Terms

- **Tokens** : are the smallest units an LLM can understand. A token is roughly equivalent to 3-4 characters, meaning most english words are 1-2 tokens

- **Nondeterminism** : Outputs vary even with identical inputs

- **Temperature** : This si a numerical value, commonly ranging from 0.0 - 2.0 that controls how "adventurours" the model is when picking its next word

- **Max Tokens** : Caps how long the response can be; too low and the models cuts off mid-sentence, too high and you pay for unneeded rambling.

> Controlling length is a cost-control measure

- **Top-p** : (nucleus sampling) is temperature's cousin. Instead of turning up o rdown the randomness across all possible words, top-p sets a shortlist

> Typically it is advised to adjust Temperature OR Top-p, but not both

- **Context Window** : A models maximum "working Memory" mesured in tokens

- **Instruction (Task)** : This is the core command or action you want from the AI, expressed witha  clear verb

- **Context (Background)** Context provides the Ai with relevant information or a scenario so it understands the situation and perspective

- **Output Format (Structure)** : Specify how you wnat the answer to look

- **Constraints (Boundaries)** : These are any rules or limits you impose on the repsonse. Constraints guide the model yo follow specific boundaries

- **System Prompts** are developer-defined, persistent instructions that set the assistant's role, tine and hard rules. They define the model's behaviour, role and constraints at the application level and remain constatnt across sessions

## How it Works

- The LLM converts each token into a unique number (an ID). The model only works with these numbers, using them to predict what number (token) should come next

- When prompting an LLM, your essentially triggering a probability machine that weighs hundres of thousands of potential next words. It calculates which tokens are statistacally likely based on patterns from training

> You can control how that probability plays out using parameters like:
>
> - Temperature
> - Max Tokens
> - Top-p

- A good prompt explicityly spells out what you want, how you want it, and any constraints to follow

>Experts often break prompts into clear components:
>
> - Instruction
> - Context
> - Output format
> - Constraints

f
