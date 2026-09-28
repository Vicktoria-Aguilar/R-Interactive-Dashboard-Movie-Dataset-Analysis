# TMDB Movie Dataset Analysis
## Exploring Movie Profitability, Industry Trends, and Audience Ratings with Python and R

**Author:** Vicktoria Aguilar  
**Tools:** Python, R, ggplot2, dplyr, tidyverse, lubridate  
**Project:** Data Analytics Visualization  

View Interactive Dashboard · View Source Code

## Project Overview

This project explores trends in the global film industry using a large-scale TMDB movie dataset containing approximately one million records before data cleaning.

Using Python for data preprocessing and R for analysis and visualization, I investigated relationships between movie release timing, production budgets, profitability, genres, studio performance, and audience ratings.

The goal was to transform a large, heterogeneous dataset into an accessible analytical dashboard that communicates industry trends and supports exploratory investigation.

### Key Questions
- **Seasonality:** How are movie profitability patterns associated with release month and weekday?  
- **Industry Growth:** How have movie releases and audience ratings changed across genres and years?  
- **Profitability:** How does return on investment (ROI) vary by genre, movie, and studio?  
- **Audience Ratings:** What relationships exist between production budget, runtime, and audience ratings?  

### Dashboard

The analysis is organized into five sections:

**1. Seasonality:** Movie profitability by release month and weekday, including their intersection.  
**2. Industry Growth:** Annual movie releases and average ratings across leading genres, with representative top-rated titles.  
**3. Profitability:** Studio and movie ROI comparisons, alongside average ROI by genre.  
**4. Ratings:** Exploratory relationships between production budget, runtime, and audience ratings.  
**5. Conclusions:** Summary of observed patterns, limitations, and potential directions for further analysis.  

### Data Source

Dataset: [TMDB Movies Dataset – Kaggle]("https://www.kaggle.com/datasets/asaniczka/tmdb-movies-dataset-2023-930k-movies")

The dataset contains movie metadata, including titles, release dates, genres, ratings, production budgets, revenue, runtime, and studios.

Approximately one million records were initially considered. The dataset was cleaned and filtered to support the analyses.

### Methodology
#### 1. Data Preprocessing: Python and pandas were used to prepare the raw dataset for analysis

Preprocessing included:

- Standardizing column names
- Removing duplicate movie IDs
- Parsing release dates and extracting release years
- Converting numerical variables to appropriate types
- Calculating movie profit as revenue minus budget
- Filtering for released movies and valid numerical records
- Removing records with missing values in key analytical fields
- Extracting primary genre for genre-level comparisons
- Exporting the cleaned dataset to CSV for analysis in R

#### 2. Exploratory Data Analysis: The cleaned dataset was analyzed using R, with packages including tidyverse, dplyr, ggplot2, and lubridate

Analyses explored:

- Aggregated profitability by release month and weekday
- Annual release volume and average ratings by primary genre
- Movie and studio ROI
- Relationships between budget, runtime, and audience ratings

#### 3. Visualization and Reporting

Visualizations were developed to communicate trends across the dataset, including comparisons of profitability, genre-level patterns, and audience ratings.

The final HTML report combines visualizations, methodological notes, and interpretations in a single presentation.

### Selected Findings

The exploratory analysis identified several patterns in the dataset:

- **Release timing:** Wednesday releases and May–June releases had higher average profitability in the analyzed data. These are observational patterns and do not establish that release timing causes higher profits.
- **Industry growth:** Annual movie release counts increased substantially in the later decades represented in the dataset, with Comedy and Drama frequently appearing among the most represented genres.
- **ROI:** Profitability relative to budget varied substantially across movies and genres. Horror films showed comparatively high median ROI in the analyzed sample.
- **Audience ratings:** Budget and runtime did not show strong apparent relationships with audience ratings in the visualized data.

These findings are exploratory and depend on the dataset's coverage, filtering decisions, and reporting conventions.

### Limitations

- **Inflation:** Financial values are nominal and have not been adjusted for inflation, limiting direct comparisons across historical periods.
- **Incomplete recent data:** The most recent years in the dataset may be incomplete and should not be interpreted as definitive industry trends.
- **Selection bias:** Filtering on release status, vote counts, and availability of financial and rating information excludes some movies and may affect observed patterns.
- **ROI interpretation:** Revenue minus budget is a simplified profitability measure. It does not account for distribution costs, marketing expenses, or other financial considerations.
- **Observational analysis:** Associations between release timing, budgets, genres, and outcomes do not establish causality.
- **Audience ratings:** TMDB audience ratings reflect platform users and should not be treated as equivalent to professional critical assessments or representative audience surveys.

### Reproducibility

To reproduce the analysis:

1. Obtain the source dataset from Kaggle and place it in the designated data directory.
2. Install the Python dependencies listed in requirements.txt.
3. Run the Python preprocessing script to generate the cleaned CSV.
4. Install the required R packages and open the R Markdown analysis source.
5. Knit the R Markdown document to HTML to regenerate the report.

Exact execution instructions and package versions will be provided alongside the source scripts.

### Future Work

Potential extensions include:

- Inflation-adjusted profitability analysis
- Statistical hypothesis testing of observed release-day and seasonal differences
- Regression modeling to evaluate associations between budget, genre, release timing, and financial outcomes
- Robustness checks across different vote-count thresholds and time periods
- Improved handling of missing data and potential selection bias
- Interactive filtering and exploration through a deployed Shiny application

### Acknowledgments

Dataset provided by the TMDB Movies Dataset contributor on Kaggle. This is an independent educational data analytics project and is not affiliated with TMDB.
