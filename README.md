# 🤖 CrewAI + Google Gemini — Multi-Agent AI Projects

A collection of **Multi-Agent AI applications built with Python, CrewAI, and Google Gemini**.

This repository demonstrates how multiple specialized AI agents can collaborate to research information, explain concepts, simplify technical topics, create study notes, generate questions, write technical content, and review the final output.

---

## 🚀 Projects Included

### 1. 🧠 CrewAI Multi-Agent Learning System

**Notebook:** `Crewai_multiagent_Gemini_Open_Source.ipynb`

This project demonstrates a **5-agent CrewAI workflow** powered by **Google Gemini**.

The agents work together to explain and analyze the difference between:

* AI Agents
* Agentic AI
* MCP (Model Context Protocol)
* Generative AI

### 🤖 Agents

| Agent         | Role       | Responsibility                                 |
| ------------- | ---------- | ---------------------------------------------- |
| 👨‍🏫 Teacher | Teacher    | Explains concepts step by step                 |
| 🔎 Researcher | Researcher | Finds important information                    |
| 🧩 Simplifier | Simplifier | Converts complex concepts into simple language |
| 🎓 Student    | Student    | Creates short study notes                      |
| 📝 Examiner   | Examiner   | Creates questions to test understanding        |

### 🔧 Tools Used

* **CrewAI** — Multi-agent orchestration
* **Google Gemini** — Large Language Model
* **SerperDevTool** — Web search
* **Python**
* **Jupyter / Google Colab**

### 🔄 Workflow

```text
                    User Topic
                        │
                        ▼
              ┌──────────────────┐
              │    CrewAI Crew   │
              └────────┬─────────┘
                       │
        ┌──────────────┼──────────────┐
        ▼              ▼              ▼
     Teacher       Researcher     Simplifier
        │              │              │
        ▼              ▼              ▼
   Explanation      Research       Simple View
        │              │              │
        └──────────────┼──────────────┘
                       │
                ┌──────┴──────┐
                ▼             ▼
             Student       Examiner
                │             │
                ▼             ▼
             Notes        Questions
                │             │
                └──────┬──────┘
                       ▼
                  Final Result
```

---

## 2. 🔬 CrewAI + Google Gemini Research & Review System

**Notebook:** `Crewai_with_google_gemini.ipynb`

This project demonstrates a **3-agent sequential workflow** for researching and preparing technical content about **Generative AI and Agentic AI**.

The system focuses on topics such as:

* Large Language Models (LLMs)
* Generative AI
* Agentic AI
* Multi-Agent Systems
* Enterprise AI adoption
* AI tools and frameworks

### 🤖 Agents

| Agent             | Role             | Responsibility                                                  |
| ----------------- | ---------------- | --------------------------------------------------------------- |
| 🔎 Research Agent | AI Researcher    | Researches Generative AI and Agentic AI trends                  |
| ✍️ Writer Agent   | Technical Writer | Converts research into structured technical content             |
| ✅ Reviewer Agent  | AI Reviewer      | Reviews accuracy, clarity, logical flow, and workshop readiness |

### 🔄 Workflow

```text
                 AI Topic
                    │
                    ▼
            ┌───────────────┐
            │ Research Agent│
            └───────┬───────┘
                    │
                    ▼
              Research Output
                    │
                    ▼
            ┌───────────────┐
            │  Writer Agent │
            └───────┬───────┘
                    │
                    ▼
             Technical Article
                    │
                    ▼
            ┌───────────────┐
            │ Reviewer Agent│
            └───────┬───────┘
                    │
                    ▼
          Final Polished Content
```

---

## 🧠 What is CrewAI?

**CrewAI** is a framework for building applications where multiple AI agents collaborate to complete complex tasks.

Each agent can have its own:

* Role
* Goal
* Backstory
* Tools
* LLM
* Task

In these projects, CrewAI coordinates multiple specialized agents and executes their assigned tasks.

---

## ✨ Key Features

