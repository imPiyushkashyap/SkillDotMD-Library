---
name: vlc
description: Use this skill when working with the VLC library. Triggers when user mentions VLC or imports from it.
---

# VLC

## What this is
VLC is a popular media player library that allows developers to play and stream various media formats. It provides a comprehensive set of APIs for controlling playback, handling media files, and customizing the player's behavior. With VLC, developers can create custom media players, stream media content, and integrate media playback into their applications.

## Installation
To install the VLC library, run the following command: `pip install python-vlc`

## Key concepts
The VLC library provides several key concepts, including:
* `MediaPlayer`: The main class for playing media files, which can be created using `instance = vlc.Instance()` and `player = instance.media_player_new()`
* `Media`: The class representing a media file, which can be created using `media = instance.media_new('file.mp3')`
* `EventHandler`: The class for handling events, such as playback start and stop, which can be created using `events = player.event_manager()

## Correct usage patterns
Here are some correct usage patterns:
```python
import vlc

# Create a new instance
instance = vlc.Instance()

# Create a new media player
player = instance.media_player_new()

# Create a new media file
media = instance.media_new('file.mp3')

# Set the media file for the player
player.set_media(media)

# Play the media file
player.play()
```

## Common mistakes to avoid
Common mistakes to avoid when using the VLC library include:
* Not releasing system resources when finished with the player
* Not handling events properly, such as playback errors
* Not checking for errors when creating media files or players

## File and folder conventions
The VLC library does not have specific file and folder conventions, but it is recommended to follow standard Python naming conventions and organization. For example, media files can be stored in a `media` folder, and player configuration files can be stored in a `config` folder.