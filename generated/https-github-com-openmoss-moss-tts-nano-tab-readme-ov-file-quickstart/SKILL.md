---
name: moss-tts-nano
description: Use this skill when working with MOSS-TTS-Nano. Triggers when user mentions MOSS-TTS-Nano or imports from it.
---

# MOSS-TTS-Nano

## What this is
MOSS-TTS-Nano is a lightweight text-to-speech (TTS) system based on the MOSS-TTS model. It provides a simple and efficient way to generate high-quality speech from text inputs. The system is designed to be compact and fast, making it suitable for a wide range of applications.

## Installation
```bash
pip install moss-tts-nano
```

## Key concepts
The MOSS-TTS-Nano system consists of several key components, including the `TTS` class, which is responsible for generating speech from text inputs. The `TTS` class takes in a text string and returns an audio waveform. Here is an example:
```python
from moss_tts_nano import TTS

tts = TTS()
audio = tts("Hello, world!")
```
Another important concept is the `save_wav` method, which saves the generated audio to a WAV file:
```python
tts.save_wav("output.wav", audio)
```

## Correct usage patterns
To use MOSS-TTS-Nano, you can create an instance of the `TTS` class and call the `__call__` method to generate speech from a text string:
```python
from moss_tts_nano import TTS

tts = TTS()
text = "This is an example sentence."
audio = tts(text)
tts.save_wav("example.wav", audio)
```
You can also specify the speaker ID and speech rate when generating speech:
```python
audio = tts("Hello, world!", speaker_id=0, speech_rate=1.0)
```

## Common mistakes to avoid
One common mistake is not checking the input text for validity before passing it to the `TTS` class. MOSS-TTS-Nano expects the input text to be a string, so passing in other types of input can result in errors.

## File and folder conventions
The MOSS-TTS-Nano library is typically installed using pip, and the installation directory will depend on the system configuration. The library itself does not have any specific file or folder conventions, but it is recommended to keep the generated audio files in a separate directory to avoid cluttering the working directory. For example:
```python
import os

output_dir = "audio_output"
os.makedirs(output_dir, exist_ok=True)
tts.save_wav(os.path.join(output_dir, "example.wav"), audio)
```