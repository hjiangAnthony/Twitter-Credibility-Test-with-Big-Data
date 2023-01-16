# Twitter-Credibility-Test-with-Big-Data
**Background**: The objective of this project is to identify whether Twitter can be considered a credible source of information, which reflects the emergence of important trends or topics in education.

**Data Source**: Approximately 100 Million Tweets about education are extracted from Twitter API from April 2022 to November 2022.

**Tools and Platform**: Performed on Google Cloud Platform, with PySpark (packages: `spark.sql` and `MLlib`, codes for `MLlib` will be updated at version 2.0), and Python (packages: `pandas`, `seaborn`, `numpy`, `geopandas`, etc.),

## Structure
- Data preparation and cleaning
- EDA (Exploratory Data Analysis)
- Influential Analysis for usr account
- Location and Time-series Analysis
- Text Duplication Analysis with LSH text similarity test

## Preview
**Filtering & Cleanup**: We intentionally control the number of filtered tweets (about 7.4 million) by filtering topics such as **racial equality, literacy, tech & digital, special need, school curriculum, higher education** to see if the tweet reflect the trending real-world online discussion*. Also, only tweets in English (`lang=’en’`) are considered
1
