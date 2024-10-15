---
title: "Self-Learning and Teacher-Guided Paradigms in Language Model Alignment"
excerpt: "Exploring Self-Learning and Teacer-Guided paradigms with Phi-2<br/><img src='images/SelfReward.png'>"
collection: portfolio
---

# Core Contribution

We explores the nature of the self-reward RLHF and introduces a novel framework based on online supervision from large language models, which significantly improves the alignment training for smaller models. Our work aims to address the the issue of manual data annotation dependency  inherent in RLHF, thereby enhancing the generalization capabilities of small models. Additionally, it provides support for future offline RLHF work, primarily driven by Direct Preference Optimization (DPO).

And our contribution includes:
- Implemented a self-reward RLHF platform with strong expandability
- Systematically evaluated the fine tuned models for both Instruction Following Ability and Reward Modeling Ability
- Introduced Gemini-based LLM-as-a-Judge and LLM-as-a-Teacher paradigms

# Framework

![Framework](images/SelfReward.png)

Our Framework consists of three pipeline: Self reward alignment, teacher reward alignment and
teacher demonstration alignment. Each pipeline iteratively trains a series of models $M_1, . . . ,M_T$
where each successive model t uses augmented training data created by the $t − 1^{th}$ model (or teacher
demonstrations). We thus define the models and the corresponding training data as follows:

- $M_0$ : Base pretrained LLM with no fine-tuning
- $M_1$ : Initialized with $M_0$, then fine-tuned on the IFT+EFT seed data using SFT
- M2 : Initialized with M1, then trained with self reward (M1) data using DPO
- M2 (Teacher reward): Initialized with M1, then trained with teacher reward data using DPO
- M2 (Teacher demonstration): Initialized with M1, then trained with teacher demonstration data using DPO

# Experiment

