# Digit Classifier with Data Augmentation and Model Training

This project focuses on building a digit classifier using the MNIST dataset. It includes data augmentation techniques to expand the dataset, preprocessing steps, and model training using Random Forest and K-Nearest Neighbors (KNN) classifiers. The goal is to achieve high accuracy in classifying handwritten digits.

---

## Features

- **MNIST Dataset**: Utilizes the MNIST dataset containing 70,000 images of handwritten digits (0-9).
- **Data Augmentation**: Expands the dataset by shifting images in four directions (up, down, left, right).
- **Model Training**: Trains models using Random Forest and K-Nearest Neighbors (KNN) classifiers.
- **Cross-Validation**: Evaluates model performance using cross-validation.
- **Grid Search**: Optimizes hyperparameters for the KNN classifier using GridSearchCV.

---

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/digit-classifier.git
   cd digit-classifier
   ```

2. **Set up a virtual environment** (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the script**:
   ```bash
   python digit_classifier.py
   ```

---

## Workflow

### 1. **Data Loading and Preprocessing**
   - Load the MNIST dataset using `fetch_openml`.
   - Reshape the data into 28x28 pixel images.

### 2. **Data Augmentation**
   - Expand the dataset by shifting images in four directions:
     - Shift Up
     - Shift Down
     - Shift Left
     - Shift Right
   - The augmented dataset increases from 70,000 to 350,000 samples.

### 3. **Data Splitting**
   - Split the augmented dataset into training and testing sets using an 80-20 split.

### 4. **Model Training**
   - Train two models:
     - Random Forest Classifier (`RandomForestClassifier`)
     - K-Nearest Neighbors Classifier (`KNeighborsClassifier`)
   - Evaluate model performance using cross-validation.

### 5. **Hyperparameter Tuning**
   - Use `GridSearchCV` to find the best hyperparameters for the KNN classifier.

### 6. **Testing**
   - Evaluate the final model on the test dataset and calculate accuracy.

---

## Code Structure

```plaintext
digit-classifier/
├── digit_classifier.py       # Main script for data loading, augmentation, and model training
├── requirements.txt          # List of dependencies
└── README.md                 # Project documentation
```

---

## Dependencies

- Python 3.8+
- `scikit-learn` for machine learning models and utilities
- `numpy` for numerical operations
- `pandas` for data manipulation
- `matplotlib` for visualization

---

## Results

- **Random Forest Classifier**:
  - Cross-validation accuracy: ~97.3%
- **K-Nearest Neighbors Classifier**:
  - Cross-validation accuracy: To be evaluated after hyperparameter tuning.

---

## Contributing

Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes.
4. Submit a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Build and train your own digit classifier with ease! 🚀🔢
