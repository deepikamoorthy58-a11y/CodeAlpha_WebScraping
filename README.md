# CodeAlpha - Web Scraping Task

## Overview
This project scrapes population and GDP data for countries from Wikipedia, 
cleans it, merges the two datasets, and analyzes the relationship between 
population and GDP.

## Tools Used
- Python
- Requests (to fetch web pages)
- BeautifulSoup / pandas.read_html (to parse HTML tables)
- Pandas (data cleaning and merging)
- Matplotlib (visualization)

## What I Did
1. Scraped country population data from Wikipedia
   (List of countries by population - United Nations)
2. Scraped country GDP data from Wikipedia
   (List of countries by GDP - nominal)
3. Cleaned both datasets:
   - Removed empty rows
   - Removed footnote tags like [a], [n 1] from country names
   - Converted GDP values from text (with commas/notes) to numbers
4. Merged the population and GDP datasets on country name
5. Found a strong correlation (0.97) between population and GDP
6. Visualized the Top 10 most populated countries in a bar chart

## Challenges Faced
- Wikipedia blocked the initial request — fixed by adding a User-Agent header
- Had to search through multiple tables on the GDP page to find the correct one
- GDP values had commas and extra text, which needed cleaning before analysis

## Files
- `webscrap.ipynb` - Jupyter/Colab notebook with all code
- `merged_population_gdp.csv` - final cleaned and merged dataset
