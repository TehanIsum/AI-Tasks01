# AI-Tasks01

Simple OpenAI Chatbot

1. ### Setup Guide

* Sources
- Python 3.8 or above
- Git
- OpenAI account and API key

### Installation Steps

1. Create the repository**
cd AI-Tasks01
git remote add origin https://github.com/TehanIsum/AI-Tasks01.git

2. Install dependencies
pip3 install -r requirements.txt
touch .gitignore
pip3 install openai python-dotenv

3. Set up .env file

4. Run chat bot
python3 main.py

2. ### Introduction & How It Works
Overview
This project connects to OpenAI's GPT-4 model and allows the user to ask questions via the terminal. It uses the new openai Python SDK (v1+) and securely stores the API key using python-dotenv.

Features -
Interactive Q&A from terminal

Uses OpenAI GPT-4

.env to keep keys secret

Clean modular code

3. ### Logics
-- Core Logic Flow
Load API key from .env

Initialize OpenAI client

Take user input

Send request to GPT-4

Show the AI's response

Repeat until user exits

4. ### Mermaid Flowchart

flowchart TD
    Start([Start Program])

    LoadEnv["Load .env and API key"]

    InitClient["Initialize OpenAI Client"]

    Input["Wait for user input"]

    Send["Send question to OpenAI API"]

    GetResponse["Receive and format response"]

    Show["Display response to user"]

    CheckExit{"User typed 'exit'?"}

    End([Exit Program])

    Start --> LoadEnv --> InitClient --> Input
    Input --> Send --> GetResponse --> Show --> CheckExit
    CheckExit -- No --> Input
    CheckExit -- Yes --> End
5. ### Weaknesses & Future Improvements
-- Current Weaknesses
No conversation history (each question is isolated)

No error retry mechanism for failed API calls

Only works in terminal (no GUI or web interface)

Requires manual .env setup

--Future Enhancements
Add conversation memory (chat session)

Handle API errors more gracefully

Add a GUI (Tkinter or web with Flask)

Add logging and analytics

Use message history for better multi-turn dialogue

Add unit tests for stability

### Project Directory

AI-Tasks01/
├── main.py
├── .gitignore
├── .env (NOT pushed to GitHub)
├── requirements.txt
└── README.md ← this file

