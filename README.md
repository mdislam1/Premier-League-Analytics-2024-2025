# Premier League Performance Analysis: 2024-2025 Season

## Overview
This project provides a comprehensive statistical and visual analysis of team performance in the Premier League during the 2024-2025 season. Leveraging advanced metrics such as expected goals (xG), goal difference, win percentages, and form trends, the study uncovers key insights into team strengths, weaknesses, and overall competitiveness. The analysis is supported by intuitive visualizations, including heatmaps, scatter plots, and distribution charts, making it a valuable resource for football analysts, coaches, and enthusiasts.

---

## Dataset Description
The dataset contains the following key columns:
- **Basic Metrics**: `Rank`, `Team`, `Matches_Played`, `Wins`, `Draws`, `Losses`, `Goals_For`, `Goals_Against`, `Goal_Difference`, `Points`
- **Advanced Metrics**: `Expected_Goals`, `Expected_Goals_Against`, `Expected_Goal_Difference`, `xGD/90`
- **Form and Attendance**: `Last_Five_Matches`, `Attendance_Per_Game`, `Top_Scorer`, `Main_Goalkeeper`
- **Derived Metrics**: `Win_Percentage`, `Goal_Difference_Per_Match`, `xG_Efficiency`, `Form_Points`, `Top_Scorer_Contribution`

---

## Key Steps in the Analysis

### 1. **Data Loading and Exploration**
- Loaded the dataset from [FBref](https://fbref.com/en/comps/9/Premier-League-Stats#all_rank_key) using `pandas.read_html()`.
- Explored the dataset using methods like `.head()`, `.info()`, and `.describe()`.
- Checked for missing values and unique values in categorical columns.

### 2. **Data Cleaning and Transformation**
- Dropped unnecessary columns (e.g., `Notes`).
- Renamed columns for clarity and consistency.
- Standardized text data (e.g., team names) by removing spaces and special characters.
- Created new features such as:
  - `Win_Percentage`: Percentage of matches won.
  - `Goal_Difference_Per_Match`: Average goal difference per match.
  - `xG_Efficiency`: Ratio of goals scored to expected goals.
  - `Form_Points`: Points earned in the last five matches.

### 3. **Statistical Analysis**
- Calculated summary statistics for numerical columns.
- Analyzed correlations between variables using a correlation matrix.
- Ranked teams based on key metrics such as points, win percentage, and goal difference.

### 4. **Visualizations**
- **Distributions**: Histograms for `Points`, `Win_Percentage`, `Goal_Difference`, and `Expected_Goals`.
- **Correlation Heatmap**: Visualized relationships between numerical variables.
- **Scatter Plots**: Explored relationships between expected goals and points, as well as goal difference and win percentage.
- **Boxplots**: Compared key metrics by team tiers (Top, Mid, Bottom).

---

## Tools and Libraries
- **Python**: Primary programming language.
- **Pandas**: Data manipulation and analysis.
- **NumPy**: Numerical operations.
- **Matplotlib/Seaborn**: Data visualization.

---

## File Structure
```
premier-league-analysis/
├── data/
│   ├── premier_league_Raw.csv           # Raw dataset from FBref
│   └── premier_league_cleaned.csv       # Cleaned and preprocessed dataset
├── notebooks/
│   └── premier_league_analysis_2024_2025.ipynb    # Jupyter Notebook for analysis
└── README.md                            # Project documentation
```

---

## How to Run the Analysis
1. Clone the repository:
   ```bash
   git clone https://github.com/mdislam1/Premier-League-Performance-Analysis-2024-2025.git
   cd premier-league-analysis
   ```
2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```
3. Run the analysis script:
   ```bash
   python scripts/premier_league_analysis_2024_2025.ipynb
   ```
4. Check the output:
   - Cleaned data: `data/premier_league_cleaned.csv`
   - Visualizations: Displayed in the script output.

---

## Key Insights
- **Top Teams**: Liverpool and Arsenal lead in points and win percentage.
- **Goal Difference**: Liverpool has the highest goal difference, indicating strong offensive and defensive performance.
- **xG Efficiency**: Wolves and Nottingham Forest outperform their expected goals, showcasing efficient scoring.
- **Form Points**: Liverpool, Arsenal, and Everton have the highest recent form points.

---

## Future Enhancements
- Add machine learning models to predict team performance based on historical data.
- Integrate with cloud storage (e.g., AWS S3) for scalability.
- Automate the analysis pipeline using workflow management tools like Apache Airflow.

---

## Author
Md Islam
GitHub: https://github.com/mdislam1
