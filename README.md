# Diabetic Retinopathy Detection using UNET and Stacked UNET Architecture
The primary objective of this research paper is to study and compare the performance UNET architecture and the stacked UNET architecture in the use case of detection of Diabetic Retinopathy.

## Dataset

- **Total Images**: 3662
- [Link to Dataset at kaggle](https://www.kaggle.com/competitions/aptos2019-blindness-detection/overview)
- **Pre-processing Applied**:
  - Resize to 256x256 
  - Converted to Grayscale

- **Augmentation Applied**:
  - Vertical Flip
### Dataset Setup

1. **Download the Dataset**:<br>
   Download the dataset from [Link](https://www.kaggle.com/competitions/aptos2019-blindness-detection/overview)
2. **Place the Dataset in the Project**:<br>
   Have the Dataset in the same directory as you will run the code in.

## Tech Stack
<div><img src="https://img.icons8.com/?size=100&id=n3QRpDA7KZ7P&format=png&color=000000" height="40px" width="40px">
<img src="https://img.icons8.com/?size=100&id=13441&format=png&color=000000" height="40px" width="40px">
<img src="https://img.icons8.com/?size=100&id=bpip0gGiBLT1&format=png&color=000000" height="40px" width="40px">
<img src="https://upload.wikimedia.org/wikipedia/commons/a/ae/Keras_logo.svg" height="40px" width="40px">

## Models Implemented
### UNET Model:
Implementing the traditional UNET architecture, which is widely known for its efficiency in medical image segmentation tasks. The model was trained on a dataset of labeled retinal images to accurately identify and segment areas affected by diabetic retinopathy. The training scripts along with the metrics are available in the Single_UNET directory of the repository.
<p align= "center">
  <img src="Architectures/UNET.png?raw=true" alt="alt text" width="500" height="300">

### Stacked UNET Model:
Developed a novel Stacked UNET model, which hierarchically integrates multiple UNET architectures to capture complex features and enhance segmentation performance. This approach aims to improve the sensitivity and specificity of the detection process, particularly for identifying early-stage diabetic retinopathy. The training procedures and model metrics are located in the Stacked_UNET folder of the repository.
<p align= "center">
  <img src="Architectures/UNET-2.png?raw=true" alt="alt text" width="900" height="300">
</p>

## Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/AmeyaUppina/Diabetic_Retinoapthy-UNET_Stacket_UNET.git
   cd Diabetic_Retinoapthy-UNET_StacketUNET

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
3. **Path your Dataset**: If you have downloaded the dataset from the given link at Kaggle, then place it in both the directories to avoid pathing issues.
<br>Run this code on the terminal before starting the script
     ```bash
     mkdir Preprocessing
     cd Preprocessing
     mkdir Data
     cd ..
4. **Some Changes to be made**
   </br>To get the scripts running, you need to update the file paths. You'll have to adjust the paths for the train.csv file, the training images, and the preprocessed data directory to reflect their correct location on your system.
  </br>

## Acknowledgments

- Thanks to Kaggle for the dataset and the brilliant interface it provided to execute our code.
- Thanks to Keras Libraries for providing us with the most flexible and robust CNN layers to build our models.
- And special thanks to the coding community at Stack Overflow for having almost all the solutions for the errors we faced.
