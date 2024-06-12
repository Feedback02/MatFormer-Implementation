# MatFormer Implementation

## Introduction

This repository contains the implementation of the MatFormer model as described in the paper "MatFormer: Nested Transformer for Elastic Inference." The MatFormer model introduces a nested Transformer architecture designed to provide elasticity in various deployment scenarios.

## Repository Contents

- `MatFormer_implementation.ipynb`: Jupyter notebook containing the implementation of the MatFormer model, training, evaluation, and results.
- `1_model_weights`: Weights of the MatFormer model.
- `1_model_weights_traditional`: Weights of the traditional Transformer model for comparison and evaluation purposes.

## Method

The MatFormer model defines a nested Transformer architecture with multiple granularities. Each granularity corresponds to a subset of neurons in the Feed Forward Network (FFN) block of the Transformer. This nested structure allows for the extraction of smaller, efficient sub-models from a single, larger model, enabling flexible deployment based on computational constraints.


## Installation

To run the code in this repository, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Feedback02/MatFormer-Implementation.git
   cd MatFormer-Implementation
   ```

2. **Set Up a Virtual Environment** (optional but recommended):
   ```bash
   python3 -m venv matformer_env
   source matformer_env/bin/activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```


## Running the Code

Open the Jupyter notebook `MatFormer_implementation.ipynb` to explore the implementation, training, and evaluation of the MatFormer model. You can run the cells step by step to understand the workflow and observe the results.

### Example Usage

1. **Load the Pre-trained Weights**:
    In the end of the notebook you will find something like:
   ```python
   model.load_state_dict(torch.load('1_model_weights')) #1_model_weights or 1_model_weights_traditional
   ```

2. **Evaluate the Model**:
   Follow the evaluation steps in the notebook to compare the performance of the MatFormer model with the traditional Transformer model.


