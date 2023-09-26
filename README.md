# Intent Detection and Slot Filling with ATIS and SNIPS Datasets using JointBERT

This repository contains the code and resources for training and evaluating a JointBERT model for intent detection and slot filling tasks using the ATIS (Airline Travel Information System) and SNIPS datasets. Additionally, this project implements a slot refinement mechanism to improve metric performance.

## Introduction

Intent detection and slot filling are essential components of natural language understanding (NLU) systems, which are crucial for building conversational AI applications. The ATIS and SNIPS datasets are commonly used benchmarks for these tasks in the context of natural language understanding.

JointBERT is a neural network architecture that combines intent detection and slot filling into a single model, allowing for more efficient and accurate processing of user utterances. Slot refinement is an additional mechanism that enhances the model's ability to predict slot values accurately.

## Datasets

### ATIS Dataset

The ATIS dataset contains queries related to airline travel, including both intent labels (e.g., flight booking, weather inquiry) and slot values (e.g., departure city, arrival city, flight number).

### SNIPS Dataset

The SNIPS dataset covers various domains, such as weather, music, and restaurants, and includes intent labels and slot values.

You can obtain the datasets from the following sources:
- [ATIS Dataset](https://github.com/yuanxiaosc/BERT-for-Sequence-Labeling-and-Text-Classification/tree/master/data/atis_Intent_Detection_and_Slot_Filling) 
- [SNIPS Dataset](https://github.com/yuanxiaosc/BERT-for-Sequence-Labeling-and-Text-Classification/tree/master/data/snips_Intent_Detection_and_Slot_Filling)
- 
## Model Architecture

Our model is based on JointBERT, which utilizes a pre-trained BERT model for contextualized word embeddings.
Additionally, we incorporate a slot refinement mechanism that leverages the predicted intent to improve slot prediction accuracy.

## Training

To train the JointBERT model with slot refinement, follow these steps:

1. Preprocess the datasets by converting them into suitable formats for training.
2. Fine-tune the pre-trained BERT model on the concatenated dataset of ATIS and SNIPS data.
3. Train the intent detection head with a cross-entropy loss.
4. Train the slot filling head with a CRF-based loss.
5. Implement and fine-tune the slot refinement mechanism.

Detailed instructions and training scripts can be found in the project's documentation.

## Evaluation

We provide evaluation scripts to assess the model's performance on intent detection and slot filling tasks. You can run these scripts on the test datasets to obtain metrics such as accuracy for intent detection and F1-score for slot filling.

## Usage

To use the trained model for intent detection and slot filling, you can utilize the provided inference scripts. Simply input a user query, and the model will return the predicted intent and slot values.

## References

- [BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding](https://aclanthology.org/N19-1423/)
- [SlotRefine: A Fast Non-Autoregressive Model for Joint Intent Detection and Slot Filling](https://aclanthology.org/2020.emnlp-main.152/)

Please refer to the project's documentation and code for more details on implementation and usage.

**Disclaimer:** This project is for research and educational purposes. The datasets used here may have their own licenses and terms of use. Please ensure compliance with those terms when using the datasets for any purpose.
