
```markdown
# Miami GP 2025 Prediction Project

## Overview
This project is a data-driven attempt to predict the **qualifying times** and **race times** for the upcoming **2025 Miami Grand Prix**. As a passionate fan of Formula 1, I created this project to explore how historical data from previous races can be used to forecast future performance using machine learning models.

The project leverages the **FastF1** library to extract historical race and qualifying data, and uses **Gradient Boosting Regressors** from scikit-learn to make predictions. The results include predicted qualifying and race times for the 2025 Miami GP, along with rankings based on predicted race performance.

---

## Features
- **Data Extraction**: Uses the FastF1 library to fetch historical data for the 2024 Miami GP (qualifying and race sessions).
- **Qualifying Time Prediction**: Predicts qualifying times for the 2025 Miami GP using a machine learning model trained on historical qualifying data.
- **Race Time Prediction**: Predicts race lap times for the 2025 Miami GP using predicted qualifying times as input.
- **Driver Rankings**: Ranks drivers based on their predicted race times.
- **Model Evaluation**: Evaluates the performance of the machine learning models using Mean Absolute Error (MAE).

---

## Project Workflow
1. **Data Collection**:
   - Historical data for the 2024 Miami GP is fetched using the FastF1 library.
   - Data includes lap times for both qualifying and race sessions.

2. **Data Preprocessing**:
   - Lap times are converted to seconds for easier numerical processing.
   - Qualifying and race data are merged to create a unified dataset for training.

3. **Model Training**:
   - A **Gradient Boosting Regressor** is trained to predict qualifying times based on historical qualifying data.
   - A second **Gradient Boosting Regressor** is trained to predict race times using qualifying times as input.

4. **Prediction**:
   - The trained models are used to predict qualifying and race times for the 2025 Miami GP.
   - Predictions are made for a predefined list of drivers.

5. **Driver Rankings**:
   - Drivers are ranked based on their predicted race times.

6. **Model Evaluation**:
   - The performance of the qualifying prediction model is evaluated using Mean Absolute Error (MAE).

---

## Installation

### Prerequisites
- Python 3.9 or higher
- Virtual environment (recommended)
- Libraries:
  - `fastf1`
  - `pandas`
  - `numpy`
  - `scikit-learn`

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/MiamiGP2025Prediction.git
   cd MiamiGP2025Prediction
   ```

2. Create and activate a virtual environment:
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate  # On macOS/Linux
   .venv\Scripts\activate     # On Windows
   ```

3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the script:
   ```bash
   python3 MiamiPrediction2025.py
   ```

---

## Usage
1. **Run the Script**:
   - The script will fetch historical data, train the models, and output the predictions for the 2025 Miami GP.

2. **Output**:
   - Predicted qualifying times for each driver.
   - Predicted race times for each driver.
   - Rankings based on predicted race times.

3. **Example Output**:
   ```
   🏁 Predicted 2025 Miami GP Results 🏁

         Driver           QualifyingTime (s)    PredictedRaceTime (s)
   1     Max Verstappen   78.12                 90.45
   2     Charles Leclerc  78.45                 90.78
   3     Lewis Hamilton   78.67                 91.12
   ...
   ```

---

## File Structure
```
MiamiGP2025Prediction/
├── MiamiPrediction2025.py   # Main script for predictions
├── f1_cache/                # Cache directory for FastF1 data
├── requirements.txt         # List of dependencies
└── README.md                # Project documentation
```

---

## Models
### Qualifying Prediction Model
- **Algorithm**: Gradient Boosting Regressor
- **Input Features**: Historical qualifying times
- **Target**: Qualifying times for the 2025 Miami GP
- **Evaluation Metric**: Mean Absolute Error (MAE)

### Race Prediction Model
- **Algorithm**: Gradient Boosting Regressor
- **Input Features**: Predicted qualifying times
- **Target**: Race lap times for the 2025 Miami GP
- **Evaluation Metric**: Mean Absolute Error (MAE)

---

## Data Sources
- **FastF1 Library**: Provides historical Formula 1 data, including lap times, driver information, and session details.
- **2024 Miami GP**: Used as the primary dataset for training the models.

---

## Limitations
- **Data Availability**: Predictions are based on historical data, which may not fully capture future race conditions (e.g., weather, track changes, car upgrades).
- **Simplified Features**: The models use only lap times as features, without considering other factors like tire strategy, pit stops, or weather conditions.

---

## Future Improvements
- Incorporate additional features such as weather data, tire strategies, and car performance metrics.
- Use data from multiple races to improve model generalization.
- Explore advanced machine learning models like neural networks for better predictions.

---

## Acknowledgments
- **FastF1 Library**: For providing easy access to Formula 1 data.
- **Scikit-learn**: For the machine learning tools used in this project.
- **Formula 1 Community**: For inspiring this project as a fan-driven initiative.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Contact
If you have any questions or suggestions, feel free to reach out:
- **Name**: Bharat Garsondiya
- **Email**: contact@bharatgarsondiya.me
- **GitHub**: [yourusername](https://github.com/bharatpatel7)
```
