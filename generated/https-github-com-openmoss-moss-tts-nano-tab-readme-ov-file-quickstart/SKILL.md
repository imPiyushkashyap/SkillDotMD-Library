---
name: MOSS-TTS-Nano
description: Use this skill when working with MOSS-TTS-Nano, a lightweight text-to-speech system. Triggers when user mentions MOSS-TTS-Nano or imports from it.
---

# MOSS-TTS-Nano

## What this is
MOSS-TTS-Nano is a lightweight text-to-speech system designed for efficient and high-quality speech synthesis. It utilizes a compact model architecture to achieve fast inference speeds while maintaining good speech quality. MOSS-TTS-Nano is suitable for applications where resources are limited, such as embedded systems or low-power devices.

## Installation
```bash
git clone https://github.com/OpenMOSS/MOSS-TTS-Nano.git
cd MOSS-TTS-Nano
pip install -r requirements.txt
```

## Key concepts
The core APIs of MOSS-TTS-Nano include the `TTS` class, which handles text-to-speech synthesis, and the `save_wav` method, which saves the synthesized audio to a WAV file. For example:
```python
from moss_tts import TTS

tts = TTS()
audio = tts("Hello, world!")
tts.save_wav("hello.wav", audio)
```

## Correct usage patterns
To synthesize speech, create an instance of the `TTS` class and call the `__call__` method with the desired text:
```python
from moss_tts import TTS

tts = TTS()
text = "This is an example sentence."
audio = tts(text)
tts.save_wav("example.wav", audio)
```

## Common mistakes to avoid
Common mistakes when using MOSS-TTS-Nano include failing to install the required dependencies, not handling audio data correctly, and not properly closing the `TTS` instance.

## File and folder conventions
The MOSS-TTS-Nano repository follows standard GitHub conventions, with the main code residing in the root directory. Configuration files, such as `requirements.txt`, are also located in the root directory. The `moss_tts` package contains the core implementation of the text-to-speech system.