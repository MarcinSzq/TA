Yousician.py info:

Coded in python 3.12 using Anaconda distro/Spyder

Used libraries: Selenium + chromedriver with Selenium classes:

from selenium import webdriver 
from selenium.webdriver.common.by import By 
from selenium.webdriver.common.keys import Keys - https://selenium-python.readthedocs.io/getting-started.html#simple-usage
from selenium.webdriver.support.ui import WebDriverWait - https://selenium-python.readthedocs.io/waits.html
from selenium.webdriver.support import expected_conditions as EC
import json  - to handle json data as the search results are provided as a json/object.

Selenium and chromedriver installation command:

'''conda install selenium
pip install chromedriver-binary'''

Code itself contains a comments with a short descriptions of all the necessary actions here is a brief of used solution below:

First i needed to locate all the necessary elements/paths and saved them as a variables (because it's easier/cleaner that way).
Then to handle the "Accept cookies button" - otherwise it won't let me execute the rest of the code -  input field click, and search by a given string.
After that it retrieves/parses the json data from @id="__NEXT_DATA__", extracts it according to its structure (found by a page inpsect on the search result page), then creates a list and prints it + a simple error handling at the end.
