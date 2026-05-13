# Predictive-Maintenance-of-Motors
## Project Overview:
This project implements a sophisticated Hybrid Physics-Informed Neural Network (PINN) framework for the real-time diagnosis of mechanical faults in rotating machinery. By fusing data-driven Deep Learning (1D-CNN) with physics-based constraints (Newton's Laws), the model achieves high interpretability and a 98% classification accuracy across six different failure modes.  The system is designed to handle raw vibration signals, performing on-the-fly preprocessing to extract critical spectral features for industrial predictive maintenance.  

## Key Features
* Hybrid Modeling: Combines a 1D-CNN branch for raw signal feature extraction with a Statistical branch for expert-engineered features.
* Physics-Informed Learning: Incorporates mechanical domain knowledge through a PINN decoder that predicts displacement while adhering to physical laws.
* Advanced Signal Processing: Utilizes Fast Fourier Transform (FFT) and Time-Domain analysis to identify spectral harmonics (1x, 2x, 3x) and fault signatures.
* Multimodal Integration: Seamlessly integrates raw vibration data with tabular features (e.g., RPM) for a comprehensive diagnostic output.  

## Dataset:
The model is trained and validated on the MaFaulda (Machinery Fault Database), which includes diverse failure modes such as imbalance, misalignment, and bearing faults. 
## Dataset Link: https://www.kaggle.com/datasets/vuxuancu/mafaulda-full

## Technical Architecture
* Preprocessing: Zero-centering, normalization, and FFT-based feature extraction.  
* CNN Branch: Captures local patterns and temporal dependencies from raw vibration signals.
* Expert Branch: Processes statistical features like RMS, Kurtosis, Skewness, and Crest Factor.
* PINN Decoder: Solves the physics-based differential equations to ensure predicted behaviors match mechanical reality.
  
## Technologies Used
* Core: Python, PyTorch
* Data Analysis: NumPy, Pandas, Scikit-learn
* Signal Processing: SciPy (Signal/Integrate)
* Visualization: Matplotlib, Seaborn

## Results
The framework demonstrated exceptional robustness on the MaFaulda dataset:  
* Overall Accuracy: 98%
* Classes Detected: Normal, Imbalance, Horizontal Misalignment, Vertical Misalignment, Bearing Faults (Inner/Outer Race).

## Repository Structure
├── Code Notebook          # Signal Preprocessing, PINN & CNN architecture definitions, Training, and Evaluation notebooks
├── requirements.txt    # Project dependencies
└── README.md
