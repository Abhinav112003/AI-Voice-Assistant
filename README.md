# README for Python Voice Assistant (FRIDAY)

## Overview
This project implements a personal voice assistant named **FRIDAY** using Python libraries such as `pyttsx3`, `speech_recognition`, `webbrowser`, `wikipedia`, `datetime`, `wolframalpha`, and others. FRIDAY is designed to listen to voice commands, perform tasks, and respond with spoken replies. It can open websites, fetch information from Wikipedia or WolframAlpha, play music, and more.

## Features
### Voice Commands Supported:
1. **Opening Websites**: FRIDAY can open:
   - YouTube (`open youtube`)
   - Google (`open google`)
   - Gmail (`open gmail`)
   
2. **Check the Time/Date**: FRIDAY will tell you the current time or date with commands like:
   - "What time is it?"
   - "What date is it?"

3. **Conversations**: 
   - You can ask FRIDAY how it's doing ("How are you?" or "What's up?").
   - FRIDAY also responds to a simple "Hello."

4. **Motivational Quotes**: If you need a boost, ask for motivational quotes:
   - "Tell me motivation quotes."
   - "Motivate me."

5. **Send Email**: 
   - Command: "Email" followed by recipient and message.
   - Requires configuration of the email credentials.

6. **Play Music**: FRIDAY can play specific music files based on the language or general request.
   - "Play music" or "Play songs"
   - Specific music by language: "Play English music", "Play Tamil music", "Play Hindi music"

7. **General Search**: FRIDAY can search for answers using WolframAlpha or Wikipedia:
   - If it fails to find information, it will redirect to Google search.

8. **End the Session**: FRIDAY can stop if you say:
   - "Nothing", "Abort", "Stop", or "Bye."

## Prerequisites
Ensure that the following Python libraries are installed:
```bash
pip install pyttsx3 SpeechRecognition wikipedia wolframalpha
```

### Additional Configuration:
1. **WolframAlpha API**: 
   - Replace `'LRWJW6'` with your own WolframAlpha API key. Sign up [here](https://developer.wolframalpha.com/).
   
2. **Email Setup**: 
   - Update the following with your Gmail credentials to enable email functionality:
     ```python
     server.login("Your_Username", 'Your_Password')
     server.sendmail('Your_Username', "Recipient_Username", content)
     ```

3. **Music Folder**: 
   - Update the path `'S:\\AI\\music\\'` to point to your music folder.

## How It Works

### 1. Initialization:
- The voice assistant uses `pyttsx3` to convert text to speech.
- The assistant greets you based on the time of day using `datetime`.

### 2. Voice Input:
- It listens for voice commands using `speech_recognition` and converts them to text for processing.

### 3. Command Processing:
- Based on the recognized command, FRIDAY performs a corresponding action (e.g., opening a website, searching for information, playing music).

### 4. Responding to Queries:
- For general knowledge queries, it uses WolframAlpha or Wikipedia to fetch and speak the answers.
- For motivational quotes, random quotes are provided from a predefined list.

### 5. Continuous Listening:
- After every action, FRIDAY asks for further commands and continues listening until the user says a termination command.

## Customization:
- **Modify the Voice**: Change the voice engine settings in the following lines:
   ```python
   voices = engine.getProperty('voices')
   engine.setProperty('voice', voices[len(voices)-1].id)
   ```
   To change the voice, try using different indexes for `voices[]`.
   
- **Add New Commands**: You can easily extend FRIDAY by adding new `elif` conditions in the main loop.

## Example Use Case:
- User: "Open YouTube"
- FRIDAY: Opens YouTube in the default browser.

- User: "What time is it?"
- FRIDAY: Tells the current time.

- User: "Play English music."
- FRIDAY: Plays a random English song from the specified music folder.

## Known Issues:
- **Speech Recognition Errors**: In noisy environments, speech recognition may fail to correctly interpret the commands.
- **Email Sending**: Requires proper configuration and may not work if Google blocks the sign-in attempt. Make sure to allow less secure apps to sign in if using Gmail.

## How to Run:
1. Install all required libraries.
2. Configure the email and WolframAlpha keys.
3. Run the script.
4. Speak commands to interact with FRIDAY!

