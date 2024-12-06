# Task1-question_answering_system

The goal of Question Answering is to find the answer to a question given a question and an accompanying context. The predicted answer will be either a span of text from the context or an empty string (indicating the question cannot be answered from the context).

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies](#technologies)

## Introduction
This repository contains a question-answering system built using an open-source large language model (LLM). The system is fine-tuned for English, providing accurate responses to general knowledge or domain-specific queries. It is designed to be lightweight, efficient, and customizable for different datasets and applications.

## Installation
To use the code in this repository, follow these steps:
1. Clone the repository: `git clone https://github.com/myself-nahid/Task1-question_answering_system.git`
2. Navigate to the project directory: `cd Task1-question_answering_system`
3. Install the required dependencies: `pip install -r requirements.txt`

## Usage
1. Prepare the Dataset
Ensure dataset is structured into train, test, and validation splits and is placed in the data/ directory. Example directory structure:
`data/
├── train.json  
├── test.json  
├── validation.json`
Each file should follow the JSON format:
`{  
  "questions": ["What is artificial intelligence?", "How does photosynthesis work?"],  
  "answers": ["Artificial intelligence is the simulation of human intelligence by machines.", "Photosynthesis is the process by which green plants convert sunlight into energy."]  
}`
2. Fine-Tune the Model
Run the train.py script to fine-tune the model using the provided train and validation splits:
`python train.py --train_file data/train.json --val_file data/validation.json --output_dir model/fine_tuned_model`
3. Evaluate the Model
Evaluate the fine-tuned model using the test dataset:
`python evaluate.py --test_file data/test.json --model_dir model/fine_tuned_model` 

## Technologies
The project is implemented using the following technologies and libraries:
- Python
- PyTorch
- transformers 
- NumPy
- BERT
- Matplotlib
- Scipy
- Ftfy
- Accelerate
