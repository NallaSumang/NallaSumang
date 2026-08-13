<div align="center">
  <h1>NALLA SUMANG</h1>
  <h3>AI Systems Engineer — Solo-Built Agentic Applications</h3>
  <p><em>Designing, deploying, and hardening asynchronous LLM pipelines and multi-agent tools — end to end, from architecture to production debugging.</em></p>

  <br/>

  <img src="https://github-readme-stats.vercel.app/api?username=NallaSumang&show_icons=true&theme=tokyonight&hide_border=true&count_private=true" alt="GitHub Stats" height="165"/>
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=NallaSumang&theme=tokyonight&hide_border=true" alt="GitHub Streak" height="165"/>

</div>

## ⚡ Summary

I design and ship agentic AI systems solo — end-to-end, from architecture through deployment and post-launch debugging. My focus is on **asynchronous execution patterns**: decoupling slow LLM inference from user-facing request paths using message queues (Redis/BullMQ), so applications stay responsive instead of blocking on multi-second model calls.

I build under real constraints — free-tier hosting, single-developer bandwidth, no dedicated QA — and treat that as a design problem, not an excuse. Several of my projects document their own operating limits directly in the repo (resource caps, scaling notes, known trade-offs) rather than glossing over them, because I'd rather an architecture be honest about what it can currently do than oversell it. Below, each project links to a live deployment and its actual repo — go check the code.

---

## 🚀 Projects

### [Distributed AI Researcher](https://github.com/NallaSumang/DISTRIBUTED-AI-RESEARCHER-) | [Live](https://distributed-ai-researcher.vercel.app)
> **Stack:** Next.js, FastAPI, LangGraph, Groq (Llama 3.3 70B), Upstash Redis, Supabase.

An autonomous research agent that breaks a topic into sub-queries, fans them out to parallel "scout" agents using Python `asyncio` (rather than blocking sequential calls), and has a synthesizer agent compile the results into a structured report. Redis is used as a persistent job queue so the frontend can poll for results instead of holding an HTTP connection open through a multi-minute research run — this avoids gateway timeouts on long-running AI tasks, which is the actual problem this architecture solves.

### [Nexus Career Intelligence](https://github.com/NallaSumang/NEXUS-CAREER-INTELLIGENCE) | [Live](https://nexus-ai-vqxe.onrender.com)
> **Stack:** React/Vite, Node.js/Express, Python/FastAPI, BullMQ + Redis, MongoDB, Docker.

A placement-prep copilot for B.Tech students — upload a resume, paste a job description, get a match score, missing-skills breakdown, a drafted cover letter, and interview questions. The Express API and FastAPI inference layer run as two processes in one Docker container; resume parsing and AI scoring are offloaded to BullMQ workers so the API responds immediately while the LLM call runs in the background.

Runs on Render's free tier (~0.1 vCPU / 512MB RAM) — worker concurrency is deliberately capped at 1 to avoid resource starvation, a tuning decision made after hitting it in practice. The repo documents ten specific production bugs found and fixed post-deployment, including a MongoDB connection storm from `initializeApp()` re-running per request, a Redis retry strategy that silently gave up after one failure, and an invalid CORS config that violated RFC 6454 — the kind of debugging you only do after something has actually broken in front of real users. Informally tested with 10+ peer users before and after those fixes.

### [Lumina-Proposals](https://github.com/NallaSumang/Lumina-Proposals)
> **Stack:** Next.js, TypeScript, in-memory vector store, custom chunking/embedding pipeline.

A local-first RAG prototype for parsing large PDFs (100+ page RFPs) into chunked, embedded, queryable text. Built to test a document-ingestion and retrieval pipeline end to end, with the vector store held in-process for zero-latency reads during development. The repo's own architecture notes are explicit about the two changes needed before this could run at real scale: ingestion currently runs synchronously inline (would need to move to a queued background job for concurrent uploads), and the in-memory store would need to move to a persistent vector DB like pgvector before handling large document volumes without hitting memory limits. Documenting that gap deliberately, rather than shipping past it silently, is the point.

### [Kaggle Concierge Agent](https://github.com/NallaSumang/kaggle-concierge-agent)
> **Stack:** Python.

A single-script local automation tool that scans, categorizes, and sorts files by extension, with a human-in-the-loop confirmation step for any ambiguous action and graceful fallback behavior when the Kaggle API is rate-limited. Deliberately kept as one script rather than a service — for a tool that runs on-demand on your own machine, a microservice architecture would be solving a problem that doesn't exist.

### [Vision AI](https://github.com/NallaSumang/VISION-AI) | [Live](https://sumang-vision-ai-jczj.vercel.app/)
> **Stack:** Next.js, Python (local backend), multimodal LLM calls.

A multimodal chat interface that holds conversation context for extended sessions (~3 hours) using local file-based history rather than a stateless single-turn design. Built as a local-first application — the README notes that persistent state via disk I/O won't survive a serverless container teardown, so this is designed as a locally-run system rather than something horizontally scaled at the edge; scaling it that way would mean swapping the local JSON store for Redis or a managed database first.

### [BrutalBench](https://github.com/NallaSumang/BrutalBench)
> **Stack:** Next.js (monolith), Supabase, n8n.

An AI code-evaluation leaderboard: incoming code submissions are graded against a rubric and the results are upserted into a Supabase-backed leaderboard, with n8n handling the webhook automation between external test runs and the database. Uses standard Supabase environment-key auth for the webhook-to-database write path.

---

## 🏆 Certifications

* **IBM RAG and Agentic AI Professional Certificate** — Coursera
* **Oracle Cloud Infrastructure Certified AI Foundations Associate** — Oracle
* **Oracle Agentic AI Certified Foundations Associate** — Oracle
* **Oracle Fusion AI Agent Studio Certified Foundations Associate (Rel 1)** — Oracle
* **AI Engineer for Data Scientists Associate** — DataCamp
* **Associate Data Engineer** — DataCamp
* **Microsoft SQL Server Professional Certificate** — Coursera
* **Google Advanced Data Analytics Professional Certificate** — Coursera

---

## 💼 Internships

**IBM SkillsBuild & Edunet Foundation** — *AI & Cloud Engineering Intern*
Built the [watsonx-nutrition-agent](https://github.com/NallaSumang/watsonx-nutrition-agent) on IBM Watsonx Orchestrate — structured prompt-behavior mapping and runtime knowledge-source grounding to keep a precision-advisory agent's outputs constrained to reference data rather than free-generating.

**NexLevr** — *AI & Automation Engineering Intern*
Built and open-sourced [LLM-Output-Variance-CLI](https://github.com/NallaSumang/LLM-Output-Variance-CLI) — a CLI that measures temperature-driven output variance and token-level drift across OpenAI, Groq, and local endpoints, for setting reliability thresholds in agentic pipelines that need deterministic-ish behavior.

---

## ⚙️ Stack

<div align="center">
  <br />
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=python,ts,nodejs,react,nextjs,fastapi,docker,redis,mongodb,postgres,supabase,linux,git,bash&perline=8" />
  </a>
  <br />
</div>

<br>

* **Async & Queues:** Redis, BullMQ, asyncio, background workers
* **Data:** MongoDB, PostgreSQL, Supabase (pgvector), vector search
* **Backend:** Node.js/Express, Python/FastAPI, Docker
* **AI/LLM:** LangChain, LangGraph, CrewAI, RAG pipelines, multi-agent orchestration
* **Frontend:** React, Next.js, Vite, TypeScript
