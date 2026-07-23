# Google Play Store Data Analysis

Exploratory data analysis of ~11,500 Google Play Store apps using Pandas and NumPy, focused on data cleaning, correlation analysis, and visualization.

## Project Structure

1. **Data Cleaning**
   - Converted `Installs`, `Price`, and `Size` from string to numeric types
   - Replaced `"Varies with device"` in `Size` with category-level median values
   - Filled missing `Rating` values using category-level medians
   - Converted `Last Updated` from string to proper datetime format
   - Mapped `In-App Purchases` and `Ad Supported` from Yes/No to boolean

2. **Analysis**
   Answered 20+ questions across several themes:
   - Ratings & popularity (top categories, top apps, reviews vs. rating)
   - Free vs. paid apps (pricing, ratings, installs)
   - Ads & in-app purchases (prevalence, overlap, category trends)
   - App size vs. rating
   - Content rating distribution
   - Update activity and maintenance trends over time
   - Android version requirements vs. rating

3. **Visualization**
   Scatter plots, bar charts, and pivot tables used to explore and confirm relationships found during analysis.

## Key Findings

- **Reviews don't predict rating.** Correlation between number of reviews and rating is essentially 0 — popularity and perceived quality appear unrelated.
- **App size has only a weak link to rating** (correlation ~0.15) — bigger apps are not meaningfully "better."
- **Minimum Android version doesn't affect rating.** Median rating stays flat (~4.0–4.2) regardless of the Android version required.
- **Update activity has grown sharply over time**, reflecting increasing developer activity in more recent years.
- **Category matters a lot** — in-app purchase prevalence, ad support, and update recency all vary widely depending on app category.

## Tools Used

- Python
- Pandas
- NumPy
- Matplotlib

## Dataset

`google_playstore_2026.csv` — Play Store app metadata including category, rating, reviews, installs, price, size, content rating, ad support, in-app purchases, and last updated date.

## How to Run

1. Clone this repository
2. Install dependencies: `pip install pandas numpy matplotlib`
3. Open `playstore_data.ipynb` in Jupyter Notebook or JupyterLab
4. Run all cells in order
