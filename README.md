
# EuroSeasonTravel

## Project Overview
**EuroSeasonTravel** is a Data Analysis and Machine Learning project that predicts the best European countries to visit based on the season of travel. Utilizing the [European Tour Destinations Dataset](https://www.kaggle.com/datasets/faizadani/european-tour-destinations-dataset) from Kaggle, the project uses a **Random Forest** model to suggest travel destinations based on seasonal factors. Additionally, data preprocessing and visualization techniques were employed to gain insights into seasonal travel trends across Europe.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Description](#data-description)
- [Model Description](#model-description)
- [Installation](#installation)
- [Usage](#usage)
- [Visualizations](#visualizations)
- [Model Evaluation](#model-evaluation)
- [Contributing](#contributing)
- [License](#license)

## Data Description
The dataset used in this project comes from Kaggle's **European Tour Destinations Dataset**. It contains the following key columns:
- `Country`: The name of the country.
- `Region`: Geographical region of the destination.
- `Best Time to Visit`: The ideal time of year to visit, including multiple seasons.
- `Latitude` and `Longitude`: Geographical coordinates.
- `Cost of Living`: Indicator of how expensive it is to live or travel in the destination.
- `Majority Religion`, `Famous Foods`, `Language`, `Currency`: Various cultural and economic attributes.
- `Approximate Annual Tourists`: Number of tourists visiting annually.

During preprocessing, the `Best Time to Visit` column was transformed to extract individual seasons and create multiple rows for destinations with multiple seasons.

## Model Description
The project implements a **Random Forest Classifier** to predict the best country for a given season. The dataset was preprocessed by:
1. Handling missing values.
2. Encoding categorical features such as `Region`, `Currency`, and `Language` using One-Hot Encoding.
3. Scaling numeric features like `Latitude`, `Longitude`, and `Cost of Living`.
4. Dealing with destinations that offer the best time to visit during multiple seasons by splitting them into multiple rows.

The Random Forest model was trained on the processed dataset and then used to predict travel destinations based on the season.

### Model Features
- Random Forest Classifier with hyperparameter tuning.
- Input: Season name (`Spring`, `Summer`, `Fall`, `Winter`, or `Year-round`).
- Output: Predicted best countries to visit in the specified season.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/EuroSeasonTravel.git
   ```
2. Navigate to the project directory:
   ```bash
   cd EuroSeasonTravel
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Google Colab
If you prefer running the project in Google Colab:
1. Open [Google Colab](https://colab.research.google.com/).
2. Upload the notebook files from this repository.
3. Install the necessary dependencies as mentioned in the notebook.

## Usage
After installing the dependencies, you can run the model and get predictions for the best travel destinations based on the season:

1. **Run the model**:
   ```python
   season_to_predict = "Winter"
   predicted_countries = predict_best_countries(season_to_predict)
   print(predicted_countries)
   ```

2. **Predict Best Destinations**:
   - Input a season (e.g., `Winter`, `Summer`, `Spring`, or `Fall`) to get predictions of the best European countries to visit during that season.

## Visualizations
<div style="display: flex; flex-wrap: wrap;">
  <img src="https://github.com/user-attachments/assets/6f39fad2-9984-46eb-9775-cf633f067181" alt="plot1" style="width: 32%; margin-right: 1%;">
  <img src="https://github.com/user-attachments/assets/93ba6be1-6ccc-4836-981d-a0ddba665bc2" alt="plot2" style="width: 32%; margin-right: 1%;">
  <img src="https://github.com/user-attachments/assets/b230cba8-71ae-4448-8753-7130900d8629" alt="plot3" style="width: 32%;">
</div>
<div style="display: flex; flex-wrap: wrap; margin-top: 10px;">
  <img src="https://github.com/user-attachments/assets/42b08ec9-e834-4db7-ae16-2ac4ff18fb5a" alt="plot4" style="width: 32%; margin-right: 1%;">
  <img src="https://github.com/user-attachments/assets/035ee1f6-cbbc-4c00-a086-19b270251308" alt="plot5" style="width: 32%; margin-right: 1%;">
  <img src="https://github.com/user-attachments/assets/c894584c-7f21-42bc-84fc-dcceb18fd4fd" alt="plot6" style="width: 32%;">
</div>
<div style="display: flex; justify-content: center; margin-top: 10px;">
  <img src="https://github.com/user-attachments/assets/f3f7dad9-0d8c-42b7-b7a9-211756638475" alt="plot7" style="width: 32%;">
</div>




## Model Evaluation
The Random Forest model was evaluated using the following metrics:
- **Accuracy**: Overall percentage of correct predictions.
- **Precision, Recall, and F1-Score**: Performance on different categories of predictions, evaluated using a classification report.
  
You can find detailed evaluation results and graphs in the notebook.

## Contributing
If you'd like to contribute to this project, feel free to fork the repository and submit a pull request with improvements, additional features, or bug fixes.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
