# Exploratory Data Analytics of Movie Datasets

![Image](https://raw.githubusercontent.com/waihiga9/Phase1_Project/main/Image.jpeg)

## Project Overview

As a data scientist,I have been tasked by **Microsoft** to conduct an **exploratory data analysis** (EDA) to generate insights on the movie industry. The project involves analyzing datasets to provide insights and recommendations.

## Business Problem

Microsoft sees all the big companies creating original video content and they want to get in on the fun. They have decided to create a new movie studio, but they don’t know anything about creating movies. In this project I will be exploring what types of films are currently doing the best at the box office. Additionally i'll translate the findings into actionable insights that the head of Microsoft's new movie studio can use to help decide what type of films to create.

## Data Understanding and Analysis

### Source of Data
In the folder `Data` are movie datasets from:

* [Box Office Mojo](https://www.boxofficemojo.com/)
* [IMDB](https://www.imdb.com/)
* [Rotten Tomatoes](https://www.rottentomatoes.com/)
* [TheMovieDB](https://www.themoviedb.org/)
* [The Numbers](https://www.the-numbers.com/)

### Data Description

Because it was collected from various locations, the different files have different formats. Some are compressed CSV (comma-separated values) or TSV (tab-separated values) files that can be opened using spreadsheet software or `pd.read_csv`, while the data from IMDB is located in a SQLite database.

![movie data erd](https://raw.githubusercontent.com/waihiga9/Phase1_Project/main/movie_data_erd.jpeg)

The above diagram shows ONLY the IMDB data.

I decide to use the folowing data files:

* `Data/im.db`
  * SQLite database
  * I selected `movie_basics` and `movie_ratings` tables 
* `Data/tn.movie_budget.csv`
  * CSV file (loaded using `pd.read_csv`)

### The Visualization

Below are links to this project's Jupyter Notebook and the presentation

- ![notebook](link)
- ![presentation](link)
  
#### 1. What are top-rated popular genres?

Here, I considered 2 factors to generate insightful analysis on the genres.

- Number of movies produced per genre
  
  ![genre_frequency](link)

- Average number of votes per Genre
  
  ![votes_per_genre](link)

- **Average rate per Genre for genres with more than 4000 movies and 3000 average votes**
  
  ![average_rate](link)

Top-rated movie genres (above a rating of 6) with movies above 3000 and number of votes about 3000 are **Biography, Drama, Adventure, Romance, Crime and Comedy**. This could suggest that these genres are popular among movie audience and have a higher likelihood of being positively received by market.

#### 2. What is the correlation between Production Budget and Gross?

Examine if the movies with the highest budget generate the highest revenue.

  ![budget_gross](link)

The above correlation coefficients and the scatter plot indicate a ***moderately strong positive correlation*** between the production budget and both measures of gross.  This analysis argues that **movies with a higher production budget tend to earn more gross income.**

#### 3. What is the trend of the Production Budget throughout the years?

Time series graph of the yearly budget.

  ![production_budget](link)

There is an **increasing trend of production budgets** in the film industry.

#### 4. Is there a seasonality trend of the release dates? When is the best time to release a movie?

Time series graph of the monthly gross

  ![gross](link)

It appears that the gross income for movies tends to be **higher during the mid months of the year**, which could correspond to the **summer period of the northern hemisphere**.

#### 5. What is the difference between Domestic Gross and Worldwide Gross?

  ![diff_gross](link)

It is evident that **movies performed well in a global market**. This could indicate that the most movies had a broad appeal that could be successful in multiple regions.

## Summary

In conclusion, we have have done the following:

- identified most popular genres 
- investigated the role of production budget in the success of movies
- analyzed production budget trend
- explored how release dates can affect revenue and
- examined domestic versus global revenue

### Recommendations

Based on the analysis this is what I would recommend:
- Explore the possibility of creating films within the genres of Biography, Drama, Adventure, Romance, Crime, and Comedy.
- Invest a substantial amount of funds in the production budget.
- Increase the production budget allocation for high-quality movie production compared to previous years.
- Consider releasing the movies during the mid months of the year, particularly in the summer months.
- Produce globally appealing movies and market them to international audiences.
