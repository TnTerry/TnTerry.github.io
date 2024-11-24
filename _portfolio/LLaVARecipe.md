---
title: "LLaVA-Recipe: Visual Instruction Tuning Enhanced Food Recipe VQA"
# excerpt: "Exploring Self-Learning and Teacer-Guided paradigms with Phi-2<br/><img src='images/SelfReward.png'>"
excerpt: |
  Augment the capability of LLaVA for generating detailed cooking recipes from visual input
  <br/>
  <img src='/images/LLaVARecipeStructure' alt="Evaluation Approach">
collection: portfolio
---

# Core Contribution

In this study, we present an approach to augmenting the capabilities of Large Language and Vision Assistant (LLaVA) for generating detailed cooking recipes from visual inputs. Leveraging the extensive Recipe1M+ dataset, our methodology involves a two-stage fine-tuning process that integrates visual and textual data, enhancing LLaVA’s ability to produce coherent and applicable cooking instructions from image-text pairs. With multiturn dialogue generation and Ingredients and Instruction Mentioned(IIM), our experiments find that visual instruction tuning on Recipe1M+ enhanced LLaVA’s performance in recipe generation. We also explore the effect of IIM and number of training epochs on LLaVA through experiments and draw the conclusion that IIM boosts performance and increased training epochs benefit IIM models.

More details can be found in the [paper](/files/LLaVARecipe.pdf).