---
name: recall-email-finder
description: Use this skill when working with Recall Email Finder. Triggers when user mentions Recall Email Finder or imports from it.
---

# Recall Email Finder

## What this is
Recall Email Finder is a Python library used to find and verify email addresses associated with a given domain name. It provides a simple and efficient way to perform email discovery and validation. The library utilizes various techniques, including DNS lookups and web searches, to identify valid email addresses.

## Installation
`pip install recall-email-finder`

## Key concepts
The Recall Email Finder library provides several key APIs and patterns for finding and verifying email addresses:
* `finder.find_emails`: This function takes a domain name as input and returns a list of email addresses associated with the domain.
* `finder.verify_email`: This function takes an email address as input and returns a boolean indicating whether the email address is valid or not.

Example:
```python
from recall_email_finder import finder

emails = finder.find_emails("example.com")
print(emails)

is_valid = finder.verify_email("test@example.com")
print(is_valid)
```

## Correct usage patterns
To use the Recall Email Finder library, you can follow these examples:
```python
# Find all email addresses associated with a domain
emails = finder.find_emails("example.com")
for email in emails:
    print(email)

# Verify a single email address
is_valid = finder.verify_email("test@example.com")
if is_valid:
    print("Email is valid")
else:
    print("Email is not valid")
```

## Common mistakes to avoid
When using the Recall Email Finder library, be sure to:
* Handle exceptions properly, as the library may raise errors during DNS lookups or web searches.
* Avoid using the library for spamming or other malicious activities, as this can result in your IP being blocked.

## File and folder conventions
The Recall Email Finder library consists of a single Python package, `recall_email_finder`, which contains the `finder` module. The library can be installed using pip, and the `finder` module can be imported in your Python scripts. Configuration files are not required, as the library uses default settings for DNS lookups and web searches.