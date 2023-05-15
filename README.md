# PM10 Value Web Scraping

Web Scraping Project in Python Jupyter Notebook, aimed for extracting the current levels of PM10 in the atmosphere over 11 different provinces in the region of Lombardy in Italy, as well as storing these data in a .csv file. The daily updated information was found through the link below:

https://www.infoaria.regione.lombardia.it/infoaria/#/stato-attivazione

In particular, the script's functionality can be broken down to the following 4 steps:

1. Importing the necessary libraries and modules:

    •	Selenium: for web scraping using the Chrome browser and

    •	Other modules for handling exceptions, regular expressions, csv operations, date formatting and data manipulation.

2. Defining the function 'PM10_Value_Web_Scraper()':

    •	Sets up Chrome options to run in headless mode (without opening a browser window).

    •	Initializes the Chrome browser using the ChromeDriver service and the specified options.

    •	Navigates to the target webpage.

    •	Retrieves the current date and formats it as a string.

    •	Creates an empty list to store PM10 values for each province.

    •	Loops through the provinces and extracts the PM10 value for each one using XPath.

    •	Processes and converts the extracted values to decimal numbers.

    •	Appends the PM10 values to the list, or adds 'None' if no value or a dash is found.

    •	Quits the browser driver.

3. Calling the function 'PM10_Value_Web_Scraper()' to perform the web scraping and store the data in a .csv file named 'PM10ValueWebScraperDataset.csv'.

4. Reading and displaying the data from the .csv file into a Pandas dataframe.

Please note that the script assumes the presence of ChromeDriver and specifies the file path for it. Additionally, it assumes the existence of the .csv file for storing the scraped data and also specifies its file path. Therefore, you may need to adjust these paths according to your local environment before running the script.

Finally note that the script is intended to be run every day automatically, so that after some significant amount of time, we can have a dataset, ready for future analysis and valuable insights regarding the whole region of Lombardy in Italy.
