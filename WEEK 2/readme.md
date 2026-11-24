# WEEK-2 Gemini and Ollama
## Objective: The main objective of this project is to create one LLM client that can work with both Gemini and Ollama. Gemini works through an API key, and Ollama runs the Llama 3.2 model locally on my computer.

For this project, I created these files:
 1. .env -> Used to store my Gemini API key safely.
 2. requirements.txt -> Used to install the required packages.
 3. llm_client.py -> Provides a common interface for Gemini and Ollama.
 4. main.py -> The main runnable Python program.
 5. test_client.py -> Checks whether the LLM client is working correctly.

How to run

First, I downloaded and installed Ollama on my computer. Then I checked the version in PowerShell:
      
      ollama --version

After that, I downloaded the Llama 3.2 model:
      
      ollama pull llama3.2

I installed the Python packages using:
      
      pip install -r requirements.txt
Then I ran the program using:
      
      python main.py

The program asks me to choose either gemini or ollama. After selecting one provider, I enter my question and the AI gives the response.

In the llm_client.py program:
1. It creates a common interface for AI models.
2. GeminiProvider connects to Gemini using the API key.
3. OllamaProvider connects to the local Llama 3.2 model.
4. LLMClient sends the prompt through the selected provider.
In test_client.py, I used a fake provider to check whether the client returns the correct answer.
