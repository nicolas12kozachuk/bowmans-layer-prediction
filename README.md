# Analysis of Corneal Biomechanical Properties and Machine Learning for Bowman’s Layer Prediction

## Project Description

This project investigates the biomechanical properties of human and porcine corneas using **Vibrational Optical Coherence Tomography (VOCT)** and applies machine learning to identify the resonance frequency of Bowman’s layer, which is present in human corneas but absent in porcine ones. The study combines experimental data, finite element modeling, and machine learning to analyze the role of Bowman’s layer and collagen fibrils in corneal stability.

## Machine Learning Component

### Objective
To classify corneal resonance frequencies and identify the 110–120 Hz resonance peak associated with Bowman’s layer using two machine learning algorithms:
1. **Variational Bayesian Gaussian Mixture Model (VBGMM)** - Unsupervised clustering.
2. **Support Vector Clustering (SVC)** - Supervised learning with cross-validation.

### Dataset
- **VOCT Data**: 40 datasets from human and porcine corneas.
- **Frequency Range**: 50 Hz to 250 Hz in 10 Hz increments.
- **Preprocessing**: Normalization of weighted displacement versus frequency plots.

### Results
- The **110–120 Hz peak** was identified as the key distinguishing feature for human corneas.
- **VBGMM Accuracy**: 92.16% at 110 Hz.
- **SVC Accuracy**: Decreased significantly when the 110 Hz peak was excluded, confirming its importance.
  - **With 110 Hz Peak**: 95.32%.
  - **Without 110 Hz Peak**: 67.85%.

## Key Findings

- Bowman’s layer contributes to the **110–120 Hz resonant frequency**, with an estimated elastic modulus of 2.5 ± 0.25 MPa.
- Machine learning confirmed the significance of this layer in distinguishing human corneas from porcine corneas.

## Code Overview

The implementation is provided in the `Bowmans_Layer_Prediction_SVC_and_BayesianGaussianMixtureModel.ipynb` notebook, which includes:
1. **Data Preprocessing**:
   - Normalizes VOCT data for consistent feature scaling.
2. **Clustering and Classification**:
   - Implements VBGMM and SVC for resonance frequency analysis.
3. **Visualization**:
   - Plots accuracy metrics and resonance frequency distributions.

## How to Run

1. Open the `Bowmans_Layer_Prediction_SVC_and_BayesianGaussianMixtureModel.ipynb` notebook.
2. Ensure Python 3.x and the following libraries are installed:
   - NumPy
   - scikit-learn
   - matplotlib
3. Run the cells to preprocess the data, train the models, and analyze results.

## Learning Outcomes

This project highlights:
- The integration of experimental data and machine learning to solve biomedical problems.
- The ability of machine learning models to provide insights into biological structures like Bowman’s layer.
- The importance of understanding corneal biomechanics for applications in diagnosing and treating degenerative diseases like keratoconus.

## References

Refer to the detailed project report for further information and methodology.
