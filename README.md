<div align="center">
  <h1>NALLA SUMANG</h1>
  <h3>AI Agent Architect & Systems Engineer</h3>
  <p><em>Designing and operating production-grade multi-agent systems, LLM pipelines, and resilient asynchronous infrastructure.</em></p>
</div>

## ⚡ Executive Summary

An AI Systems Architect specializing in the rapid integration, design, and orchestration of autonomous agentic workflows. The core engineering focus is heavily rooted in replacing legacy system bottlenecks with high-availability, AI-driven asynchronous architectures that can scale dynamically.

Expertise lies in high-level system orchestration—leveraging advanced Large Language Models (LLMs) to architect, automate, and integrate production-grade infrastructures at unprecedented speeds. Rather than treating AI as a simple chatbot interface, the focus is on utilizing AI as a core reasoning engine embedded deep within enterprise systems, enabling autonomous decision-making and real-time data synthesis across decoupled microservices.

This technical execution encompasses deploying autonomous execution swarms over asynchronous message queues (Redis/BullMQ), enforcing robust, persistent state management through high-dimensional vector databases (Supabase pgvector), and bridging complex, zero-downtime containerized ecosystems (Docker) capable of handling massive telemetry and inference workloads without failure.

---

## 🚀 Core Architectural Implementations

### [Distributed AI Researcher](https://github.com/NallaSumang/DISTRIBUTED-AI-RESEARCHER-) | [Live App](https://distributed-ai-researcher.vercel.app)
> **Stack:** Next.js 16 · FastAPI · LangGraph · Groq (LLaMA 3.3 70B) · Upstash Redis · Supabase PostgreSQL
> **Deploy:** Vercel (frontend) · Hugging Face Spaces Docker (backend + worker on port 7860)
* Distributed research engine that decomposes complex queries into parallel execution threads via a LangGraph agent swarm (Architect → Scouts → Synthesizer).
* Backend worker runs as a background process in the same Docker container, consuming jobs from Upstash Redis via BRPOP and archiving synthesized reports to Supabase.
* Scouts execute concurrent web searches via `duckduckgo-search` + Python `asyncio`, eliminating I/O bottlenecks.

### [Nexus Career Intelligence](https://github.com/NallaSumang/NEXUS-CAREER-INTELLIGENCE) | [Live App](https://nexus-ai-vqxe.onrender.com)
> **Stack:** React 18/Vite · Node.js/Express · Python/FastAPI · BullMQ · Upstash Redis · MongoDB Atlas · Firebase Auth
> **Deploy:** Single Docker container on Render free tier (Node + Python via `concurrently`)
* Full-stack career copilot — resume parsing (PDF → GridFS → LLM), job matching, cover letter generation, and interview prep, all offloaded to BullMQ workers.
* Python is a pure stateless HTTP service; Node BullMQ workers consume queue jobs and call Python over localhost HTTP. Python never touches Redis.
* Switchable LLM providers (OpenAI / Groq / Gemini) via `AI_PROVIDER` env var with 55s timeouts.

### [Autonomous Vision AI](https://github.com/NallaSumang/VISION-AI) | [Live App](https://sumang-vision-ai-jczj.vercel.app/)
> **Stack:** Next.js 16 · Python/FastAPI · Google Gemini (`gemini-2.0-flash-lite`) · Pinecone
> **Deploy:** Vercel (frontend) · Render (backend: `my-ai-brain`)
* Multimodal AI engine processing text + image inputs through Google Gemini for inference, with persistent vector memory via Pinecone (`vision-memory` index) for long-duration context retention.
* Conversation state serialized to `chat_history.json` for local backup alongside Pinecone's durable vector layer.

### [Lumina-Proposals](https://github.com/NallaSumang/Lumina-Proposals)
> **Stack:** Next.js 15 · TypeScript · shadcn/ui · Zustand · TanStack Query · Custom RAG pipeline
> **Status:** Local development prototype (not deployed)
* Local-first RAG engine for processing corporate RFPs — complete document ingestion pipeline with semantic chunking, embedding, and retrieval services.
* RAG service layer is fully implemented (7 TypeScript modules) but currently operates on mock embeddings; OpenAI integration is stubbed but not yet wired to a live key.

