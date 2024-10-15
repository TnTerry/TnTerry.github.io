---
title: "Self-Learning and Teacher-Guided Paradigms in Language Model Alignment"
# excerpt: "Exploring Self-Learning and Teacer-Guided paradigms with Phi-2<br/><img src='images/SelfReward.png'>"
excerpt: |
  Exploring Self-Learning and Teacher-Guided paradigms with Phi-2
  <br/>
  <img src='/images/SelfReward.png' alt="Self-Learning Paradigm Illustration">
collection: portfolio
date: 2024-5-1
---

# Core Contribution

We explores the nature of the self-reward RLHF and introduces a novel framework based on online supervision from large language models, which significantly improves the alignment training for smaller models. Our work aims to address the the issue of manual data annotation dependency  inherent in RLHF, thereby enhancing the generalization capabilities of small models. Additionally, it provides support for future offline RLHF work, primarily driven by Direct Preference Optimization (DPO).

And our contribution includes:
- Implemented a self-reward RLHF platform with strong expandability
- Systematically evaluated the fine tuned models for both Instruction Following Ability and Reward Modeling Ability
- Introduced Gemini-based LLM-as-a-Judge and LLM-as-a-Teacher paradigms

# Framework

![Framework](/images/SelfReward.png)

Our Framework consists of three pipeline: Self reward alignment, teacher reward alignment and
teacher demonstration alignment. Each pipeline iteratively trains a series of models M1, . . . ,MT
where each successive model t uses augmented training data created by the t − 1th model (or teacher
demonstrations). We thus define the models and the corresponding training data as follows:

- M0 : Base pretrained LLM with no fine-tuning
- M1 : Initialized with M0, then fine-tuned on the IFT+EFT seed data using SFT
- M2 : Initialized with M1, then trained with self reward (M1) data using DPO
- M2 (Teacher reward): Initialized with M1, then trained with teacher reward data using DPO
- M2 (Teacher demonstration): Initialized with M1, then trained with teacher demonstration data using DPO

# Experiment

We use Phi-2 as our base model, Gemini Pro 1.0 as our teacher model, and GPT-4 turbo as our AI preference model. We evaluate the performance of our models on AlpacaEval 2.0 benchmark and head-to-head comparisons for instruction following ability. For reward modeling, we evaluate the correlation with GPT-4 rankings. 

![AlpacaEval](/images/SelfReward-AlpacaEval.png)

![Head-to-Head1](/images/SelfReward-head2head1.png)

![reward](/images/SelfReward-corr.png)

More details can be found in the [paper](/files/Exploring_Self-Learning_and_Teacher-Guided_Paradigms_in_Language_Model_Alignment.pdf).