# Enhancing Diabetic Retinopathy Detection with CNN-Based Models: A Comparative Study of UNET and Stacked UNET Architectures

This repository compares the performance of UNET and Stacked UNET architectures for diabetic retinopathy detection / segmentation tasks.

## Repository Structure

- `Single_UNET/`  
  Notebook and metrics for the single UNET model.
- `Stacked_UNET/`  
  Notebook and metrics for the stacked UNET model.
- `Architectures/`  
  Architecture diagrams/images.
- `requirements.txt`  
  Python dependencies.

## Dataset

This project uses the APTOS 2019 Blindness Detection dataset from Kaggle:

- https://www.kaggle.com/c/aptos2019-blindness-detection

### Expected folder layout

Download the dataset files from Kaggle (at minimum `train.csv` and the training images folder), then place them in the following structure:

```text
Preprocessing/
  Data/
    train.csv
    train_images/
      <image files>
```

Create the folders:

```bash
mkdir -p Preprocessing/Data
```

> Note: The dataset is not included in this repository. You must download it from Kaggle.


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

1. Clone the repository:

   ```bash
   git clone https://github.com/AmeyaUppina/Diabetic_Retinopathy-UNET_Stacked_UNET.git
   cd Diabetic_Retinopathy-UNET_Stacked_UNET
   ```

2. (Recommended) Create and activate a virtual environment:

   ```bash
   python -m venv .venv
   # Windows:
   .\.venv\Scripts\activate
   # macOS/Linux:
   source .venv/bin/activate
   ```

3. Install the requirements:

   ```bash
   pip install -r requirements.txt
   ```

## Usage

Open the notebook you want to run:

- `Single_UNET/Single_Stack_UNET.ipynb` (single UNET)
- `Stacked_UNET/2_Stacked_UNET.ipynb` (stacked UNET)

If the notebooks reference dataset paths, update them to match your local layout (see **Dataset** section above).

## Tech Stack

<div align="center">

<img src="https://img.shields.io/badge/Python%20-%2314354C.svg?&style=for-the-badge&logo=python&logoColor=white" alt="Python" />
<img src="https://img.shields.io/badge/TensorFlow%20-%23FF6F00.svg?&style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow" />
<img src="https://img.shields.io/badge/Keras%20-%23D00000.svg?&style=for-the-badge&logo=keras&logoColor=white" alt="Keras" />
<img src="https://img.shields.io/badge/OpenCV%20-%23white.svg?&style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV" />
<img src="https://img.shields.io/badge/NumPy%20-%23013243.svg?&style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy" />

</div>

## Acknowledgments

- Thanks to Kaggle for the dataset and the brilliant interface it provided to execute our code.
- Thanks to Keras Libraries for providing us with the most flexible and robust CNN layers to build our models.
- And special thanks to the coding community at Stack Overflow for having almost all the solutions for the errors we faced.

