# Rainfall-Prediction
Rainfall Prediction with Random Forest Classifier &amp; Logistic Regression 
# Rainfall Prediction Classifier

A machine learning project that predicts whether it will rain today based on historical weather data from Australia. This project implements and compares two classification algorithms: Random Forest and Logistic Regression.

## 📋 Project Overview

This project uses weather data from the Australian Government's Bureau of Meteorology to build predictive models for rainfall prediction. The dataset contains observations from 2008 to 2017 with various meteorological features.

### Key Features
- **Data preprocessing**: Feature engineering including seasonal categorization
- **Model comparison**: Random Forest vs Logistic Regression
- **Hyperparameter optimization**: Grid search with cross-validation
- **Performance evaluation**: Comprehensive metrics and visualizations
- **Feature importance analysis**: Understanding which weather factors matter most

## 🎯 Objectives

- Explore and perform feature engineering on real-world weather data
- Build robust classifier pipelines with preprocessing
- Optimize models using grid search cross-validation
- Evaluate model performance using various metrics
- Compare different classification algorithms
- Identify the most important weather features for rainfall prediction

## 📊 Dataset

The dataset contains weather observations with the following features:

| Feature | Description | Unit | Type |
|---------|-------------|------|------|
| Date | Date of observation | YYYY-MM-DD | Date |
| Location | Location of observation | - | Categorical |
| MinTemp | Minimum temperature | Celsius | Numerical |
| MaxTemp | Maximum temperature | Celsius | Numerical |
| Rainfall | Amount of rainfall | Millimeters | Numerical |
| Evaporation | Amount of evaporation | Millimeters | Numerical |
| Sunshine | Amount of bright sunshine | Hours | Numerical |
| WindGustDir | Direction of strongest gust | Compass Points | Categorical |
| WindGustSpeed | Speed of strongest gust | Kilometers/Hour | Numerical |
| WindDir9am/3pm | Wind direction at 9am/3pm | Compass Points | Categorical |
| WindSpeed9am/3pm | Wind speed at 9am/3pm | Kilometers/Hour | Numerical |
| Humidity9am/3pm | Humidity at 9am/3pm | Percent | Numerical |
| Pressure9am/3pm | Atmospheric pressure at 9am/3pm | Hectopascal | Numerical |
| Cloud9am/3pm | Cloud coverage at 9am/3pm | Eights | Numerical |
| Temp9am/3pm | Temperature at 9am/3pm | Celsius | Numerical |
| RainToday | Target variable | Yes/No | Binary |

**Data Source**: Australian Government's Bureau of Meteorology via Kaggle

## 🔧 Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/rainfall-prediction.git
cd rainfall-prediction
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

## 🚀 Usage

1. **Run the Jupyter Notebook**:
```bash
jupyter notebook RainFall.ipynb
```

2. **Execute all cells** to reproduce the complete analysis:
   - Data loading and exploration
   - Feature engineering and preprocessing
   - Model training and optimization
   - Performance evaluation and comparison

## 🧠 Models Implemented

### 1. Random Forest Classifier
- **Best Parameters**: 
  - n_estimators: 100
  - max_depth: None
  - min_samples_split: 2
- **Performance**: 84% accuracy on test set
- **Strengths**: Better recall for positive class, handles feature interactions well

### 2. Logistic Regression
- **Best Parameters**:
  - solver: liblinear
  - penalty: l1/l2 (optimized)
  - class_weight: balanced/None (optimized)
- **Performance**: 83% accuracy on test set
- **Strengths**: Faster training, good interpretability

## 📈 Results

### Model Performance Comparison

| Model | Accuracy | Precision (No Rain) | Recall (No Rain) | Precision (Rain) | Recall (Rain) |
|-------|----------|-------------------|-----------------|-----------------|---------------|
| Random Forest | 84% | 86% | 95% | 76% | 50% |
| Logistic Regression | 83% | 86% | 93% | 68% | 51% |

### Key Insights

1. **Most Important Features for Rainfall Prediction**:
   - Humidity levels (9am and 3pm)
   - Pressure readings
   - Cloud coverage
   - Temperature variations

2. **Model Observations**:
   - Both models show strong performance in predicting "No Rain" days
   - Random Forest slightly outperforms Logistic Regression
   - Class imbalance affects recall for rainy days (fewer rain samples)

3. **Geographic Focus**: Analysis focused on Melbourne area locations for consistency

## 📁 Project Structure

```
rainfall-prediction/
├── RainFall.ipynb          # Main analysis notebook
├── README.md               # Project documentation
├── requirements.txt        # Python dependencies
├── conclusion.md          # Detailed findings and insights
└── data/                  # Data directory (if local data used)
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Create a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Australian Government's Bureau of Meteorology for the weather data
- Kaggle for hosting the dataset
- Scikit-learn community for the excellent machine learning tools

## 📧 Contact

If you have any questions or suggestions, feel free to reach out or open an issue.

---

**Note**: This project is for educational and research purposes. For production weather forecasting, please consult professional meteorological services.
