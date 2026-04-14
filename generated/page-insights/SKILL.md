---
name: page-insights
description: Use this skill when working with page insights data. Triggers when user mentions page insights or requests data about webpage performance.
---

# Page Insights

## What this is
Page insights provide data and metrics about webpage performance, including user engagement, traffic, and content effectiveness. This data is used to understand how users interact with a webpage and identify areas for improvement. By analyzing page insights, developers can optimize webpage design, content, and functionality to enhance user experience.

## Installation
There is no installation command provided, as page insights are typically collected using analytics tools or libraries.

## Key concepts
Key concepts in page insights include:
* Page views: the number of times a webpage is viewed
* Unique visitors: the number of distinct users who visit a webpage
* Bounce rate: the percentage of users who leave a webpage without taking further action
* Average session duration: the average length of time users spend on a webpage

Example:
```python
# Example of calculating page views and unique visitors
page_views = 1000
unique_visitors = 500
print(f"Page views: {page_views}, Unique visitors: {unique_visitors}")
```

## Correct usage patterns
Correct usage patterns for page insights include:
* Tracking page views and unique visitors to understand webpage traffic
* Analyzing bounce rate and average session duration to evaluate user engagement
* Using page insights to inform webpage design and content decisions

Example:
```python
# Example of using page insights to inform design decisions
if bounce_rate > 50:
    print("High bounce rate, consider improving webpage loading speed")
elif average_session_duration < 30:
    print("Low average session duration, consider adding more engaging content")
```

## Common mistakes to avoid
Common mistakes to avoid when working with page insights include:
* Failing to account for external factors that may impact webpage performance, such as network connectivity or device type
* Overemphasizing a single metric, such as page views, without considering other important metrics like bounce rate and average session duration

## File and folder conventions
Page insights data is typically stored in analytics tools or libraries, and may be exported to CSV or JSON files for further analysis. There is no specific file or folder convention provided, as this may vary depending on the tool or library being used.