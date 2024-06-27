# Cloud Classification through Machine Learning and Global Horizontal Irradiance Data Analysis

This repository contains the pre-trained model and code to prepare GHI data and perform cloud classification as described in our paper "Cloud Classification through Machine Learning and Global Horizontal Irradiance Data Analysis".

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
  - [Data Preparation](#data-preparation)
  - [Running the Model](#running-the-model)
- [Contributing](#contributing)
- [License](#license)
- [Citation](#citation)

## Introduction
This project provides a pre-trained machine learning model to classify cloud types using Global Horizontal Irradiance (GHI) data. Users can prepare their GHI data, run the pre-trained model, and get predictions.

## Installation
To get started with this project, clone the repository and install the necessary dependencies.

```bash
git clone https://github.com/anabelalusi/cloud-classification.git
cd cloud-classification
pip install -r requirements.txt
```


## Usage
### Data Preparation
Prepare your dataset by organizing your GHI data and corresponding cloud type labels. Ensure your data is in the format expected by the scripts.

## Running the Model
### Run the cloud classification using the pre-trained model:
python run_model.py --model_path https://github.com/anabelalusi/cloud-classification/blob/main/cloud-classification-XGBoost.pkl --input_data path/to/processed/data --output_predictions path/to/save/predictions

## Contributing
We welcome contributions to this project. Please follow the standard GitHub workflow: fork the repository, create a new branch, make your changes, and submit a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Citation
If you use this code or our models in your research, please cite our paper:

@article{yourpaper2024,
  title={Cloud Classification through Machine Learning and Global Horizontal Irradiance Data Analysis},
  author={Anabela Rocío Lusi, Pablo Facundo Orte, Elian Wolfram, José Ignacio Orlando},
  journal={Journal Name},
  year={2024},
  volume={X},
  number={Y},
  pages={Z-ZZ},
  doi={yourdoi}
}

For more information, please contact us at anabelalusi@gmail.com

