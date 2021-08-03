# Module 08 Challenge - Movies-ETL Refactored

## Overview

The purpose of this project is to create an automated ETL (Extract, Transform, Load) Pipeline
to be used for daily database updates for Amazing Prime.

The completed Pipeline will take in new data, perform the appropriate
transformations, and load the data into existing SQL Tables.

It is refactored from previous code that accomplished a similar task
using separate functions.

Here, the process will be completed from within one single Function.

### Resources

- Software:
	- PostgreSQL 11 (Input/Output, and Queries processed via pgAdmin 4)
	- Jupyter notebook server 6.3.0, running Python 3.7.10 64-bit (Dependencies: json, numpy, os, pandas, psycopg2, re, sqlalchemy[create_engine], sys, time)
- Data: Provided by Amazing Prime, and retrieved from external sources. Retrieved and saved to disk July 24, 2021:
	`wikipedia-movies.json`
	`movies_metadata.csv`
	`ratings.csv`

Note that `wikipedia-movies.json` and `movies_metadata.csv` are hosted for reference here on GitHub in their original unmodified form under `./Resources`. `ratings.csv` is omitted in the interest of conserving disk space, but is freely available for direct download from the web resources listed below.


Additional information about these resources is outlined below in Table 1.

**Table 1:**
| File Name                   | Brief Description of Contents |
|-----------------------------|-------------------------------|
| `wikipedia-movies.json`     |Amazing Prime Internal Script scraped a list of movies from [Wikipedia](https://en.wikipedia.org/wiki/Main_Page) released between 1990 and 2018 and extracted the data from the sidebar into a JSON. Original script lost, run date unknown, JSON retained. 7,311 entries listed in raw form.|
| `movies_metadata.csv`       |Movies Metadata from GroupLens Research Group at the University of Minnesota ([MovieLens Website](https://movielens.org/)). Details about the movies retrieved from The Movie Database ([TMDb](https://www.themoviedb.org/?language=en-US)). Dataset hosted and downloaded from [Kaggle](https://www.kaggle.com/). 24 Fields describing 45,572 movies. Field list not reproduced here, but available on request.|
| `ratings.csv`               |Ratings data from [MovieLens](https://movielens.org/), also hosted and downloaded from [Kaggle](https://www.kaggle.com/). 4 Fields (userId, movieId, rating, timestamp) describing 26,024,289 ratings. movieId corresponds to id in `movies_metadata.csv`. Ratings in rating range from 0.5 to 5.0 in increments of 0.5. timestamp corresponds to Unix time.|


### General workflow
1. Import three files 1) `wikipedia-movies.json` 2) `movies_metadata.csv` and 3) `ratings.csv`
2. Clean and Transform Data
3. Add the data to a PostgreSQL Database. Non-destructively append on successive updates.

## Deliverables

### Deliverable 1

Write an ETL Function to Read Three Data Files

### Deliverable 2

Extract and Transform the Wikipedia Data

### Deliverable 3

Extract and Transform the Kaggle Data

### Deliverable 4

Create the Movie Database
