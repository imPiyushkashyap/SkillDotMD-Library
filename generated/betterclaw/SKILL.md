---
name: betterclaw
description: Use this skill when working with the betterclaw library. Triggers when user mentions betterclaw or imports from it.
---

# BetterClaw

## What this is
BetterClaw is a Python library used for web scraping and data extraction. It provides an efficient and easy-to-use way to extract data from websites. BetterClaw is designed to handle common web scraping tasks, such as handling different types of content, rotating user agents, and avoiding anti-scraping measures.

## Installation
```bash
pip install betterclaw
```

## Key concepts
The most important APIs and patterns in BetterClaw include:
- `betterclaw.Client`: The main entry point for making HTTP requests and extracting data.
- `betterclaw.Parser`: Used to parse HTML and XML content.
- `betterclaw.RotationPolicy`: Defines how user agents are rotated to avoid anti-scraping measures.

Example:
```python
from betterclaw import Client

client = Client()
response = client.get("https://www.example.com")
print(response.text)
```

## Correct usage patterns
When using BetterClaw, make sure to handle exceptions and errors properly:
```python
from betterclaw import Client
from betterclaw.exceptions import RequestException

client = Client()
try:
    response = client.get("https://www.example.com")
    print(response.text)
except RequestException as e:
    print(f"An error occurred: {e}")
```

## Common mistakes to avoid
- Not handling exceptions and errors properly
- Not rotating user agents, leading to IP blocks
- Not checking the library's documentation for updates and changes

## File and folder conventions
- Configuration files should be named `betterclaw.cfg` and placed in the root directory of the project.
- Log files should be named `betterclaw.log` and placed in the `logs` directory.
- User-defined parsers and rotation policies should be placed in separate modules and imported as needed.