# Twitter-Credibility-Test-with-Big-Data
**Background**: The objective of this project is to identify whether Twitter can be considered a credible source of information, which reflects the emergence of important trends or topics in education.

**Data Source**: Approximately 100 Million Tweets about education are extracted from Twitter API from April 2022 to November 2022.

**Tools and Platform**: Performed on Google Cloud Platform, with PySpark (packages: `spark.sql` and `MLlib`, codes for `MLlib` will be updated at version 2.0), and Python (packages: `pandas`, `seaborn`, `numpy`, `scikit-learn`, `geopandas`, etc.)

## Structure
- Data preparation and cleaning
- EDA (Exploratory Data Analysis)
- Influential Analysis for usr account
- Location and Time-series Analysis
- Text Duplication Analysis with Jaccard Distance & LSH test on text similarity

## Preview
**Filtering & Cleanup**: We intentionally control the number of filtered tweets (about 7.4 million) by filtering topics such as **racial equality, literacy, tech & digital, special need, school curriculum, higher education** to see if the tweet reflect the trending real-world online discussion*. Also, only tweets in English (`lang=’en’`) are considered.


**Location Analysis**:
The geological distribution of tweets within our period of data collection indicate features (very-likely) caused by shocking news incidents of [the school shooting in 05/24/2022 at Robb Elementary School in Texas](https://www.texastribune.org/series/uvalde-texas-school-shooting/) had risen a huge online disgruntled in school gun control.
<div align=center>
<img width="800" height="400" src="https://github.com/hjiangAnthony/Twitter-Credibility-Test-with-Big-Data/blob/ec11073760e41060646c1cf2e1e48d31effc5a1c/IMAGE/figure%201.png"/>
</div>


**Time Analysis**
One of our findings is about time and the spike of tweet volume. Recall that we included certain heated topics while filtering the data and EDA. There is a obvious spike in the U.S.’s tweets in August, 2022. The corresponding news is that [the Biden Administration announced a $10 Billion student debt relief](https://www.ed.gov/news/press-releases/thanks-temporary-changes-us-department-education-announces-public-service-loan-forgiveness-surpasses-10-billion-debt-relief). This was a series of news announcements in August, which could explain part of the spike in tweets.

<div align=center>
<img width="775" height="250" src="https://github.com/hjiangAnthony/Twitter-Credibility-Test-with-Big-Data/blob/9abd31ddb97a1a19ccc02af00a8b5fd6288b0d5b/IMAGE/figure%202.png"/>
</div>


**LSH Similarity**
Given the limitation on and our selection (during data cleaning) of the tweets' length, this is a text similarity tes rather than topic modeling (LDA/LSA). It turned out that all organizations had a high percentage of unique tweets, which indicates that they are posting original content. News & Media had the least percentage of duplicate content, which indicates that they might be sharing similar education information. Schools and NGOs also have lower results of unique content.

<div align=center>
<img width="1200" height="400" src="https://github.com/hjiangAnthony/Twitter-Credibility-Test-with-Big-Data/blob/9abd31ddb97a1a19ccc02af00a8b5fd6288b0d5b/IMAGE/figure%203.png"/>
</div>

