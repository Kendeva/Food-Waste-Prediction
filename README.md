# AI-Based Food Waste Prediction

An Artificial Intelligence project designed to help reduce potential food waste in urban supermarkets using a **Decision Tree Classifier**.

The system predicts whether food stock is classified as **Safe** or **Potentially Wasted** based on stock quantity, sales, weather conditions, holidays, and remaining stock.



## Features

- Load supermarket sales data from a CSV dataset
- Process stock, sales, weather, holiday, and remaining stock data
- Train a Decision Tree classification model
- Split the dataset into training and testing data
- Evaluate model accuracy
- Visualize the Decision Tree
- Predict new stock conditions
- Classify stock as **Safe** or **Potentially Wasted**

---

## Pipeline

```text
Dataset → Preprocessing → Train/Test Split → Decision Tree Training → Evaluation → Visualization → Prediction
```

---

## ML Model

| Model | Method |
|---|---|
| Food Waste Prediction | Decision Tree Classifier |

Model configuration:

- Criterion: `entropy`
- Maximum Depth: `4`
- Training Data: `80%`
- Testing Data: `20%`

The Decision Tree Classifier was selected because it is simple, easy to understand, suitable for small datasets, and provides a clear visualization of the decision-making process.

---

## Dataset

The project uses a **simulated dataset** designed to represent daily supermarket sales conditions.

| Feature | Description |
|---|---|
| `stok` | Available stock quantity |
| `terjual` | Number of items sold |
| `hari_ke` | Day index |
| `cuaca` | Weather condition |
| `hari_besar` | Holiday or special day indicator |
| `sisa_persen` | Remaining stock percentage |
| `label` | Stock condition label |

Prediction classes:

- `0` → Safe
- `1` → Potentially Wasted

---

## Results

The Decision Tree model achieved **100% accuracy** on the simulated testing dataset.

The result indicates that the simulated dataset has a highly consistent pattern that can be learned effectively by the model.

Based on the Decision Tree visualization, the most dominant variables in determining the prediction are:

- Remaining stock
- Items sold
- Weather condition

The model is also able to classify new input data that is not included in the training dataset.

---

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

---

## How to Run

```bash
# Install dependencies
pip install -r requirements.txt

# Run the program
python src/main.py
```

The program will display:

- Dataset preview
- Dataset information
- Model accuracy
- Decision Tree visualization
- Prediction result for new input data

---

## SDG Contribution

This project supports **Sustainable Development Goal 12: Responsible Consumption and Production**.

By predicting potential food waste, the system can support more efficient stock management, reduce food waste, save resources, and encourage more sustainable consumption.

---

## Limitations

- The dataset used in this project is simulated.
- The dataset is still relatively simple.
- The model has not yet been tested using real supermarket data.
- The current project only uses a Decision Tree Classifier.

---

## Future Development

- Use real supermarket sales data
- Add more relevant variables
- Test more complex machine learning algorithms
- Improve the system for real supermarket operational scenarios
