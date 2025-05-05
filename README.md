
# 🐳 Auto Dockerfile Generator with Local LLMs

A tool that generates production-ready Dockerfiles for any project using local Large Language Models (LLMs). Offline, fast, and intelligent — perfect for developers who want quick containerization without depending on cloud APIs.

## Features

- Supports multiple languages (Python, Dart, Node.js, etc.)
- Uses local LLMs — no internet needed
- Detects project type and structure automatically
- Outputs clean, ready-to-use Dockerfiles

##  How It Works

1. Clone the repo  
2. Install dependencies  
3. Point to your project folder  
4. Generates a Dockerfile

## Install dependencies

pip install -r requirements.txt

## Run your local LLM (e.g., using Ollama)

ollama run mistral


## Generate a Dockerfile

python generate_dockerfile.py

## Example Output

Generated Dockerfile:

```dockerfile
# Use the official Python 3.9 image as the base
FROM python:3.9-slim-buster AS builder

# Set the working directory in the container to /app
WORKDIR /app

# Install dependencies specified in requirements.txt
RUN pip install --trusted-host pypi.python.org -r requirements.txt

# Copy source code to the working directory
COPY . .

# Make port 8000 available to the world outside this container
EXPOSE 8000

# Run the command to start the development server when the container launches
CMD ["python", "app.py"]
```
