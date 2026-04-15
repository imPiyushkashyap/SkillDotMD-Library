---
name: bland-ai
description: Use this skill when working with bland.ai. Triggers when user mentions bland.ai or imports from it.
---

# Bland AI

## What this is
Bland.ai is a library that provides a simple way to interact with AI models. It allows users to effortlessly integrate AI capabilities into their applications. The library offers a range of tools and features for building, training, and deploying AI models.

## Installation
```bash
pip install bland_ai
```

## Key concepts
The most important APIs in bland.ai include `BlandModel`, `BlandDataset`, and `BlandTrainer`. Here's an example:
```python
from bland_ai import BlandModel

# Create a new BlandModel instance
model = BlandModel()
```

## Correct usage patterns
To train a model using bland.ai, you can use the following code:
```python
from bland_ai import BlandModel, BlandDataset, BlandTrainer

# Load a dataset
dataset = BlandDataset()

# Create a new BlandModel instance
model = BlandModel()

# Create a new BlandTrainer instance
trainer = BlandTrainer(model, dataset)

# Train the model
trainer.train()
```

## Common mistakes to avoid
One common mistake when using bland.ai is forgetting to import the necessary modules. Another mistake is not properly initializing the `BlandModel` instance before using it.

## File and folder conventions
The bland.ai library expects files to be organized in the following structure:
```markdown
project/
|--- bland_ai/
|    |--- __init__.py
|    |--- model.py
|    |--- dataset.py
|    |--- trainer.py
|--- config.json
|--- main.py
```
Note: The `config.json` file is used to store configuration settings for the library.