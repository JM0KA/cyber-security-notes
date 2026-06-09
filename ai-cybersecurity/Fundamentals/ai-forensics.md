# AI Forensics

## Key Concepts

- The AI Forensics Landscape
- AI & DFIR
- AI Legal & Ethical Implications

## Important Terms

- **Accuracy** : Refers to the overal rate of correct predictions

- **Precision** : Measyres how often a model's positive predictions are correct

- **Recall** : Measures how successful the model was in identifying all positices in the provided dataset

- **Convolutional Neural Network (CNN)** : A type of neural newtork that automatically learns patterns in data using small filters commonly used for images

- **Error Level Analysis (ELA)** : A technique used in image forensics to detect areas of an image that may have been digitally altered

- **Generative Adversarial Networks (GAN)** : A setup where two neural networks compete: one generates fake media, and the other tries to detect it

- **Daubert Test** : A U.S. legal rile that determines the admissibility of expert testimony, particularly scientific testimony, in federal court

- **Chain of Custody** : Process of docuemnting the complete journey of evidence during a legal case lifetime, from the collection to final presentation in court

## How It Works

- Anomaly Detection / UEBA
  - Flags unusual user/system behaviour compared to learned 'normal'
    - AI uses unsupervised learning techniques to learn baseline behaviours for users and systems. Deviations from this baseline are flagged as potential threats.

- Phishing & Communication
  - Detects phishing emails and flags risky language in chat/email logs
    - Transformer-based language models clssify messages as phishing or benign based on tine, structure, and known attack patterns

- Malware/File Classification
  - Classifies files as malicious or benign based on extracted static/dynamic features
    - AI systems analyse file metadata code signatures, and sandbox behaviour to detect threats

- Alert Triage & Prioritisation
  - Automatically scores, ranks and filters alerts to reduce analyst workload
    - AI analyses past alert data, analyst feedback, and incident outcomes to rank alerts by severity and relevance.
  
- Timeline & Event Correlation
  - Reconstructs attack timelines by clustering and linkning logs across sources
    - AI clusters similar log events, identifies casual relationships, and aligns activity across systems

- AI systems and modern machine learning models are generally probabilistic
  - Instead of following a fixed ruleset that provides a fixed outcome, they use statistical models to learn from data and make predictions with certain possibilities.

- AI's non-deterministic nature allows itself to handle uncertainty and adapt to new patterns

> Extensive prompt engineering is required when using Ai in evaluative contexts due to the non-deterministic nature

- Important metrics to consider when evaluating AI performance are:
  - **Accuracy**
    - It is important when assessing an AI's performance to not only consider accuracy, as in isolation, it can be very misleading
  - **Precision**
    - Higher Precision = Fewer False Positives
    - This metric also suffers in isolation as the mdoel can choose to be very selective, only flagging the very obvious maliciious files
  - **Recall**
    - In Isolation, this metric would be ineffective as a model could simply cast a wide net, flagging every file as malicious

- The GIGO (Garbage In, Garbage Out) principle is just as trus for Ai systems than it is for any system

The non-determinism, evaluation challenges, and performance trade-offs of AI means it should never replace human expertise

> It can enhance our work but human oversight, judgementm and validation will always remain essential

- Communications analysis involves the processing and analysis of large volumes of text; Large Language Models use deep learning to process vast amounts of data, so we can leverage this technology to help in forensics

- Reconstructing incident timelines is a common and critical part of an investigation; it is also labour intensiv and time-consuming. ML is now being harnessed to help with Automated Reconstruction and Anomaly Detection
  - AI systems are particularly adept at correlating *time-sequenced data* from multiple sources and putting together what happened before, during, and after an incident

  - AI is incredibly good at identifying patterns. This ability can give you an eagle eye, flagging things like impossiible logins, where a user was logged in at two places simultaneously, or behaviour unusual for this specific event

- Breakthroughs in being able to represent malware files in ways processible by deep neural networks have made it possible to classify a file as malicious or benign

- ML is also being considered for use in dynamic analysis, observing how a program behaves to identify whether it is malicious or not

- Mant AI mdoels are 'black boxes', meaning they don't readily explain how they came to a conclusion

> Without explainability and expert validation, AI-generated insights may not survive a courtroom challenge

- ML models are trained on historical data; if that data contains skewed representations or prejudices, the model's output will reflect them

> Legally, if a defence can show an AI technique is biased, judges may exclude its results
>
> Ethically, forensics experts have a duty to validate and correct biases present in AI tools. Doing this ensures equitable treatment and upholds the integrity of the investigation

- In terms of trust and accountability, courts require the digital evidennce be handled in a traceable and preservable manner and that integrity is preserved at each step
  - This is achieved by maintining the chain of custofy and an audit trail

> AI processes must be carfully documented and secured, and using on-premise or controlled systems can help achieve this and satisfy legal scrutiny


## Examples

- CNN-Based Forgery Detection
  - Researchers have started combining traditional forensics methods such as ELA (Error Level Analysis) with CNN models to identify image tampering

- Deepfake Detection
  - CNN models have recently been used in conjunction with some other AI tehnologies to develop specialised detectors; These detectors are used to analyze subtle inconsistencies in facial videos

- GANs
  - Forensics tools are now using GANs to train detectors on AI-generated fakes, making htem better at apotting subtle manipulations that even humans miss

- Using transformer-based models that are trained for NLP excel at identifying phishing emails
  - This technology allows us to move away from a rule-based approach for detecting incoming phishing emails and adopt deep learning, context aware models

  - This same technology can is harnessed by some forensics platforms, allowing forensic investigators to automatically scan chats for keywords or patterns related to threats and perform sentiment analysis to guage emotional tone
