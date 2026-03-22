# AI assistant

# Todoist AI Assistant (CLI)

## Project Description

This project is a simple command-line (CLI) assistant that integrates with Todoist and allows you to manage tasks using natural language.

The application uses the Google Gemini language model (`gemini-2.5-flash`) along with the LangChain framework to interpret user input and perform appropriate task operations.

---


## How It Works

The program runs in a loop:

1. The user enters a command in the terminal  
2. The language model analyzes the intent  
3. The agent selects the appropriate tool:
   - `add_task` → adds a task to Todoist  
   - `show_tasks` → retrieves all tasks  
4. The result is displayed to the user  

The agent is built using LangChain’s `tools-based agents` (`create_openai_tools_agent`).

---

## Tech Stack

- Python  
- LangChain  
- Google Gemini API  
- Todoist API  
- python-dotenv  

---

## Requirements

To run the project, you need:

- A Todoist API key (`TODOIST_API_KEY`)  
- A Gemini API key (`GEMINI_API_KEY`)  

Create a `.env` file in the project directory and add:

```env
TODOIST_API_KEY=your_todoist_api_key
GEMINI_API_KEY=your_gemini_api_key

```
## Example usage

You: Add a task: buy milk
Assistant: Task has been added.

You: show tasks
Assistant:
- buy milk
- learn LangChain

