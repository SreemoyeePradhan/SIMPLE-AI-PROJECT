# SIMPLE-AI-PROJECT
A beginner-friendly AI agent built using Python, LangChain, LangGraph, and OpenAI. Runs in the command line via VS Code and supports tool-based interactions like arithmetic calculations and greetings. Demonstrates prompt handling, tool execution, and live response streaming.
## PROJECT DETAILS
This project demonstrates the creation of a simple AI assistant using Python, built and run inside VS Code. It leverages the power of LangChain, LangGraph, and OpenAI's language models to build an interactive command-line agent capable of understanding user input and responding appropriately. The assistant is designed to perform basic tasks such as simple arithmetic calculations and greeting the user by name, showcasing how language models can be integrated with custom tool functions.

The assistant uses two tools: a calculator that adds two numbers and a say_hello function that generates a personalized greeting. These tools are defined using LangChain’s @tool decorator, which allows the AI model to intelligently select and invoke them based on the context of the user's natural language query. For example, if the user asks "What is the sum of 5 and 3?", the calculator tool is triggered automatically, and the model replies with the result.

Internally, the application uses OpenAI's ChatOpenAI class with a zero temperature setting to keep responses deterministic. The tools are registered and passed to LangGraph’s create_react_agent, which handles the reasoning and tool selection behind the scenes. The program runs in an infinite loop, taking user input from the terminal and streaming output from the assistant. It continues until the user types "quit" to exit.

Environment variables are managed using the python-dotenv package. The OpenAI API key is stored in a .env file and loaded at runtime using load_dotenv() for secure configuration. All necessary libraries including langchain, langgraph, openai, and dotenv can be installed via pip.
