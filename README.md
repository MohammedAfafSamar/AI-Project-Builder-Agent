# AI-Project-Builder-Agent
An AI agent that turns a one-line project idea into a complete project plan — problem statement, modules, tech stack, database design, roadmap, testing plan, and future enhancements. Built with a local open-source LLM (Qwen2.5), no API key required
# AI Project Builder Agent 🧠

Give it a single sentence like:

> "I want to build an AI attendance system."

...and it generates a full, structured project plan:

- 📝 **Problem Statement** — goal, target users, pain point, success criteria
- 🧩 **Module Breakdown** — the core functional components
- ⚙️ **Tech Stack Recommendation** — frontend, backend, AI/ML, database, deployment
- 🗄️ **Database Design** — tables/collections, fields, relationships
- 🛣️ **Development Roadmap** — phased, actionable build steps
- ✅ **Testing Plan** — unit, integration, UAT, and edge cases
- 🚀 **Future Enhancements** — realistic post-launch roadmap

Each step's output feeds the next, so the final plan stays internally consistent — the database matches the modules, the roadmap matches the tech stack, and so on.

## How it works

The agent runs entirely on a small local instruction-tuned model (Qwen2.5-1.5B-Instruct via 🤗 Transformers), so it needs no paid API key — just a free Colab GPU (or CPU, slower).

It also demonstrates core AI-agent concepts along the way: **tool orchestration**, **memory**, **human-in-the-loop approval**, **execution tracing**, and a sketch of how the pipeline could be split into a **multi-agent** system.

## Usage

```python
project_result = run_project_builder_agent("I want to build an AI attendance system.")
```

## Tech

- Python, PyTorch, 🤗 Transformers
- Qwen/Qwen2.5-1.5B-Instruct (local inference)
- Designed to run in Google Colab
