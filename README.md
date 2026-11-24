# Meridian

A free, self-paced path into AI engineering. Sixteen levels, from a plain Python service to production agents, evals, security, and interviews. Read the lesson, do the exercise, tick it off. No account, no video, no tuition.

The app is the study guide. You do the builds in your own repos (Python, FastAPI, Docker, an LLM API, and so on). Meridian does not call a model for you and does not need an API key.

## What you get

| | |
|---|---|
| Levels | 16 (numbered 0–15) |
| Phases | 7 |
| Modules | 151 |
| Lessons | 997, each with a short exercise |
| Study sessions | about 286, as sized in the curriculum |
| Capstones | 13, plus a portfolio menu of public builds |
| Shorter cut | a 100-day sprint through the modules that matter most |

Progress (checkboxes and notes) stays in this browser under the `meridian-progress` key. Clearing site data clears it. There is no server account.

## How to use it

1. **Start where you are.** Each level says what it assumes. Skip a level you already know.
2. **One level at a time.** Modules stack: ordinary software before APIs, orchestration before agents, evals before you call it production.
3. **Finish by building.** Checkboxes only track reading. A level is done when its project runs.
4. **Or take the 100-day cut.** Home → “100-day cut”. It is a subset (model behavior, APIs, prompts, RAG, agents, then evals, security, design, and a release you can roll back), not a replacement for the full path.
5. **Search** any lesson from the header. Two characters is enough.

## What it covers

### 01 · Foundations — levels 0–3

Software, how a model actually produces text, API orchestration, and prompts you can retest.

| Level | Title | You leave able to… |
|---|---|---|
| 0 | Software Engineering Fundamentals | Write, test, and ship an ordinary service. Python for this work, HTTP/REST/JSON, FastAPI, persistence, Git, coding agents, containers. **Capstone:** a no-AI REST service with PostgreSQL and Docker. Assumes nothing. |
| 1 | LLM 101 | Explain next-token prediction without treating the API like a search box. Tokens, embeddings, attention, training, inference, sampling, reasoning models, the context window, failure modes, and how to pick a model. |
| 2 | Working with LLM APIs | Turn one-off calls into software: messages, streaming, structured output, tools, multi-step workflows, concurrency, retries, cost, and traces. LangChain plus where other orchestrators fit. **Capstone:** a streaming assistant with two or three real tools. |
| 3 | Prompt Engineering | Keep instructions steady: prompt anatomy, few-shot examples, decomposition, system rules, output control, a tiny test set, versioning, caching, and why wording is not a security boundary. **Capstone:** optimize one real prompt on a frozen test set. |

### 02 · Retrieval — level 4

| Level | Title | You leave able to… |
|---|---|---|
| 4 | RAG | Turn files into an index that can cite or refuse. Ingest, chunk, embeddings, vector search, hybrid (keyword + vector) retrieval, reranking, query rewriting, grounding, and the patterns past “search once, answer once.” **Capstone:** a hybrid search API over a real document set. |

### 03 · Agentic — levels 5–6

| Level | Title | You leave able to… |
|---|---|---|
| 5 | AI Agents | Let the model pick the next step inside a harness: ReAct and planning, tools, MCP, memory, multi-agent splits, LangGraph, sandboxes, and failure recovery. **Capstone:** one production-style agent (research desk, MCP operator, or sandboxed code agent) — not a tour of every library. |
| 6 | Context Engineering | Treat the context window as a budget. What to load, what to compact, what to keep outside the prompt, caching, and a harness that still holds the goal after the transcript outgrows one window. **Capstone:** the same agent, now measured against a numeric budget. |

### 04 · Evaluation & trust — levels 7–8

| Level | Title | You leave able to… |
|---|---|---|
| 7 | LLM Evaluations | Prove a feature works. Offline vs online evals, model benchmarks vs your task, golden sets, regression gates, and deep dives on RAG evals (retriever, generator, the RAG triad, safety) and agent evals (trajectory, tool args, recovery). |
| 8 | AI Security | Threat-model prompts, retrieved text, tools, and model output as untrusted input. Injection and exfiltration, jailbreaks, agent permissions, poisoned knowledge, PII, red teaming, and governance. **Capstone:** attack an app you already built and close each hole with a regression test, not a longer system prompt. |

