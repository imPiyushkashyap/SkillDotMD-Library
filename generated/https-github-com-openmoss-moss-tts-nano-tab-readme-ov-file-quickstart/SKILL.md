---
name: moss-tts-nano
description: Use this skill when working with MOSS-TTS-Nano. Triggers when user mentions MOSS-TTS-Nano or imports from it.
---

# MOSS-TTS-Nano

## What this is
MOSS-TTS-Nano is a lightweight text-to-speech (TTS) system. It is designed to be compact and efficient, making it suitable for resource-constrained devices. MOSS-TTS-Nano provides a simple and easy-to-use API for generating high-quality speech synthesis.

## Installation
```bash
pip install moss-tts-nano
```

## Key concepts
The most important APIs in MOSS-TTS-Nano include the `TTS` class, which provides methods for generating speech synthesis. For example:
```python
from moss_tts import TTS

tts = TTS()
audio = tts('Hello, world!')
```
This code creates a `TTS` object and uses it to generate an audio clip for the text "Hello, world!".

## Correct usage patterns
To use MOSS-TTS-Nano, you can follow these examples:
```python
from moss_tts import TTS

# Create a TTS object
tts = TTS()

# Generate speech synthesis for a given text
audio = tts('Hello, world!')

# Save the audio to a file
audio.save('hello.wav')
```
This code demonstrates how to create a `TTS` object, generate speech synthesis for a given text, and save the resulting audio to a file.

## Common mistakes to avoid
One common mistake to avoid when using MOSS-TTS-Nano is not handling exceptions properly. For example, if the `TTS` object is not properly initialized, it may raise an exception when trying to generate speech synthesis. To avoid this, you can use try-except blocks to catch and handle any exceptions that may occur.

## File and folder conventions
MOSS-TTS-Nano uses the following file and folder conventions:
* The `moss_tts` package contains the main API classes and functions.
* The `models` folder contains pre-trained models for speech synthesis.
* The `utils` folder contains utility functions for tasks such as audio processing.
* Configuration files are typically stored in the `config` folder.