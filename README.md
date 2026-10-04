<div align="center">

<img src="https://capsule-render.vercel.app/api?type=venom&color=0:0d1117,50:3a2a00,100:FFB000&height=230&section=header&text=Ansh%20Pathak&fontSize=62&fontColor=ffffff&fontAlignY=38&desc=AI%20%26%20Backend%20Engineer&descAlignY=58&descSize=22&animation=fadeIn" width="100%"/>

<img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&weight=500&size=20&pause=1000&color=FFB000&center=true&vCenter=true&width=720&lines=LangGraph+%C2%B7+Multi-Agent+Workflows+%C2%B7+Hybrid+RAG;Spring+Boot+3.5+%C2%B7+Apache+Kafka+%C2%B7+Redis+GEO;FastAPI+%C2%B7+pgvector+%C2%B7+Qdrant+%C2%B7+MCP;Kubernetes+%C2%B7+GitHub+Actions+CI%2FCD" alt="Typing SVG" />

<br/><br/>

<a href="https://portfolio-zhir.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-FFB000?style=for-the-badge&logo=vercel&logoColor=0B0D10" alt="Portfolio"/></a>
<a href="https://www.linkedin.com/in/anshpathak/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
<a href="https://leetcode.com/u/ansh62949/"><img src="https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black" alt="LeetCode"/></a>
<a href="mailto:ansh62949@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>

<br/><br/>

<i>B.Tech CSE (Artificial Intelligence) · GL Bajaj Institute of Technology and Management · 2023 – 2027<br/>
Open to AI/LLM Engineering and Software Engineering roles.</i>

</div>

<br/>

## 👋 About

I build **agentic AI systems** and the **distributed backends** they run on. My projects pair a Java/Spring Boot core with Python/FastAPI AI services, and I ship them with Kubernetes and CI/CD.

- 🤖 **AI:** LangGraph StateGraphs, hybrid RAG (Qdrant + pgvector), MCP servers, human-in-the-loop agents
- ⚙️ **Backend:** event-driven services with Kafka, Redis GEO, STOMP WebSockets, JWT security
- ☸️ **Infra:** 5-service Kubernetes cluster, GitHub Actions CI/CD publishing to GHCR
- 💬 **Ask me about:** LangGraph, Kafka event streams, RAG pipelines, Spring Boot / FastAPI architecture

<br/>

## 🚀 Featured projects

### 🚗 HerRide: women-only ride-hailing platform
<img src="https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Boot_3.5-6DB33F?style=flat-square&logo=springboot&logoColor=white"/> <img src="https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white"/> <img src="https://img.shields.io/badge/Redis_GEO-DC382D?style=flat-square&logo=redis&logoColor=white"/> <img src="https://img.shields.io/badge/PostgreSQL_16-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/React_18-61DAFB?style=flat-square&logo=react&logoColor=black"/>

A safety-first ride-hailing MVP for India that connects verified female drivers with passengers. It has real-time driver matching, trusted-contact SOS escalation and an admin safety dispatch board.

```mermaid
flowchart TB
    subgraph Clients["Clients · React 18 + Zustand"]
        RA["Rider app"]
        DA["Driver app"]
        AD["Admin safety board"]
    end

    subgraph Core["Spring Boot 3.5 core"]
        SEC["Spring Security<br/>JWT access + refresh"]
        TS["Trip service"]
        SS["Safety service"]
        CH["STOMP chat handler"]
    end

    GEO[("Redis GEO<br/>GEOADD / GEORADIUS")]
    K{{"Kafka<br/>trip.requested · trip.accepted<br/>trip.completed · trip.sos"}}
    PG[("PostgreSQL 16")]
    SMS["SMS gateway<br/>trusted contacts"]

    RA -->|REST| SEC
    DA -->|"REST · location ping every 8s"| SEC
    AD -.->|"WSS · STOMP"| SEC
    SEC --> TS
    SEC --> SS
    SEC --> CH
    TS --> PG
    TS -->|"driver coordinates"| GEO
    TS --> K
    SS --> PG
    SS --> K
    K -->|"trip.sos"| SMS
    K -->|"/topic/admin/sos"| AD

    classDef svc fill:#FFB000,stroke:#B37A00,color:#0d1117;
    classDef data fill:#1f6feb,stroke:#0b3d91,color:#ffffff;
    classDef ext fill:#30363d,stroke:#6e7681,color:#ffffff;
    class SEC,TS,SS,CH svc;
    class GEO,PG,K data;
    class RA,DA,AD,SMS ext;
```