* 🤖 Multi-agent AI architecture
* 🧠 Google Gemini integration
* 🔎 AI-powered research
* 🌐 Web search integration
* 📚 Educational content generation
* 📝 Automated study-note generation
* ❓ AI-generated questions
* ✍️ Technical content generation
* ✅ AI-based content review
* 🔄 Sequential agent workflows
* ⚡ Asynchronous CrewAI execution
* ☁️ Google Colab compatible

---

## 🛠️ Technologies Used

| Technology       | Purpose                   |
| ---------------- | ------------------------- |
| Python           | Programming language      |
| CrewAI           | Multi-agent orchestration |
| Google Gemini    | LLM                       |
| Serper           | Web search                |
| CrewAI Tools     | External tools            |
| Google Colab     | Notebook environment      |
| Jupyter Notebook | Development environment   |

---

## 📂 Project Structure

```text
crewai-gemini-multi-agent/
│
├── Crewai_multiagent_Gemini_Open_Source.ipynb
├── Crewai_with_google_gemini.ipynb
├── README.md
├── requirements.txt
└── .gitignore
```

---

## 📦 Installation

Install CrewAI:

```bash
pip install crewai
```

For the first project, install CrewAI tools:

```bash
pip install "crewai[tools]"
```

For asynchronous notebook execution, the second project also uses:

```bash
pip install nest_asyncio
```

---

## 🔑 API Keys

The projects require a **Google Gemini API key**.

The first project also uses a **Serper API key** for web search.

Create environment variables rather than committing real API keys to GitHub.

Example:

```env
GEMINI_API_KEY=your_gemini_api_key
SERPER_API_KEY=your_serper_api_key
```

### ⚠️ Security

**Never upload API keys to GitHub.**

Do not place real keys directly inside a notebook that you plan to publish.

Use:

```text
.env
```

and add it to `.gitignore`:

```gitignore
.env
venv/
__pycache__/
.ipynb_checkpoints/
```

---

## ▶️ Running the Projects

### Google Colab

Upload either notebook to Google Colab and run the cells sequentially.

### Jupyter Notebook

Start Jupyter:

```bash
jupyter notebook
```

Open the required notebook and execute the cells.

---

## ⚙️ CrewAI Execution

Both projects use asynchronous CrewAI execution:

```python
result = await crew.kickoff_async()

print(result)
```

This allows the crew to execute its workflow and return the final output.

---

## 📌 Example Topic — Project 1

The first project uses the topic:

```text
What is the difference between Agents,
Agentic AI, MCP (Model Context Protocol),
and Generative AI?
```

The crew produces:

1. Step-by-step explanation
2. Research points
3. Beginner-friendly explanation
4. Short study notes
5. Five questions for assessment

---

## 📌 Example Research Areas — Project 2

The second project researches:

```text
Generative AI and Agentic AI trends
```

with focus on:

* Large Language Models
* Agentic AI
* Multi-agent systems
* Enterprise adoption
* AI tools and frameworks

The result is converted into a technical article and then reviewed for:

* Accuracy
* Clarity
* Logical flow
* Workshop suitability

---

## 🏗️ Multi-Agent Architecture

The general architecture used in these projects is:

```text
                    User / Topic
                         │
                         ▼
                 ┌──────────────┐
                 │    CrewAI    │
                 └──────┬───────┘
                        │
              ┌─────────┴─────────┐
              │                   │
              ▼                   ▼
          Agent 1              Agent 2
              │                   │
              ▼                   ▼
           Task 1               Task 2
              │                   │
              └─────────┬─────────┘
                        ▼
                    Agent 3
                        │
                        ▼
                   Final Output
```

---

## 🎯 Learning Objectives

These projects help demonstrate:

* How AI agents work
* How multiple agents collaborate
* How to define agent roles and goals
* How to assign tasks to agents
* How to connect Gemini with CrewAI
* How to use external tools
* How to create sequential AI workflows
* How AI agents can research and generate content
* How one agent can review another agent's output

---

## 👩‍💻 Author

**Swati Jadhav**

AI & Data Science Student
Python Developer | Generative AI | Agentic AI | Machine Learning

---

## ⭐ If You Like This Project

If you find these **CrewAI + Gemini Multi-Agent projects** useful, consider giving the repository a ⭐ on GitHub.
