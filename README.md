# Hey, I'm Jonathan Armstrong

### 🌐 Portfolio &amp; live work → **[jarmstrong158.github.io](https://jarmstrong158.github.io)**

AI/ML engineer. Multi-agent infrastructure, reinforcement learning agents, and MCP servers: production systems built from scratch, from transformer-based PPO agents to serverless agent coordination.

Warehouse manager by day, building nights and weekends. Looking for a full-time role in applied AI, forward-deployed engineering, or ML engineering.

## Latest

**[Xylem](https://github.com/jarmstrong158/Xylem)** is a multi-agent AI development stack: durable memory, decentralized coordination, and a trust-gated knowledge lifecycle for AI coding agents, shipped as local-first MCP servers with Cloudflare Worker remote transports. The core insight: `git push` and the GitHub Contents API enforce the same "only save if nobody changed this first" rule, so a phone and a desktop share one coordination board as equal peers with no central server between them. A single installer also ships the habit layer, so agents remember, coordinate, and ask by default instead of only when prompted. Start with the [interactive explainer](https://jarmstrong158.github.io/Xylem/).

The stack runs its own development: it audited my RL agent's recorded decisions against training reality, found a learning-rate bug, fixed it, and relaunched the training run, coordinated from my phone.

- [context-keeper](https://github.com/jarmstrong158/context-keeper) — rationale-first project memory. Records why, not just what. Published evals: up to 92% context reduction vs. dumping the store, Hit@5 of 13/15, calibrated abstention. Dual-write mirror to a Worker + D1 remote with timestamp-guarded upserts, so desktop and mobile read one memory.
- [agentsync](https://github.com/jarmstrong158/agentsync) — multi-agent coordination with no server. Claims live in one claims.json where git push is the compare-and-swap. 1,000 simulated concurrent races: zero lost claims, zero double-grants, with the test harness caveats documented in the repo.
- [cambium](https://github.com/jarmstrong158/cambium) — the knowledge lifecycle. Distills completed work into recallable lessons and promotes them by earned trust: local, then team, then org, with org promotion as reviewed pull requests rendered to a human-readable knowledge base.
- [context-keeper-remote](https://github.com/jarmstrong158/context-keeper-remote) / [agentsync-remote](https://github.com/jarmstrong158/agentsync-remote) — the same protocols over Cloudflare Workers, so claude.ai on a phone is a full peer in the mesh, not a viewer.

## What I Build

**Reinforcement Learning & ML** — a deliberate progression on one hard problem: [Dolly](https://github.com/jarmstrong158/Dolly) (warehouse RL simulation) → [Jack](https://github.com/jarmstrong158/Jack) (a working single-facility agent) → [Clark](https://github.com/jarmstrong158/Clark) (the variable-N foundation generalization).

- [Clark](https://github.com/jarmstrong158/Clark) — Foundation RL model for warehouse workforce scheduling. Variable-shape transformer + LSTM (~18M params), 3-stage curriculum across thousands of synthetic facility configs, per-worker PPO ratio + symlog value targets, multi-process env runner with pipelined CPU/GPU overlap. Holding ~93% order completion uniformly across 5 to 50-worker facilities, the generalization signal, with reward convergence still being tuned.
- [Jack](https://github.com/jarmstrong158/Jack) — PPO + LSTM warehouse RL agent with temporal memory. 98.2% order completion, 58% A-grade days across ~9.4 simulated years on a single facility. The validated single-facility predecessor to Clark.
- [Balatron](https://github.com/jarmstrong158/Balatron) — Autonomous Balatro agent combining PPO, forward-simulating planning, and heuristic tactics. 814-dimensional state, phase-aware reward shaping, confirmed white-stake wins, supervised training runs with regime-tracked metrics. Its decision history is recorded in context-keeper and audited against results, which is how a live learning-rate bug was caught and fixed.
- [Dolly](https://github.com/jarmstrong158/Dolly) — The earliest warehouse RL simulation; where the Jack → Clark line started.

**MCP Servers & Agentic Tooling**

- [Skein](https://github.com/jarmstrong158/skein) — A2A observability + MCP server. Flask + HTMX dashboard, deterministic failure cascade detection via `referenceTaskIds` + `contextId`, W3C `traceparent` capture, passive spec validator. 71/71 tests, `ruff` + `mypy` clean in CI.
- [Waveform MCP](https://github.com/jarmstrong158/waveform-MCP) — Gives Claude full control of Tracktion Waveform: compose, mix, master, render. 150+ tools, 6 genre composers, music theory + mix-balance heuristics baked in. The largest agent tool-surface I've built.
- [Conductor](https://github.com/jarmstrong158/Conductor) + [Conductor-mcp](https://github.com/jarmstrong158/Conductor-mcp) — Local automation dashboard with a web UI. Redis workers, scheduled tasks, Claude control via 22 MCP tools. Shipped Windows product with bundled Redis and auto-update.
- [SkillMatch MCP](https://github.com/jarmstrong158/skillmatch-mcp) — Job fit analyzer: parses JDs, compares against your GitHub portfolio and resume, tracks applications in SQLite.

**LLM Platform**

- [llm-evals](https://github.com/jarmstrong158/llm-evals) — eval framework with swappable executors and scorers. Pluggable model adapters, structured scoring, per-run artifacts.
- [rag-pipeline](https://github.com/jarmstrong158/rag-pipeline) — fully local RAG with llama-cpp-python + Llama 3.2 + nomic-embed-text. FastAPI front door, no cloud.

**Automation & Full-Stack**

- [Ship.exec Metrics Tracker](https://github.com/jarmstrong158/Ship.exec-metrics-tracker) — Python/Selenium automation for daily ShipExec reporting. Measured time savings project to roughly \$17K/yr per location in reporting labor at a 200+ order/day warehouse. Proof of concept, not a sanctioned deployment.
- [Barcode Label Maker](https://github.com/jarmstrong158/barcode-label-maker) — Print-ready Avery barcode labels (PDF) from an Excel pick-list. Auto-shrinking SKUs, width-fit Code 39 barcodes, looked-up descriptions. Ships a synthetic catalog so proprietary data stays private.
- [AI Profile Builder](https://github.com/jarmstrong158/ai-profile-builder) — Team AI profiling platform. 14 behavioral spectrums, 9 archetypes, team health dashboard. React 19, Supabase, deployed on [Vercel](https://ai-profile-builder-wheat.vercel.app).

## Tech

Python • PyTorch • Transformer (built from scratch) • PPO / LSTM • IPPO factored action spaces • symlog value targets (DreamerV3) • Curriculum Learning • MCP Protocol • A2A Protocol • Cloudflare Workers + D1 • git-as-CAS coordination • Claude API • FastAPI • Flask + HTMX • SQLite • Redis • React • Supabase • Selenium • Multi-process Python (spawn / Pipe IPC)

## Links

- [Xylem interactive explainer](https://jarmstrong158.github.io/Xylem/)
- [LinkedIn](https://linkedin.com/in/jonathan-armstrong-71b959361)
- [Email](mailto:jarmstrong158@gmail.com)
