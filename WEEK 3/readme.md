## LLM Monitoring Using MongoDB
# Objective: The main objective of this experiment is to monitor LLM API usage and save the details in MongoDB Atlas. It records token usage, response time, estimated cost, and request status.

Project Folder Structure
1. .env -> Used to store the Gemini API key, MongoDB URL, and pricing values.
2. requirements.txt -> Used to install the required packages.
3. llm_client.py -> Provides Gemini and Ollama models and monitors their usage.
4. usage_logger.py -> Connects to MongoDB and saves LLM usage details.
5. test_client.py -> Tests the LLM client without calling the real API or MongoDB.
6. main.py -> The main runnable Python program.

How to run it
1. Activate the virtual environment.
2. Install the required packages:

       pip install -r requirements.txt
3. Create a MongoDB Atlas cluster and create a database user.
4. Add your current IP address in MongoDB Atlas Network Access.
5. Copy the MongoDB connection string and save it in the .env file with the Gemini API key.
6. Run the unit test:

          python -m unittest test_client.py
8. Run the main program:

         python main.py
10. Choose either gemini or ollama.
11. Enter the prompt. The AI gives the response and the usage details are saved in MongoDB.

For Ollama, download the model first:

        ollama pull llama3.2
 then 
      
      ollama run llama3.2
Expected output:-
In MongoDB Atlas, the llm_monitoring database and api_usage collection store one record for each request. It saves the provider name, model name, input tokens, output tokens, total tokens, response latency, estimated cost in USD, request status, and retry attempts.
