---
name: moss-tts-nano
description: Use this skill when working with MOSS-TTS-Nano. Triggers when user mentions MOSS-TTS-Nano or imports from it.
---

# MOSS-TTS-Nano

## What this is
MOSS-TTS-Nano is an open-source, state-of-the-art text-to-speech (TTS) system. It is designed to be highly efficient and scalable, making it suitable for a wide range of applications. MOSS-TTS-Nano provides a simple and easy-to-use API for generating high-quality speech synthesis.

## Installation
```bash
pip install moss-tts-nano
```

## Key concepts
The most important APIs and patterns in MOSS-TTS-Nano include:
* `TTSModel`: The core class for generating speech synthesis.
* `synthesize`: The method used to generate speech from text.
* `save_wav`: The method used to save the generated speech to a WAV file.

Example:
```python
from moss_tts_nano import TTSModel

model = TTSModel()
audio = model.synthesize("Hello, world!")
model.save_wav(audio, "hello.wav")
```

## Correct usage patterns
To use MOSS-TTS-Nano, you can follow these steps:
* Initialize the `TTSModel` class.
* Use the `synthesize` method to generate speech from text.
* Use the `save_wav` method to save the generated speech to a WAV file.

Example:
```python
from moss_tts_nano import TTSModel

model = TTSModel()
text = "This is an example of MOSS-TTS-Nano."
audio = model.synthesize(text)
model.save_wav(audio, "example.wav")
```

## Common mistakes to avoid
* Not installing the required dependencies.
* Not initializing the `TTSModel` class before using it.
* Not saving the generated speech to a WAV file.

## File and folder conventions
* The `moss_tts_nano` package lives in the root directory of your project.
* The `TTSModel` class is located in the `moss_tts_nano` package.
* The generated WAV files are saved in the current working directory.
* The configuration files for MOSS-TTS-Nano are not required, as it uses default settings.