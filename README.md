<div align="center">
  <h1>Hi, I'm Nalla Sumang 👋</h1>
  <h3>AI Systems Architect & Backend Engineer</h3>
  <p><em>Designing autonomous workflows, multi-agent LLM pipelines, and resilient asynchronous infrastructure.</em></p>
  
  <p align="center">
    <a href="mailto:sumangsumang41@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email" /></a>
    <a href="https://linkedin.com/in/nalla-sumang-03180139b"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  </p>
</div>

---

## ⚡ About Me

I am an AI Systems Architect specializing in bridging the gap between advanced Large Language Models and production-grade software engineering. My focus is on moving beyond simple chatbots to embed **AI as a core reasoning engine** within decoupled, microservice-based architectures.

I build systems that can autonomously synthesize data, orchestrate complex parallel tasks via message queues (Redis/BullMQ), and maintain persistent state using high-dimensional vector databases. 

---

## 🚀 Featured Engineering Projects

### 🌐 [Distributed AI Researcher](https://github.com/NallaSumang/DISTRIBUTED-AI-RESEARCHER-)
*An autonomous agentic swarm that parallelizes deep-dive internet research.*
- **Architecture:** Orchestrates a LangGraph agent swarm (Architect → Scouts → Synthesizer) to decompose complex queries into parallel execution threads, eliminating I/O bottlenecks.
- **Infrastructure:** Frontend deployed on **Vercel**; backend deployed via **Docker** on **Hugging Face Spaces**. Uses **Upstash Redis** as an asynchronous job queue (preventing HTTP timeouts) and **Supabase (PostgreSQL)** for permanent report archival.
- **Tech Stack:** ![Next.js](https://img.shields.io/badge/Next.js-black?style=flat-square&logo=next.js) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![LangGraph](https://img.shields.io/badge/LangGraph-FF9900?style=flat-square) ![Groq](https://img.shields.io/badge/Groq_LLaMA_3.3-f3f4f6?style=flat-square&logo=meta) ![Redis](https://img.shields.io/badge/Upstash_Redis-DC382D?style=flat-square&logo=redis&logoColor=white) 
- **Live Demo:** [distributed-ai-researcher.vercel.app](https://distributed-ai-researcher.vercel.app)

### 💼 [Nexus Career Intelligence](https://github.com/NallaSumang/NEXUS-CAREER-INTELLIGENCE)
*A decoupled full-stack career copilot for automated resume parsing, job matching, and interview prep.*
- **Architecture:** A hybrid Node.js and Python microservice ecosystem. CPU-heavy resume parsing (PDF → LLM) and inference tasks are offloaded to asynchronous **BullMQ** workers to keep the HTTP layer strictly stateless and non-blocking.
- **Infrastructure:** Deployed as a unified Docker container on **Render**, utilizing **MongoDB Atlas** (GridFS) for document storage and switchable AI providers (Groq/Gemini/OpenAI) with enforced 55s timeouts.
- **Tech Stack:** ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) ![Express](https://img.shields.io/badge/Express-black?style=flat-square&logo=express) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![BullMQ](https://img.shields.io/badge/BullMQ-FF4081?style=flat-square) ![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=flat-square&logo=mongodb&logoColor=white)
- **Live Demo:** [nexus-ai-vqxe.onrender.com](https://nexus-ai-vqxe.onrender.com)

### 👁️ [Autonomous Vision AI](https://github.com/NallaSumang/VISION-AI)
*A multimodal visual reasoning engine with persistent memory retention.*
- **Architecture:** Captures text and image inputs to perform multimodal inference using **Google Gemini 2.0 Flash Lite**.
- **Infrastructure:** Split deployment with a **Vercel** Next.js frontend and a **Render** Python backend. Implements persistent conversation memory using a **Pinecone** vector store index, alongside local JSON state backup, ensuring unbroken context across long-duration sessions.
- **Tech Stack:** ![Next.js](https://img.shields.io/badge/Next.js-black?style=flat-square&logo=next.js) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Gemini](https://img.shields.io/badge/Google_Gemini-4285F4?style=flat-square&logo=google) ![Pinecone](https://img.shields.io/badge/Pinecone-000000?style=flat-square)
- **Live Demo:** [sumang-vision-ai-jczj.vercel.app](https://sumang-vision-ai-jczj.vercel.app/)

### 📄 [Lumina-Proposals](https://github.com/NallaSumang/Lumina-Proposals)
*An enterprise Retrieval-Augmented Generation (RAG) prototype for corporate RFPs.*
- **Architecture:** A local-first pipeline for ingesting, semantically chunking, embedding, and retrieving complex 100+ page corporate documents.
- **Implementation Status:** Engineered 7 modular TypeScript RAG services (chunking, embedding, retrieval, prompting) natively within Next.js. Currently designed as a local development prototype utilizing structural mock embeddings for rapid iteration, with OpenAI integration architected but stubbed.
- **Tech Stack:** ![Next.js](https://img.shields.io/badge/Next.js-black?style=flat-square&logo=next.js) ![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white) ![Zustand](https://img.shields.io/badge/Zustand-4A3629?style=flat-square) ![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?style=flat-square) 

### ⚔️ [BrutalBench](https://github.com/NallaSumang/BrutalBench)
*An AI-powered evaluation framework and automated scoring leaderboard.*
- **Architecture:** Evaluates LLM-generated code against strict engineering rubrics using Google Gemini, counting tokens via `js-tiktoken`.
- **Infrastructure:** Local monolithic Next.js execution environment utilizing **Supabase (PostgreSQL)** for leaderboard state and **n8n** webhooks for automated metric ingestion. Protected by NextAuth GitHub OAuth.
- **Tech Stack:** ![Next.js](https://img.shields.io/badge/Next.js-black?style=flat-square&logo=next.js) ![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white) ![Gemini](https://img.shields.io/badge/Google_Gemini-4285F4?style=flat-square&logo=google) ![n8n](https://img.shields.io/badge/n8n-FF6C37?style=flat-square&logo=n8n&logoColor=white)

### 🤖 [Kaggle Concierge Agent](https://github.com/NallaSumang/kaggle-concierge-agent)
*A local autonomous file-system orchestrator leveraging MCP tools.*
- **Architecture:** Engineered a strict human-in-the-loop (SCAN → PLAN → CONFIRM) workflow tool to categorize and sort local unstructured directories.
- **Infrastructure:** Built purely in Python using Google's **Agent Development Kit (ADK) 2.0** and **Gemini 2.5 Flash**. The agent securely interacts with the host filesystem via a local **Model Context Protocol (MCP)** server over standard I/O streams.
- **Tech Stack:** ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Google ADK 2.0](https://img.shields.io/badge/Google_ADK-4285F4?style=flat-square&logo=google) ![MCP](https://img.shields.io/badge/Model_Context_Protocol-000000?style=flat-square) 

---

## 🏆 Advanced Certifications

- **IBM RAG and Agentic AI Professional Certificate** — Coursera
- **Oracle Cloud Infrastructure Certified AI Foundations Associate** — Oracle
- **Oracle Agentic AI Certified Foundations Associate** — Oracle
- **Oracle Fusion AI Agent Studio Certified Foundations Associate (Rel 1)** — Oracle
- **AI Engineer for Data Scientists Associate** — DataCamp
- **Associate Data Engineer** — DataCamp
- **Microsoft SQL Server Professional Certificate** — Coursera
- **Google Advanced Data Analytics Professional Certificate** — Coursera

---

## 💼 Fellowships & Technical Engagements

### IBM SkillsBuild & Edunet Foundation | *AI & Cloud Engineering Intern*
- Participated in an intensive, project-based enterprise engineering track focused on emerging cloud platforms and agentic AI architectures under the IBM SkillsBuild initiative.
- Designed and engineered the `watsonx-nutrition-agent` utilizing **IBM Watsonx Orchestrate**, implementing structured prompt behavior mapping, runtime knowledge-source ingestion, and automated multi-turn reasoning pipelines tailored for precision advisory domains.
- Explored real-world enterprise agent integration patterns, leveraging cloud-native tools to orchestrate deterministic workflows and minimize hallucination vectors in conversational interfaces.

### NexLevr | *AI & Automation Engineering Intern*
- Engaged in advanced automation engineering workflows, focusing heavily on execution resilience, system integration, and large language model output governance.
- Developed and open-sourced the `LLM-Output-Variance-CLI`, an auxiliary developer tool engineered to systematically audit temperature parameters, measure probabilistic generation drift, and evaluate token-level variance across high-parameter inference endpoints.
- Focused on bridging production reliability gaps by establishing reproducible measurement scripts for runtime model stability.

---

## 🛠️ Open Source & Infrastructure Contributions

I actively audit and contribute to the execution layers of major open-source frameworks, focusing heavily on memory safety and runtime stability:

* **[n8n (Enterprise AI Automation) — PR #31726](https://github.com/n8n-io/n8n/pull/31726)**
  * Engineered a critical patch to resolve a fatal Model Context Protocol (MCP) server crash in the webhook execution layer by safe-chaining uninitialized node parameters.
* **[Pydantic (Data Validation) — Issue #13272](https://github.com/pydantic/pydantic/issues/13272)**
  * Diagnosed and staged a recursion-guard patch to prevent a core C-level segmentation fault during PEP 695 self-referential type alias unwrapping.

---

## 💼 Enterprise Engineering Experience

- **Walmart Global Tech:** Designed highly normalized relational database schemas and optimized massive data munging operations to support high-load backend retail environments.
- **JPMorgan Chase & Co.:** Implemented high-throughput, fault-tolerant data storage and messaging solutions integrating Kafka data streams.
- **Commonwealth Bank:** Executed complex full-stack engineering requirements, migrating and modifying core .NET backend services and React frontend components.
- **Deloitte:** Formulated advanced threat mitigation architectures and executed rigorous security protocols to neutralize simulated enterprise network vulnerabilities.

---

## ⚙️ Core Technology Stack

<div align="center">
  <br />
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=python,ts,nodejs,react,nextjs,fastapi,docker,redis,mongodb,postgres,supabase,linux,git,bash,aws,gcp&perline=8" />
  </a>
  <br />
</div>

<br>

* **System Design:** Microservices, Event-Driven Queues, Container Orchestration (Docker), Serverless Functions.
* **Data Infrastructure:** PostgreSQL, MongoDB, Supabase (pgvector), Redis (BullMQ), Vector Search (Pinecone).
* **AI Integration:** LLM Orchestration (LangGraph, Google ADK), RAG Architecture, Multi-Agent Swarms.
