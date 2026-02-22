# PersonalBot – Streamlit AI Chatbot using Gemini

PersonalBot is a simple AI-powered chatbot built using **Streamlit** and **Google Gemini**.  
The project demonstrates how a Python script can be converted into an interactive web application without any front-end development.

The chatbot accepts user queries, sends them to the Gemini model, and displays intelligent, real-time responses in a chat-style interface.

---

## Project Overview

Streamlit allows rapid development of web applications using pure Python.  
In this project:

- Streamlit is used to build the web interface.
- Google Gemini is used as the large language model.
- Environment variables are used to securely manage API keys.
- Session state is used to preserve chat history.

This project is ideal for beginners learning AI app development and rapid prototyping.

---

## Features

- Interactive chat-based interface
- Real-time AI responses using Google Gemini
- Persistent chat history using Streamlit session state
- Secure API key handling with `.env` file
- Simple and lightweight architecture
- Easy to extend and deploy

---

## Tech Stack

- Python 3.10+
- Streamlit
- Google Gemini (google-generativeai)
- python-dotenv

---


---

## Installation

Clone the repository:
Install dependencies:

pip install streamlit python-dotenv google-genai
API Key Setup

Create a .env file in the project directory and add:

GEMINI_API_KEY="your_api_key_here"

Note:
The API key is not included in this repository for security reasons.

# How the Application Works

The API key is loaded from the .env file.

The Gemini model (models/gemini-2.5-flash) is initialized.

User messages are captured using Streamlit input fields.

Messages are sent to Gemini for response generation.

Chat history is stored using st.session_state.

The interface refreshes after every interaction.

# Running the Application

Start the Streamlit app using:

python -m streamlit run app.py

The application will open in your browser at:

http://localhost:8501
Example Usage

Open the application in your browser.

Type a question or prompt.

Click Send.

The chatbot responds instantly.

Continue the conversation or refresh the page.

# Advantages

Rapid deployment of AI applications

No front-end development required

Clean and interactive user interface

High-quality AI responses using Gemini

Easy to scale and customize

# Future Enhancements

Add conversation memory across sessions

Deploy on cloud platforms

Add user authentication

Integrate external APIs or databases

Improve UI styling
