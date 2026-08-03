# Verified Projects — Quick Analysis & Runbook

This document provides concise, repository-level analyses and minimum reproducible checks for the projects linked from the main portfolio README. The goal: make each project verifiable by a technical reviewer or recruiter without changing external deployments or other repositories.

---

## Distributed AI Researcher
- Live demo: https://distributed-ai-researcher.vercel.app
- Source repo: https://github.com/NallaSumang/DISTRIBUTED-AI-RESEARCHER-
- Key tech (observed): Next.js frontend (app/), Node/TS, Supabase client in frontend, Tailwind, Redis/BullMQ mentioned in portfolio text.
- What I inspected: frontend/package.json, frontend/README.md

Quick run/check (local)
1. cd DISTRIBUTED-AI-RESEARCHER-/frontend
2. npm install
3. npm run dev
4. Open http://localhost:3000 and verify the main page loads; check console for missing env keys.

Minimum recommended repo changes (small, safe):
- Add a short `HOW_TO_RUN.md` with exact env var names and sample values or `.env.example` in the frontend directory.
- Add Vercel deployment badge to README and a "Last tested: YYYY-MM-DD" line.

---

## Nexus Career Intelligence
- Live demo: https://nexus-ai-vqxe.onrender.com
- Source repo: https://github.com/NallaSumang/NEXUS-CAREER-INTELLIGENCE
- Key tech (observed): Node/Next.js client (client/), Python/FastAPI server (server/), Dockerfile present, render.yaml, package.json at repo root.
- What I inspected: package.json, Dockerfile, render.yaml, .env.example

Quick run/check (local)
1. Review .env.example and populate any required env values.
2. To run locally (client only): cd client && npm install && npm run dev
3. To run server (if Python/FastAPI): check server/ for requirements/pyproject, then run uvicorn server:app
4. If Docker is preferred: docker build -t nexus-career . && docker run --env-file .env -p 3000:3000 nexus-career

Minimum recommended repo changes:
- Add explicit `README` sections for both `client/` and `server/` showing exact commands to run each part and sample envs.
- Add small smoke tests (one curl request against an unauthenticated health endpoint) and a CI workflow that runs them.
- Add a Render/Vercel badge and a short "How I validated the deployed demo" note.

---

## Lumina-Proposals (Enterprise RAG)
- Live demo: (linked in main README)
- Source repo: https://github.com/NallaSumang/Lumina-Proposals
- Key tech (observed): Next.js app (app/), RAG modules in ai-rag/, Tailwind, pgvector/Supabase mentioned in portfolio.
- What I inspected: package.json, next.config.ts, ai-rag folder present, README.md

Quick run/check (local)
1. cd Lumina-Proposals
2. npm install
3. npm run dev
4. Test upload or query flows used in the demo (follow README examples if present)

Minimum recommended repo changes:
- Add a short ARCHITECTURE.md describing the RAG pipeline (vector DB, embedding model, retriever) with key files referenced.
- Add a `SAMPLE_DATA/` folder with a small sample document and a script that ingests it into the pipeline for local testing.

---

## Kaggle Concierge Agent
- Live demo: (linked in main README)
- Source repo: https://github.com/NallaSumang/kaggle-concierge-agent
- Key tech (observed): Single-file agent.py (Python), designed for local autonomous file-system operations.
- What I inspected: agent.py, README.md

Quick run/check (local)
1. Create a Python virtualenv
2. Inspect top of agent.py for dependency list; pip install -r requirements.txt if present, otherwise install common libs used in the script
3. Run `python agent.py --help` or open the script to see the CLI entry and run a dry-run mode (if implemented)

Minimum recommended repo changes:
- Add a `requirements.txt` or `pyproject.toml` listing exact dependencies and a short `USAGE.md` with example commands and a safe dry-run option.
- Add a clear safety note and example safe directory to run the agent on to avoid accidental destructive ops.

---

## Vision AI
- Live demo: https://sumang-vision-ai-jczj.vercel.app
- Source repo: https://github.com/NallaSumang/VISION-AI
- Key tech (observed): Next.js app + backend directory, TypeScript, ESLint, Tailwind. package.json, next.config.ts present.
- What I inspected: README.md, package.json, next.config.ts, app/ and backend/ directories present

Quick run/check (local)
1. cd VISION-AI
2. npm install
3. npm run dev
4. Visit http://localhost:3000 and test multi-modal upload UI if available

Minimum recommended repo changes:
- Add a `HEALTHCHECK.md` showing a short list of manual steps to validate visual upload and multi-modal inference.
- Add simple unit or integration test for backend endpoints and a GitHub Actions workflow that runs `npm ci && npm test`.

---

## BrutalBench
- Live demo: (linked in main README)
- Source repo: https://github.com/NallaSumang/BrutalBench
- Key tech (observed): Next.js frontend in frontend/, supabase folder, README present
- What I inspected: README.md and repo layout

Quick run/check (local)
1. cd BrutalBench/frontend
2. npm install
3. npm run dev
4. Check for supabase config and sample envs (supabase/ directory)

Minimum recommended repo changes:
- Add a CONTRIBUTING.md and small demo dataset if the project evaluates code automatically.
- Add a SECURITY.md or responsible disclosure note if the project executes code for evaluation.

---

General, repo‑level safe improvements I can add to each portfolio-linked repository (single-file changes per repo — low-risk):
1. `PROJECT_OVERVIEW.md` — 1-page summary (purpose, tech stack, entry point, quick run commands).
2. `BADGES.md` or badge line in README — Vercel/Render/Netlify deploy badge + CI badge placeholder.
3. `.github/workflows/ci.yml` — a minimal CI that installs deps and runs a smoke check (npm ci && npm run build OR python -m pytest) depending on the repo.
4. `README` additions: "How I validated the live demo" and a small smoke test command.

What I changed here
- I added this file `PROJECTS-VERIFIED.md` to your main portfolio repository to collect these per-project quick analyses and run steps. It does not change any linked project or deployment.

Next steps I can take (pick one or more):
- Apply the minimal, low-risk edits listed above to ONE repository of your choice (create PROJECT_OVERVIEW.md or CI workflow). I will only modify that single target repo and leave all other repos and deployments untouched.
- Or, create ready-to-paste PR text & files you can use to submit those changes manually to each repo.

Tell me which repository you want me to update first (or say "portfolio only" to only update the main repo). If you choose a project repo, I will: (a) add a single safe file (PROJECT_OVERVIEW.md or .env.example), and (b) add a minimal CI smoke workflow. These will be minimal edits aimed at making the project easier to verify and more professional for HR and senior reviewers.
