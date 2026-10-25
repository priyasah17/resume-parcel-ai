\# Resume Parcel — AI-Powered Resume Screening



Resume Parcel is a Python-based resume screening and job-matching tool that uses a Large Language Model (LLM) to extract candidate information, compare resumes against a job description, and rank candidates by their AI-generated match scores.



\## Features



\- \*\*Multi-resume processing:\*\* Process multiple PDF and DOCX resumes in one run.

\- \*\*Resume parsing:\*\* Extract candidate names, skills, education, experience, projects, and certifications.

\- \*\*Job description analysis:\*\* Extract required skills, preferred skills, education requirements, and responsibilities.

\- \*\*AI-powered matching:\*\* Compare candidate profiles against job requirements using the Groq API.

\- \*\*Candidate ranking:\*\* Sort candidates by their match scores and display the highest- and lowest-scoring candidates.

\- \*\*Structured outputs:\*\* Use Pydantic models to validate extracted job and resume information.



\## Tech Stack



\- Python

\- Groq API

\- LLM-based information extraction and matching

\- Pydantic

\- PyPDF

\- python-docx

\- python-dotenv



\## Project Structure



```text

Resume-Parcel/

├── job\_parser.py

├── requirements.txt

├── README.md

├── .gitignore

├── .env.example

└── resumes/           # Local test files; excluded from Git

```



\## Setup and Installation



\### 1. Clone the repository



```bash

git clone YOUR\_GITHUB\_REPOSITORY\_URL

cd Resume-Parcel

```



\### 2. Create a virtual environment



Windows PowerShell:



```powershell

python -m venv .venv

.\\.venv\\Scripts\\Activate.ps1

```



\### 3. Install dependencies



```powershell

python -m pip install -r requirements.txt

```



\### 4. Configure the API key



Create a `.env` file in the project root:



```env

GROQ\_API\_KEY=your\_groq\_api\_key

```



Never commit your actual API key.



\### 5. Add resumes locally



Create a folder named `resumes` in the project root and place your test PDF or DOCX files inside it.



\### 6. Run the application



```powershell

python job\_parser.py

```



The script analyzes the configured job description, processes supported resumes, generates match scores, and prints ranked candidate results.



\## Current Limitations



\- The job description is currently defined in the Python script.

\- Resume files must be placed in the local `resumes` folder.

\- Matching scores are LLM-generated estimates, not validated measures of hiring suitability.

\- Results may vary depending on the resume content and model output.

\- The current version is command-line based; a web interface is a potential future enhancement.



\## Responsible Use



Use candidate information only with appropriate permission. Review AI-generated results manually, protect personal information, and do not use match scores as the sole basis for hiring decisions.



\## Future Enhancements



\- Streamlit-based resume upload interface

\- User-provided job descriptions

\- Downloadable candidate ranking reports

\- Improved scoring validation and evaluation

\- Database integration and candidate history



