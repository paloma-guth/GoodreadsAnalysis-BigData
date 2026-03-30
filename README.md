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
