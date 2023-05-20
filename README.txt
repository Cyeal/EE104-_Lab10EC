Glenn Francisco
Due: 5-20-2023
EE104
Professor Christopher Pham
============================================================================================================================================================
Disclaimer: 
This file contains instructions and descriptions for the following programs. It includes steps for successfully operating each program without encountering errors, as well as video demonstrations for those who prefer visual aids. Please note that users who wish to run the programs will need to install previously uploaded libraries to Python to access a wider range of commands and programs.
============================================================================================================================================================
Youtube Links:
https://youtu.be/xGuxSGWMhNA

Github Links:


============================================================================================================================================================
References through this project:
https://www.twilio.com/blog/openai-gpt-3-chatbot-python-twilio-sms
https://www.python.org/
https://www.twilio.com/docs/usage/tutorials/how-to-use-your-free-trial-account
https://openai.com/
https://pypi.org/project/openai/
https://www.twilio.com/docs/libraries/python
https://palletsprojects.com/p/flask/
https://pypi.org/project/python-dotenv/
https://pypi.org/project/pyngrok/
https://platform.openai.com/api-ref

============================================================================================================================================================
The following modules should already be installed, but still useful to recommend:
-numpy
-scipy
-math
-matplotlib
-pint
-pandas
-pgzrun
-pygame
-pgzero
-sympy
-random
-heartpy
-tensorflow
-keras
-CUDA
-UPDATE NUMPY

mkdir chatgpt-sms-python
cd chatgpt-sms-python
python -m venv venv
venv\Scripts\activate
pip install openai twilio flask python-dotenv
pip install pyngrok
ngrok http 5000
cd chatgpt-sms-python
venv\Scripts\activate
python app.py

============================================================================================================================================================
Download the necessary libraries, users should open their Anaconda Powershell and follow the steps outlined below:
1) Open Anaconda Powershell Prompt
2) Type "pip install (missing module name)"
3) Allow the Powershell to install the module
4) Repeat the same steps for other modules
5) Once the module finishes downloading, the program should be ready to go!
6) If the program encounters any issues, try updating Spyder or restarting the IDE.

============================================================================================================================================================
Description and Brief Instructions of the following Programs:
============================================================================================================================================================
Part 1: SMS Chatbot

This guide explains how to create a simple SMS chatbot using Twilio and OpenAI's GPT-3.5 language model. The chatbot is built using Flask, a Python web framework, and it uses Twilio's messaging service to send and receive SMS messages. By leveraging the power of OpenAI's language model, the chatbot can generate responses to incoming messages.

A) Setting Up
	1. Clone the repository or create a new Python file.
	2. Install the necessary Python libraries by running the command "pip install flask twilio" in your project directory.
	3. Replace the placeholder "OPENAI_API_KEY" in the code with your actual OpenAI API key.
	4. Save the file with a .py extension, for example, "chatbot.py".

B) Running the Chatbot
	To run the chatbot, follow these steps:
	1. Open a terminal or command prompt.
	2. Navigate to the directory where the Python file is located.
	3. Run the command "python chatbot.py" to start the Flask server.

C) How It Works

	1. The Flask web application is set up with a single route ("/sms") that listens for incoming POST requests from Twilio.
	2. When an SMS message is received, Twilio sends the message details to the "/sms" route, and Flask captures it.
	3. The incoming message is retrieved from the request and converted to lowercase for consistency.
	4. The OpenAI GPT-3.5 language model is invoked with the incoming message as the prompt to generate a response.
	5. The response is extracted from the result obtained from the OpenAI API and stored.
	6. Twilio's MessagingResponse is created to compose the reply message.
	7. The generated response is added to the MessagingResponse object as the reply message.
	8. The MessagingResponse object is converted to a string and returned as the response to the Twilio request.
