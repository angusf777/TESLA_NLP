# FINA4350 Project

This project contains Jupyter notebooks and scripts for financial and news sentiment analysis, focusing on Tesla sales and related news. The analysis includes data cleaning, feature engineering, sentiment analysis (VADER and Transformers), and the relationship between news sentiment and sales.

---

## Project Structure

- **FINA4350_project.ipynb**  
  Main notebook for financial data analysis and modeling, including Random Forest and LSTM models.

- **news_analysis.ipynb**  
  Jupyter notebook for in-depth news data analysis, including:
  - Data loading and cleaning
  - Feature engineering
  - Sentiment analysis using VADER and Transformers
  - Visualization of sentiment and sales relationships
  - Saving and loading of sentiment results

- **requirements.txt**  
  List of Python package dependencies.

- **data/**  
  Directory containing raw and processed data files:
  - `tesla_sales.csv`: Monthly Tesla sales data.
  - `news.csv`: News articles related to Tesla.
  - `tesla_2018_to_2020.csv`: (Large) Tesla data for 2018-2020.

- **results/**  
  Directory for generated sentiment analysis results:
  - `vader_sentiment_analysis_<timestamp>.csv`: VADER sentiment results.
  - `transformers_sentiment_analysis_<timestamp>.csv`: Transformers sentiment results (if present).

- **graphs/**  
  Directory for saving generated plots and figures (currently empty or for user output).

- **.venv/**  
  Python virtual environment directory (created after setup).

---

## Usage

1. **Setup the environment:**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # or .venv\Scripts\activate on Windows
   pip install -r requirements.txt
   ```

2. **Run the analysis:**
   - Open `FINA4350_project.ipynb` or `news_analysis.ipynb` in Jupyter Notebook.
   - Follow the notebook instructions to run data analysis and generate results.

3. **Sentiment Analysis Results:**
   - Results are saved in the `results/` directory with method-specific filenames.
   - Use the provided loading functions in the notebook to access the latest results for VADER or Transformers.
   - Moving averages for sales are computed on the full available data before merging with sentiment, ensuring correct alignment and early-month coverage.

---

## Dependencies

- pandas, numpy, matplotlib, seaborn
- scikit-learn, tensorflow, xgboost
- wordcloud, nltk, vaderSentiment
- jupyter, kagglehub, transformers (for advanced sentiment analysis)

---

## Notes

- Ensure Python 3.8+ is installed.
- Use the virtual environment to avoid package conflicts.
- Some data files (e.g., `tesla_2018_to_2020.csv`) are large and may not be needed for all analyses.
- Sentiment results are saved with timestamps for reproducibility.
- All data alignment and moving average calculations are performed before merging with sentiment data for accurate analysis.

---

## License

[Your license information here] 