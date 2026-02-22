# MCP Context Sharing Server (Python)

A lightweight multi-agent context sharing server built using the Model Context Protocol (MCP).  
This project demonstrates how multiple agents (AI assistants, applications, or processes) can store, retrieve, and share contextual information such as user preferences, chat history, or instructions through a centralized MCP server.

The server exposes callable tools and is tested using the MCP Inspector GUI.

---

## Features

- Multi-agent context storage  
- Global context search (case-insensitive)  
- View all stored contexts  
- MCP-compatible tool interface  
- Inspector GUI support for testing  
- Simple in-memory data store (easy to extend to files or databases)

---

## Project Overview

In this project:

1. An MCP server is built in Python.  
2. Agents push context data to the server.  
3. Clients search and retrieve stored context.  
4. Tools are exposed via MCP.  
5. The server is tested interactively using MCP Inspector.

This project is intended as a learning and portfolio project for understanding:

- MCP fundamentals  
- Tool-based APIs  
- Async Python  
- Multi-agent architectures  

---

## Tech Stack

- Python 3.10+  
- MCP (FastMCP)  
- Async programming  
- MCP Inspector GUI  

---




## Installation

## 1. Clone or download this repository

bash
git clone <<YOUR_GITHUB_REPO_LINK>>
cd mcp-context-sharing

## 2. Install dependencies
pip install mcp[cli]

Running the Server

From the project root:

python src/server/main.py

You should see:

MCP server started...

Keep this terminal open.

Launch MCP Inspector

Open a new terminal window:

mcp dev src/server/main.py

The Inspector GUI opens at:

http://localhost:3000
Connecting in Inspector

In the MCP Inspector GUI:

Transport: STDIO

Command: python

Arguments: src/server/main.py

Click Connect.

After connecting, open the Tools tab.

# Available Tools
share_context

Stores context for a given agent.

Inputs:

agent (string)

content (string)

retrieve_context

Searches all stored context by keyword.

## Inputs:

query (string)

list_all_context

Returns all stored contexts from every agent.

## Example Use Cases

Sharing memory between AI agents

Storing user preferences

Managing conversation history

Prototyping multi-agent systems

Learning MCP and tool-based APIs
