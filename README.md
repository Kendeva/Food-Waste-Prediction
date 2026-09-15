# AI-Based Food Waste Prediction

A simple Artificial Intelligence project developed to predict potential food waste in supermarkets using a Decision Tree Classifier.

The model analyzes supermarket stock and sales conditions to determine whether the remaining stock is classified as **Safe** or **Potentially Wasted**.

## Project Overview

Food waste is one of the common problems faced by supermarkets, especially when the amount of available stock does not match customer demand.

This project applies a machine learning approach to analyze supermarket sales data and predict the potential risk of food waste based on several factors such as stock quantity, items sold, weather conditions, holidays, and remaining stock percentage.

## Features

- Load supermarket sales data from a CSV dataset
- Process features and prediction labels
- Split data into training and testing sets
- Train a Decision Tree Classifier
- Evaluate model accuracy
- Visualize the Decision Tree
- Predict new stock conditions

## Technologies Used

- Python
- Pandas
- Scikit-learn
- Matplotlib

## Machine Learning Model

The project uses a **Decision Tree Classifier** with the following configuration:

- Criterion: Entropy
- Maximum Depth: 4
- Training Data: 80%
- Testing Data: 20%

## Dataset

The dataset contains simulated supermarket sales data with the following features:

| Feature | Description |
| --- | --- |
| `stok` | Total available stock |
| `terjual` | Number of items sold |
| `hari_ke` | Day index |
| `cuaca` | Weather condition |
| `hari_besar` | Holiday or special day indicator |
| `sisa_persen` | Remaining stock percentage |
| `label` | Prediction target |

The prediction is divided into two categories:

- **Safe**
- **Potentially Wasted**

## Project Structure

```text
food-waste-prediction/
├── data/
│   └── data_penjualan.csv
├── src/
│   └── main.py
├── .gitignore
├── README.md
└── requirements.txt
```

## Installation

Clone this repository:

```bash
git clone https://github.com/Kendeva/food-waste-prediction.git
```

Move into the project directory:

```bash
cd food-waste-prediction
```

Install the required libraries:

```bash
pip install -r requirements.txt
```

## How to Run

Run the program from the project directory:

```bash
python src/main.py
```

The program will display:

- Dataset preview
- Dataset information
- Model accuracy
- Decision Tree visualization
- Prediction result for new input data

## Prediction Example

The model can classify new supermarket stock conditions into:

```text
Safe
```

or:

```text
Potentially Wasted
```

## Future Development

This project can be further improved by:

- Using real supermarket sales data
- Adding more relevant features
- Comparing different machine learning algorithms
- Developing a web-based prediction interface

## SDG Contribution

This project supports **Sustainable Development Goal 12: Responsible Consumption and Production** by exploring how Artificial Intelligence can help improve stock management and reduce potential food waste.
