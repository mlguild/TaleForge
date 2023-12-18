# ARCHITECTURE.md

## Overview

Zargonian's architecture comprises several key components, including a text interface for command input, a game engine for managing game state, and multiple layers for handling Speech to Text, Text to Speech, and Text to Image functionalities.

### Text Interface
This is the user's primary interaction point with the game. They input commands (e.g., 'go north', 'talk to character') and receive feedback (e.g., 'you see a castle', 'the character says hello').

### Game Engine
The game engine maintains the game state, including the world map, entity locations and states, and the user's current quest and inventory status.

### Speech to Text (Whisper)
This module listens to the user's voice commands and converts them into text that the game engine can understand.

### Text to Speech (ElevenLabs)
This module takes the game engine's textual feedback and converts it into spoken language.

### Text to Image (SDXL or SDXL-turbo)
This module generates images based on the game's narrative context.

### GPT3 Integration
This module uses GPT3 for dynamic narration and interaction, creating an immersive and ever-changing game experience.

## Workflow
The typical workflow of Zargonian is as follows:

1. The user issues a command via text or speech.
2. The Speech to Text module (if used) converts the spoken command into text.
3. The game engine processes the command, updates the game state, and generates a textual response.
4. The Text to Speech module converts the textual response into speech.
5. The Text to Image module generates an image based on the narrative context.
6. The user receives audio-visual feedback and the cycle repeats.

