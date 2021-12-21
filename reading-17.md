# Web Scraper

## [Web Scrape with Python in 4 minutes](https://towardsdatascience.com/how-to-web-scrape-with-python-in-4-minutes-bc49186a8460)
- Purpose:
  - Automate the process of retreiving data from a website
- Steps:
  - Inspect
    - Find the element you want to target using the dev tools element selector
  
```python
import requests
import urllib.request
import time
from bs4 import BeatifulSoup
url = "websit.you.targeted"
response = requests.get(url)
soup = BeatifulSoup(response.text, "html.parser") // parses out the webpage data as an html file
soup.findAll('a') // finds all a tags

one_a_tag = soup.findAll('a')[38]
link = one_a_tag['href']
```

## [Web Scraping](https://en.wikipedia.org/wiki/Web_scraping)
- Types
  - Human Copypasta
    - `ctrl + c`, `ctrl + v`
  - Text pattern matching
    - regex targets the stuff you want
  - HTTP programming
    - making a direct HTTP request for the data
  - HTML Parsing
    - use established html practices to identify contect that is generated dynamically
  - Dom parsing
    - This scrapes data from the DOM tree to access content
  - Vertical aggregation

## [How to scrape without getting blocked](https://www.scrapehero.com/how-to-prevent-getting-blacklisted-while-scraping/)
1. Respect Robots.txt
2. Make the crawoling slower
3. Do no follow the dame crawling pattern
4. Make requests through Proxies and rotate them as needed
5. Rotate User Agents and corresponding HTTP Request Headers between requests
6. Yse a headless Browser like Puppeteer, Selenium or Playwright
7. Beware of Honey Pot Traps
8. Check if Webisite is Changeing Layours
9. Avoid scraping data behind a login
10. Use Captcha Solving Servieces
- First and Foremost:
  - Be Nice

[Return Home](README.md)