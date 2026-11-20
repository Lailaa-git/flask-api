# Flask API – Building, Testing, and Containerizing

## Project Description

This project is a REST API built with Python and Flask. It contains a health check endpoint that returns the status of the API in JSON format.

**Endpoint:**
- GET /health

**Example response:**
json
{
  "status": "ok"
}

## Requirements

- Python
- Flask
- Docker Desktop
- pytest

## Run Locally
1. Create and activate a virtual environment:

python3 -m venv venv
source venv/bin/activate


2. Install dependencies:

pip install -r requirements.txt


3. Start the application:

python app.py


4. Open http://127.0.0.1:5001/health
   
## Run Tests
Run the automated test with:
pytest


The test checks the HTTP status code and JSON response.

## Run with Docker
1. Build the Docker image:

docker build -t flask-api .


2. Start the container:

docker run -d --name flask-api-container -p 5002:5001 flask-api


3. Open http://127.0.0.1:5002/health
   
## Project Structure
flask-api
- app.py
- test_app.py
- requirements.txt
- Dockerfile
- .dockerignore
- README.md


## Technologies
- Python
- Flask
- pytest
- Docker
