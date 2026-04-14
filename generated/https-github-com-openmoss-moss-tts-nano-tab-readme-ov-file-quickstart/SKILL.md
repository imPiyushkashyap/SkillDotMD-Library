---
name: moss-tts-nano
description: Use this skill when working with MOSS-TTS-Nano. Triggers when user mentions MOSS-TTS-Nano or imports from it.
---

# MOSS-TTS-Nano

## What this is
MOSS-TTS-Nano is a lightweight text-to-speech (TTS) system developed by OpenMOSS. It is designed to provide a compact and efficient TTS solution for various applications. MOSS-TTS-Nano supports multiple languages and can be easily integrated into different projects.

## Installation
```bash
pip install moss-tts-nano
```

## Key concepts
The most important APIs and patterns in MOSS-TTS-Nano include:
* `TTS` class: The main class for text-to-speech conversion.
* `synthesize` method: This method takes a text string as input and returns the corresponding audio waveform.
* `save` method: This method saves the audio waveform to a file.

Example:
```python
from moss_tts import TTS

tts = TTS()
audio = tts.synthesize("Hello, world!")
tts.save(audio, "hello.wav")
```

## Correct usage patterns
To use MOSS-TTS-Nano, create an instance of the `TTS` class and call the `synthesize` method with the desired text. Then, use the `save` method to save the audio waveform to a file.
```python
from moss_tts import TTS

def text_to_speech(text, filename):
    tts = TTS()
    audio = tts.synthesize(text)
    tts.save(audio, filename)

text_to_speech("Hello, this is a test.", "test.wav")
```

## Common mistakes to avoid
Common mistakes when using MOSS-TTS-Nano include:
* Forgetting to install the required dependencies.
* Not checking the language support for the desired language.
* Not handling exceptions properly.

## File and folder conventions
MOSS-TTS-Nano follows standard Python package conventions. The main package is named `moss_tts`, and the `TTS` class is located in the `moss_tts` module. Configuration files should be placed in the same directory as the Python script using MOSS-TTS-Nano.