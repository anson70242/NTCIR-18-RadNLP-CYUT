# NTCIR-18 RadNLP - Team CYUT

This repository contains the codebase for the NTCIR-18 RadNLP Main Task, developed by Team CYUT. The code is designed to automate lung cancer staging from radiology reports using Large Language Models (LLMs) and ensemble learning techniques.

## Overview

This work investigates LLMs for automated TNM staging of lung cancer based on radiology reports. We address the challenge of inconsistent model predictions by employing an ensemble fusion framework, which aggregates outputs from multiple reasoning models, including OpenAI’s O-series and DeepSeek-R1, enhanced with Chain-of-Thought (CoT) reasoning.

Our method integrates:

- **Systematic prompt engineering** to optimize LLM performance
- **Ensemble methods**, including weighted majority voting and XGBoost, to reduce prediction inconsistencies
- **Evaluation of multiple LLM architectures**, such as GPT-4o, DeepSeek-R1, and Llama 3, for robust performance

Our approach secured **Rank 2** in the NTCIR-18 RadNLP Main Task (English), demonstrating the effectiveness of ensemble learning for medical NLP applications.



## Features

- **Multi-LLM Fusion:** Uses multiple LLMs to improve reliability in medical text classification.
- **Reasoning Model:** Leverage advanced reasoning models, including OpenAI’s O-series and DeepSeek-R1, enhanced with Chain-of-Thought (CoT) reasoning for superior inference capabilities.
- **Advanced Ensemble Learning:** Applies Weighted Majority Voting and XGBoost to refine classification accuracy.
- **Custom Prompt Engineering:** Ensures stable and structured TNM classification predictions.
- **Comparative Model Evaluation:** Benchmarks proprietary and open-source LLMs for lung cancer staging.



## Dataset

We utilize the **NTCIR-18 RadNLP dataset**, which includes radiology reports with TNM staging labels. The dataset consists of:

- **108 training samples**
- **54 validation samples**
- **Class distributions for T, N, and M categories**, addressing imbalances with ensemble techniques.



## Model Implementation

Our model pipeline consists of:

1. **Preprocessing:** Standardizing radiology reports for consistent input.
2. **Prompt Engineering:** Optimized prompts with explicit formatting and guidelines.
3. **LLM Inference:** Predictions from DeepSeek-R1, OpenAI-o1-mini, and other reasoning models.
4. **Ensemble Fusion:** Combining outputs with Weighted Majority Voting and XGBoost.
5. **Post-processing & Evaluation:** Analyzing model errors and refining classification strategies.



## Results

Our experiments show that ensemble learning significantly improves accuracy over individual models. Key findings include:

- **Joint (fine) Accuracy:** Improved from 0.81 (DeepSeek-R1) to 0.83 (ensemble model)
- **Error Analysis:** Identified common misclassification patterns, particularly in **T category staging**
- **Test Set Performance:** Achieved **0.60 Joint (fine) Accuracy**, indicating areas for further optimization



## Future Work

- **Integration of Multimodal Learning:** Combining text and imaging data for improved staging accuracy.
- **Fine-tuning LLMs:** Using domain-specific datasets to enhance performance.
- **Advanced RAG (Retrieval-Augmented Generation):** Improving few-shot learning for structured medical classifications.



## Citation

If you use this code or our approach in your research, please cite our paper:

```
@article{cyut_ntcir18,
  author    = {Tsz-Yeung Lau and Shih-Hung Wu},
  title     = {From Divergent LLM Predictions to Reliable Lung Cancer Staging with Ensemble Fusion: CYUT at the NTCIR-18 RadNLP Main Task},
  journal   = {NTCIR-18 RadNLP Proceedings},
  year      = {2025},
}
```

## Contact

For any questions or collaboration inquiries, please contact:

- **Tsz-Yeung Lau** - s11327605@gm.cyut.edu.tw
- **Shih-Hung Wu (Corresponding Author)** - shwu@cyut.edu.tw
