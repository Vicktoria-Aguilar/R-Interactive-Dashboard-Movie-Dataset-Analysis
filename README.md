# TMDB Movie Dashboard
## Exploring Movie Profitability, Industry Trends, and Audience Ratings with Python and R

**Author:** Vicktoria Aguilar  
**Tools:** Python, R, ggplot2, dplyr, tidyverse, lubridate  
**Project:** Data Analytics Visualization  

## [![Launch Dashboard](https://img.shields.io/badge/Launch-Live%20Dashboard-blue?style=for-the-badge&logo=r)](https://9slkla-vicktoria0aguilar.shinyapps.io/tmdb_dashboard/)

### Interactive Dashboard

The dashboard includes six interactive sections:

- **Overview:** Explore the dataset using year and genre filters, with summary metrics for movie counts, audience ratings, budgets, and ROI.
- **Seasonality:** Compare average movie profitability by release month and weekday, including their intersection.
- **Industry Trends:** Examine annual movie release counts and audience ratings across frequently represented genres.
- **Profitability:** Explore production-budget ROI across studios, movies, and genres.
- **Ratings:** Investigate relationships between production budgets, runtime, and TMDB audience ratings.
- **Methodology:** Review data preparation, analytical definitions, assumptions, and limitations.

Interactive filters allow users to explore different year ranges and primary genres throughout the dashboard.

### Key Questions

- **Seasonality:** How does observed movie profitability vary by release month and weekday?
- **Industry Trends:** How have movie release volumes and audience ratings changed over time and across genres?
- **Profitability:** How does return on investment (ROI) vary across movies, genres, and production studios?
- **Audience Ratings:** What relationships are observable between production budgets, runtime, and audience ratings?

### Data Source

**Dataset:** TMDB Movies Dataset – Kaggle

The dataset contains movie metadata, including titles, release dates, genres, audience ratings, production budgets, revenue, runtime, and production companies.

Approximately one million records were initially considered. The data were cleaned and filtered to support the analyses, with the resulting dataset used in the interactive R Shiny application.

## Methodology

### 1. Data Preprocessing — Python

Python and pandas were used to prepare the raw dataset for analysis.

Preprocessing included:

- Standardizing column names and data types
- Removing duplicate movie IDs
- Parsing release dates and extracting release years
- Converting numerical variables to appropriate types
- Calculating movie profit as revenue minus production budget
- Filtering for released movies and valid numerical records
- Applying runtime and vote-count thresholds
- Removing records with missing values in key analytical fields
- Extracting primary genre and production company information for grouped comparisons
- Exporting the cleaned dataset to CSV for analysis in R

### 2. Exploratory Data Analysis — R

The cleaned dataset was analyzed using R and packages including tidyverse, dplyr, ggplot2, lubridate, and scales.

Analyses explored:

- Average profitability by release month and weekday
- Annual movie release volume and audience ratings by primary genre
- Movie and studio production-budget ROI
- Median ROI comparisons across genres
- Relationships between production budgets, runtime, and audience ratings

### 3. Interactive Visualization — Shiny and Plotly

The final dashboard was developed using R Shiny, bslib, ggplot2, and Plotly.

Interactive features include:

- Year-range and primary-genre filters
- Reactive summary metrics
- Interactive visualizations and hover details
- Genre, studio, and movie-level comparisons
- Methodology and limitations documentation

The dashboard is deployed using shinyapps.io.

## Selected Exploratory Findings

The initial exploratory analysis identified several patterns in the dataset:

- **Release timing:** Wednesday releases and May–June releases exhibited higher average profitability in the analyzed sample. These are observational differences and do not establish that release timing causes higher profits.
- **Industry trends:** Annual movie release counts increased substantially in later decades represented in the dataset. Comedy and Drama were frequently among the most represented primary genres.
- **ROI:** Production-budget ROI varied substantially across movies and genres. Horror films exhibited comparatively high median ROI in the initial analysis.
- **Audience ratings:** Production budget and runtime showed no strong apparent relationships with audience ratings in the visualized sample.

These findings are descriptive and depend on dataset coverage, filtering decisions, and reporting conventions. They should not be interpreted as causal effects or universal industry patterns.

## Analytical Definitions

**Profit:** revenue minus production budget (Profit = Revenue − Production Budget)

**Production-Budget ROI:** Profit divided by production budget (ROI = (Revenue − Production Budget) / Production Budget)
- ROI is calculated only where production budget is positive. It represents revenue relative to production budget, not complete financial profitability.

**Primary Genre and Production Company:** For grouped comparisons, the first listed genre and production company are used as the primary classifications. Movies with multiple genres or production companies may therefore be represented by only one category in these analyses.

## Limitations

- **Inflation:** Financial values are nominal and have not been adjusted for inflation, limiting direct comparisons across historical periods.
- **Incomplete recent data:** Recent years may be incompletely represented and should not be interpreted as definitive industry trends.
- **Selection bias:** Filtering by release status, vote counts, and availability of financial and rating information excludes some movies and may affect observed patterns.
- **Simplified profitability:** Revenue minus production budget excludes marketing, distribution, financing, and other costs. ROI should be interpreted as production-budget ROI rather than net profit or studio return.
- **Observational analysis:** Associations between release timing, budgets, genres, and outcomes do not establish causality.
- **Audience ratings:** TMDB ratings reflect users of the platform and may not represent the broader moviegoing population or professional critics.
- **Classification:** Using the first listed genre and production company simplifies comparisons but may not capture the full classification of each movie.

## Reproducibility

To run the dashboard locally:

- Clone or download this repository.
- Obtain the source dataset from Kaggle and place it in the designated data directory.
- Run the Python preprocessing script to generate the cleaned dataset.
- Ensure the resulting CSV is saved as data/TMDB_movies_clean.csv.
- Install the required R packages.
- Open the project in RStudio and run app.R.

The deployed dashboard uses the cleaned CSV included in the project. Refer to the source files for preprocessing and analytical implementation details.

## Future Work

Potential extensions include:

- Inflation-adjusted profitability analysis
- Statistical hypothesis testing of observed release-day and seasonal differences
- Regression modeling to examine associations between budget, genre, release timing, and financial outcomes
- Robustness checks across alternative vote-count thresholds and time periods
- Improved handling of missing data and potential selection bias
- More detailed analysis of genre combinations and multiple production companies
- Incorporating additional financial or industry data to improve profitability estimates

## Acknowledgments

Dataset provided by the TMDB Movies Dataset contributor on Kaggle. This is an independent educational data analytics project and is not affiliated with TMDB.

## Acknowledgments

Dataset provided by the TMDB Movies Dataset contributor on Kaggle. This is an independent educational data analytics project and is not affiliated with TMDB.
