# LLM Fine-Tuning and Evaluation on Topical Chat Dataset

This project fine-tunes a causal language model for conversational response generation using the Topical-Chat dataset. The goal is to compare the behavior of the original base model with a fine-tuned version and evaluate whether fine-tuning improves conversational quality, relevance, and response consistency.

The project was developed and tested on Kaggle using GPU acceleration. It includes separate workflows for training, evaluation, perplexity measurement, and interactive conversation testing.

## Project Overview

The notebook performs supervised fine-tuning on conversational data by converting multi-turn dialogues into training examples where the model learns to generate assistant-style responses. A base language model is loaded from Hugging Face, prepared for fine-tuning, trained on a selected portion of the dataset, and then evaluated using validation loss and perplexity.

A separate notebook is used to test the original base model through an interactive chat interface. This allows direct comparison between the base model and the fine-tuned model using the same prompts.

## Main Features

- Loads and preprocesses the Topical-Chat dataset
- Converts conversations into instruction-style training samples
- Fine-tunes a Hugging Face causal language model
- Supports controlled dataset fraction selection
- Computes evaluation loss and perplexity
- Provides an interactive chat interface for testing
- Allows comparison between base model and fine-tuned model responses
- Saves model outputs and chat logs for later analysis

## Evaluation

The model is evaluated using:

- **Evaluation Loss**: Measures how well the model predicts validation responses.
- **Perplexity**: Indicates how uncertain the model is when generating text. Lower perplexity generally means better language modeling performance.
- **Qualitative Chat Testing**: The same prompts are tested on both the base model and the fine-tuned model to compare response quality.

## Base Model Comparison

Before fine-tuning, the base model is tested in a separate notebook using an interactive conversation loop. This provides baseline responses that can be compared against the fine-tuned model after training.

Example comparison workflow:

1. Load the base model.
2. Ask a fixed set of prompts.
3. Save the base model responses.
4. Fine-tune the model.
5. Ask the same prompts again using the fine-tuned model.
6. Compare response relevance, fluency, and conversational behavior.

## Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- Kaggle Notebooks
- CUDA GPU acceleration
- Topical-Chat dataset

## Purpose

This project was created to understand the complete workflow of fine-tuning a conversational LLM, evaluating it with perplexity, and comparing its outputs against the original base model. It is useful for learning practical LLM fine-tuning, dataset preparation, training configuration, and model evaluation.
