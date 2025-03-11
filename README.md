# Land Cover Classification

## Overview
This project provides a Land Cover Classification system using deep learning. The system can classify images into different land cover categories using a pre-trained ResNet50 model. The project includes a **Streamlit-based web application** and a **Flask API** for predictions.

## Features
- Classifies images into ten land cover categories:
  - AnnualCrop
  - Forest
  - HerbaceousVegetation
  - Highway
  - Industrial
  - Pasture
  - PermanentCrop
  - Residential
  - River
  - SeaLake
- **Streamlit Web Application** for easy interaction.
- **Flask API** for programmatic access.
- Uses a pre-trained **ResNet50** model.
- Accepts **JPEG image uploads** for prediction.

## Installation
### Prerequisites
Ensure you have Python installed (recommended: Python 3.8+).

### Install Dependencies
Run the following command to install required dependencies:
```bash
pip install -r requirements.txt
```

## Usage
### Running the Streamlit Web App
To launch the Streamlit-based application, run:
```bash
streamlit run app.py
```
Then, open the displayed local URL in a web browser.

### Running the Flask API
To start the Flask API, run:
```bash
python flask_app.py
```
The API will be available at `http://127.0.0.1:8000/predict/`. You can send a request using:
```bash
http://127.0.0.1:8000/predict/?filename=path_to_image.jpg
```

## Data
The dataset used for training is sourced from **EuroSAT**, a public dataset containing labeled land cover images derived from Sentinel-2 satellite data. It consists of images categorized into ten classes as defined in `config.py`. The data is preprocessed and fed into a ResNet50 model for classification. The dataset is not included in this repository but can be accessed from the official **EuroSAT** dataset repository.


## Model Details
The project uses **ResNet50**, a deep convolutional neural network, trained for classification tasks. The model architecture is loaded from `model.json`, and weights are loaded from `model.h5`.



