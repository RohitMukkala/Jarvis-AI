# Jarvis-AI
Jarvis AI is a voice-activated personal assistant developed using Python, integrating speech recognition, OpenAI's GPT-3 API, and automation features. The project aims to replicate a basic version of the iconic Jarvis assistant from the Iron Man series, allowing users to interact with their computer through natural language voice commands.

# 1. Project Setup
## 1.1 Install Required Libraries
You need to install the required libraries using pip. Run the following commands:

```bash
pip install openai
pip install SpeechRecognition
pip install numpy
```
## 1.2 Setup OpenAI API Key
Sign up for an API key at OpenAI.
Store your API key in a config.py file for security.
config.py:

```python
apikey = "Your-Open-AI-Key"
```


# 2. Implementation Details
## 2.1 Chat Functionality
The chat(query) function integrates OpenAI’s GPT-3 API for generating responses to the user's queries. It keeps track of the conversation history, enhancing the interaction by maintaining context across multiple queries.

## 2.2 AI Functionality
The ai(prompt) function generates a response for a given prompt using GPT-3 and saves the response to a text file. It creates a directory named Openai to store the generated responses.

## 2.3 Voice Command Handling
The takeCommand() function uses speech_recognition to capture and transcribe voice commands from the user. The recognized text is returned and used to trigger various actions.

## 2.4 Command Processing
Opening Websites: If the user asks to open YouTube, Wikipedia, or Google, the script opens the corresponding site using the default web browser.
Playing Music: The script can play a specific song from a pre-defined path.
Time Query: If the user asks for the current time, the script fetches and vocalizes the time.
AI Queries: If the user requests an action using "artificial intelligence," the AI function processes the request.
Quitting: The script quits when the user says "Jarvis Quit."
2.5 Text-to-Speech
The say(text) function uses the os.system command to vocalize responses on macOS. You can replace this with pyttsx3 for cross-platform TTS.

# 3. Running the Jarvis AI Project
## 3.1 Execution
Save the code in a Python file, e.g., jarvis_ai.py.
Ensure the config.py file with your OpenAI API key is in the same directory.
Run the script using:
```bash
python jarvis_ai.py
```
## 3.2 Interaction
Speak commands into the microphone.
Jarvis will recognize, respond, and perform tasks like opening websites, answering AI-related queries, and playing music.

# 4. Potential Improvements
Error Handling: Implement try-except blocks around API calls and I/O operations for robustness.
Cross-Platform Compatibility: Replace os.system(f'say "{text}"') with a platform-independent TTS engine like pyttsx3.
Additional Features: Add more commands and functionalities, like sending emails, controlling IoT devices, etc.
