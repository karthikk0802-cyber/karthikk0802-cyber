<div align="center">

# Hi, I'm Karthikeyan 👋

**Full-Stack / MERN Developer — AI-assisted systems for real-world problems**

I build production-style web applications end to end: React frontends, Node/Express
APIs, MongoDB data models — and increasingly the AI layer behind them (RAG pipelines,
LLM orchestration with deterministic fallbacks).

I care about the unglamorous parts: schemas that don't need migrating every sprint,
APIs that degrade gracefully when a third-party API is down, and UIs that respect
the person using them.

</div>

---

## 🛠 Tech Stack

<table>
<tr><td valign="top" width="50%">

**Frontend**
- React 19, Vite, Context API
- Tailwind CSS
- Plotly, Lucide icons
- Responsive, mobile-first layouts

**Backend**
- Node.js, Express
- FastAPI, Uvicorn, Pydantic v2
- REST API design, RBAC
- JWT-style session auth

</td><td valign="top" width="50%">

**Data & AI**
- MongoDB, MySQL, SQLite (SQLAlchemy 2.x)
- ChromaDB vector store, `BAAI/bge-small-en-v1.5`
- RAG pipelines, Mistral AI
- NetworkX graph algorithms

**Tooling**
- Git/GitHub Actions, Vercel
- pytest, Oxlint
- PyMuPDF / Tesseract OCR

</td></tr>
</table>

---

## 🚀 Featured Projects

### 1. OnboardIQ — Adaptive Onboarding & Knowledge Coach `⭐ flagship`
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)](https://github.com/karthikk0802-cyber/OnboardIQ)
[![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=black)](https://github.com/karthikk0802-cyber/OnboardIQ)
[![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)](https://github.com/karthikk0802-cyber/OnboardIQ)
[![Chroma](https://img.shields.io/badge/ChromaDB-646CFF)](https://github.com/karthikk0802-cyber/OnboardIQ)

An AI onboarding platform that diagnoses what a new hire doesn't know, teaches it
adaptively, and reports readiness to their manager.

**What makes it interesting**
- **RAG with receipts** — ChromaDB + BGE-small retrieval where cosine distance maps to a
  `Strong → General AI Guidance` confidence label, and draft/unapproved docs are
  excluded from search entirely.
- **Spaced repetition that adapts** — deterministic mastery math (`+20/+10/+5` scaled by
  difficulty) on a `1 → 3 → 7 → 14 → 30` day review ladder.
- **Prerequisite graph** — NetworkX DAG turns a flat topic list into a topological
  learning order.
- **Degrades without AI** — every LLM path falls back to deterministic output when no
  API key is present.
- **51 REST endpoints · 25 service modules · ~6.7k lines Python · ~3.3k lines React · 4 pytest suites**

[Repo →](https://github.com/karthikk0802-cyber/OnboardIQ)

---

### 2. PESDMS — Police Security Deployment & Duty Management
[![MERN](https://img.shields.io/badge/MERN-3DDC84?logo=mongodb&logoColor=white)](https://github.com/karthikk0802-cyber/police-deployment-system)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://github.com/karthikk0802-cyber/police-deployment-system)

Digitizing police bandobust planning — the officer roster, deployment posts and duty
orders for festivals, rallies and VIP visits.

- **Excel-first ingestion** — uploads `.xlsx` rosters and validates missing records,
  duplicate Police IDs and rank standards with smart column mapping.
- **No double-allocation** — deterministic backend rules prevent overlapping-shift
  conflicts, with reasons recorded in an **immutable audit log**.
- **Station isolation** — RBAC so personnel only ever see their own station's records.
- **Official output** — generates formatted PDF deployment orders with signature blocks.

Deliberately **zero AI dependencies** — deterministic, auditable logic only.

[Repo →](https://github.com/karthikk0802-cyber/police-deployment-system)

---

### 3. College Bus Live Tracking
[![MERN](https://img.shields.io/badge/MERN-3DDC84?logo=mongodb&logoColor=white)](https://github.com/karthikk0802-cyber/CollegeTransport)
[![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?logo=socketdotio&logoColor=white)](https://github.com/karthikk0802-cyber/CollegeTransport)

Real-time bus tracking where the driver's phone browser *is* the GPS hardware — no
dedicated device, no cost.

- **Heartbeat freshness model** — `LIVE` (<30s), `STALE` (≥30s), `OFFLINE` (≥3m or
  socket drop), so the UI never lies about where a bus is.
- **Socket.IO** location stream with throttled 8s sends; Google Maps live view.
- **Speed-based ETAs**, sequential stops, autocomplete bus search.
- **Auto-expiry worker** — trips terminate when idle >20min or exceed 4 hours.

[Repo →](https://github.com/karthikk0802-cyber/CollegeTransport)

---

### 4. TerraCheck AI — Land Record Verification
[![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)](https://github.com/karthikk0802-cyber/TerraCheck-AI)
[![Flask](https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white)](https://github.com/karthikk0802-cyber/TerraCheck-AI)

OCR-based verification for Tamil Nadu *Patta Chitta* land records — citizens submit
documents, the system extracts and validates them, and officers review before
authentication.

- Tesseract OCR pipeline with image preprocessing and report generation
- Citizen dashboard, officer verification queue, request status tracking
- Tamper-detection heuristics on extracted field values

[Repo →](https://github.com/karthikk0802-cyber/TerraCheck-AI)

---

## 💡 How I work

- **Determinism where it matters.** Model-generated content is fine; model-decided
  business logic is not. Mastery math, scoring and authorisation are pure functions.
- **Secrets stay out of git.** `.env`, databases and caches are gitignored and
  untracked from day one — only `.env.example` is committed.
- **Contracts before features.** API contracts are frozen and versioned (`/api/v2/*`)
  rather than edited in place, so clients never break mid-refactor.
- **Test the logic that counts.** Suites target the rules that would be expensive to
  get wrong, not coverage vanity metrics.

## 📫 Let's connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/karthikeyan-k-3b2073374)
[![Gmail](https://img.shields.io/badge/Email-EA4335?logo=gmail&logoColor=white)](mailto:karthikk0802@gmail.com)

---

<div align="center">
<sub>Built with curiosity · <a href="https://github.com/karthikk0802-cyber/OnboardIQ">Currently deep in AI-assisted learning systems</a></sub>
</div>