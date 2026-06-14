# AI Career Copilot

AI Career Copilot is a complete machine-learning product for resume analysis, job matching, interview preparation, and career improvement planning.

It helps students and job seekers answer four important questions:

- Is my resume ATS-friendly?
- How well do I match a job description?
- Which skills am I missing?
- How should I prepare for interviews?

## Features

- Resume upload and parsing for PDF, DOCX, TXT, and pasted text
- ATS resume score with detailed improvement suggestions
- Job match score using NLP keyword and TF-IDF similarity analysis
- Missing skills and strength analysis
- Personalized technical, HR, and behavioral interview questions
- AI-style interview answer evaluation
- Learning roadmap for missing skills
- Streamlit dashboard for an interactive demo
- FastAPI backend for API-based integration

## Tech Stack

- Python
- Streamlit
- FastAPI
- Scikit-learn
- Pandas
- PyPDF
- python-docx

## Project Structure

```text
ai-career-copilot/
  app/
    streamlit_app.py
  api/
    main.py
  src/
    career_copilot/
      analyzer.py
      interview.py
      parser.py
      roadmap.py
      schemas.py
      skills.py
  sample_data/
    job_description.txt
    sample_resume.txt
  tests/
    test_analyzer.py
  requirements.txt
  README.md
```

## Quick Start

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it:

```bash
# Windows
.venv\Scripts\activate

# macOS/Linux
source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the Streamlit app:

```bash
streamlit run app/streamlit_app.py
```

Run the FastAPI backend:

```bash
uvicorn api.main:app --reload
```

Then open:

- Streamlit: http://localhost:8501
- FastAPI docs: http://localhost:8000/docs

## How It Works

1. The user uploads or pastes a resume.
2. The user pastes a job description.
3. The system extracts skills from both texts.
4. It calculates ATS quality and job match scores.
5. It identifies missing skills and strengths.
6. It generates interview questions from the job role and gaps.
7. It evaluates interview answers using skill coverage, clarity, relevance, and STAR structure.
8. It creates a learning roadmap for career improvement.

## Machine Learning Concepts Used

- NLP text cleaning and tokenization
- Skill extraction using domain taxonomy matching
- TF-IDF vectorization
- Cosine similarity
- Recommendation logic
- Generative-style question generation
- Heuristic answer scoring

## Future Improvements

- Add Sentence Transformers for deeper semantic similarity
- Add PostgreSQL user accounts and score history
- Add FAISS for large-scale job search
- Add LLM-based feedback using OpenAI or another model provider
- Add charts for interview progress and skill growth

## GitHub Push Commands

```bash
git init
git add .
git commit -m "Initial commit: AI Career Copilot"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/ai-career-copilot.git
git push -u origin main
```

