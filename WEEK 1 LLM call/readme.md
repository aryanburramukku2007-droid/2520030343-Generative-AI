LLM_API_CALL USING PYTHON
The main objective of this experiment is to use an AI model through an OpenAI API key.

First, I created the required files for the experiment:
1. .env -> Used to store my OpenAI API key safely. I should not share this key with anyone.
2. .gitignore -> Used to avoid pushing important files like .env into the repository.
3. requirements.txt -> Used to install the required packages.
4. main.py -> The main Python program.
Before running the code, I activated the existing virtual environment. If it was not active, I used:
..\.venv\Scripts\Activate.ps1
Then, I installed the required packages using:
python -m pip install -r requirements.txt
In the .env file, I saved my API key like this:
OPENAI_API_KEY=your_actual_openai_api_key
For this experiment, I used the OpenAI API. My ChatGPT account and OpenAI API credits are separate, so API billing or credits may be needed.

In the main.py program:
1. It loads the API key from the .env file.
2. It creates the OpenAI client.
3. It sends the prompt to the OpenAI model.
4. It receives and prints the AI answer.
I ran the program using:
python main.py
