# ETL pipeline using AI and Python

This project was based on studies about data science, web scrapping and the use of generative AI using Python and its libraries, such as Requests, Beautiful Soup, NumPy, Pandas and openAI. The main goal was to create from scratch an ETL pipeline that enriches data using the power of artificial intelligence.

The process was documented using [Jupyter Notebooks](https://docs.jupyter.org/en/latest/).

## Tools

![Python](https://img.shields.io/badge/Python-000?style=for-the-badge&logo=python&logoColor=30A3DC)&nbsp;
![Jupyter Notebook](https://img.shields.io/badge/Jupyter_Notebook-000?style=for-the-badge&logo=jupyter&logoColor=30A3DC)&nbsp;
![openAI](https://img.shields.io/badge/Open_AI-000?style=for-the-badge&logo=openai&logoColor=30A3DC)&nbsp;
![NumPy](https://img.shields.io/badge/NumPy-000?style=for-the-badge&logo=numpy&logoColor=30A3DC)&nbsp;
![Pandas](https://img.shields.io/badge/Pandas-000?style=for-the-badge&logo=pandas&logoColor=30A3DC)&nbsp;
![JSON](https://img.shields.io/badge/JSON-000?style=for-the-badge&logo=json&logoColor=30A3DC)&nbsp;
![Beautiful Soup](https://img.shields.io/badge/Beautiful_Soup-000?style=for-the-badge&logo=beautifulSoup&logoColor=30A3DC)&nbsp;
![Requests](https://img.shields.io/badge/Requests-000?style=for-the-badge&logo=requests&logoColor=30A3DC)&nbsp;
![Tkinter](https://img.shields.io/badge/Tkinter-000?style=for-the-badge&logo=tkinter&logoColor=30A3DC)&nbsp;
![Time](https://img.shields.io/badge/Time-000?style=for-the-badge&logo=time&logoColor=30A3DC)&nbsp;
![Warnings](https://img.shields.io/badge/Warnings-000?style=for-the-badge&logo=warnings&logoColor=30A3DC)&nbsp;
![Random](https://img.shields.io/badge/Random-000?style=for-the-badge&logo=random&logoColor=30A3DC)&nbsp;

## Overview

### Web scraping

> Data scraped from: [IMDB](https://imdb.com/)

The first part of the project consisted of scraping through the documentary movies pages from IMDB to retrieve information from the top 50 movies. Data cleaning was implemented while scraping the content.

After the data was organized into lists, Pandas was used to create a dataframe and export it to a CSV file.

**Info collected and its classes**

| Title | Year | Rating | Runtime | Genre(s) | IMDB rating | Metascore | Votes |Director(s) | Stars |
| :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: |
| str | int | str | int | list | float | int | int | str or list | list |

### ETL

The second part of the project consisted of:

#### Extract

I extracted the movie titles from the CSV file previously exported.

#### Transform

I connected to the openAI API, created a function to generate movie reviews and recommendations with the chatGPT 3.5 model, run the function and stored the result to some variables.

#### Load

I used Pandas to create a new dataframe, combine it with the existing dataframe and export the final result to a new CSV file.

**Final CSV cells and its classes**

| Title | Year | Rating | Runtime | Genre(s) | IMDB rating | Metascore | Votes |Director(s) | Stars | Review | Recommendations
| :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: |
| str | int | str | int | list | float | int | int | str or list | list | list | list |

*PS.: I encapsulated each review into a list so that it fitted into a cell*