# 🌿 Energeiaa Wellness AI

**An AI-powered wellness application that generates personalized health and wellness reports using user profiles, symptoms, medical parameters, and observations.**

## Overview

Energeiaa Wellness AI is a Python-based web application designed to analyze health-related inputs and generate personalized reports using AI-powered agents. It combines structured patient information, symptom analysis, and medical datasets to provide organized wellness insights through a web interface.

The application is built using FastAPI and integrates with Groq's language models for AI-powered processing.

## Features

- **AI-Powered Wellness Reports:** Generate reports from user health profiles and observations.
- **Patient Profile Analysis:** Process age, gender, occupation, and medical history.
- **Symptom Analysis:** Analyze symptoms such as fever, cough, and fatigue.
- **Medical Parameter Processing:** Incorporate parameters such as blood pressure and cholesterol.
- **Dataset Analysis:** Load and explore patient records from a CSV dataset.
- **Web Interface:** Access application features through HTML templates and static assets.
- **REST API:** Interact with application endpoints through FastAPI.
- **API Documentation:** Explore available endpoints using Swagger UI.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Core application logic |
| FastAPI | Web framework and REST APIs |
| Uvicorn | ASGI server |
| Groq API | AI-powered language processing |
| Pandas | Dataset processing |
| Pydantic | Input validation and data schemas |
| Jinja2 | HTML templating |
| HTML, CSS, JavaScript | Web interface |

## Project Structure

```text
Flexi-Project-Energeiaa/
├── agents/                              # AI agent modules
├── models/                              # Data schemas and models
├── static/                              # CSS, JavaScript, and assets
├── templates/                           # HTML templates
├── utils/                               # Utility functions
├── main.py                              # FastAPI application entry point
├── requirements.txt                     # Python dependencies
├── Disease_symptom_and_patient_profile_dataset.csv
├── test_agent.py                        # Agent tests
├── test_dataset.py                      # Dataset tests
├── .gitignore                           # Git exclusions
└── README.md                            # Project documentation
```

## ⚙️ Prerequisites

Before running the project, install:

- Python 3.10 or a compatible version supported by the dependencies
- Git (optional, if cloning the repository)
- A Groq API key

##  Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/sonalika-singha/Flexi-Project-Energeiaa.git
cd Flexi-Project-Energeiaa
```

Alternatively, download and extract the ZIP file, then open the extracted project folder in VS Code.

### 2. Create a virtual environment

**Windows PowerShell:**

```powershell
python -m venv venv
```

### 3. Activate the virtual environment

```powershell
.\venv\Scripts\Activate.ps1
```

If activation is successful, `(venv)` will appear at the beginning of your terminal prompt.

### 4. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 5. Configure the Groq API key

Create a `.env` file in the project root directory, alongside `main.py`.

Add the following:

```dotenv
GROQ_API_KEY=your_groq_api_key_here
```

Replace the placeholder with your own API key from the [Groq Console](https://console.groq.com/keys).

**Security note:** Never commit your `.env` file or expose your API key publicly.

### 6. Start the application

```bash
uvicorn main:app --reload
```

When the server starts successfully, the terminal will display a local address.


## API Endpoints

The application defines the following endpoints in `main.py`:

| Method | Endpoint | Description |
|---|---|---|
| GET | `/` | Serves the home page |
| GET | `/health` | Checks application status |
| POST | `/generate-report` | Generates a wellness report from structured health inputs |
| GET | `/report` | Serves the report page |
| GET | `/dataset` | Serves the dataset page |
| GET | `/dataset-patients` | Returns patient records from the dataset |
| POST | `/run-dataset-patient` | Generates a report using a selected dataset patient |

## Testing

The repository includes test files for agent functionality and dataset-related operations.

Run:

```bash
python test_agent.py
python test_dataset.py
```

These commands execute the test scripts. Ensure the required dependencies and configuration are available before running them.

## Environment Variables

| Variable | Description |
|---|---|
| `GROQ_API_KEY` | API key used for Groq integration |

Keep secrets in environment variables rather than hardcoding them in Python files.



**Build Command**
```bash
pip install -r requirements.txt
```

**Start Command**
```bash
uvicorn main:app --host 0.0.0.0 --port $PORT
```

Add `GROQ_API_KEY` in the hosting platform's environment-variable settings before deployment.



## Author

**Sonalika Singha**

GitHub: [@sonalika-singha](https://github.com/sonalika-singha)

---

*Built as an AI-powered wellness project exploring intelligent agents, health data processing, and web application development.*
