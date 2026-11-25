# Week 6 – LLM Baseline Evaluation

## About
In this practical, I created a basic LLM evaluation system using Python, Ollama and Llama 3.2. I prepared 30 questions with expected answers and keywords, then tested the model's responses.

## Technologies Used
- Python
- Ollama (Llama 3.2)
- VS Code
- JSON and CSV

## Project Files
- `golden_set.json` – Contains 30 questions and expected answers.
- `main.py` – Runs the LLM evaluation.
- `requirements.txt` – Required Python library.
- `baseline_results.csv` – Stores evaluation results.

## Execution
```bash
pip install -r requirements.txt
ollama pull llama3.2
python main.py
```

## Outcome
The program checks keyword matching, calculates scores, and classifies answers as PASS, REVIEW or ERROR. It generates `baseline_results.csv` automatically.

**Release Version:** v0.1
