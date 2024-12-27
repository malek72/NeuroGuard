# NeuroGuard

![Project Banner](https://github.com/malek72/NeuroGuard/blob/main/Screenshot%202024-12-27%20at%2016.10.28.png)

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Installation](#installation)
  - [Prerequisites](#prerequisites)
  - [Clone the Repository](#clone-the-repository)
  - [Create a Virtual Environment](#create-a-virtual-environment)
  - [Install Dependencies](#install-dependencies)
- [Data Preparation](#data-preparation)
  - [T5 Model Dataset](#t5-model-dataset)
  - [LLaMA Model Dataset](#llama-model-dataset)
- [Usage](#usage)
  - [Training the T5 Model](#training-the-t5-model)
  - [Fine-Tuning the LLaMA 3.1 Model](#fine-tuning-the-llama-31-model)
  - [Inference](#inference)
- [Model Deployment](#model-deployment)
  - [Containerization with Docker](#containerization-with-docker)
  - [API Setup](#api-setup)
  - [Scalability and Monitoring](#scalability-and-monitoring)
- [Configuration](#configuration)
  - [Environment Variables](#environment-variables)
  - [Hyperparameters](#hyperparameters)
- [Evaluation](#evaluation)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)
- [Contact](#contact)

## Overview

Mental Health Support AI is an innovative project designed to assist individuals facing mental health challenges by providing accurate diagnoses and personalized action plans. The system integrates two state-of-the-art language models:

1. **T5 (Text-to-Text Transfer Transformer):** Specially trained to classify and diagnose the type of mental health issue based on user input.
2. **LLaMA 3.1:** Fine-tuned to generate compassionate, actionable, and evidence-based step-by-step plans to help users manage and overcome their mental health crises.

By combining these models, the system can effectively identify the user's mental health concerns and offer tailored guidance to support their well-being.

## Features

- **Automatic Classification:** Utilizes the T5 model to accurately diagnose mental health issues from user inputs.
- **Personalized Action Plans:** Generates customized, step-by-step plans using the LLaMA 3.1 model to help users address their specific mental health challenges.
- **Efficient Fine-Tuning:** Implements LoRA adapters and 4-bit quantization with Unsloth for memory-efficient and faster model fine-tuning.
- **Scalable Inference:** Supports rapid and scalable inference with optimized memory usage, ensuring responsiveness even under high demand.
- **User-Friendly Interface:** Provides intuitive scripts and functions for training, evaluation, and inference, making it accessible to users with varying levels of expertise.
- **Ethical Considerations:** Incorporates guidelines and safety measures to ensure responses are supportive, non-judgmental, and encourage professional help when necessary.

## Architecture

![Architecture Diagram](https://github.com/yourusername/mental-health-support-ai/blob/main/architecture.png)

1. **Data Processing:**
   - **Data Cleaning:** Removes any incomplete or irrelevant data to ensure high-quality inputs.
   - **Data Formatting:** Structures the data appropriately for each model, preparing it for training and fine-tuning.

2. **Model Training:**
   - **T5 Model:** Trained on a dataset of user texts and corresponding mental health labels to perform classification tasks.
   - **LLaMA 3.1 Model:** Fine-tuned using the Alpaca dataset (or a custom dataset) to generate supportive and actionable plans based on the classifications provided by the T5 model.

3. **Inference Pipeline:**
   - **User Input:** Receives and processes user queries.
   - **Classification:** The T5 model identifies the specific mental health concern.
   - **Plan Generation:** The LLaMA model generates a tailored step-by-step plan to assist the user.

4. **Deployment:**
   - **API Integration:** Models are deployed behind an API for easy access and integration into various platforms.
   - **Scalability:** Ensures the system can handle multiple requests efficiently, maintaining performance and reliability.

## Installation

### Prerequisites

Before setting up the project, ensure you have the following installed on your system:

- **Operating System:** Linux or macOS (Windows is supported but may require additional configuration)
- **Python:** Version 3.8 or higher
- **CUDA:** Compatible CUDA version for GPU acceleration (optional but recommended)
- **Git:** For cloning the repository

### Clone the Repository

Begin by cloning the repository to your local machine:

```bash
git clone https://github.com/yourusername/mental-health-support-ai.git
cd mental-health-support-ai
