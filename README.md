F.R.I.D.A.Y - Personal Voice Assistant
F.R.I.D.A.Y is a Python-based personal voice assistant that can perform various tasks like opening websites, sending emails, playing music, fetching current time/date, and providing motivational quotes. It can also retrieve data from Wolfram Alpha or Wikipedia.

Features
Voice Recognition: Uses SpeechRecognition library to capture and recognize voice commands.
Text-to-Speech (TTS): Uses Pyttsx3 to convert text responses into speech.
Web Browsing: Opens websites like YouTube, Google, and Gmail.
Email Sending: Sends emails via SMTP after recognizing the recipient and content.
Music Playback: Plays random or specific tracks from a predefined music folder.
Motivational Quotes: Provides random motivational quotes.
Wolfram Alpha & Wikipedia Queries: Fetches information from Wolfram Alpha (if available) or Wikipedia.
Current Time & Date: Tells the current time or date.
Greetings: Offers personalized greetings based on the time of day.
Requirements
To run this assistant, you need to install the following Python packages:

pyttsx3: For text-to-speech conversion
bash
Copy code
pip install pyttsx3
webbrowser: To open websites
smtplib: For sending emails via SMTP
random: To randomly select motivational quotes or music
speech_recognition: For recognizing spoken commands
bash
Copy code
pip install SpeechRecognition
wikipedia: To retrieve summaries from Wikipedia
bash
Copy code
pip install wikipedia
wolframalpha: For fetching results from Wolfram Alpha
bash
Copy code
pip install wolframalpha
Setup
Wolfram Alpha API: You need to create a Wolfram Alpha account and obtain an API key. Replace 'LRWJW6' in the script with your own key.
SMTP Email Settings: Configure the smtplib settings to match your email credentials (Username, Password).
Music Folder: Add your music files to the directory specified in music_folder.
Usage
Run the script in your Python environment.
The assistant will greet you and ask for commands.
Speak into your microphone to give commands. F.R.I.D.A.Y will recognize the command and execute the appropriate task.
Supported commands:
Open websites: "open youtube", "open google", "open gmail"
Ask for time/date: "what time is it", "what date is it"
Play music: "play music", "play english songs", "play tamil songs", etc.
Send an email: "email me", etc.
Get motivational quotes: "Tell me motivation quotes", "motivate me"
Search information: Any general query will be fetched via Wolfram Alpha or Wikipedia.
Customization
You can modify the list of motivational quotes or music tracks in the corresponding sections.
You can add more functions or improve existing ones by expanding the command checks inside the if-elif block.
Notes
Ensure that your microphone and speakers are properly set up for voice recognition and TTS functionalities.
You can modify or extend the functionalities by adding new commands and integrating additional APIs.
