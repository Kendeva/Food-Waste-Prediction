# AI-Based Food Waste Prediction

A simple Artificial Intelligence project that uses a **Decision Tree Classifier** to predict potential food waste in supermarkets.

The model analyzes supermarket sales data and supporting factors such as stock quantity, items sold, weather conditions, holidays, and remaining stock percentage to classify stock as **Safe** or **Potential Waste**.

## Project Overview

Food waste can occur when supermarket stock does not match actual customer demand. This project applies a basic machine learning approach to identify stock conditions that may lead to food waste and support better inventory decisions.

## Features

- Loads supermarket sales data from a CSV file
- Splits the dataset into training and testing data
- Trains a Decision Tree classification model
- Evaluates model accuracy
- Visualizes the trained Decision Tree
- Predicts the status of new stock data

## Dataset Features

The model uses the following input features:

| Feature | Description |
| --- | --- |
| `stok` | Total stock available |
| `terjual` | Number of products sold |
| `hari_ke` | Day index |
| `cuaca` | Weather condition represented numerically |
| `hari_besar` | Holiday or special-day indicator |
| `sisa_persen` | Remaining stock percentage |
| `label` | Classification target |

Target labels:

- `0` = Safe
- `1` = Potential Waste

## Machine Learning Model

The project uses a **Decision Tree Classifier** with the following configuration:

```python
DecisionTreeClassifier(
    criterion="entropy",
    max_depth=4,
    random_state=42
)
```

The dataset is divided into:

- **80% training data**
- **20% testing data**

## Project Structure

```text
food-waste-prediction/
├── data/
│   └── README.md
├── docs/
│   └── AI-Food-Waste-Report.pdf
├── images/
│   └── .gitkeep
├── src/
│   └── main.py
├── .gitignore
├── README.md
└── requirements.txt
```

> The original `data_penjualan.csv` dataset is not included because it was not available in the uploaded project files. Add it to the `data/` directory before running the program.

## Requirements

- Python 3.9 or newer
- Pandas
- Scikit-learn
- Matplotlib

Install the required libraries with:

```bash
pip install -r requirements.txt
```

## How to Run

1. Place the dataset in:

```text
data/data_penjualan.csv
```

2. Run the program from the project root:

```bash
python src/main.py
```

3. The program will display:

- The first five rows of the dataset
- Dataset information
- Model accuracy
- Decision Tree visualization
- Prediction result for a sample input

The generated Decision Tree image will also be saved as:

```text
images/decision_tree.png
```

## Technologies Used

- Python
- Pandas
- Scikit-learn
- Matplotlib

## Project Purpose

This project demonstrates a simple application of Artificial Intelligence for supermarket inventory management and food waste reduction. It also supports the idea of **Responsible Consumption and Production (SDG 12)** by encouraging more efficient stock management.

## Future Improvements

Possible improvements include:

- Using real supermarket sales data
- Adding more relevant features
- Comparing multiple machine learning algorithms
- Improving model evaluation with additional metrics
- Building a web-based interface for easier prediction input

## Documentation

The full academic report is available in the `docs/` folder.
