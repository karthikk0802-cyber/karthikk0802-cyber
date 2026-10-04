<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=30&pause=1000&color=4F8EF7&center=true&width=720&lines=Full-Stack+Developer+%E2%80%A2+MERN+%2B+AI%2FLLM+Integration" alt="Karthikeyan — Full-Stack Developer" />

**Hi, I'm Karthikeyan 👋** — I build production-grade web applications end to end,
with a growing focus on the AI layer behind them.

[![Profile](https://img.shields.io/badge/Profile-karthikk0802--cyber-181717?logo=github&style=flat-square)](https://github.com/karthikk0802-cyber)
[![Top Lang](https://img.shields.io/badge/Language-JavaScript%20%2F%20Python%20%2F%20PHP-blue?style=flat-square)](#-stack)
[![Focus](https://img.shields.io/badge/Focus-RAG%20%7C%20LLM%20Orchestration-orange?style=flat-square)](#-featured-work)

</div>

---

## 💼 About

I'm a developer who likes the unglamorous half of engineering as much as the
interesting half — the schemas that don't need migrating every sprint, the APIs that
degrade gracefully when a third party is down, and the UI that respects the person
using it.

Most of my work sits at the intersection of **full-stack product engineering** and
**applied AI**: RAG pipelines, LLM orchestration with deterministic fallbacks, and the
business logic that has to stay correct when a model is in the loop.

- 🔭 Currently building **OnboardIQ** — adaptive onboarding powered by RAG
- 🌱 Learning production LLM engineering: evals, fallbacks, guardrails
- 💬 Ask me about RAG retrieval tuning, spaced-repetition algorithms, or MERN architecture
- ⚡ Believe a model should generate *content*, never *decide business logic*

---

## 🛠 Stack

<table>
<tr><td valign="top" width="50%">

**Frontend**
`React 19` `Vite` `Context API` `Tailwind CSS` `Plotly` `Lucide`

Responsive, mobile-first interfaces with deliberate
information hierarchy and design systems
(Poppins, monochrome/glassmorphism themes).

</td><td valign="top" width="50%">

**Backend**
`Node.js` `Express` `FastAPI` `Uvicorn` `Pydantic v2` `REST` `RBAC`

REST API design, session auth, role-based access
control, deterministic business rules.

</td></tr>
<tr><td valign="top">

**Data**
`MongoDB` `MySQL` `SQLite` `SQLAlchemy 2.x`

Schema modelling, migrations, indexed query design.

</td><td valign="top">

**AI / ML**
`ChromaDB` `BGE-small` `RAG` `Mistral AI` `NetworkX` `Tesseract OCR`

Vector retrieval with confidence scoring,
spaced repetition, prerequisite graphs, document parsing.

</td></tr>
<tr><td valign="top">

**Tooling**
`Git` `GitHub Actions` `Vercel` `pytest` `Oxlint` `Postman`

</td><td valign="top">

**Practices**
Tested core logic · Frozen API contracts ·
Secrets never committed · AI fallbacks ·
Accessibility-minded UI

</td></tr>
</table>

---

## 🚀 Featured Work

### ⭐ OnboardIQ — Adaptive Onboarding & Knowledge Coach
`React 19` · `FastAPI` · `ChromaDB` · `BGE-small` · `Mistral AI` · `NetworkX`

An AI platform that diagnoses what a new hire *doesn't know*, teaches it adaptively,
and reports readiness back to their manager.

**What makes it interesting**
- **RAG with receipts** — cosine distance from ChromaDB maps to a
  `Strong → General AI Guidance` confidence label; draft and unapproved documents are
  excluded from retrieval entirely.
- **Adaptive spaced repetition** — deterministic mastery math (`+20/+10/+5` scaled by
  difficulty) on a `1 → 3 → 7 → 14 → 30` day review ladder.
- **Prerequisite graph** — a NetworkX DAG converts a flat topic list into a topological
  learning order, so nobody is taught CI/CD before the basics.
- **Degrades without AI** — every LLM path falls back to deterministic output when no
  API key is present, so the app never hard-fails.

`51 REST endpoints` · `25 service modules` · `4 pytest suites` · `~6.7k lines Python` · `~3.3k lines React`

[**View repository →**](https://github.com/karthikk0802-cyber/OnboardIQ)

---

### PESDMS — Police Security Deployment & Duty Management
`MongoDB` · `Express` · `React` · `Node.js` · `Tailwind CSS`

Digitising police *bandobust* planning — officer rosters, deployment posts and duty
orders for festivals, rallies and VIP visits.

- **Excel-first ingestion** — uploads `.xlsx` rosters and validates missing records,
  duplicate Police IDs and rank standards via smart column mapping.
- **Zero double-allocation** — deterministic rules prevent overlapping-shift conflicts,
  with every decision recorded in an **immutable audit log**.
- **Station isolation** — RBAC guarantees personnel only ever see their own station's data.
- **Official output** — generates formatted PDF deployment orders with signature blocks.

Deliberately **zero AI dependencies** — auditable, deterministic logic only.

[**View repository →**](https://github.com/karthikk0802-cyber/police-deployment-system)

---

### College Bus Live Tracking
`MongoDB` · `Express` · `React` · `Socket.IO` · `Google Maps`

Real-time bus tracking where the driver's phone browser *is* the GPS hardware — no
dedicated device, no hardware cost.

- **Heartbeat freshness model** — `LIVE` (<30s) · `STALE` (≥30s) · `OFFLINE` (≥3m or
  socket drop), so the UI never lies about where a bus is.
- **Socket.IO** location stream with throttled 8-second sends and a live map view.
- **Speed-based ETAs**, sequential stops, autocomplete search, admin force-stop.
- **Auto-expiry worker** — trips terminate when idle >20 min or exceed 4 hours.

[**View repository →**](https://github.com/karthikk0802-cyber/CollegeTransport)

---

### TerraCheck AI — Land Record Verification
`Python` · `Flask` · `Tesseract OCR`

OCR-based verification for Tamil Nadu *Patta Chitta* land records — citizens submit
documents, the system extracts and validates them, and officers review before
authentication.

- OCR extraction pipeline with image preprocessing and PDF report generation
- Citizen dashboard, officer verification queue, request status tracking
- Tamper-detection heuristics on extracted field values

[**View repository →**](https://github.com/karthikk0802-cyber/TerraCheck-AI)

---

## 🧠 Engineering Principles

<table>
<tr><td width="50%">

**Determinism where it counts**
Model-generated content is fine. Model-*decided* business logic is not. Mastery math,
scoring, and authorisation are pure functions with no model in the loop.

**Contracts before features**
API contracts are frozen and versioned (`/api/v2/*`) instead of edited in place, so
clients never break mid-refactor.

</td><td>

**Secrets never committed**
`.env`, databases and caches are gitignored and untracked from day one. Only
`.env.example` is versioned.

**Test the logic that counts**
Suites target rules that would be expensive to get wrong — not coverage vanity metrics.

</td></tr>
</table>

---

## 📊 Stats

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=karthikk0802-cyber&show_icons=true&theme=default&hide_border=true&include_all_commits=true&count_private=true" alt="Karthikeyan's GitHub stats" />
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs?username=karthikk0802-cyber&layout=compact&theme=default&hide_border=true" alt="Top languages" />

</div>

---

## 📫 Let's Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white&style=for-the-badge)](https://www.linkedin.com/in/karthikeyan-k-3b2073374)
[![Email](https://img.shields.io/badge/Email-EA4335?logo=gmail&logoColor=white&style=for-the-badge)](mailto:karthikk0802@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white&style=for-the-badge)](https://github.com/karthikk0802-cyber)

**Open to full-stack / MERN developer roles.** If you're hiring and want to talk about
RAG in production, adaptive learning systems, or just say hi — my inbox is open.

---

<div align="center">

<sub>Built with curiosity — mostly late at night. ☕</sub>

</div>