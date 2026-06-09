# Agentic AI Crash Course

Welcome to the Agentic AI Crash Course. This repository is a hands-on learning path for new AI developers who want to understand how to build intelligent, agent-driven systems using Python and modern language-model tools.

Whether you are just starting with large language models or want to see how agents, memory, retrieval, and multimodal workflows fit together, this repo is designed to help you learn by doing.

## What You Will Learn

- How to call LLMs from Python and get structured results
- How to build simple agents with decision logic
- How vector search and RAG work in an AI pipeline
- How to add memory and state to agents
- How to combine text and images in multimodal workflows
- How to keep agents safe with guardrails and validation
- How to evaluate and test agent behavior
- How to assemble complete small projects like a shopping assistant and a telecom chatbot

## Contents

| Folder | What it teaches |
|--------|-----------------|
| `1_simple_llm_calling` | Learn the basics of calling LLM APIs and reading responses |
| `2_health_analysis` | Build a health data analysis agent that reads and interprets health metrics |
| `3_vector_db` | Learn vector database fundamentals using ChromaDB |
| `4_rag_basics` | Understand retrieval-augmented generation (RAG) workflows |
| `5_single_agent` | Explore a single-agent architecture and task flow |
| `6_memory` | Add memory to agents so they can remember prior interactions |
| `7_multimodal` | Work with both vision and text in multimodal agents |
| `8_guardrails` | Add safety checks, validation, and guardrails to agents |
| `9_eval` | Evaluate agent behavior and score responses |
| `10_project_shopping_agent` | Full project: build a shopping assistant agent |
| `11_project_telecom_chatbot` | Full project: build a telecom customer support RAG chatbot |

## Getting Started

### Prerequisites

- Python 3.14 or newer
- Git
- `pip` or `uv` (optional but recommended)
- Optional: Jupyter Notebook / JupyterLab for notebooks

> The repository includes a `.python-version` file pinned to `3.14`. This is a helpful signal for tools like `pyenv`, but the active interpreter must still be Python 3.14 or newer.

> If your Python version is older than 3.14, install Python 3.14+ before proceeding.

### 1. Clone the repository

```bash
git clone <repo-url>
```

### 2. Install dependencies

#### Recommended: using `uv`

If you have `uv` installed, this is the easiest way to install dependencies and keep the environment consistent.

```bash
uv sync
```

#### Alternative: using `pip`

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate

python -m pip install --upgrade pip
python -m pip install -e .
```

### 3. Configure environment variables

Copy the sample environment file to `.env` and add your API keys.

```bash
copy .env.sample .env
```

Open `.env` and fill in the values:

```ini
GOOGLE_API_KEY=your_google_api_key_here
GROQ_API_KEY=your_groq_api_key_here
LANGSMITH_API_KEY=your_langsmith_api_key_here
```

If you do not have all keys yet, you can still run the examples that do not require them.

### 4. Run examples

#### Notebooks

Start Jupyter Notebook from the project root:

```bash
jupyter notebook
```

Then open any notebook from the numbered folder list.

#### Streamlit apps

For folders that include a Streamlit app, run:

```bash
streamlit run <folder>/app.py
```

For example:

```bash
streamlit run 2_health_analysis/streamlit_app/app.py
```

## Recommended learning path

1. Start with `1_simple_llm_calling` to verify your environment and understand basic API usage.
2. Move to `3_vector_db` and `4_rag_basics` to learn how retrieval and search work.
3. Try `5_single_agent` and `6_memory` to see how agents are structured and how memory is added.
4. Explore `7_multimodal` and `8_guardrails` to learn advanced concepts.
5. Finish with `10_project_shopping_agent` and `11_project_telecom_chatbot` for complete end-to-end examples.

## Tips for new learners

- Read the notebook text before running code to understand the goal of each example.
- Run one folder at a time to keep the learning path simple.
- Use the `.env` file only for API keys; do not commit secrets to Git.
- If you see an error about Python version, make sure your active interpreter is Python 3.14 or later.

## Recommended `.gitignore`

If you create a Git repository for this project, ignore the local environment and temporary files:

```gitignore
.venv/
__pycache__/
*.pyc
.ipynb_checkpoints/
.env
.DS_Store
```

