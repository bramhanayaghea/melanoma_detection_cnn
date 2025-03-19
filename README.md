# Skin Cancer Detection using Convolutional Neural Networks (CNN)

## Problem Statement
Develop a machine learning model to detect melanoma and other skin conditions early. Melanoma accounts for 75% of skin cancer deaths, making early detection crucial. This project aims to create an AI-powered tool to assist dermatologists in preliminary skin cancer screening.

## Dataset Overview
- Source: International Skin Imaging Collaboration (ISIC)
- Total Images: 2,357
- Image Resolution: 180x180 pixels

### Skin Conditions Classified
1. Actinic keratosis
2. Basal cell carcinoma
3. Dermatofibroma
4. Melanoma
5. Nevus
6. Pigmented benign keratosis
7. Seborrheic keratosis
8. Squamous cell carcinoma
9. Vascular lesion

## Project Methodology

### 1. Data Preprocessing
- Loaded images from train and test directories
- Resized all images to 180x180 pixels
- Split training data into training (80%) and validation (20%) sets
- Batch size: 32 images

### 2. Model Development Iterations

#### First Model (Baseline)
- Simple CNN architecture
- Layers:
  - Rescaling layer
  - 3 Convolutional layers with ReLU activation
  - MaxPooling layers
  - Dense layers
- Identified overfitting issues

#### Second Model (Regularization)
- Added data augmentation techniques:
  - Random horizontal flips
  - Random rotations (±10 degrees)
  - Random zoom
- Introduced dropout layers to reduce overfitting

#### Final Model (Balanced Dataset)
- Enhanced CNN architecture
- Class balancing through data augmentation
- Improved regularization
- More convolutional filters
- Trained for 50 epochs

### 3. Key Techniques Implemented
- Data Augmentation
- Dropout Regularization
- Class Imbalance Handling
- Learning Rate Optimization


## Performance Improvements

### Overfitting Mitigation
- Initial model showed significant overfitting
- Dropout layers reduced the gap between training and validation accuracy
- Data augmentation helped improve generalization

### Class Imbalance Resolution
- Identified significant variations in class sample sizes
- Used Augmentor library to add 500 samples to each class
- Balanced dataset improved model performance

## Technologies and Libraries
- Python 3.x
- TensorFlow & Keras
- NumPy
- Pandas
- Matplotlib
- Augmentor
- PIL (Python Imaging Library)

## Installation and Setup

### Prerequisites
- Python 3.7+
- pip package manager

### Installation Steps
1. Clone the repository
   ```bash
   git clone https://github.com/bramhanayaghea/melanoma_detection_cnn.git
   cd melanoma_detection_cnn
   ```

2. Install required packages
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter Notebook
   ```bash
   jupyter notebook Bramhanayaghe_Arumugam_NN.ipynb
   ```

## Model Evaluation
- Final model achieved improved validation accuracy
- Demonstrated better generalization across different skin conditions

## Future Work
- Fine-tune hyperparameters
- Explore transfer learning
- Implement more advanced CNN architectures
- Collect more diverse training data

## Ethical Considerations
- Intended as a screening tool, not a replacement for professional medical diagnosis
- Requires validation by healthcare professionals

## Contributing
Contributions, issues, and feature requests are welcome. Feel free to check the issues page.

## License
NA

## Acknowledgments
- International Skin Imaging Collaboration (ISIC) for the dataset
- Open-source machine learning community
