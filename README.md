# Hey, I'm Jonathan Armstrong

AI/ML engineer. Reinforcement-learning agents, MCP servers, and A2A observability tooling — production systems built from scratch: Transformer-based PPO agents, Claude API integrations, and workflow automation.

Warehouse Manager by day. Building nights and weekends. Looking for a full-time role in applied AI, LLM platform, or ML engineering.

## Latest

**[Clark](https://github.com/jarmstrong158/Clark)** — foundation reinforcement learning model for warehouse workforce scheduling. Transformer + LSTM hybrid (~18M params) over a variable number of workers and tasks, so one pre-trained model can fine-tune to a new facility instead of training from scratch. Per-worker PPO ratio (IPPO-style factored action space), symlog value-target compression (DreamerV3), multi-process env runner with pipelined CPU/GPU overlap, and an audit-driven reward design. Successor to [Jack](https://github.com/jarmstrong158/Jack); foundation pre-training in progress — currently holding **~93% order completion uniformly across 5–50-worker facilities** (the generalization signal), with reward-convergence still being tuned.

## What I Build

**Reinforcement Learning & ML** — a deliberate progression on one hard problem: [**Dolly**](https://github.com/jarmstrong158/Dolly) (warehouse RL simulation) → [**Jack**](https://github.com/jarmstrong158/Jack) (a working single-facility agent) → [**Clark**](https://github.com/jarmstrong158/Clark) (the variable-N foundation generalization).
- [Clark](https://github.com/jarmstrong158/Clark) — Foundation RL model for warehouse workforce scheduling. Variable-shape transformer + LSTM (~18M params), 3-stage curriculum across thousands of synthetic facility configs, per-worker PPO ratio + symlog value targets, feasibility-bounded synthetic generator, multi-process env runner with pipelined CPU/GPU overlap. Diagnosed and tuned through independent multi-agent audits with strict attribution discipline; pre-training in progress.
- [Jack](https://github.com/jarmstrong158/Jack) — PPO + LSTM warehouse RL agent with temporal memory. 98.2% order completion, 58% A-grade days across ~9.4 simulated years on a single facility. The validated single-facility predecessor to Clark.
- [Balatron](https://github.com/jarmstrong158/Balatron) — PPO RL agent playing Balatro autonomously. 814-dimensional state vector, hybrid neural+heuristic decision layer, 17+ confirmed wins.
- [Dolly](https://github.com/jarmstrong158/Dolly) — The earliest warehouse RL simulation; where the Jack → Clark line started.

**MCP Servers & Agentic Tooling**
- [Skein](https://github.com/jarmstrong158/skein) — A2A observability + MCP server. Flask + HTMX dashboard, deterministic failure cascade detection via `referenceTaskIds` + `contextId`, W3C `traceparent` capture, passive spec validator. 71/71 tests, `ruff` + `mypy` clean in CI.
- [Conductor](https://github.com/jarmstrong158/Conductor) + [Conductor-mcp](https://github.com/jarmstrong158/Conductor-mcp) — Local automation dashboard with a web UI. Redis workers, scheduled tasks, Claude control via 22 MCP tools. Shipped Windows product with bundled Redis and auto-update.
- [Context Keeper](https://github.com/jarmstrong158/context-keeper) — MCP server that persists project decisions, pipelines, and constraints across Claude conversations. Relevance scoring without embeddings. Zero external dependencies.
- [SkillMatch MCP](https://github.com/jarmstrong158/skillmatch-mcp) — Job fit analyzer: parses JDs, compares against your GitHub portfolio and resume, tracks applications in SQLite.

**LLM Platform**
- [llm-evals](https://github.com/jarmstrong158/llm-evals) — eval framework with swappable executors and scorers. Pluggable model adapters, structured scoring, per-run artifacts.
- [rag-pipeline](https://github.com/jarmstrong158/rag-pipeline) — fully local RAG with llama-cpp-python + Llama 3.2 + nomic-embed-text. FastAPI front door, no cloud.

**Automation & Full-Stack**
- [Ship.exec Metrics Tracker](https://github.com/jarmstrong158/Ship.exec-metrics-tracker) — Python/Selenium automation saving ~\$17,000/yr in manual reporting at a 200+ order/day warehouse.
- [AI Profile Builder](https://github.com/jarmstrong158/ai-profile-builder) — Team AI profiling platform. 14 behavioral spectrums, 9 archetypes, team health dashboard. React 19, Supabase, deployed on [Vercel](https://ai-profile-builder-wheat.vercel.app).

## Tech

Python • PyTorch • Transformer (built from scratch) • PPO / LSTM • IPPO factored action spaces • symlog value targets (DreamerV3) • Curriculum Learning • MCP Protocol • A2A Protocol • Claude API • FastAPI • Flask + HTMX • SQLite • Redis • React • Supabase • Selenium • Multi-process Python (spawn / Pipe IPC)

## Links

- [LinkedIn](https://linkedin.com/in/jonathan-armstrong-71b959361)
- [Email](mailto:jarmstrong158@gmail.com)