### 05 · Production — levels 9–11

| Level | Title | You leave able to… |
|---|---|---|
| 9 | AI System Design | Turn a product need into a design you can defend: where knowledge lives, model routing, latency, caching, degradation, orchestration, and monitoring. Includes case studies. **Capstone:** a design doc with latency, cost, and quality reasons — and the alternatives you dropped. |
| 10 | LLMOps | Put the RAG app or the agent on a release path. Versioned prompts, evals as a gate, runtime guardrails, containers, GitHub Actions, AWS, monitoring, incidents, and rollbacks. **Capstone:** one app through that loop, with a dashboard and one practised rollback. |
| 11 | Managed AI Platforms | Run a model when a personal API key is not allowed. Bedrock, Vertex AI, Azure AI Foundry, open-weight hosts, routers and gateways, identity, residency, quotas, and lock-in. **Capstone:** move an existing app onto a managed catalog without rewriting what the user sees. |

### 06 · Frontier & proof — levels 12–14

| Level | Title | You leave able to… |
|---|---|---|
| 12 | Multimodal 101 | Treat images, audio, and video as more tokens in the same model. Vision and documents, image and video generation, speech, realtime voice, cross-modal search, and on-device models. **Capstone:** one product that crosses at least two modalities, with delay and cost per stage. |
| 13 | Fine-Tuning | Fine-tune only after a prompt, retrieval, and a stronger base model miss a metric you wrote down. Data, SFT, LoRA and QLoRA, DPO, distillation, held-out comparison, and serving the adapter. **Capstone:** a small LoRA that beats the prompted baseline on a set that never chose the checkpoint. |
| 14 | Projects | No new theory. A menu of public builds: document Q&A, resume screening, a multi-agent research report, an MCP server, a monitored API, a voice or multimodal build, and how you position the portfolio. Ship three to five. Put the score next to the demo. |

### 07 · Interview — level 15

| Level | Title | You leave able to… |
|---|---|---|
| 15 | GenAI / AI Engineer Interview Prep | Defend the roadmap on a clock. Role positioning, RAG and agent scenarios, fine-tuning, production debugging, system design, portfolio defense, and behavioral answers. **Capstone:** a timed mock loop — positioning, one live incident, one design, one hard defense of a single build. |

## Run it on your machine

You need [Node.js 22](https://nodejs.org/) (20.19 or newer also works) and npm. No database and no API keys.

```bash
git clone <your-repo-url>
cd <repo-folder>
npm install
npm run dev
```

Open [http://localhost:8080](http://localhost:8080). The dev server binds `0.0.0.0:8080`, so it is also reachable from other devices on your network.

Stop it with Ctrl+C.

### Production build

```bash
npm run build
npm run preview
```

The preview server listens on [http://127.0.0.1:8081](http://127.0.0.1:8081). `npm run build` skips database migrations when `DATABASE_URL` is unset, which is what you want for a local copy of this study site.

### Other scripts

| Command | What it does |
|---|---|
| `npm run typecheck` | Typecheck with `tsc --noEmit` |
| `npm run lint` | ESLint |
| `npm test` | Script and library unit tests |

## Project layout

```text
src/data/levels/     One JSON file per level (lessons, exercises, capstone)
src/data/phases.ts   The seven phases
src/data/sprint.ts   The 100-day cut
src/data/curriculum.ts  Loads and validates the JSON (zod)
src/routes/          Pages: home, level, sprint, projects, search
src/lib/progress.ts  Checkbox and note state (browser localStorage)
```

To change a lesson, edit the matching file in `src/data/levels/`. Each topic has a `title`, a `body`, and a `try` (the exercise). The dev server reloads when you save.

## Stack

[TanStack Start](https://tanstack.com/start) (React 19, file routes), Vite, Tailwind CSS v4. Curriculum content is static JSON validated at startup. Auth and a hosted database are wired in the template but **off** for this app: nothing here is per-user.
