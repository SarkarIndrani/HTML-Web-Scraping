# HTML-Web-Scraping
## Background
The aim of this project is to apply full web-scraping for the mission to Mars by collecting data, organizing and storing data, and then visually communicating our insights. 
I extracted the information via both automated browsing with Splinter and HTML parsing with Beautiful Soup.

This project consists of two technical products.

  * Part 1: Scrape titles and preview text from Mars news articles.
  * Part 2: Scrape and analyze Mars weather data, which exists in a table.
  ---

## Part 1: Scrape Titles and Preview Text from Mars News

  1. Used automated browsing to visit the <a href="https://static.bc-edx.com/data/web/mars_news/index.html">Mars news site</a>. Inspected the page to identify which elements to scrape.
  2. Created a Beautiful Soup object and used it to extract text elements from the website.
  3. Extracted the titles and preview text of the news articles that I scraped. Stored the scraping results in Python data structures as follows:
      * Stored each title-and-preview pair in a Python dictionary and, gave each dictionary two keys: ```title``` and ```preview```. An example is the following:

      ```python
      {'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm",
      'preview': "For the first time in its eight years orbiting Mars, NASA's MAVEN mission witnessed two different types of ultraviolet aurarae simultaneously, the result of solar sorms that began on Aug. 27."}  
      ```
     * Stored all the dictionaries in a Python list.
     * Printed the list in my notebook.

-----
## Part 2:Scrape and Analyze Mars Weather Data

  1. Used automated browsing to visit the <a href="https://static.bc-edx.com/data/web/mars_facts/temperature.html">Mars Temperature Data Site </a>.
  2. Created a Beautiful Soup object and used it to scrape the data in the HTML table. Note that this can also be achieved by using the Pandas ```read_html``` function. However, used Beautiful Soup here to continue sharpening my web scraping skills.
  3. Assembled the scraped data into a Pandas DataFrame. The columns should have the same headings as the table on the website. Here's an explanation of the column headings:
      * ```id```: the identification number of a single transaction from the Curiosity rover 
      * ```terrestrial_date```: the date on EArth
      * ```sol```: the number of elapsed sols (Martian Days) since Curiosity landed on Mars 
      * ```ls```: the solar longitude
      * ```month```: the Martian monthe
      * ```min_temp```: the minimum temperature, in Celsius, of a single Martian day (sol)
      * ```pressure```: The atmospheric pressure at Curiosity's location  

  4. Examined the data types that are currently associated with each column. I converted the data to the appropriate ```datetime```, ```int```, or ```float``` data types.
  5. Analyzed my dataset by using Pandas functions to answer the following questions:
      * How many months exist on Mars?
      * How many Martian (and not Earth) days worth of data exist in the scraped dataset?
      * What are the coldest and the warmest months on Mars (at the location of Curiosity)?
      To answer this question:
        * Found the average minimum daily temperature for all of the months. 
        * Plotted the results as a bar chart.

      * Whick months have the lowest and the highest atmospheric pressure on Mars? To answere this question:
        * Found the average daily atmospheric pressure of all the months.
        * Plotted the results as a bar chart.
      * About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
        * Consider how many days elapse on Earth in the time that Mars in the that Mars circles the Sun once.
        * Visually estimate the result by plotting the daily minimum temperature.
  6. Exported the DataFrame to a CSV file.
        


      




 
  
    


   





