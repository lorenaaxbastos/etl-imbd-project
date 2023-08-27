# ETL pipeline using AI and Python

This project was based on studies about data science, web scrapping and the use of generative AI using Python and its libraries, such as Requests, Beautiful Soup, NumPy, Pandas and openAI. The main goal was to create from scratch an ETL pipeline that enriches data using the power of artificial intelligence.

The process was documented using [Jupyter Notebooks](https://docs.jupyter.org/en/latest/).

## Overview

### Web scraping

> Data scraped from: [IMDB](https://imdb.com/)

The first part of the project consisted of scraping through the documentary movies pages from IMDB to retrieve information from the top 250 movies. Data cleaning was implemented while scraping the content.

After the data was organized into lists, Pandas was called to create dataframes and export it to a CSV file.

**Info collected and its classes**

| Title | Year | Rating | Runtime | Genre(s) | IMDB rating | Metascore | Director(s) | Stars | Votes |
| :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: |
| str | int | str | int | list | float | int | str or list | list | int |

### Extraction

### Transformation

### Load