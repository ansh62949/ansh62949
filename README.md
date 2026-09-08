# Ansh Pathak

### AI & Backend Engineer

Building intelligent AI systems, distributed backends, and developer infrastructure.

<p align="left">
  <a href="https://portfolio-zhir.vercel.app/">
    <img src="https://img.shields.io/badge/Portfolio-portfolio--zhir.vercel.app-FFB000?style=for-the-badge&logo=vercel&logoColor=0B0D10&labelColor=0B0D10" alt="Portfolio"/>
  </a>
  <a href="https://www.linkedin.com/in/anshpathak/">
    <img src="https://img.shields.io/badge/LinkedIn-in%2Fanshpathak-FFB000?style=for-the-badge&logo=linkedin&logoColor=0B0D10&labelColor=0B0D10" alt="LinkedIn"/>
  </a>
  <a href="mailto:ansh62949@gmail.com">
    <img src="https://img.shields.io/badge/Email-ansh62949%40gmail.com-FFB000?style=for-the-badge&logo=gmail&logoColor=0B0D10&labelColor=0B0D10" alt="Email"/>
  </a>
  <a href="https://github.com/ansh62949">
    <img src="https://img.shields.io/badge/GitHub-ansh62949-FFB000?style=for-the-badge&logo=github&logoColor=0B0D10&labelColor=0B0D10" alt="GitHub"/>
  </a>
  <a href="https://leetcode.com/u/ansh62949/">
    <img src="https://img.shields.io/badge/LeetCode-ansh62949-FFB000?style=for-the-badge&logo=leetcode&logoColor=0B0D10&labelColor=0B0D10" alt="LeetCode"/>
  </a>
</p>

<p align="left">
  <code>AI/LLM</code> &bull; <code>RAG</code> &bull; <code>LangGraph</code> &bull; <code>FastAPI</code> &bull; <code>Spring Boot</code> &bull; <code>Kafka</code> &bull; <code>Redis</code> &bull; <code>PostgreSQL</code> &bull; <code>Docker</code>
</p>

<p align="left">
  <img src="https://komarev.com/ghpvc/?username=ansh62949&label=PROFILE%20VIEWS&color=FFB000&style=flat-square" alt="Profile Views"/>
</p>

---

## About

I am a **Computer Science (Artificial Intelligence) undergraduate** at **GL Bajaj Institute of Technology and Management** (2023–2027), Greater Noida, India.

I specialize in building production-style **AI/LLM engineering systems** and **scalable backend architecture**. My technical focus centers on constructing multi-agent orchestration workflows, RAG pipelines, and event-driven microservices built for resilience, isolation, and performance.

---

## Engineering Domains

<table width="100%">
  <tr>
    <td width="33%" valign="top">
      <h4>🤖 AI / LLM Engineering</h4>
      <ul>
        <li>RAG & Vector Retrieval (pgvector)</li>
        <li>Multi-Agent Workflows (LangGraph)</li>
        <li>Repository Embeddings & Semantic Search</li>
        <li>Adaptive AI Prompt Orchestration</li>
      </ul>
    </td>
    <td width="33%" valign="top">
      <h4>⚙️ Backend Engineering</h4>
      <ul>
        <li>REST APIs & WebSockets (Spring Boot, FastAPI)</li>
        <li>JWT Auth & Security Rotation</li>
        <li>Layered Controller → Service → Repo</li>
        <li>Database Schema & Indexing</li>
      </ul>
    </td>
    <td width="33%" valign="top">
      <h4>🌐 Distributed Systems</h4>
      <ul>
        <li>Event-Driven Pipelines (Apache Kafka)</li>
        <li>Asynchronous Job Queues (RabbitMQ)</li>
        <li>Redis Caching & Spatial GEO Queries</li>
        <li>Docker Container Sandboxing</li>
      </ul>
    </td>
  </tr>
</table>

---

## Tech Stack

### Languages
<p>
  <img src="https://skillicons.dev/icons?i=py,java,js,c&perline=7" alt="Languages"/>
</p>

### AI & Backend Engineering
<p>
  <img src="https://skillicons.dev/icons?i=spring,fastapi,postgres,mysql,mongodb&perline=7" alt="AI & Backend"/>
</p>

### Messaging & Infrastructure
<p>
  <img src="https://skillicons.dev/icons?i=kafka,rabbitmq,redis,docker,linux,git,maven&perline=7" alt="Messaging & Infrastructure"/>
</p>

---

## Featured Projects

### 🤖 PRSense — AI-Powered Pull Request Review Platform

