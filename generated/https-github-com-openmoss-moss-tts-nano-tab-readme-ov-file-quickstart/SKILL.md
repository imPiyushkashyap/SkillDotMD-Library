---
name: moss-tts-nano
description: Use this skill when working with MOSS-TTS-Nano. Triggers when user mentions MOSS-TTS-Nano or imports from it.
---

# MOSS-TTS-Nano

## What this is
MOSS-TTS-Nano is a lightweight, open-source text-to-speech (TTS) system. It is designed to be efficient and scalable, making it suitable for a wide range of applications. MOSS-TTS-Nano provides a simple and easy-to-use API for generating high-quality speech from text input.

## Installation
```bash
pip install moss-tts-nano
```

## Key concepts
The MOSS-TTS-Nano API provides several key concepts, including:
* `TTS`: The main class for generating speech from text. It takes a text string as input and returns a WAV file containing the synthesized speech.
* `Speaker`: A class that represents a speaker in the TTS system. It can be used to customize the voice and tone of the synthesized speech.
* `Vocoder`: A class that converts the output of the TTS model into a WAV file.

Example:
```python
from moss_tts_nano import TTS

tts = TTS()
wav = tts("Hello, world!")
```

## Correct usage patterns
To use MOSS-TTS-Nano, you can follow these patterns:
* Initialize the `TTS` class and pass a text string to the `__call__` method to generate speech.
* Use the `Speaker` class to customize the voice and tone of the synthesized speech.
* Save the generated WAV file to a file using the `save` method.

Example:
```python
from moss_tts_nano import TTS, Speaker

tts = TTS()
speaker = Speaker("en")
wav = tts("Hello, world!", speaker)
wav.save("hello.wav")
```

## Common mistakes to avoid
* Not installing the required dependencies before using MOSS-TTS-Nano.
* Not passing a valid text string to the `TTS` class.
* Not customizing the speaker and vocoder settings to achieve the desired voice and tone.

## File and folder conventions
* The MOSS-TTS-Nano library is installed using pip and can be imported in Python code using `import moss_tts_nano`.
* The `TTS` class is the main entry point for generating speech from text.
* The `Speaker` and `Vocoder` classes can be used to customize the voice and tone of the synthesized speech.
* The generated WAV files can be saved to a file using the `save` method.