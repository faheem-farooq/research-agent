# Autonomous AI Research Agent

An extensible, tool-calling AI research assistant built with Python and LangChain. The agent autonomously queries live web sources, aggregates findings, enforces structured JSON-schema outputs via Pydantic, and executes file system operations to persist generated reports.

## Key Features

- **Tool-Calling Architecture:** Dynamically selects and chains execution tools, including live web search via DuckDuckGo and structured queries via Wikipedia.
- **Structured Data Extraction:** Guarantees predictable responses by parsing LLM outputs into strictly typed Pydantic models (Topic, Summary, Sources, Tools Used).
- **Multi-LLM Provider Support:** Modular setup allowing seamless switching between OpenAI (GPT-4o) and Anthropic (Claude 3.5 Sonnet) models.
- **Custom Tool Integration:** Extensible interface for custom python tools, such as automated local file persistence (`.txt` generation).
- **Environment Isolation:** Clean dependency management and secure API credential handling via `python-dotenv`.

## Tech Stack

- **Language:** Python 3.10+
- **Frameworks:** [LangChain](https://www.langchain.com/), [Pydantic](https://docs.pydantic.dev/)
- **LLM Integrations:** OpenAI API, Anthropic API
- **External Tools:** DuckDuckGo Search, Wikipedia API

## Quickstart

### 1. Prerequisites & Installation

Clone the repository and install required dependencies:

```bash
# Clone repository
git clone [https://github.com/faheem-farooq/research-agent.git](https://github.com/faheem-farooq/research-agent.git)
cd research-agent

# Set up virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
