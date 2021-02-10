#  Question

Scrap a website using python and extract text from it and write the data to the text file.<br />
Take any blog or article website to test it.<br />
Please also list the libraries/sdks you used to achieve this and recommend the one that you think is good with reason.<br />
Deliverables:<br />
 -code <br />
 -Readme(instruction how to setup and execute it)<br />
don't use any library for scrapping such as BeautifulSoap 
it should only scrap text and not any html/tags.

---
###  Answer:
Modules used:
   


``` python
import fileinput                 // This module implements a helper class and functions to quickly write a loop over standard input or a list of  files. If you just want to read or write one file see
import re  (re.findall)          // This module provides regular expression matching operations (Return all non-overlapping matches of pattern in string, as a list of strings.)
import html                      // Imports data from  a HTML page.
from urllib.request import urlopen  //Python module for fetching URLs (Uniform Resource Locators)

```

_**Setup & Execution:**_<br />
Save this file in your directory and open your console run it and result will be displayed

---