### [BrutalBench](https://github.com/NallaSumang/BrutalBench)
> **Stack:** Next.js 16 · Supabase PostgreSQL · Google Gemini · NextAuth (GitHub OAuth) · n8n
> **Status:** Local development (not deployed)
* AI-powered code evaluation framework with a leaderboard dashboard. Google Gemini scores LLM-generated code against engineering rubrics.
* n8n webhook integration upserts evaluation metrics into Supabase via stored procedures, automating the scoring pipeline.

### [Kaggle Concierge Agent](https://github.com/NallaSumang/kaggle-concierge-agent)
> **Stack:** Google ADK 2.0 · Gemini 2.5 Flash · MCP Filesystem Server · Python
> **Status:** Local CLI tool
* Autonomous file-system organizer using Google's Agent Development Kit 2.0 Workflow API with a strict human-in-the-loop approval boundary (SCAN → PLAN → CONFIRM).
* LLM agent interfaces with a local MCP Filesystem Server via stdio to scan, categorize, and sort files without any cloud dependencies.

---


## 🏆 Advanced Certifications

* **IBM RAG and Agentic AI Professional Certificate** — Coursera.
* **Oracle Cloud Infrastructure Certified AI Foundations Associate** — Oracle.
* **Oracle Agentic AI Certified Foundations Associate** — Oracle.
* **Oracle Fusion AI Agent Studio Certified Foundations Associate (Rel 1)** — Oracle.
* **AI Engineer for Data Scientists Associate** — DataCamp.
* **Associate Data Engineer** — DataCamp.
* **Microsoft SQL Server Professional Certificate** — Coursera.
* **Google Advanced Data Analytics Professional Certificate** — Coursera.

---
## 💼 Fellowships & Technical Engagements

* **IBM SkillsBuild & Edunet Foundation** | *AI & Cloud Engineering Intern*
  * Participated in an intensive, project-based enterprise engineering track focused on emerging cloud platforms and agentic AI architectures under the IBM SkillsBuild initiative. 
  * Designed and engineered the [watsonx-nutrition-agent](https://github.com/NallaSumang/watsonx-nutrition-agent) utilizing **IBM Watsonx Orchestrate**, implementing structured prompt behavior mapping, runtime knowledge-source ingestion, and automated multi-turn reasoning pipelines tailored for precision advisory domains.
  * Explored real-world enterprise agent integration patterns, leveraging cloud-native tools to orchestrate deterministic workflows and minimize hallucination vectors in conversational interfaces.

* **NexLevr** | *AI & Automation Engineering Intern*
  * Engaged in advanced automation engineering workflows, focusing heavily on execution resilience, system integration, and large language model output governance.
  * Developed and open-sourced the [LLM-Output-Variance-CLI](https://github.com/NallaSumang/LLM-Output-Variance-CLI), an auxiliary developer tool engineered to systematically audit temperature parameters, measure probabilistic generation drift, and evaluate token-level variance across high-parameter inference endpoints.
  * Focused on bridging production reliability gaps by establishing reproducible measurement scripts for runtime model stability.

---
## ⚙️ Core Architecture & Technology Stack 

<div align="center">
  <br />
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=python,ts,nodejs,react,nextjs,fastapi,docker,redis,mongodb,postgres,supabase,linux,git,bash,aws,gcp&perline=8" />
  </a>
  <br />
</div>

<br>

* **System Design:** Microservices, Event-Driven Queues, Container Orchestration (Docker), Serverless Functions.
* **Data Infrastructure:** Relational SQL, MongoDB (NoSQL), Supabase (pgvector), Redis (BullMQ), Vector Search (Pinecone).
* **Backend Frameworks:** Node.js, Next.js (Edge), Python (FastAPI).
* **AI Integration:** LLM Orchestration (LangGraph, Google ADK), RAG Architecture, Multi-Agent Swarms, Google Gemini, Groq.
