
# Anti-Cancer Prediction with Graph Neural Networks

## Introduction

This project aims to predict the anti-cancer properties of chemical compounds using Graph Neural Networks (GNN). We build a classification model to determine whether a chemical compound is effective against non-small cell lung cancer, using chemical compound graphs as input data.

## Input Data

The input data consists of graphs representing chemical compounds. In these graphs, atoms are nodes, and bonds are edges. The goal is to classify these compounds into two classes:
- 1: Positive class (effective against non-small cell lung cancer)
- 0: Negative class (not effective against non-small cell lung cancer)

## Data Mining Function

The primary data mining function used in this project is classification and prediction.

## Challenges

Several challenges need to be addressed during this project, including:
- Reading the SDF format for chemical compound representation
- Handling data imbalance between classes
- Extracting relevant features from the data
- Implementing strategies to prevent overfitting

## Impact

The project's ultimate goal is to determine whether a specific drug or compound has potential anti-cancer properties, providing valuable insights for medical research.

## Experimental Protocol

The experimental protocol involves the following steps:
1. Loading and cleaning the data.
2. Data preprocessing and splitting into training and validation sets.
3. Training the GNN model.
4. Evaluating the model's performance using metrics like AUROC.
5. Making predictions on the test dataset.

## Key Trials

I conducted several trials with different configurations to find the best model setup. Here is a comparison of the key trials:

| Trial | Model   | Data       | Message Calculation | Hidden Dim | Training Accuracy | Kaggle Public Score |
|-------|---------|------------|----------------------|------------|-------------------|---------------------|
| 1     | GNN     | Not Upsampled  | N/A                | 32         | 83.47%            | 79.30%              |
| 2     | GNN     | Upsampled  | N/A                | 32         | 79.30%            | 77.54%              |
| 3     | GNN     | Upsampled  | GGNN               | 32         | 90.61%            | 86.60%              |
| 4     | GNN     | Upsampled  | RGCN               | 32         | 83.42%            | 80.48%              |
| 5     | GNN     | Upsampled  | RGAT               | 32         | 85.39%            | 81.05%              |
| 6     | GNN     | Upsampled  | RGIN               | 32         | 86.02%            | 82.35%              |
| 7     | GNN     | Upsampled  | GNN_Edge_MLP       | 32         | 84.66%            | 85.20%              |
| 8     | GNN     | Upsampled  | GNN_FiLM           | 32         | 80.38%            | 81.58%              |
| 9     | GNN     | Upsampled  | GCNN               | 64         | 93.15%            | 84.13%              |
| 10    | GNN     | Upsampled  | GNN_Edge_MLP       | 64         | 88.79%            | 83.97%              |


Please refer to the notebook for more details on each trial.

## Questions

For additional information on the input file format, tensor dimensions, and model architecture, please refer to the notebook.
