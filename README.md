# Hey, I'm Jonathan Armstrong

AI/ML engineer. Shipping MCP servers, A2A observability tooling, and RL agents. Production systems built from scratch — Claude API integrations, Transformer-based PPO agents, FastAPI services, and workflow automation.

Warehouse Manager by day. Building nights and weekends. Looking for a full-time role in applied AI, LLM platform, or ML engineering.

## Latest

**[Clark](https://github.com/jarmstrong158/Clark)** — foundation reinforcement learning model for warehouse workforce scheduling. Transformer + LSTM hybrid (~18M params) that handles variable numbers of workers and tasks, so one pre-trained model fine-tunes to any facility in 200–500 episodes instead of training from scratch. Per-worker PPO ratio (IPPO-style factored action space), PopArt value normalization, multi-process env runner with pipelined CPU/GPU overlap. Successor to [Jack](https://github.com/jarmstrong158/Jack); foundation pre-training in progress.

## What I Build

**MCP Servers & Agentic Tooling**
- [Skein](https://github.com/jarmstrong158/skein) — A2A observability + MCP server. Flask + HTMX dashboard, deterministic failure cascade detection via `referenceTaskIds` + `contextId`, W3C `traceparent` capture, passive spec validator. 71/71 tests, `ruff` + `mypy` clean in CI.
- [Conductor](https://github.com/jarmstrong158/Conductor) + [Conductor-mcp](https://github.com/jarmstrong158/Conductor-mcp) — Local automation dashboard with a web UI. Redis workers, scheduled tasks, Claude control via 22 MCP tools. Shipped Windows product with bundled Redis and auto-update.
- [Context Keeper](https://github.com/jarmstrong158/context-keeper) — MCP server that persists project decisions, pipelines, and constraints across Claude conversations. Relevance scoring without embeddings. Zero external dependencies.
- [SkillMatch MCP](https://github.com/jarmstrong158/skillmatch-mcp) — Job fit analyzer: parses JDs, compares against your GitHub portfolio and resume, tracks applications in SQLite.

**LLM Platform**
- [llm-evals](https://github.com/jarmstrong158/llm-evals) — eval framework with swappable executors and scorers. Pluggable model adapters, structured scoring, per-run artifacts.
- [rag-pipeline](https://github.com/jarmstrong158/rag-pipeline) — fully local RAG with llama-cpp-python + Llama 3.2 + nomic-embed-text. FastAPI front door, no cloud.

**Reinforcement Learning & ML**
- [Clark](https://github.com/jarmstrong158/Clark) — Foundation RL model for warehouse workforce scheduling. Variable-shape transformer + LSTM hybrid (~18M params), 3-stage curriculum across thousands of synthetic facility configs, per-worker PPO ratio + PopArt value head, multi-process env runner with pipelined CPU/GPU overlap, FastAPI multi-facility API. Generalizes Jack's single-facility approach so one foundation model fine-tunes per facility in ~30 minutes.
- [Jack](https://github.com/jarmstrong158/Jack) — PPO + LSTM warehouse RL agent with temporal memory. 98.2% order completion, 58% A-grade days across ~9.4 simulated years on a single facility. Validated single-facility predecessor to Clark.
- [Balatron](https://github.com/jarmstrong158/Balatron) — PPO RL agent playing Balatro autonomously. 814-dimensional state vector, hybrid neural+heuristic decision layer, 17+ confirmed wins.
- [Dolly](https://github.com/jarmstrong158/Dolly) — Earlier warehouse RL simulation; Jack's predecessor.

**Automation & Full-Stack**
- [Ship.exec Metrics Tracker](https://github.com/jarmstrong158/Ship.exec-metrics-tracker) — Python/Selenium automation saving ~\$17,000/yr in manual reporting at a 200+ order/day warehouse.
- [AI Profile Builder](https://github.com/jarmstrong158/ai-profile-builder) — Team AI profiling platform. 14 behavioral spectrums, 9 archetypes, team health dashboard. React 19, Supabase, deployed on [Vercel](https://ai-profile-builder-wheat.vercel.app).

## Tech

Python • PyTorch • Transformer (built from scratch) • PPO / LSTM • IPPO factored action spaces • PopArt value normalization • Curriculum Learning • MCP Protocol • A2A Protocol • Claude API • FastAPI • Flask + HTMX • SQLite • Redis • React • Supabase • Selenium • Multi-process Python (spawn / Pipe IPC)

## Links

- [LinkedIn](https://linkedin.com/in/jonathan-armstrong-71b959361)
- [Email](mailto:jarmstrong158@gmail.com)
