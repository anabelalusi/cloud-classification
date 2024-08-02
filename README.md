# Cloud Classification through Machine Learning and Global Horizontal Irradiance Data Analysis

This repository contains the pre-trained model and code to prepare GHI data and perform cloud classification as described in our paper "Cloud Classification through Machine Learning and Global Horizontal Irradiance Data Analysis".

## Table of Contents
- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
  - [Data Preparation](#data-preparation)
  - [Running the Model](#running-the-model)
  - [Detailed Steps](#detailed-steps)
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
1. Organize your data: Ensure your data file (for example "data.csv") is placed in the project directory
2. Data format: Your data.csv file should contain the following columns: ghi (ghi data at minute resolution), ghi_cs (a clear sky model), kt_modificado (the value of the modified clearness index), delta_kt_modificado (variation between consectuvie kt* values)

### Running the Model
1. Ensure correct input data: Your input data files should be in the correct format and located in the project directory.
2. Run the provided script: Execute the script in a Python environment to prepare the data, compute features, and make predictions using the pre-trained model.

```bash
python run_model.py --model_path https://github.com/anabelalusi/cloud-classification/blob/main/cloud-classification-XGBoost.pkl --input_data path/to/processed/data --output_predictions path/to/save/predictions
```
### Detailed steps
1. Insert Site Data: Provide the solar total irradiance (Gs), cosine of the zenith angle (cz), and the orbital correction factor (Fn).
2. Load data: Load the GHI and clear sky GHI data from the provided CSV files.
3. Calculate Clearness Index: Compute the clearness index and the modified clearness index from the loaded data.
4. Create DataFrame: Organize the data into a DataFrame and clean any rows with NaN values.
5. Feature Calculation: Define a function to calculate the necessary features from 33-minute windows of data.
6. Run the Pre-trained Model: Load the pre-trained model, make predictions based on the calculated features, and map numerical predictions to cloud class names.
7. Display Results: Output the predictions and their corresponding cloud class names.

## Contributing
We welcome contributions to this project. Please follow the standard GitHub workflow: fork the repository, create a new branch, make your changes, and submit a pull request.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Citation
If you use this code or our models in your research, please cite our paper:

```bash
@article{Lusi2024cloudclassification,
  title={Cloud Classification through Machine Learning and Global Horizontal Irradiance Data Analysis},
  author={Anabela Rocío Lusi, Pablo Facundo Orte, Elian Wolfram, José Ignacio Orlando},
  journal={Journal Name},
  year={2024},
  volume={X},
  number={Y},
  pages={Z-ZZ},
  doi={yourdoi}
}
```

For more information, please contact us at anabelalusi@gmail.com

