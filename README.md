# AI Recruiter

A multi-page Streamlit app that supports hiring tasks with a locally running LLM. The pages cover generating job descriptions, scanning and scoring resumes, interviewing candidates by voice, and generating MCQs. All LLM calls go to `llama3` through [Ollama](https://ollama.com) with `langchain_ollama`.

## Pages

| Page | What it does |
|---|---|
| `authenticator-mainpage.py` | Entry point. Shows the login page. |
| Platform Details | Describes the "AI based Ethical Hiring Platform" workflow steps. |
| Job Description Generator | Generates a job description with the LLM. |
| Resume Evaluator | Upload a PDF or Word resume and paste a job description. The LLM analyses how relevant the resume is and shows a candidate relevance score. |
| Resume Scanner | Upload a PDF or Word resume and the LLM turns it into structured data. |
| Repository Q&A | Asks questions about a GitHub repository, and lets you type your own answer. |
| AI-Interviewer | Voice interviewer that runs a chat with an Ollama model. |
| Dashboard | "Dashboard Slicer" page. |
| Customer Support Chatbot | Chat with the Ollama LLM. |
| Chat with Repo | Ask questions about a GitHub repository. |
| MCQ Generator | Generates multiple-choice questions by category and shows your score. |

## Tech stack

Python, Streamlit, LangChain (`langchain_ollama`), Ollama (`llama3`), PyTorch and `facenet-pytorch`, OpenCV, FastAPI, Gradio, PyMongo and `pyttsx3` (all listed in `requirements.txt`).

## Run

1. Install [Ollama](https://ollama.com) and pull the model: `ollama pull llama3`
2. Install the dependencies: `pip install -r requirements.txt`. The file is a full environment export, so you may prefer to install only the packages you need.
3. Start the app: `streamlit run authenticator-mainpage.py`
