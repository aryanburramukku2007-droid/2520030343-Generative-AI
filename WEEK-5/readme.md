## Token Economics Cost and Rate Limit Budgeting
# Objective: The main objective of this experiment is to estimate token usage, API cost, and rate limits before building an LLM application.

Project Folder Structure
1. .env -> Used to store planning values such as input price, output price, RPM limit, TPM limit, and budget limits.
2. requirements.txt -> Used to install the required package.
3. budget.py -> Calculates token usage, daily cost, monthly cost, RPM, TPM, and budget status.
4. test_budget.py -> Checks whether the budget calculations are working correctly.

How it works
1. Create and activate the virtual environment.
2. Install the required package:
pip install -r requirements.txt
3. Add the token prices, expected requests, average input and output tokens, RPM/TPM limits, monthly budget, and safety margin in the .env file.
4. Run the program:

        python budget.py
5. The program calculates input tokens per day, output tokens per day, total tokens, daily cost, monthly cost, peak RPM, and peak TPM.
6. It applies the safety margin and checks whether the API traffic is within the RPM, TPM, daily budget, and monthly budget limits.
7. It gives a recommendation showing whether the feature is within the configured planning limits or needs changes.

Run the test file using:
 
       python -m unittest test_budget.py
Expected Output
The program prints a Token Economics Report showing token usage, estimated daily and monthly cost, peak RPM, and peak TPM.

It also shows these checks:
- RPM capacity
- TPM capacity
- Daily budget
- Monthly budget
