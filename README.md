
# Neuro shell

AI Task Agent is a Visual Studio Code extension designed to streamline and automate development tasks using natural language. Just describe what you want, hit F5, and let the AI generate, refine, and execute shell commands to accomplish the job for you — all while running on your local Python backend powered by OpenRouter or OpenAI.

Ideal for developers who want to speed up repetitive tasks, fix issues, or prototype ideas, this tool combines the power of LLMs with native shell execution and a customizable Python backend.

#  🚀 How to Use (VS Code Extension)
🧩 Prerequisites
VS Code

Node.js & npm

Python 3.8+

Your .env file with OpenAI API key and base URL.

Backend files (included in this repo)

# ⚙️ Setup & Run
npm install

npm run compile

F5

You’ll see a new command in the command palette:
“Run AI Task Agent”

# 📦 Backend Setup (Python)
1. Create and activate a virtual environment:
    
    python -m venv venv

source venv/bin/activate  
#On Windows:venv\Scripts\activate

2. Install dependencies:

pip install -r requirements.txt

3. Create a .env file:
API_KEY=your_openai_or_openrouter_api_key
API_URL=https://api.openai.com/v1/chat/completions  # or OpenRouter's URL
COMMAND_TIMEOUT=30

4. Run a task:

python agent.py "Enter your task here"

# 🧪 Example Tasks
->"Install numpy and create a requirements.txt"

->"Initialize a git repo and make first commit"

->"Create a Flask app with hello world"

# 🧠 How It Works.
->You input a task via the extension.

->The backend (agent.py) generates a shell command plan using GPT.

->You approve the plan.

->Commands are executed sequentially.

->If a command fails, you provide feedback.

->The AI refines the plan and tries again.


