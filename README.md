# NLP Project - Personalized Recommendation System

## Project Overview

This project implements a personalized recommendation system using Natural Language Processing (NLP) techniques. The system focuses on user-based personalization with multiple knowledge levels (k1, k2, k3) and includes both base model and fine-tuned model implementations.

## Project Structure

```
NLP_Project-main/
├── LaMP_format/                    # Training and validation datasets
│   ├── personalized_train_k*.json  # Training data for different knowledge levels
│   └── personalized_validation_k*.json  # Validation data for different knowledge levels
├── Outputs_LaMP_format/            # Fine-tuned model outputs
├── Outputs_LaMP_format_base/       # Base model outputs
├── Evaluation.ipynb                # Model evaluation and metrics
├── Fine_tuning.ipynb               # Model fine-tuning implementation
├── model_new.ipynb                 # Main model implementation
└── preprocess_new.ipynb            # Data preprocessing pipeline
```

## Features

- **Multi-level Personalization**: Supports three knowledge levels (k1, k2, k3) for personalized recommendations
- **Dual Model Approach**: Implements both base models and fine-tuned models for comparison
- **Synonym Handling**: Includes datasets with and without synonyms for robust training
- **Comprehensive Evaluation**: Built-in evaluation metrics and comparison tools
- **LaMP Format**: Uses LaMP (Language Model Personalization) format for structured data

## Getting Started

### Prerequisites

- Python 3.7+
- Jupyter Notebook
- Required NLP libraries (see requirements.txt)

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd NLP_Project-main
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Set up your environment variables in a `.env` file:
```
OPENAI_API_KEY=your_api_key_here
```

## Usage

### 1. Data Preprocessing
Start with `preprocess_new.ipynb` to prepare your training and validation datasets.

### 2. Model Training
Use `Fine_tuning.ipynb` to fine-tune your base models on the personalized datasets.

### 3. Model Evaluation
Run `Evaluation.ipynb` to compare base and fine-tuned model performance across different knowledge levels.

### 4. Main Model
Access the core model implementation through `model_new.ipynb`.

## Dataset Structure

The project uses LaMP format datasets with the following naming convention:
- `personalized_train_k{level}_Input_UserBased_PNC.json` - Training data
- `personalized_validation_k{level}_Input_UserBased_PNC.json` - Validation data
- `without_synonyms_*` - Datasets excluding synonym variations

## Retrieval Parameters

- **K1**: Retrieves 1 document from the knowledge base for context
- **K2**: Retrieves 2 documents from the knowledge base for context
- **K3**: Retrieves 3 documents from the knowledge base for context

These parameters control how many relevant documents are retrieved and used to generate personalized responses in the RAG system.

## Output Analysis

Results are organized in two main directories:
- `Outputs_LaMP_format/` - Fine-tuned model predictions
- `Outputs_LaMP_format_base/` - Base model predictions

This allows for direct comparison between model versions and evaluation of personalization improvements.
