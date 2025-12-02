# 🤖 Basic Greeting Agent — Google ADK

This project demonstrates how to build a simple AI Agent using Google's Agentic Development Kit (ADK). The agent greets the user, asks for their name, and responds with a personalized greeting.

## 🚀 Features

* Uses Google ADK to create a conversational agent
* Powered by Gemini 2.0 Flash model (`gemini-2.0-flash`)
* Minimal starter project — great for beginners
* Environment variable support using `.env`

## 🧠 Project Structure

```
1-basic-agent/
│
├── greeting_agent/
│   ├── __init__.py
│   ├── agent.py
│
├── example.env
└── requirements.txt
```

**Description**
* `greeting_agent/` — contains the main agent code
* `agent.py` — defines the root Google ADK agent
* `example.env` — example structure for environment variables
* `requirements.txt` — all dependencies required to run the project

## 📦 Installation

### 1️⃣ Clone the Repository

```bash
git clone <your-repository-url>
cd 1-basic-agent
```

### 2️⃣ Create a Virtual Environment

Recommended to avoid conflicts.

```bash
python -m venv .venv
```

**Activate it:**

* **Windows**
  ```bash
  .venv\Scripts\activate
  ```

* **MacOS / Linux**
  ```bash
  source .venv/bin/activate
  ```

### 3️⃣ Install Dependencies

Make sure `requirements.txt` contains:

```
google-adk[database]==0.3.0
yfinance==0.2.56
psutil==5.9.5
litellm==1.66.3
google-generativeai==0.8.5
python-dotenv==1.1.0
```

Then install:

```bash
pip install -r requirements.txt
```

## 🔑 Environment Setup

Create a `.env` file in the project root (next to `example.env`).

**Example:**

```env
GOOGLE_API_KEY=your_api_key_here
```

Replace `your_api_key_here` with your actual Gemini API key.

## 🧩 Agent Code Explanation

**greeting_agent/agent.py**

```python
from . import agent
from google.adk.agents import Agent

root_agent = Agent(
    name="greeting_agent",
    model="gemini-2.0-flash",
    description="Greeting-2.0-flash",
    instruction="""
    You are a helpful assistant that greets the user.
    Ask for the user's name and greet them by name.
    """,
)
```

✔ Defines a base agent  
✔ Uses Gemini model  
✔ Provides simple instruction-based behavior

## ▶️ Running the Project

You can run your agent using Python or ADK runner scripts, depending on your setup.

**Example:**

```bash
python greeting_agent/agent.py
```

**If you're using ADK CLI:**

```bash
adk run greeting_agent
```

> **Note:** Depending on your ADK integration, the entry point may vary.

## 🧪 How It Works

The agent:

1. Prompts the user for their name
2. Waits for input
3. Greets them: → `"Nice to meet you, Bipin!"`

## 💡 Tips

* Change the `instruction` field to customize how your agent behaves
* Use different models if you need more reasoning or memory
* Add tools, database connectors, or other modules as your agent evolves

## 📚 Useful Links

* 🔗 [Google ADK Documentation](https://developers.google.com/adk)
* 🔗 [Gemini API Documentation](https://ai.google.dev/docs)
* 🔗 [Official ADK Examples](https://github.com/google/adk-examples)

## 🤝 Contributing

Feel free to fork and enhance this tiny project — add tools, routing logic, or memory!

## 📜 License

This project can be shared and modified freely. Add a license file if you plan to open-source it publicly.