- **Kafka decoupling:** ride requests, driver matches, completions and SOS alarms are published as events, so notifications and audits never block the API threads.
- **Redis GEO:** drivers ping every 8 seconds, and `GEORADIUS` returns riders their nearby drivers within 5 km without SQL geometric scans.
- **SOS pipeline:** `trip.sos` triggers an SMS with a live location link to trusted contacts and a STOMP broadcast to the admin dispatch board.
- **Security:** a female-only signup rule enforced in the API, plus JWT with refresh-token rotation. Docs via Swagger, metrics via Prometheus/Grafana.

[**Code**](https://github.com/ansh62949/Herride) · [**Live demo**](https://herride-six.vercel.app) · [**Swagger**](https://herride.onrender.com/swagger-ui.html)

<br/>

### 🤖 PRSense AI: repository-aware PR review
<img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white"/> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/> <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square"/> <img src="https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black"/> <img src="https://img.shields.io/badge/GitHub_Webhooks-181717?style=flat-square&logo=github&logoColor=white"/>

When a pull request opens, PRSense reviews the diff against the repository's own indexed code and flags issues in security, architecture, style and test coverage.

```mermaid
flowchart LR
    GH["GitHub<br/>PR webhook"] -->|"signature validated"| SB
    UI["React frontend"] --> SB
    SB["Spring Boot<br/>orchestrator · JWT"] -->|"HTTP · 202 Accepted"| FA

    subgraph FA["FastAPI analysis service · BackgroundTasks"]
        direction TB
        CL["Clone repo<br/>chunk + embed"]
        RV["LangGraph review<br/>security · architecture<br/>style · test coverage"]
    end

    FA <-->|"HNSW · cosine similarity"| PG[("PostgreSQL<br/>+ pgvector")]
    FA -->|"callback with results"| SB

    classDef svc fill:#FFB000,stroke:#B37A00,color:#0d1117;
    classDef data fill:#1f6feb,stroke:#0b3d91,color:#ffffff;
    classDef ext fill:#30363d,stroke:#6e7681,color:#ffffff;
    class SB,CL,RV svc;
    class PG data;
    class GH,UI ext;
```

- **Two independently deployable services:** Spring Boot handles auth, webhooks and persistence, and FastAPI handles indexing and LLM analysis.
- **Grounded reviews:** repository code is chunked and embedded into pgvector (1536-dimension vectors), and each review retrieves the nearest context for the diff.
- **Deliberate trade-off:** direct HTTP with async callbacks instead of a message queue, to keep deployment simple for small and mid-sized workloads.

[**Code**](https://github.com/ansh62949/prsense-ai) · [**Live demo**](https://prsense-ai.vercel.app/)

<br/>

### 📬 FlowInbox AI: agentic email workspace
<img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square"/> <img src="https://img.shields.io/badge/MCP-6E56CF?style=flat-square"/> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/> <img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square"/> <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white"/>

[![CI](https://github.com/ansh62949/FlowInbox/actions/workflows/ci.yml/badge.svg)](https://github.com/ansh62949/FlowInbox/actions/workflows/ci.yml) [![CD](https://github.com/ansh62949/FlowInbox/actions/workflows/cd.yml/badge.svg)](https://github.com/ansh62949/FlowInbox/actions/workflows/cd.yml)

An AI-native workspace where LangGraph agents triage Gmail threads, analyze intent, sender context, sentiment and urgency, and draft grounded replies. Consequential actions wait for human approval.

```mermaid
flowchart TB
    WEB["React 18 + Vite<br/>Nginx proxy"] -->|"REST · SSE"| API
    GW["Google Workspace<br/>Gmail + Calendar · OAuth 2.0"] --> API

    subgraph API["FastAPI async backend"]
        direction TB
        LG["LangGraph agent<br/>email analysis + reply drafting"]
        HITL{"Human approval gate<br/>send_email · create_calendar_event"}
        LG --> HITL
    end

    LG -->|"primary tool caller"| GROQ["Groq<br/>llama-3.3-70b"]
    LG -.->|fallback| GEM["Gemini"]
    LG --> RAG["Hybrid RAG"]
    RAG --> Q[("Qdrant<br/>dense vectors")]
    RAG --> FTS[("PostgreSQL<br/>full-text search")]
    Q & FTS -->|"Reciprocal Rank Fusion"| LG
    API --> R[("Redis cache")]
    MCP["MCP servers<br/>stdio · HTTP/SSE"] -.-> API
    CD["Claude Desktop · Cursor"] -.->|"inbox + calendar tools"| MCP

    classDef svc fill:#FFB000,stroke:#B37A00,color:#0d1117;
    classDef data fill:#1f6feb,stroke:#0b3d91,color:#ffffff;
    classDef ext fill:#30363d,stroke:#6e7681,color:#ffffff;
    class LG,HITL,RAG,MCP svc;
    class Q,FTS,R data;
    class WEB,GW,GROQ,GEM,CD ext;
```

- **Hybrid retrieval:** dense vectors from Qdrant and PostgreSQL full-text results are merged with Reciprocal Rank Fusion.
- **Safe by design:** sending an email or creating a calendar event creates a pending approval request, and nothing is dispatched without human sign-off.
- **MCP:** inbox and calendar tools are exposed to Claude Desktop and Cursor over stdio and HTTP/SSE.
- **Shipped like a product:** a 5-service Kubernetes manifest set (backend, frontend, PostgreSQL, Qdrant, Redis) with health probes, persistent volumes and a documented self-healing demo. GitHub Actions runs 16 Pytest cases and publishes images to GHCR.

[**Code**](https://github.com/ansh62949/FlowInbox) · [**Live demo**](https://flow-inbox.vercel.app)

<br/>

### 🎯 AI Mock Interview Coach: adaptive multi-agent interviewer
<img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square"/> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/> <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white"/> <img src="https://img.shields.io/badge/Pydantic_V2-E92063?style=flat-square&logo=pydantic&logoColor=white"/> <img src="https://img.shields.io/badge/Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white"/>

An interview platform that adapts to the candidate instead of following a fixed question list. A Reflection agent decides each turn whether to probe, simplify, change difficulty or finish.

```mermaid
flowchart TD
    A["Candidate"] --> B["Streamlit UI"]
    B --> C["FastAPI"]
    C --> D["LangGraph workflow"]
    D --> E["Planner agent"]
    E --> F["Interviewer agent"]
    F --> G["Evaluator agent<br/>scores 1-10"]
    G --> H{"Reflection agent"}
    H -->|"probe / simplify"| F
    H -->|"adjust difficulty"| I["Difficulty Controller<br/>Junior · Mid · Senior · Staff"]
    I --> F
    H -->|"finish"| J["Coach agent"]
    J --> K["Final coaching report"]

    classDef svc fill:#FFB000,stroke:#B37A00,color:#0d1117;
    classDef ext fill:#30363d,stroke:#6e7681,color:#ffffff;
    class E,F,G,H,I,J svc;
    class A,B,C,D,K ext;
```

- **Why a graph:** interviews are non-linear, and conditional routing edges model probing, difficulty changes and topic transitions better than a fixed chain.
- **Separation of concerns:** the Evaluator scores objectively and the Reflection agent decides routing, which keeps rules like the follow-up cap (`probe_count <= 2`) deterministic.
- **Typed contracts:** Pydantic V2 schemas (`InterviewStrategy`, `EvaluationResult`, `ReflectionOutput`, `FinalReport`) sit over a shared `InterviewState`. 13/13 Pytest cases cover agents, schemas, graph and API.

[**Code**](https://github.com/ansh62949/AI-Mock-Interview-Coach)

<br/>

## 🛠️ Tech stack

<div align="center">

| | |
|:--|:--|
| **🤖 Agents & Orchestration** | <img src="https://img.shields.io/badge/LangGraph_StateGraph-1C3C3C?style=flat-square"/> <img src="https://img.shields.io/badge/Multi--Agent_Systems-FFB000?style=flat-square&labelColor=0d1117"/> <img src="https://img.shields.io/badge/Human--in--the--Loop-6E56CF?style=flat-square"/> <img src="https://img.shields.io/badge/MCP-6E56CF?style=flat-square"/> <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square"/> |
| **🔎 RAG & Retrieval** | <img src="https://img.shields.io/badge/Hybrid_Retrieval_(RRF)-FFB000?style=flat-square&labelColor=0d1117"/> <img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square"/> <img src="https://img.shields.io/badge/pgvector_(HNSW)-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/Postgres_Full--Text_Search-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/Embeddings-0d1117?style=flat-square"/> |
| **🧠 LLMs & Prompting** | <img src="https://img.shields.io/badge/Groq_(Llama_3.3_70B)-F55036?style=flat-square"/> <img src="https://img.shields.io/badge/Gemini-4285F4?style=flat-square&logo=googlegemini&logoColor=white"/> <img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white"/> <img src="https://img.shields.io/badge/LLM_Routing_%26_Fallback-0d1117?style=flat-square"/> <img src="https://img.shields.io/badge/Prompt_Engineering-0d1117?style=flat-square"/> |
| **⚡ AI Services (Python)** | <img src="https://skillicons.dev/icons?i=py,fastapi&perline=8"/>   <img src="https://img.shields.io/badge/Pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white"/> |
| **⚙️ Backend (Java)** | <img src="https://skillicons.dev/icons?i=java,spring,maven&perline=8"/> <img src="https://img.shields.io/badge/Spring_Security_%2B_JWT-6DB33F?style=flat-square&logo=springsecurity&logoColor=white"/> <img src="https://img.shields.io/badge/WebSockets_(STOMP)-0d1117?style=flat-square"/> <img src="https://img.shields.io/badge/REST_%2B_Swagger-85EA2D?style=flat-square&logo=swagger&logoColor=black"/> |
| **🔀 Distributed Systems** | <img src="https://skillicons.dev/icons?i=kafka,redis&perline=8"/> <img src="https://img.shields.io/badge/Event--Driven_Architecture-0d1117?style=flat-square"/> <img src="https://img.shields.io/badge/Microservices-0d1117?style=flat-square"/> |
| **🗄️ Databases** | <img src="https://skillicons.dev/icons?i=postgres,mysql&perline=8"/> |
| **☸️ Deployment** | <img src="https://skillicons.dev/icons?i=kubernetes,githubactions&perline=8"/> <img src="https://img.shields.io/badge/CI%2FCD_%2B_GHCR-0d1117?style=flat-square"/> |

</div>

<br/>

## 🏆 Achievements & certifications

- 🌍 **Hack the Globe 2026 (GlobalSpark):** selected for Round 2 out of thousands of global applicants
- 🧩 **LeetCode:** 300+ problems across Arrays, Trees, Graphs, DP and Greedy
- 🤗 **Hugging Face:** Agents Course, Certificate of Excellence (Sep 2026)
- 💻 **Claude Academy:** Claude Code in Action (Sep 2026)
- 🏢 **Walmart Global Tech & Hewlett Packard Enterprise:** SWE Virtual Experience Programs, Forage (Feb 2025)

<br/>

## 📊 GitHub stats

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=ansh62949&show_icons=true&theme=tokyonight&hide_border=true&border_radius=10" width="48%" alt="GitHub stats"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=ansh62949&layout=compact&theme=tokyonight&hide_border=true&border_radius=10" width="48%" alt="Top languages"/>
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com?user=ansh62949&theme=tokyonight&hide_border=true&border_radius=10" alt="GitHub streak"/>
</p>

<div align="center">

<br/>

<i>Building resilient backends and intelligent agentic workflows.</i>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:FFB000,100:0d1117&height=110&section=footer" width="100%"/>

</div>
