# LF5.4: Writing the Logic

## 👥 Epic User Story

> As IT Consultants,  
> we want to implement the core logic of our system using appropriate programming paradigms and containerize the application,  
> so that we can deliver a functional, easily deployable prototype to our stakeholders without "it works on my machine" excuses.

## 🎉 Celebration Criteria (Core Competencies)

- We can **select** and **justify** the appropriate programming paradigms for different parts of our solution. (K5)
- We **know how to develop** an automated environment setup script using Bash. (K5)
- We can **implement** the core business logic in Python based on our analog architecture blueprints from LF5.2. (K4)
- We can **containerize** our Python application using a custom Dockerfile to ensure consistent deployment. (K6)

## 🧩 Comprehensive Task: The Prototype (13 SP)

**The Mission:** It is time to build! Using your UML and PAP blueprints from Epic 5.2, you will now write the actual code for your chosen scenario (Neustadt Museum, Mutti's Bakery, or Metropolis Library). You will write a Bash script to prepare the OS, implement the core logic in Python, and finally wrap the entire application in a Docker container.

### Tasks:

1. **The Setup Script (Bash):** Write a Bash script (`setup.sh`) that automates the preparation of the Ubuntu environment. It should create a specific directory structure for your project (e.g., `src/`, `data/`, `logs/`), create empty placeholder files, and output a success message.
2. **The Data Structure (Python OOP):** Based on your UML Class Diagram, write the Python classes for your core entities (e.g., `Artifact` for the Museum, `Recipe` for the Bakery). Implement the `__init__` methods and encapsulation logic.
3. **The Core Algorithm (Python Procedural):** Based on your PAP/Structogram, write a Python script (`main.py`) that executes the main logic (e.g., calculating ingredient amounts, validating a book loan). This script must instantiate objects from your classes and use them.
4. **Containerization (Docker):** Write a `Dockerfile` that uses an official Python base image. It must copy your Python scripts into the container and execute `main.py` automatically when the container starts.
5. **Deployment & Run:** Build the Docker image on your Ubuntu machine and run it as a container. Take a screenshot of the successful terminal output showing your prototype in action, and document the build/run commands in your Docmost instance.

## 📦 Result Artifact

A GitHub repository containing the complete source code (`setup.sh`, `main.py`, class files) and the `Dockerfile`, alongside a documentation page in Docmost showing screenshots of the running Docker container.