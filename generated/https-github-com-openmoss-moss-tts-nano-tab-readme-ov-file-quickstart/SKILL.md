---
name: moss-tts-nano
description: Use this skill when working with MOSS-TTS-Nano. Triggers when user mentions MOSS-TTS-Nano or imports from it.
---

# MOSS-TTS-Nano

## What this is
MOSS-TTS-Nano is a lightweight, open-source text-to-speech (TTS) system developed by OpenMOSS. It is designed to provide high-quality speech synthesis with low computational requirements, making it suitable for embedded systems and other resource-constrained devices. MOSS-TTS-Nano supports multiple languages and can be easily integrated into various applications.

## Installation
```bash
pip install moss-tts-nano
```

## Key concepts
The most important APIs and patterns in MOSS-TTS-Nano include:
* `TTS` class: The main class for text-to-speech synthesis, which takes a string input and produces an audio output.
* `synthesize` method: A method of the `TTS` class that generates audio from a given text input.
* `save` method: A method that saves the synthesized audio to a file.

Example:
```python
from moss_tts_nano import TTS

tts = TTS()
audio = tts.synthesize("Hello, world!")
tts.save(audio, "hello.wav")
```

## Correct usage patterns
To use MOSS-TTS-Nano, create an instance of the `TTS` class and call the `synthesize` method with a string input. The resulting audio can be saved to a file using the `save` method.

Example:
```python
from moss_tts_nano import TTS

def synthesize_text(text, filename):
    tts = TTS()
    audio = tts.synthesize(text)
    tts.save(audio, filename)

synthesize_text("Hello, this is a test.", "test.wav")
```

## Common mistakes to avoid
* Forgetting to install the `moss-tts-nano` package before using it.
* Not handling exceptions that may occur during speech synthesis or audio saving.
* Using the `synthesize` method without checking if the input text is empty or null.

## File and folder conventions
* The `moss_tts_nano` package is installed using pip and can be imported in Python scripts.
* Synthesized audio files can be saved in various formats, such as WAV or MP3, and can be stored in any folder.
* Configuration files for MOSS-TTS-Nano are not explicitly mentioned in the documentation, but it is recommended to store them in a separate folder or file to keep the code organized.