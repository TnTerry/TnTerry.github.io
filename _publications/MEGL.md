---
title: "MEGL: Multimodal Explanation-Guided Learning"
collection: publications
category: preprint
permalink: /publication/MEGL
excerpt: 'Yifei Zhang*, Tianxu Jiang* (Equal Contribution), Bo Pan, Jingyu Wang, Guangji Bai, Liang Zhao'
date: 2024-11-15
paperurl: 'https://arxiv.org/abs/2411.13053'
# venue: 'Journal 1'
# slidesurl: 'http://academicpages.github.io/files/slides2.pdf'
# citation: 'Your Name, You. (2010). &quot;Paper Title Number 2.&quot; <i>Journal 1</i>. 1(2).'
---

Explaining the decision-making processes of Artificial Intelligence (AI) models is crucial for addressing their "black box" nature, particularly in tasks like image classification. Traditional eXplainable AI (XAI) methods typically rely on unimodal explanations, either visual or textual, each with inherent limitations. Visual explanations highlight key regions but often lack rationale, while textual explanations provide context without spatial grounding. Further, both explanation types can be inconsistent or incomplete, limiting their reliability. To address these challenges, we propose a novel Multimodal Explanation-Guided Learning (MEGL) framework that leverages both visual and textual explanations to enhance model interpretability and improve classification performance. Our Saliency-Driven Textual Grounding (SDTG) approach integrates spatial information from visual explanations into textual rationales, providing spatially grounded and contextually rich explanations. Additionally, we introduce Textual Supervision on Visual Explanations to align visual explanations with textual rationales, even in cases where ground truth visual annotations are missing. A Visual Explanation Distribution Consistency loss further reinforces visual coherence by aligning the generated visual explanations with dataset-level patterns, enabling the model to effectively learn from incomplete multimodal supervision. We validate MEGL on two new datasets, Object-ME and Action-ME, for image classification with multimodal explanations. Experimental results demonstrate that MEGL outperforms previous approaches in prediction accuracy and explanation quality across both visual and textual domains.

The paper has been submitted to CVPR 2025 and is available [here](https://arxiv.org/abs/2411.13053). The code and data will be released upon acceptance.