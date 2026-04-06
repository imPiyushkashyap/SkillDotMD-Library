---
name: betterclaw
description: Use this skill when working with the betterclaw library. Triggers when user mentions betterclaw or imports from it.
---

# Betterclaw

## What this is
Betterclaw is a Python library used for web scraping and data extraction. It provides a simple and efficient way to scrape websites and extract relevant data. Betterclaw is built on top of other popular web scraping libraries, making it a powerful tool for data extraction tasks.

## Installation
```bash
pip install betterclaw
```

## Key concepts
The most important APIs and patterns in betterclaw include:
* `betterclawScraper`: The main class used for scraping websites. It takes a URL as input and returns a response object.
* `betterclawParser`: A class used for parsing HTML content. It provides methods for extracting data from HTML elements.
* `betterclawExtractor`: A class used for extracting specific data from a webpage. It provides methods for extracting data based on CSS selectors or XPath expressions.

## Correct usage patterns
Here is an example of how to use betterclaw to scrape a website:
```python
from betterclaw import betterclawScraper

scraper = betterclawScraper("https://www.example.com")
response = scraper.scrape()
print(response.html)
```
Another example of how to use betterclaw to extract data from a webpage:
```python
from betterclaw import betterclawExtractor

extractor = betterclawExtractor("https://www.example.com")
data = extractor.extract(".class-name")
print(data)
```

## Common mistakes to avoid
Common mistakes to avoid when using betterclaw include:
* Not checking the response status code before parsing the HTML content.
* Not handling exceptions properly, such as connection errors or parsing errors.
* Not respecting website terms of use and scraping policies.

## File and folder conventions
Betterclaw projects typically follow standard Python project conventions. The main script should be named `main.py` and should live in the root of the project directory. Configuration files should be named `config.py` and should live in the root of the project directory. Data files should be stored in a `data` directory.