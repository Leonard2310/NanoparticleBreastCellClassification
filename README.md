# Nanoparticle Breast Cell Classification**

## Description
This project involves predicting the class of each breast cell (benign/malignant) after exposure to carbon nanoparticles. The objective is to determine whether nanoparticle exposure affects the recognition of tumor tissue. 

## Evaluation
The evaluation metric for this competition is Accuracy, which is calculated as the percentage of correctly classified instances with respect to the total evaluated instances.

Accuracy = (True Positive + True Negative) / Evaluated Instances

## Dataset Description
The dataset provided by the DICMAPI research group includes multichannel images of breast cell samples captured under different imaging modalities. Each sample consists of multiple cells, and each acquisition is represented as a distinct folder containing images of individual cells in .npy format. The training set comprises 40 acquisitions, while the test set comprises 10 acquisitions without separate folders.

## Project Description
The project follows these main steps:

### 1. Drive Linking
To facilitate easy access to data, Google Drive is linked to Google Colab. This allows for loading and saving data directly from the cloud.

### 2. Library Import
The project imports various libraries essential for data manipulation, model building, and evaluation. These include libraries for handling arrays and data frames, deep learning frameworks, and utilities for data visualization and performance measurement.

### 3. Check Device
The code checks the availability of a GPU. If a GPU is available, it is used to speed up the model training process. If not, the CPU is used.

### 4. Data Preprocessing
Data preprocessing involves loading the multichannel images of breast cells, handling any missing values, normalizing the data, and splitting it into training and testing sets. This ensures that the data is in the right format for model training and evaluation.

### 5. Custom Dataset Class
A custom dataset class is implemented to handle the breast cell images stored in `.npy` format. This class helps in loading the images and applying necessary transformations before feeding them into the model.

### 6. Data Augmentation and Transformation
To enhance model performance and generalization, data augmentation techniques such as random horizontal and vertical flips are applied. These transformations increase the diversity of the training data.

### 7. Load Data
The datasets are loaded using PyTorch's DataLoader, which helps in managing and feeding the data to the model in batches. This is crucial for efficient training and evaluation.

### 8. Model Training
The project uses transfer learning with a pre-trained model to leverage existing knowledge for better performance. The final layer of the pre-trained model is modified to suit the binary classification task of identifying benign and malignant cells.

### 9. Training Loop
A training loop is implemented to train the model over multiple epochs. In each epoch, the model is trained on the training data and evaluated on the validation data. Performance metrics such as loss and accuracy are calculated and used to monitor the training process.

### 10. Evaluation
The trained model is evaluated on the test data to measure its accuracy. This involves making predictions on the test data and comparing them to the true labels to calculate the percentage of correctly classified instances.

## Requirements
The majority of experiments were performed on the Colaboratory cloud platform for deep learning, specifically using a T4 GPU with 12.7GB of memory.

## Results
The solution achieved an accuracy of 97.6%.

## Contributions
We welcome contributions from the community. Feel free to fork this repository, make your changes, and submit a pull request. Please ensure that your contributions are well-documented and tested.

## Author
- [Leonardo Catello](https://github.com/Leonard2310)

## Acknowledgements
We thank Prof. Mariano Sirignano and Prof. Valeria Panzetta from DICMAPI (Dipartimento di Ingegneria Chimica, dei Materiali e della Produzione Industriale - University of Naples Federico II) for providing the task and the data. Please note that the dataset is not publicly available.
