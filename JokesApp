import requests
import pyttsx3
import speech_recognition as sr

r= sr.Recognizer()
mic = sr.Microphone()

engine = pyttsx3.init()
engine.setProperty('rate',175)

def take_input():
	with mic as source:
		r.adjust_for_ambient_noise(source)
		audio = r.listen(source)
	speech = r.recognize_google(audio)
	return speech

def text_to_speech(text):
	engine.say(Joke)
	engine.runAndWait()
	engine.stop()

print("Waiting for input: ")
input = take_input()
print(input + "\n")

while True:
	if "joke" in input or "funnu" in input:
		response= requests.get('https://icanhazdadjoke.com', headers={'Accept':'application/json'})
		Joke = response.json()['joke']
		print(Joke)
		text_to_speech(Joke)
		continue

	if "close" in input  or "quit" in input:
		engine.stop()
		exit()
	engine.stop()
