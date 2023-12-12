# Data-Science-Project
Data-Driven Taxi-Fare Prediction based on Weather Condition

## Background and Motivation
Considering the recent criticisms faced by ride-hailing services, such as Uber and Lyft, for surging fare prices during a flash flood emergency in NYC, underscores the broader impact of weather on transportation costs. This scrutiny serves as motivation for our inquiry into whether similar patterns exist within the traditional Yellow Taxi system. Motivated by observed impacts on ride-hailing prices and our intuitive sense that Yellow Taxi fares are similarly affected by weather conditions, this research seeks to unravel the intricate relationships between weather and taxi fares. By scrutinizing comprehensive datasets from the NYC Yellow Taxi Dataset and Weather Dataset and leveraging machine learning models, we aim to contribute to a more nuanced understanding of fare dynamics in the face of adverse weather conditions, ultimately benefiting both taxi service providers and consumers. Detailed version of it is illustrated in final project report.

- Taget variable (Y) = Average Yellow Taxi Fare per Day Ride

- Features (X) = Average temperature, average precipitation, average snow, weather icon and trip distance


## Dataset Description
The dataset is comprehensively described, including its types and details in the final project report. We utilized two datasets, namely the Yellow Taxi Dataset and the Weather Dataset, covering the period from January 1st, 2022, to December 31st, 2022. The Yellow Taxi Dataset is collected from NYC Taxi and Limousine Commission (TLC) and The weather data is collected from Visual Crossing which is a leading provider of weather data. The Weather Dataset has (365, 33) dimension, and Yellow Taxi Dataset has (39656098, 19) dimension. The links can be found as below:

[1] TLC Trip Record Data - TLC. (n.d.). Www.nyc.gov. https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page

[2] Weather Data Services | Visual Crossing. (n.d.). Www.visualcrossing.com. https://www.visualcrossing.com/weather/weather-data-services

Detailed description of datasets can be found in the final project report.

## Methodology
## Step 1. Data Preprocessing
- Downsample 5% of the datasets
- Dropping irrelevant and duplicate columns
- Integration between Yellow Taxi Dataset and Weather Dataset
- Feature Alignment: Converting the temporal features into 'datetime'
- One-Hot-Encoding: 'icon' feature

## Step 2. Correlation Heatmap (Pearson Correlation Coefficients)
- Correlation Heatmap generation: Target variable & All features
- Correlation Heatmap generation: Target variable & Selected features
- Correlation Heatmap generation: Target variable & icon feature

## Step 3. Statistical Analysis
- Drop the samples where 'total_amount' < 0
- See the detailed statistical description for each variable

## Step 4. Graphical Representation: Histogram Plot
- Plot the Histograms for each variable
- Determine the suitable categorization for each variable before implementing ML
- Ordinal Encoding: Categorize each variable for ML implementation

## Step 5. Machine Learning Implementation
- Decision Tree on Binary Classification:
      - Evaluation metric: Accuracy, Confusion Matrix, AUCROC
- Decision Tree on Multiclass Classification: Accuracy, Confusion Matrix
      - Evaluation metric: Accuracy, Confusion Matrix
- Random Forest Tree on Multiclass Classification: Accuracy, Confusion Matrix
      - Evaluation metric: Accuracy, Confusion Matrix
      - Hyper parameter tuning: GridSearchCV = (n_estimators = 200, max_depth = None, min_samples_split = 2, min_samples_leaf = 1)
- Deep Learning: Recurrent Neural Network (RNN): Accuracy
      - Evaluation metric: Accuracy
      - Batch Size = 64, Input Layer = 4, Hidden Layer = 32, Output Layer = 3, #epochs = 5, Loss = Cross Entropy Loss, Optimizer = Adam, Learning Rate = 0.001

## Step 6. Conclusion: Correlation between Taxi-Fare and Weather Condition
- Histogram Plot
- Interpretation

Detailed explanation of these steps are illustrated in code and final project report.

