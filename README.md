# Task Manager CLI Tool

A modular Python Command-Line Interface (CLI) application that allows users to manage tasks directly from the terminal.

This project demonstrates the integration of:

argparse for CLI command handling

Object-Oriented Programming (OOP)

Modular project structure

Input validation and error handling

## Features

The CLI tool allows users to:

Add tasks to a user

Mark tasks as complete

Receive helpful error messages

Interact through structured subcommands

All data is maintained in memory during runtime.

## Project Structure
course-7-module-7-python-cli-tool-lab/
│
├── lib/
│   ├── cli_tool.py
│   └── models.py
│
└── README.md

models.py contains the Task and User classes.

cli_tool.py contains CLI logic using argparse.

## Architecture Overview

This project separates concerns clearly:

1️⃣ Models Layer (OOP)

Task class

Stores task title

Tracks completion status

Handles marking tasks complete

User class

Stores user name

Maintains a list of tasks

Searches for tasks by title

2️⃣ CLI Layer

Uses argparse subparsers

Maps commands to functions

Calls class methods to execute logic

CLI commands trigger OOP methods, maintaining clean separation between user input and business logic.

## Installation

Ensure Python 3.8+ is installed.

Clone the repository:

git clone <your-repo-url>
cd course-7-module-7-python-cli-tool-lab

Navigate into the lib directory:

cd lib
▶️ Usage
Add a Task
python cli_tool.py add-task Alice "Write unit tests"

Output:

📌 Task 'Write unit tests' added to Alice.
Complete a Task
python cli_tool.py complete-task Alice "Write unit tests"

Output:

✅ Task 'Write unit tests' completed.
View Help
python cli_tool.py --help
🛑 Error Handling

The CLI provides clear error messages when:

A user does not exist

A task cannot be found

A task title is empty

Example:

❌ User 'Bob' not found.
⚠️ Important Note About Data Persistence

This tool maintains data in memory only.

Each time the script runs, the users dictionary resets.

Future improvements could include:

JSON file storage

Database integration

Task listing functionality

Task deletion

## Development Workflow

Feature branch used:

git checkout -b feature-cli-tool

Changes were committed and merged via Pull Request into main.

## Learning Objectives Demonstrated

CLI design with argparse

Subparsers and command mapping

Object-Oriented design

Separation of concerns

Input validation

Clean modular architecture

## Author

Lydia Khasoa
Python CLI Development Lab