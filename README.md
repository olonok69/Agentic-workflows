# Agentic Workflows Learning Repository

This repository accompanies the "Introduction to Agentic Workflows with Python and OpenAI" learning materials. It collects runnable Python demonstrations and supporting media that showcase different agentic workflow patterns—from simple sequential hand-offs to LLM-driven orchestration.

Most examples rely on the [`openai`](https://pypi.org/project/openai/) SDK and expect an `.env` file containing `OPENAI_API_KEY` (and optionally `OPENAI_BASE_URL`). You can install shared dependencies with:

```powershell
pip install -r requirements.txt
```

## Folder-by-Folder Guide

### `Welcome to Introduction to Agentic Workflows with Python and OpenAI`

**Python scripts**
- `main.py` &mdash; Compares a hardcoded Q&A knowledge base against an OpenAI-powered agent for program management questions, highlighting how LLMs can augment traditional logic.
- `demo.py` &mdash; Demonstrates parallels between keyword-driven helper functions and LLM agents by answering sample user queries with both approaches.

**Notebooks**
- _None in this folder._

### `Introduction to Implementing Agentic Workflows with Python`

**Python scripts**
- `main.py` &mdash; Wires together reusable agents to fetch and process mock user data, illustrating how to build a simple production-style workflow facade.
- `demo.py` &mdash; Runs an end-to-end "information processing" workflow (research → fact check → summarize) using lightweight stand-in agents.
- `fastchecker.py` &mdash; Extends the demo workflow with keyword flagging to show how agent responsibilities can evolve.

**Modules**
- `workflow_agents/agent_definitions.py` &mdash; Defines the reusable base `Agent` class plus `DataFetchingAgent` and `DataProcessingAgent` used by `main.py`.
- `workflow_agents/__init__.py` &mdash; Empty package marker for the helper module.

**Notebooks**
- _None in this folder._

### `AI Agents and Agentic Workflows`

**Python scripts**
- `main.py` &mdash; Compares deterministic workout planning rules with an LLM-based agent that reasons about user profiles and emits JSON schedules.
- `demo-no-llm.py` &mdash; Baseline examples of deterministic vs. simple agentic task processing without any LLM calls.
- `demo-llm.py` &mdash; Expands the baseline with an LLM "strategy advisor" that selects between priority- and efficiency-driven task execution.

**Notebooks**
- _None in this folder._

### `Prompt Chaining Workflow`

**Python scripts**
- `main.py` &mdash; Builds a four-agent refinery optimization chain (analysis → planning → market research → production optimization) powered by OpenAI chat completions.
- `demo.py` &mdash; Minimal researcher → writer prompt chain that showcases how intermediate outputs can shape later agent prompts.

**Notebooks**
- _None in this folder._

## Additional Resources

Other top-level folders mainly contain video lessons and subtitle archives (zip files) that pair with the Python examples. No Jupyter notebooks are currently included in the repository.

## Running the Examples

1. Create a virtual environment (optional but recommended) and install dependencies with `pip install -r requirements.txt`.
2. Add an `.env` file at the project root with your `OPENAI_API_KEY` (and any custom `OPENAI_BASE_URL`).
3. Execute the desired script with `python path\to\script.py`. Scripts that call the OpenAI API will automatically warn you if the API key is missing.

Enjoy exploring the different patterns for building agentic workflows!
