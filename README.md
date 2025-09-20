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

1. **Download the Dataset**
   Download the dataset from [Link](https://www.kaggle.com/competitions/aptos2019-blindness-detection/overview)
2. **Place the Dataset in the Project**
   Have the Dataset in the same directory as you will run the code in.

## Tech Stack
<div><img src="https://img.icons8.com/?size=100&id=n3QRpDA7KZ7P&format=png&color=000000" height="40px" width="40px">
<img src="https://img.icons8.com/?size=100&id=13441&format=png&color=000000" height="40px" width="40px">
<img src="https://img.icons8.com/?size=100&id=bpip0gGiBLT1&format=png&color=000000" height="40px" width="40px">
<img src="https://upload.wikimedia.org/wikipedia/commons/a/ae/Keras_logo.svg" height="40px" width="40px">

## Models Implemented
### UNET Model:
<br> 
Implementing the traditional UNET architecture, widely known for its efficiency in medical image segmentation tasks. The model was trained on a dataset of labeled retinal images to accurately identify and segment areas affected by diabetic retinopathy. The training scripts along with the metrics are available in the Single_UNET directory of the repository.
</br>
</br>

<p align= "center">
  <img src="Architectures/UNET.png?raw=true" alt="alt text" width="500" height="300">
</p>

</br>

### Stacked UNET Model:
<br> 
Developed a novel Stacked UNET model, which hierarchically integrates multiple UNET architectures to capture complex features and enhance segmentation performance. This approach aims to improve the sensitivity and specificity of the detection process, particularly for identifying early-stage diabetic retinopathy. The training procedures and model metrics are located in the Stacked_UNET folder of the repository.

</br>
</br>
<p align= "center">
  <img src="Architectures/UNET-2.png?raw=true" alt="alt text" width="900" height="300">
</p>
</br>

## Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/Diabetic_Retinoapthy-UNET_StacketUNET.git
   cd Diabetic_Retinoapthy-UNET_StacketUNET

2. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
3. **Path your Dataset**
   -If you have downloaded the dataset from the given link at Kaggle, then place it in both the directories to avoid pathing issues.
  -Run this code on the terminal before starting the script
     ```bash
     mkdir Preprocessing
     cd Preprocessing
     mkdir Data
     cd ..
4. **Some Changes to be made**
   </br>In each of the scripts (Single_Stack_UNET.ipynb & 2_Stacked_UNET.ipynb) in cell numbers 1, 3 and 8 the paths needs to be changed,</br> 1 -> "aptos2019-blindness-detection/train.csv"</br> 3 ->"aptos2019-blindness-detection/train_images/{x}.png" & "Preprocessed/Data" </br>8 -> "/Preprocessed/Data" 
  </br>

## Acknowledgments

- Thanks to Kaggle for the dataset and the brilliant interface it provided to execute our code.
- Thanks to Keras Libraries for providing us with the most flexible and robust CNN layers to build our models.
- And special thanks to the coding community at Stack Overflow for having almost all the solutions for the errors we faced.
