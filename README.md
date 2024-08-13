# data-scraping-challenge

## Overview

This repository contains a Python-based data scraping process focused on extracting and analyzing Mars-related data from the web. The project is divided into two main deliverables:

1. **[Scrape Mars News Articles](#deliverable-1-scrape-mars-news-articles)**: Extract titles and preview text from the latest Mars news articles.
2. **[Scrape and Analyze Mars Weather Data](#deliverable-2-scrape-and-analyze-mars-weather-data)**: Collect and analyze Mars weather data presented in a table format.

## Deliverables

### [Deliverable 1: Scrape Mars News Articles](https://github.com/eeanguyen/data-scraping-challenge/blob/main/Starter_Code/part_1_mars_news.ipynb)

- **Objective**: Retrieve titles and preview text from Mars-related news articles.
- **Process**:
  - Use Python libraries such as `BeautifulSoup` and `requests` to scrape the webpage containing the articles.
  - Extract the titles and preview text for each article.
  - Store the extracted data in a structured dictionary.

### [Deliverable 2: Scrape and Analyze Mars Weather Data](https://github.com/eeanguyen/data-scraping-challenge/blob/main/Starter_Code/part_2_mars_weather.ipynb)

- **Objective**: Scrape Mars weather data from a table and perform basic analysis.
- **Process**:
  - Use Python to scrape the table data from a web source containing Mars weather information.
    ```
    rowElements = marsSoup.find_all('tr', class_='data-row')
    rowElements
    ```
  - Clean and organize the data for analysis.
    ```
    # Create an empty list
    data = []
    # Loop through the scraped data to create a list of rows
    for row in rowElements:
        cellValues = row.find_all('td')
        values = []
        for value in cellValues:
            values.append(value.text)
    data.append(values)
    ```
  - Perform a basic analysis to identify trends or significant insights related to Mars weather.
  - Present the analysis results in a clear and concise manner using visualizations.
 
    The bar graph below shows the average minimum temperature on Mars by month:

    ![Average Minimum Temperature by Month on Mars](https://github.com/eeanguyen/data-scraping-challenge/blob/main/Starter_Code/images/%20sorted_avg_min_temp.png)

    As shown in the graph, the average minimum temperature on Mars varies throughout the year, with the coldest months typically being the third and forth month. On the opposite end the ninth and eigth month are the highest minimum temperature month.

    ![Average Pressure on Mars by Month](https://github.com/eeanguyen/data-scraping-challenge/blob/main/Starter_Code/images/%20avg_pressure.png)

    The graph provides insights into these dynamic changes in Martian atmospheric pressure, helping us understand the complex interplay between temperature, seasonality, and altitude on the Red Planet. The highest atomospheric pressure months are second and ninth. As for the lowest atomospheric pressure months are the sixth and fifth month.

    ![Terrestrial Days in Martian Years](https://github.com/eeanguyen/data-scraping-challenge/blob/main/Starter_Code/images/%20Number_of_Terrestrial_days_in_Martian_year.png)
    The distance from peak to peak is roughly 1425-750, or 675 days. A year on Mars appears to be about 675 days from the plot. Internet search confirms that a Mars year is equivalent to 687 earth days.


    
    
