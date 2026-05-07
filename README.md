ReAct Agent using Python
Overview

This project demonstrates a minimal implementation of a ReAct (Reasoning + Acting) Agent using Python. The agent accepts a user query, reasons through the problem step-by-step, calls a tool to perform an action, and returns the final answer.

The project is designed to run in Google Colab and can also be executed locally using Python.

Features
Simple ReAct workflow implementation
Step-by-step reasoning output
Tool calling support
Minimal and beginner-friendly code
Runnable in Google Colab
Easy GitHub integration
ReAct Workflow

The agent follows these steps:

User Query
Accepts input from the user
Thought
Reasons about what action to take
Action
Calls an external tool (calculator)
Observation
Receives tool output
Final Answer
Returns the response to the user
Project Structure
react-agent/
│
├── react_agent.ipynb
├── react_agent.py
├── README.md
└── screenshots/
    └── output.png
    Technologies Used
Python
Google Colab
Basic Python Functions
ReAct Agent Pattern
Sample Code
def calculator(expression):
    return eval(expression)

def react_agent(user_query):

    print(f"User Query: {user_query}")

    print("Thought: I should use the calculator tool.")

    expression = user_query.replace("What is", "").replace("?", "").strip()

    print(f"Action: calculator('{expression}')")

    result = calculator(expression)

    print(f"Observation: {result}")

    print(f"Final Answer: The answer is {result}")

query = "What is 25 * 4 + 10?"
react_agent(query)
Sample output
User Query: What is 25 * 4 + 10?

Thought: I should use the calculator tool.

Action: calculator('25 * 4 + 10')

Observation: 110

Final Answer: The answer is 110

How to Run
Option 1 — Google Colab
Open Google Colab
Upload or paste the notebook code
Run all cells
Option 2 — Local Python

Install Python and run:
</> Bash
python react_agent.py
