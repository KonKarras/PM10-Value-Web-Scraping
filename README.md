# PM10 Value Web Scraping

Web Scraping Project in Python Jupyter Notebook, aimed for extracting the current level of PM10 in the atmosphere over the province of Bergamo in Italy. The daily updated information was found through the link below:

https://www.infoaria.regione.lombardia.it/infoaria/#/stato-attivazione

In particular, I imported the necessary modules from the Selenium library as well as the Re module and set up Chrome options to run in headless mode, so that I avoid opening a browser window. Then, I set up the Chrome driver’s path (downloaded from https://chromedriver.chromium.org/downloads) to initialize Chrome browser with the specified service and options, and navigated to the website.

After spending some time to inspect the desired value with the help of my browser’s developer tool, I found all elements with the tag name ‘strong’ and selected the first element in the list, which should always be the last updated one. I got the inner HTML of the selected ‘strong’ element and defined a regular expression pattern to match the number in the inner HTML. Then, I used the findall() method from the Re module to extract the number from the string.

Finally, if the regular expression pattern finds a match in the extracted PM10 value string, the value gets converted to a float and printed to the console as the current PM10 level for the province of Bergamo. Otherwise, a dash is printed.

Note that the .ipynb file can be run immediately on every machine where Anaconda Navigator in installed, however the path to the Chrome driver file needs to be adjusted according to where each individual has stored the relevant file in their machine.

Also note that the same script, with a single number change in the second line of the third cell (element = elements[...]), could be used for extracting other values of PM10 in different provinces/dates, according to one's interest.
