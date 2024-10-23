# AdvTG: An Adversarial Traffic Generation Framework to Deceive DL-Based Malicious Traffic Detection Models
AdvTG is an adversarial traffic generation framework designed to deceive deep learning-based malicious traffic detection models.  
It leverages large language models (LLMs) and reinforcement learning (RL) to generate adversarial traffic while ensuring semantic coherence and protocol compliance.  
This repository provides the code for the AdvTG framework.

The AdvTG framework consists of three main stages:

## Detection Model Training
Multiple deep learning-based detection models are trained using different traffic features and architectures to serve as adversarial attack targets and reward evaluators.
```bash
python train_detection_models.py
```

## Domain-Specific LLMs Fine-tuning
The general-purpose LLM is fine-tuned with a large set of domain-specific HTTP traffic data to better understand and generate compliant and contextually accurate traffic.
```bash
python finetune_llm.py
```

 
## RL-based Adversarial Generation
Reinforcement learning optimizes the fine-tuned LLM’s adversarial attack strategy based on feedback from the detection models, enhancing its ability to generate undetectable traffic.
```bash
python ppo.py
```
