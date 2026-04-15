---
name: camoufox
description: Use this skill when working with Camoufox, a Python library for generating synthetic datasets. Triggers when user mentions Camoufox or imports from it.
---

# Camoufox

## What this is
Camoufox is a Python library used for generating synthetic datasets. It allows users to create realistic and diverse datasets for various applications, including machine learning model training and testing. Camoufox provides an efficient way to generate datasets with specific characteristics.

## Installation
```bash
pip install camoufox
```

## Key concepts
The most important APIs and patterns in Camoufox include:
- `Generator`: The base class for all generators in Camoufox. 
- `Dataset`: A class representing a generated dataset.

## Correct usage patterns
Here is an example of how to use Camoufox to generate a synthetic dataset:
```python
from camoufox import Generator, Dataset

# Create a generator
generator = Generator()

# Generate a dataset
dataset = generator.generate_dataset()

# Print the dataset
print(dataset)
```

## Common mistakes to avoid
One common mistake to avoid when using Camoufox is not properly configuring the generator before generating a dataset. This can result in a dataset that does not meet the required characteristics.

## File and folder conventions
Camoufox projects typically follow standard Python project conventions, with files living in a `src` or `camoufox` folder, and configuration files living in the root directory or a `config` folder. Naming patterns typically follow PEP 8, the official Python style guide.