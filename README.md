# Protein-Family-Classification
Protein Family Classification using Random Forest and 1D CNN on UniProt protein sequences
# Protein Family Classifier – AI in Bioinformatics

## Project Overview
Protein classification using Machine Learning and Deep Learning techniques.

Classes:
- Kinase
- Protease
- Receptor
- Transporter

## Student B Tasks
- Random Forest with k-mer (k=3, k=4)
- Performance comparison
- Confusion Matrix

## Results

Random Forest (k=3): 0.375

Random Forest (k=4): 0.350



Best Result:
Random Forest with k=3


## Student C Tasks

### Data Collection and Dataset Preparation

Tasks completed:

- Downloaded protein sequence data from UniProt
- Collected four protein families:
  - Kinases
  - Proteases
  - Transporters
  - Receptors

- Parsed FASTA files using BioPython
- Filtered protein sequence lengths (50–1000 amino acids)
- Created labeled dataset
- Converted records into a Pandas DataFrame
- Applied stratified train-test split:
  - Training set: 80%
  - Testing set: 20%

- Generated:
  - train.fasta
  - test.fasta

## Results

Dataset statistics:

Training samples: 531 sequences  
Testing samples: 133 sequences  

Class distribution:

- Proteases: 149
- Transporters: 131
- Receptors: 129
- Kinases: 122

Generated FASTA files successfully:

train.fasta → 531 sequences  
test.fasta → 133 sequences
### BLAST Baseline Evaluation

Tasks completed:

- Implemented BLAST as a baseline method
- Compared protein sequences using similarity search
- Generated prediction labels
- Evaluated baseline performance using Confusion Matrix
- Visualized classification performance

## BLAST Results

Confusion Matrix observations:

- Kinases correctly classified: 25
- Proteases correctly classified: 35
- Transporters correctly classified: 14
- Receptors correctly classified: 25

Minor misclassifications observed between related protein families.

BLAST baseline achieved strong performance and was used as a reference for comparison with Machine Learning and CNN models.


## 1D CNN Protein Family Classification
Dataset

A balanced dataset of protein sequences was prepared:

Class	Samples
Kinase	100
Protease	100
Transporter	100
Receptor	200

Total samples: 500 protein sequences

CNN Architecture

The model was implemented using TensorFlow/Keras:

Conv1D (32 filters, kernel size = 3, ReLU)
MaxPooling1D
Conv1D (64 filters, kernel size = 3, ReLU)
MaxPooling1D
Flatten
Dense (128 neurons, ReLU)
Dense (4 neurons, Softmax)

Total parameters:

1,014,596
Training Configuration
Optimizer: Adam
Loss Function: Sparse Categorical Crossentropy
Epochs: 10
Batch Size: 32
Validation Split: 20%
CNN Results
Test Accuracy
51.99%
Classification Report
Class	Precision	Recall	F1-score
Kinase	0.16	0.20	0.18
Protease	0.61	0.55	0.58
Receptor	0.90	0.90	0.90
Transporter	0.06	0.05	0.05

Overall Accuracy:

0.52

Macro Average F1-score:

0.43

Weighted Average F1-score:

0.52
Confusion Matrix Observations
Receptor achieved the highest classification performance.
Protease showed moderate classification accuracy.
Kinase and Transporter were more difficult to distinguish.
CNN outperformed Random Forest on the prepared dataset.
Final Model Comparison
Model	Accuracy
##Random Forest (k=3)	37.5%
##Random Forest (k=4)	35.0%
##1D CNN	52.0%
Best Model

## Student
Mohamed Karim 221010054

Yousef abdallah khamis 221002152