> **Repository:** [ansh62949/prsense-ai](https://github.com/ansh62949/prsense-ai) &nbsp;|&nbsp; **Live Demo:** [prsense-ai.vercel.app](https://prsense-ai.vercel.app/)

An AI-powered pull request review platform using multi-agent workflows and RAG to analyze code changes and provide contextual review feedback.

- **Multi-Agent Orchestration:** Architected a stateful review workflow using **LangGraph**, delegating specialized security, architectural consistency, style, and test-coverage audits across GitHub PR diffs.
- **Contextual Retrieval:** Engineered a RAG pipeline utilizing repository embeddings and **pgvector (HNSW, cosine similarity)** on PostgreSQL for deep semantic context.
- **Non-Blocking Execution:** Connected **GitHub Webhooks** via async background tasks in **FastAPI** with a **Spring Boot** service layer for continuous code audits.

`LangGraph` &bull; `FastAPI` &bull; `pgvector` &bull; `Spring Boot` &bull; `PostgreSQL` &bull; `GitHub Webhooks`

<p align="left">
  <a href="https://github.com/ansh62949/prsense-ai">
    <img src="https://img.shields.io/badge/View%20Project-0B0D10?style=flat-square&logo=github&logoColor=FFB000" alt="View Project"/>
  </a>
  <a href="https://prsense-ai.vercel.app/">
    <img src="https://img.shields.io/badge/Live%20Demo-FFB000?style=flat-square&logo=vercel&logoColor=0B0D10" alt="Live Demo"/>
  </a>
</p>

---

### 🧠 CodeSphere — Distributed Online Judge & Sandbox Execution Engine

> **Repository:** [ansh62949/codesphere](https://github.com/ansh62949/codesphere)

A distributed coding platform built with a microservices architecture designed to process concurrent code submissions in isolated environments.

- **Microservices Architecture:** Architected 7 independently deployable services (API Gateway, Auth, Submission Engine, Leaderboard) in **Spring Boot** with **Eureka** service discovery.
- **Asynchronous Queueing:** Offloaded untrusted code execution to **RabbitMQ** queues, maintaining low-latency rank queries via **Redis sorted sets**.
- **Isolated Sandboxing:** Engineered a secure **Linux/Docker sandbox** supporting Java, Python, and C++ execution with resource quotas and fork-bomb prevention.

`Java` &bull; `Spring Boot` &bull; `Docker` &bull; `RabbitMQ` &bull; `Redis` &bull; `MySQL` &bull; `MongoDB` &bull; `Eureka`

<p align="left">
  <a href="https://github.com/ansh62949/codesphere">
    <img src="https://img.shields.io/badge/View%20Project-0B0D10?style=flat-square&logo=github&logoColor=FFB000" alt="View Project"/>
  </a>
</p>

---

### 🚗 HerRide — Event-Driven Ride-Hailing Backend & Safety System

> **Repository:** [ansh62949/herride](https://github.com/ansh62949/herride) &nbsp;|&nbsp; **Live Demo:** [herride-six.vercel.app](https://herride-six.vercel.app/)

An event-driven ride-hailing and safety platform engineered for real-time driver matching and immediate emergency escalation for female passengers.

- **Event-Driven Messaging:** Decoupled ride matching, driver status updates, and emergency SOS escalations across 4 **Apache Kafka** topics.
- **Spatial Discovery & WebSockets:** Implemented nearby-driver lookup using **Redis GEO** (`GEOADD`/`GEORADIUS`) and real-time emergency dashboard streaming via **WebSockets**.
- **Security & JWT:** Secured REST and WebSocket endpoints via **JWT token rotation** with Spring Security, monitored by **Prometheus & Grafana**.

`Java 21` &bull; `Spring Boot 3.5` &bull; `Kafka` &bull; `Redis GEO` &bull; `PostgreSQL` &bull; `WebSockets` &bull; `JWT`

<p align="left">
  <a href="https://github.com/ansh62949/herride">
    <img src="https://img.shields.io/badge/View%20Project-0B0D10?style=flat-square&logo=github&logoColor=FFB000" alt="View Project"/>
  </a>
  <a href="https://herride-six.vercel.app/">
    <img src="https://img.shields.io/badge/Live%20Demo-FFB000?style=flat-square&logo=vercel&logoColor=0B0D10" alt="Live Demo"/>
  </a>
</p>

---

### 🎯 AI Mock Interview Coach — Adaptive Technical Interview Simulator

> **Repository:** [ansh62949/AI-Mock-Interview-Coach](https://github.com/ansh62949/AI-Mock-Interview-Coach)

An adaptive technical interview simulator that dynamically evaluates candidate responses and adjusts question difficulty in real time.

- **Six-Agent StateGraph:** Constructed a modular **LangGraph** flow (Planner, Interviewer, Evaluator, Reflection, Controller, Coach) with dynamic conditional routing.
- **Adaptive Difficulty Control:** Dynamically tuned interview question difficulty in real time based on candidate performance using structured **Pydantic** schemas.
- **Full-Stack Validation:** Built a **FastAPI backend** and **Streamlit UI**, thoroughly verified with 13 Pytest test suites covering graph state and API handlers.

`Python` &bull; `LangGraph` &bull; `FastAPI` &bull; `Streamlit` &bull; `Pydantic` &bull; `Pytest`

<p align="left">
  <a href="https://github.com/ansh62949/AI-Mock-Interview-Coach">
    <img src="https://img.shields.io/badge/View%20Project-0B0D10?style=flat-square&logo=github&logoColor=FFB000" alt="View Project"/>
  </a>
</p>

---

## Coding & LeetCode

Active problem solver on **[LeetCode](https://leetcode.com/u/ansh62949/)** with **300+ DSA problems solved** across Arrays, Trees, Graphs, Dynamic Programming, and Greedy algorithms.

<div align="center">
  <a href="https://leetcode.com/u/ansh62949/">
    <img src="https://leetcard.jacoblin.cool/ansh62949?theme=dark&font=Fira+Code&ext=contest" alt="LeetCode Stats Card"/>
  </a>
</div>

<br>

<p align="center">
  <a href="https://leetcode.com/u/ansh62949/">
    <img src="https://img.shields.io/badge/LeetCode%20Profile-ansh62949-FFB000?style=for-the-badge&logo=leetcode&logoColor=0B0D10&labelColor=0B0D10" alt="LeetCode Profile"/>
  </a>
</p>

---

## GitHub Activity

<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=ansh62949&hide_border=true&background=0B0D10&stroke=FFB000&ring=FFB000&fire=FFB000&currStreakNum=F5F7FA&sideNums=F5F7FA&currStreakLabel=FFB000&sideLabels=8B949E&dates=8B949E" alt="GitHub Streak"/>
</div>

---

## Engineering Proof

* **Hack the Globe 2026 (GlobalSpark):** Selected for Round 2 out of thousands of international university applicants.
* **Walmart Global Tech — Software Engineering Virtual Experience (Forage):** Completed job simulation focusing on enterprise data structures, algorithmic processing flows, and backend logic design (*February 2025*).
* **Hewlett Packard Enterprise — Software Engineering Virtual Experience (Forage):** Completed job simulation covering REST API workflow handlers and object-oriented backend architecture (*February 2025*).

---

## Education

**B.Tech in Computer Science & Engineering (Artificial Intelligence)**  
GL Bajaj Institute of Technology and Management — Greater Noida, UP, India  
*September 2023 — May 2027*

---

## Currently Building

```yaml
currently_building:
  learning:
    - Advanced System Design & High-Availability Architecture
    - Distributed Consensus Protocols & Event Sourcing
  building:
    - PRSense: Multi-Agent AI Code Review Platform
    - Distributed Spring Boot & Kafka Event Pipelines
  exploring:
    - Vector Indexing Optimization (pgvector HNSW)
    - LangGraph Complex State Routing Patterns
  open_to:
    - AI Engineering Roles
    - Backend Engineering Roles
    - Scalable Distributed Systems Collaboration
```

---

## Let's Connect

<p align="center">
  <a href="https://portfolio-zhir.vercel.app/">
    <img src="https://img.shields.io/badge/Portfolio-portfolio--zhir.vercel.app-FFB000?style=for-the-badge&logo=vercel&logoColor=0B0D10&labelColor=0B0D10" alt="Portfolio"/>
  </a>
  <a href="https://www.linkedin.com/in/anshpathak/">
    <img src="https://img.shields.io/badge/LinkedIn-in%2Fanshpathak-FFB000?style=for-the-badge&logo=linkedin&logoColor=0B0D10&labelColor=0B0D10" alt="LinkedIn"/>
  </a>
  <a href="mailto:ansh62949@gmail.com">
    <img src="https://img.shields.io/badge/Email-ansh62949%40gmail.com-FFB000?style=for-the-badge&logo=gmail&logoColor=0B0D10&labelColor=0B0D10" alt="Email"/>
  </a>
  <a href="https://github.com/ansh62949">
    <img src="https://img.shields.io/badge/GitHub-ansh62949-FFB000?style=for-the-badge&logo=github&logoColor=0B0D10&labelColor=0B0D10" alt="GitHub"/>
  </a>
  <a href="https://leetcode.com/u/ansh62949/">
    <img src="https://img.shields.io/badge/LeetCode-ansh62949-FFB000?style=for-the-badge&logo=leetcode&logoColor=0B0D10&labelColor=0B0D10" alt="LeetCode"/>
  </a>
</p>

<p align="center">
  <i>"Build systems. Ship intelligence."</i>
</p>
