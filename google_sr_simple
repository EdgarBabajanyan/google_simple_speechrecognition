# The first step is to import Speech recognition because it is a dependency. Install by running pip and typing    "pip install SpeechRecognition"
import speech_recognition as sr 

# The next step is the actual important part which is where google sr obtains the speech as a query
# You do this by creating a function. I chose "takeCommand" as the function
# As you can see below, you assign the recognizer to a variable
# You open the microphone up with the statement below the variable line
# You can only use the microphone when Pyaudio is installed     You do this by typing "pip install pyaudio" in a terminal or the ide terminal
# You do require an exception handler incase anything was missed by google.

def takeCommand():
    r = sr.Recognizer()

    with sr.Microphone() as source:

        print("Listening...")
        r.pause_threshold = 1
        audio = r.listen(source)

    try:
        print("Recognizing...")
        query = r.recognize_google(audio, language='en-us')
        print("User said: {query}\n")

    except Exception as e:
        print(e)
        print("Google didn't Understand.")
        return "None"

    return query
    
    # This can be used many different ways. If any questions come up, please tell me and I can even provide samples of programs featuring this!
