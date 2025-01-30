# ADHD Detection Using EEG Data and Machine Learning

## Project Overview
This project implements a machine learning pipeline to detect Attention Deficit Hyperactivity Disorder (ADHD) using EEG (Electroencephalogram) data. The system processes raw EEG signals and extracts both structural and functional features to classify whether a subject has ADHD or not.

## Features
- EEG signal processing and feature extraction
- Both structural and functional connectivity analysis
- Advanced graph theoretical measures
- Machine learning classification using Support Vector Machine (SVM)
- RESTful API deployment using FastAPI

## Technical Details

### Data Processing
- **Structural Features**:
  - Power spectral density for different frequency bands (Delta, Theta, Alpha, Beta)
  - Spectral entropy
  - Band-specific power analysis

- **Functional Features**:
  - Global efficiency
  - Clustering coefficients
  - Graph density
  - Node strength analysis
  - Band-specific connectivity measures

### Machine Learning Pipeline
1. **Feature Extraction**: Custom transformer for EEG feature extraction
2. **Feature Alignment**: Ensures consistent feature ordering
3. **Standardization**: StandardScaler for feature normalization
4. **Classification**: SVM with RBF kernel

### Model Performance
- Achieved high classification accuracy
- Robust cross-validation results
- Successfully deployed as a FastAPI service

## Results
The SVM classifier achieved the following metrics:
- High precision and recall for both ADHD and control groups
- Good generalization on unseen data
- Reliable performance across different EEG recordings

## Installation & Usage
1. Install required packages:
```bash
pip install -r requirements.txt
```

2. Run the API:
```bash
uvicorn main:app --reload
```

3. Make predictions using the API endpoint:
- POST request to `/predict` with EEG data in CSV format

## Project Structure
```
├── main.py                # FastAPI application
├── requirements.txt       # Project dependencies
├── adhd_diagnostic_pipeline.joblib  # Trained ML pipeline
└── README.md             # Project documentation
```

## Future Improvements
- Implement real-time EEG processing
- Add more advanced feature extraction methods
- Explore deep learning approaches
- Enhance API functionality

## Technology Stack
- Python 3.10
- scikit-learn
- FastAPI
- pandas
- numpy
- networkx
- scipy

## License
[MIT License](LICENSE)
