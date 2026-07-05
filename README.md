# 🌦️ Monsoon Laundry Concierge: Autonomous AI Agent

An intelligent, context-aware AI agent built using the Google GenAI SDK and the Gemini 2.5 model. This application acts as a dynamic household concierge that autonomously reasons through fabric constraints, hygiene rules, and real-time environmental data to optimize laundry schedules during unpredictable monsoon seasons.

## 🚀 Key Features

* **Advanced System Prompting:** Constrained by strict logical routing rules to isolate baby clothes for hygiene, protect delicate silks, separate colors, and prioritize uniform readiness.
* **Autonomous Function Calling (Tools):** Integrates an external Python tool to simulate/fetch local weather data based on user input. 
* **Dynamic Decision Trees:** The agent reads data from the weather tool and completely rewrites its plan on the fly—switching from outdoor sunlight drying to indoor dehumidifier/fan strategies if precipitation is detected.
* **Production-Safe Security:** Built using secure environment variable sourcing via Kaggle Secrets to prevent API key exposure in version control.

---

## 🛠️ Architecture & Tech Stack

The system moves away from traditional static prompts and utilizes an **Agentic Workflow** where the Large Language Model determines its own execution steps based on user variables.

* **Core Model:** Gemini 2.5 (`gemini-2.5-flash`)
* **Language & SDK:** Python, Google GenAI SDK
* **Environment:** Jupyter Notebook / Kaggle Environment
* **Key Concept:** Function Calling / Tool Use

---

## 📂 Project Structure

* `notebook.ipynb` - The complete implementation containing the agent instructions, the Python weather tool, and execution cells.
* `README.md` - Technical project documentation and architectural breakdown.

---

## ⚙️ Installation & Usage

To run this agent locally or inside a Jupyter workspace:

1. Clone this repository:
   ```bash
   git clone [https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPO_NAME.git](https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPO_NAME.git)

2. Install the official Google GenAI library:
   ```bash
    pip install google-genai

3. Initialize your API key securely as an environment variable:
   ```bash
    import os
    os.environ["GEMINI_API_KEY"] = "your_actual_api_key_here"

5. Run the workspace cells sequentially to spin up the agent workspace and execute custom laundry lists.


## 📊 Sample Output Analysis:
​  When tested with a target location experiencing a shift from heavy rainfall to sunny intervals, the agent successfully executed the following plan:
​  Automatically invoked the weather tool to gather real-time regional metrics.
​  Sorted delicate silk fabrics into non-tumble, flat-dry protocols away from direct UV exposure.
​  Isolated infant clothing into high-temperature, sanitization-focused wash queues.
​  Strategically delayed or prioritized specific loads to leverage peak solar windows for heavy fabrics like denim.
  
