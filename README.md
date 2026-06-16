# LLM Gateways Demo

This repository contains an interactive **Jupyter Notebook demo** for building a unified LLM gateway experience using `LiteLLM`, `LangChain`.

The notebook is designed to show how to:

- unify multiple LLM providers under a single API
- use automatic model fallbacks and load balancing
- track cost, latency, and call metadata
- cache repeated prompts for lower cost and faster responses
- integrate LiteLLM with LangChain for agentic workflows
- apply simple guardrails for prompt injection and sensitive data

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Tools and Technologies](#tools-and-technologies)

## Introduction

This demo uses `llm_gateway.ipynb` to demonstrate a practical LLM gateway architecture. It is notebook-first and intended for interactive experimentation with:

- provider-agnostic LLM calls via `LiteLLM`
- routing and fallback chains for higher availability
- cost and usage tracking through built-in LiteLLM tooling
- caching to avoid repeated request costs
- LangChain integration for downstream pipelines and agents
- guardrails to sanitize PII and block prompt injection

## Features

- **Unified LLM API** with `litellm.completion()` across multiple providers
- **Automatic fallback chains** when a model or provider fails
- **In-memory caching** to speed repeated queries and reduce cost
- **Router-based model selection** for task-aware workflows
- **Observability callbacks** for logging prompt, latency, and cost
- **LangChain integration** with `langchain-litellm`
- **Simple guardrails** for prompt injection and sensitive data redaction

## Installation

1. Clone the repository:

```bash
git clone https://github.com/srijosh/LLM-Gateway-using-LiteLLM.git
```

2. Navigate to the project directory:

```bash
cd LLM-Gateway-using-LiteLLM
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Set up environment variables by creating a `.env` file from `.env.sample`.

## Usage

Open the notebook and run the cells in order:

```bash
jupyter notebook llm_gateway.ipynb
```

## Tools and Technologies

- **LiteLLM**: unified LLM gateway and multi-provider orchestration
- **LangChain**: workflow orchestration and prompt chaining
- **langchain-litellm**: LangChain wrapper for LiteLLM models
- **python-dotenv**: environment variable loading from `.env`
- **Jupyter Notebook**: interactive exploration and demo execution
