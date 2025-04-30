# KinyarwandaAssistant
Mini Kinyarwanda Assistant

A simple voice-based AI assistant for Kinyarwanda that supports:

- Speech-to-Text (STT) using NeMo ASR
- NLP Question Matching using fuzzy logic
- Text-to-Speech (TTS) using gTTS or Hugging Face

Installation:

This project is designed to run on Google Colab. To run locally:

sudo apt-get -y install sox
pip install -r requirements.txt

Features:

1. STT:
   Converts user-recorded or uploaded Kinyarwanda audio into text.
   Uses mbazaNLP/Kinyarwanda_nemo_stt_conformer_model.

2. NLP Matching:
   Matches questions to pre-defined answers using fuzzywuzzy.

3. TTS:
   Converts responses into audio using gTTS or Hugging Face TTS models.

Usage on Colab:

- Upload or record a .wav file
- The assistant will transcribe, match, and speak the response

Hugging Face Login:

from google.colab import userdata
from huggingface_hub import login
login(userdata.get("SecretName"))

Fallback to gTTS if Hugging Face fails.

File Structure:

- mini_kinya_assistant.py
- requirements.txt
- README.txt

Acknowledgements:

- MbazaNLP, Digital Umuganda, Hugging Face, NeMo Toolkit

Made with love for the Kinyarwanda-speaking AI community.
