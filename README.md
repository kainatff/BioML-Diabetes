Overview

This repository implements the paper "Bio-Inspired Machine Learning Approach to Type 2 Diabetes Detection" by Al-Tawil et al. The original paper uses bio-inspired metaheuristic algorithms (Cuttlefish Algorithm and Genetic Algorithm) for feature selection, combined with traditional classifiers (KNN, SVM, NB, RF, DT, LR). This implementation reproduces those results and extends the work by adding a Multi-Layer Perceptron (MLP) as an additional classifier.
Key Additions

    MLP Implementation: A neural network classifier not explored in the original paper

    Reproduced Results: Validation of original paper's findings with CFA/GA feature selection

    Extended Analysis: Comparison of MLP performance against original classifiers

Requirements

    Python 3.8+

    Required packages:

pip install numpy pandas scikit-learn tensorflow matplotlib seaborn

Expected Output

The script will generate:

    Performance metrics (Accuracy, Kappa, MAE) for all classifiers

    Comparison plots between original and MLP results

    Execution time analysis

MLP Architecture

The implemented MLP has:

    Input layer: Size varies by selected features

    Hidden layers: 32 → 16 neurons (ReLU activation)

    Output layer: 1 neuron (Sigmoid activation)

    Optimizer: Adam

    Loss: Binary crossentropy

    Training: 100 epochs, batch_size=16

Notes

    The implementation uses the same train/test split (70%/30%) as the original paper

    Feature selection follows the paper's methodology exactly

    Random seeds are fixed for reproducibility

Citation

If you use this implementation, please cite the original paper:

Al-Tawil, M.; Mahafzah, B.A.; Al Tawil, A.; Aljarah, I. 
Bio-Inspired Machine Learning Approach to Type 2 Diabetes Detection. 
Symmetry 2023, 15, 764. https://doi.org/10.3390/sym15030764
