Yousician.py info:

Task:

1. Create a code to check the search results for the page:
https://yousician.com/songs
2. The program should take a string to search with as an input argument.
3. The program should then use the search with the given string, and get all the
search results (a list of songs with song and artist name).
4. It should then print all the found songs in alphabetical order, sorted first by
the artist name, and then by the song name.
5. If any error is encountered (e.g., the user does not have an internet
connection), the program should print an error message instead and exit.

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

The code itself contains comments with short descriptions of all the necessary actions; here is a brief of the solution used below:
First I needed to locate all the necessary elements/paths and save them as variables (because it's easier/cleaner that way).
Then to handle the "Accept cookies" button—otherwise it won't let me execute the rest of the code—input field click, and search by a given string.
After that, it retrieves/parses the JSON data from @id="__NEXT_DATA__", extracts it according to its structure (found by a page inspect on the search result page), then creates a list and prints it with simple error handling at the end.
