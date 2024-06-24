

# Speech-to-Speech Translation System

This project provides a real-time speech-to-speech translation system using AssemblyAI for speech transcription and ElevenLabs for voice generation. It's designed to transcribe speech in one language, translate it to another language, and then synthesize the translated text into speech.

## Structure

The project is structured as follows:

- `README.md`: This file.
- `S2S/`: Contains the main Python script and its README.
  - `README.md`: Provides information specific to the S2S script.
  - `S2S.py`: The main script for speech-to-speech translation.
- `speech2speech_code.ipynb`: A Jupyter notebook version of the S2S script for interactive use.

## Dependencies

- AssemblyAI: Used for real-time speech transcription.
- ElevenLabs: Utilized for generating speech from text.
- `langchain_openai`: For translation leveraging OpenAI's GPT models.
- `langchain_core`: Core functionalities for running and parsing outputs.

## Setup

1. **Install Required Libraries**: Ensure you have Python installed and then install the required libraries using pip:

   ```sh
   pip install assemblyai elevenlabs langchain_openai langchain_core


2.**API Keys**: You need to obtain API keys from AssemblyAI, ElevenLabs, and OpenAI. Once obtained, replace the placeholders in S2S/S2S.py with your actual API keys.
Usage
Running the Script
Navigate to the S2S directory and run:

This will start the speech-to-speech translation system. Speak into your microphone, and the system will transcribe, translate, and generate speech from the translated text.

If you prefer an interactive approach, open speech2speech_code.ipynb in Jupyter Notebook or JupyterLab. Ensure you have Jupyter installed:

pip install notebook

Run the notebook cells in order to start the system interactively.

Functions Overview

*translate(sentence, language="French"): Translates the given sentence to the specified language.
*gen_dub(text): Generates audio from the given text using ElevenLabs.
*on_open(session_opened): Called when the transcription session is established.
*on_data(transcript): Called when a new transcript is received. It handles transcription, translation, and speech generation.
*on_error(error): Called when an error occurs in the transcription session.
*on_close(): Called when the transcription session is closed.

# Closing the Session
To close the session gracefully, ensure you call transcriber.close() at the end of your session.

# Contributing
Contributions to this project are welcome. Please ensure you follow the coding standards and submit pull requests for any enhancements.