# NeuroGuard

![Project Banner](https://github.com/yourusername/mental-health-support-ai/blob/main/banner.png)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Installation](#installation)
- [Usage](#usage)
  - [Training the T5 Model](#training-the-t5-model)
  - [Fine-Tuning the LLaMA 3.1 Model](#fine-tuning-the-llama-31-model)
  - [Inference](#inference)
- [Dataset](#dataset)
- [Model Deployment](#model-deployment)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Overview

Mental Health Support AI is a comprehensive project aimed at developing an advanced language model system to assist individuals facing mental health challenges. The system leverages two powerful models:

1. **T5 (Text-to-Text Transfer Transformer):** Trained to classify and diagnose the type of mental health issue based on user input.
2. **LLaMA 3.1:** Fine-tuned to generate compassionate, actionable, and evidence-based step-by-step plans to help users overcome their mental health crises.

By combining these models, the system can accurately identify the user's mental health concerns and provide personalized guidance to support their well-being.

## Features

- **Automatic Classification:** Uses T5 to diagnose mental health issues from user inputs.
- **Personalized Plans:** Generates tailored step-by-step plans to help users manage and overcome their mental health challenges.
- **Efficient Fine-Tuning:** Utilizes LoRA adapters and 4-bit quantization for efficient model fine-tuning.
- **Scalable Inference:** Supports fast and scalable inference with optimized memory usage.
- **User-Friendly Interface:** Provides easy-to-use functions for training, evaluation, and inference.

## Architecture

![Architecture Diagram](https://github.com/yourusername/mental-health-support-ai/blob/main/architecture.png)

1. **Data Processing:**
   - Cleans and formats user input data.
   - Prepares datasets for model training.

2. **Model Training:**
   - **T5 Model:** Trained for classification of mental health issues.
   - **LLaMA 3.1 Model:** Fine-tuned to generate supportive and actionable plans based on T5's classification.

3. **Inference Pipeline:**
   - Receives user input.
   - T5 classifies the mental health issue.
   - LLaMA generates a step-by-step plan to assist the user.

## Installation

### Prerequisites

- Python 3.8 or higher
- CUDA-enabled GPU (recommended for training and inference)
- Git

### Clone the Repository

```bash
git clone https://github.com/yourusername/mental-health-support-ai.git
cd mental-health-support-ai
