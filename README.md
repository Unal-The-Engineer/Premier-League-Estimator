# ⚽️ Premier League Estimator 🏆

![Premier League Logo](https://upload.wikimedia.org/wikipedia/en/f/f2/Premier_League_Logo.svg)

---

## 🌟 About the Project

**Premier League Estimator** is a data-driven tool designed to predict football match outcomes. By integrating historical data, player ratings, and recent team performance, it offers insights into upcoming matches in the Premier League.

### Key Features 📝

- 🏟 **Team Analysis**: Calculates match outcomes based on team statistics.
- 🌟 **Player Ratings**: Utilizes player SofaScore ratings to assess team strength.
- 📊 **Recent Form Integration**: Accounts for the last 5 matches to determine current performance trends.
- 🛠 **Customizable Weights**: Adjust weights for player ratings, team form, and model predictions to optimize results.

---

## 📂 Project Structure

```plaintext
Premier-League-Estimator/
├── data/             # Contains datasets like player ratings and team form.
├── notebooks/        # Jupyter notebooks for data processing and model training.
├── README.md         # This project documentation.
```

---

## 🚀 How It Works

1. **Data Loading**: Historical match data, player ratings, and team form data are loaded from `.csv` files.
2. **Data Preprocessing**: Handles missing values, encodes categorical variables, and creates team-based statistics.
3. **Model Training**: Trains a Gradient Boosted Trees model using TensorFlow Decision Forests.
4. **Prediction**: Combines model predictions with player ratings and team form to provide probabilistic match outcomes.

---

## 🛠 Setup Instructions

Follow these steps to set up the project on your local machine:

### Prerequisites

- 🐍 Python 3.8 or higher
- 📦 Libraries:
  - `tensorflow_decision_forests`
  - `pandas`
  - `numpy`
  - `openpyxl`

### Installation Steps

1. Clone the repository:

    ```bash
    git clone https://github.com/yourusername/Premier-League-Estimator.git
    ```

2. Navigate to the project directory:

    ```bash
    cd Premier-League-Estimator
    ```

3. Create and activate a virtual environment:

    ```bash
    python -m venv venv
    source venv/bin/activate   # On Windows: venv\Scripts\activate
    ```

4. Install the required libraries:

    ```bash
    pip install -r requirements.txt
    ```

5. Run the Jupyter Notebook:

    ```bash
    jupyter notebook notebooks/Premier_League_Estimator.ipynb
    ```

---

## 📊 Data Sources

1. **Historical Match Data**: Match statistics scraped using `BeautifulSoup` and preprocessed for analysis.
2. **Player Ratings**: SofaScore player ratings stored in `data/sofascore_ratings.csv`.
3. **Recent Form Data**: Team form data stored in `data/last_5_matches.csv`.

---

## 🔮 Prediction Workflow

1. Input team names and their respective player lists.
2. Calculate:
   - Average player ratings.
   - Team form values.
3. Combine with model predictions using predefined weights.
4. Output probabilities for:
   - Home team win 🎉
   - Draw 🤝
   - Away team win 🛡

---

## 🧪 Example Output

```
Enter the Home Team: Arsenal
Enter player names for Arsenal (11 players):
Player 1: Bukayo Saka
Player 2: Gabriel Jesus
...
Player 11: Aaron Ramsdale

Enter the Away Team: Manchester City
Enter player names for Manchester City (11 players):
Player 1: Kevin De Bruyne
Player 2: Erling Haaland
...
Player 11: Ederson

Final Prediction Results:
Home Win Probability: 0.45
Draw Probability: 0.30
Away Win Probability: 0.25
```

---

## ⚙️ Customization

Adjust the weights for prediction components in the code:

```python
SOFASCORE_WEIGHT = 0.4
FORM_WEIGHT = 0.3
MODEL_WEIGHT = 0.3
```

---

## 🛡 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## 🤝 Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

---

## 📧 Contact

- Name: Ünal Büyükköroğlu
- Email: ubuyukkoroglu.26@gmail.com

---

### ⭐️ Acknowledgments

- SofaScore for player ratings.
- TensorFlow Decision Forests for the machine learning framework.
- BeautifulSoup for web scraping data.

---