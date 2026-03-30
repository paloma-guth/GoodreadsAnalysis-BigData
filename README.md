# Goodreads Books Analysis: Sentiment & Complex Networks

## Project Overview
This project was a collaborative exploration by two students for a "Computational Analysis of Big Data" course. Using a custom-scraped dataset of approximately 4,000 titles from 1960–2024, we investigated the relationships between book features (like genre and author), reader sentiment in reviews, and the structural connections between books as a complex network

## Key Research Questions
1.**Network Modeling:** How can books be modeled as complex networks based on shared features like genre and author, and what does this reveal about literary structures? <br>
2.**Sentiment vs. Ratings:** Does the emotional tone of user reviews actually correlate with the 1-5 star rating of a book? 

## Methodology
- **Data Collection:** Because of high missing values in existing Kaggle sets, we built a custom scraper using ISBNs and titles to gather metadata and the top four user comments for each book
- **Sentiment Analysis:** We used the **VADER** tool to process reader comments, comparing "clean" vs. "raw" text pipelines to find the most consistent results.
- **Complex Network Analysis:** We applied the **Louvain community algorithm** to find clusters of genres and authors who frequently overlap.
- **Statistical Testing:** We used ANOVA and log-transformations to handle outliers and verify if our findings (like genre-based differences) were statistically significant.

## Key Findings
- **Genre & Sentiment:** Romance reviews tend to have more positive sentiment, while Mystery/Thriller reviews skew more negative. However, the correlation between sentiment and star rating is surprisingly weak, suggesting ratings don't capture the full emotional tone of a review.
- **Genre Overlap:** Most books are tagged with multiple genres. Our network analysis showed that "Politics" and "Children’s" genres often act as "bridges" (high betweenness centrality) connecting different parts of the literary world.
- **Author Communities:** We were able to build a recommendation system based on author communities, identifying authors who write in similar genre clusters (e.g., Stephen King's extensive multi-genre bibliography).

## Datasets & Final Report

Due to file size restrictions on GitHub's web uploader (>25MB), the primary datasets used in this analysis are hosted on Google Drive.

* **[Download Raw Metadata & Comments (45MB)](https://drive.google.com/file/d/19ioD5u37lvmnbggQQDZvMeU9kh8wtbS5/view?usp=sharing)**: The initial scraped data including titles, ISBNs, and 16,000+ user comments.
* **[Download Cleaned Book Data (42.7MB)](https://drive.google.com/file/d/1E62IK066i-4imX7mqIZUjh73cXZIgXdX/view?usp=sharing)**: The filtered dataset used for VADER sentiment scoring and network modeling.
* **[Final Research Report (PDF)](https://drive.google.com/file/d/1KPhJhRNQXZiqeBQa5jw_U72Oi2T2bn34/view?usp=sharing)**: Our complete analysis, methodology, and visualization results.
