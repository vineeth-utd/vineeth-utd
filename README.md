# Hi, I'm Vineeth 👋

![ASU](https://img.shields.io/badge/Arizona_State_University-MS_Computer_Science-8C1D40?style=flat-square)
![Experience](https://img.shields.io/badge/Experience-3%2B_Years_SWE-2563EB?style=flat-square)
![Focus](https://img.shields.io/badge/Focus-Backend_%7C_Distributed_Systems_%7C_Data_%7C_AI-0F766E?style=flat-square)
![Open to Work](https://img.shields.io/badge/2027-Full--Time_Opportunities-16A34A?style=flat-square)

I'm an M.S. Computer Science student at Arizona State University, graduating in May 2027, with 3+ years of professional Software Engineering experience at **Swym Technologies**, where I built and scaled production SaaS systems used by millions of shoppers.

My core strengths are in **backend engineering, distributed systems, data engineering, and databases**. I'm also actively deepening my expertise in **AI Engineering** by building reliable AI-powered applications with agentic AI, RAG, tool orchestration, semantic retrieval, evaluation, and guardrails.

I'm particularly interested in engineering at the intersection of **scalable systems, data, and AI** — building reliable products that solve real-world problems.

[LinkedIn](https://www.linkedin.com/in/vineeth-subramaniam-j/) · [Email](mailto:vineeth.jaisankar@gmail.com)

---

## ⚡ Engineering Highlights

- **Built and scaled production SaaS systems at Swym Technologies** used by millions of shoppers, working across backend services, data workflows, databases, APIs, and customer-facing products.
- **Redesigned a high-volume shopper segmentation workflow** from synchronous processing to Redis-based asynchronous distributed processing, reducing runtime for 100K shoppers from **7–8 hours to 1–2 hours** while enabling horizontal scalability.
- **Led the end-to-end development of Nudges**, a personalized marketing automation platform, from early development through production and go-to-market, contributing to approximately **$520K in revenue across 25 pilot merchants**.

---

## 🚀 Featured Projects

### Customer Intelligence Platform
**Jul 2026 – Present** · Event-Driven Systems · Data Engineering · Backend · AI Engineering

A production-inspired, event-driven platform that transforms merchant, shopper, product, and campaign activity into authoritative operational data, reproducible analytics, and actionable customer intelligence.

- Engineered reliable **Kafka-based event processing** with versioned Pydantic contracts, idempotent processing, controlled offset commits, and dead-letter queue isolation, preserving event history alongside authoritative operational state in PostgreSQL.
- Built a decoupled **analytics and derived-data architecture** with scheduled, idempotent processing, historical point-in-time state reconstruction, and incremental regeneration of changed entities while preserving reproducibility from source data.
- Exposed operational and analytical intelligence through **typed FastAPI APIs and React/TypeScript dashboards**, with merchant, platform, feature, and campaign analytics and end-to-end validation from generated business activity to visualization.
- Currently extending the platform toward **evidence-grounded AI investigations** using controlled business tools, exact and semantic retrieval, LangGraph, Qdrant, and an AI Gateway — keeping deterministic business data authoritative while AI assists with investigation and explanation.

**Tech:** Python · FastAPI · Apache Kafka · PostgreSQL · React · TypeScript · Docker · LangGraph · Qdrant

[View Repository](https://github.com/vineeth-utd/customer-intelligence-platform)

### TimeLedger — AI-Powered Time Tracking & Productivity Platform
**Jul 2026 – Oct 2026** · Agentic AI · Full-Stack Engineering · Reliable AI Workflows

A production-deployed productivity platform for time tracking, weekly goals, analytics, and AI-powered workflows, built from a personal tool into an application used for daily time management.

- Engineered a **LangGraph/LangChain multi-tool AI assistant** with authenticated server-side tool execution, durable conversation state, ambiguity resolution, and server-controlled confirmations with at-most-once execution for safe conversational actions.
- Built **Whisper-powered voice input** that feeds into the same controlled assistant workflow, with transcription review before execution, and developed deterministic agent evaluations covering tool selection, ambiguity, confirmations, concurrency, and failure scenarios.
- Built an **AI Productivity Agent** where authoritative weekly analytics are computed deterministically and the LLM generates validated insights and recommendations, with persisted report history, concurrency-safe scheduled generation, bounded recovery, and optional email delivery.
- Optimized prompts and tool schemas to reduce fixed LLM context by approximately **30%**, while keeping model access separated from authentication, business logic, and direct database operations.

**Tech:** Next.js · React · PostgreSQL/Supabase · Prisma · LangGraph · LangChain · Whisper · Vercel

[Live Demo](https://timeledger-app.vercel.app) · [View Repository](https://github.com/vineeth-utd/TimeLedger)

### AeroTrace — AI-Powered Legacy Code Intelligence
**Oct 2026** · Static Analysis · Impact Analysis · Evidence-Grounded AI

Built at the **Honeywell Aerospace Devils Invent Hackathon**, AeroTrace analyzes legacy C/C++ and Ada code to help engineers understand unfamiliar codebases, trace dependencies, and assess the impact and risk of code changes.

- Built a compiler-based **static-analysis pipeline** using libclang and Tree-sitter to extract functions, calls, reads, writes, and data relationships into a language-neutral code graph, including resolution of virtual-dispatch dependencies.
- Developed **graph-based impact analysis** that traces affected callers, data dependencies, files, and entry points, enabling deterministic change-risk analysis without relying on LLM inference.
- Engineered **graph-verified LLM explanations** that validate referenced functions and side effects against static-analysis evidence, flag unverifiable claims for human review, and preserve links back to source code.
- Validated the system on real open-source C++ and Ada codebases spanning approximately **188K lines across 570+ files**, demonstrating the approach across large multi-language legacy codebases.

**Tech:** Python · TypeScript · libclang · Tree-sitter · FastAPI · React · Static Analysis · Graph Analysis · LLMs

[View Repository](https://github.com/aayushswami123/aerotrace-hack/)

### GeoTrack — Distributed Parcel Tracking & ETA Service
**Aug 2025 – Dec 2025** · Distributed Systems · Event Streaming · Distributed Databases

A geo-distributed, event-driven parcel tracking system designed to process real-time parcel movement events across multiple geographic regions while preserving per-parcel event ordering and regional workload isolation.

- Designed and implemented the **Kafka ingestion layer** with region-based topics, tracking ID-based partitioning, distributed producers and consumers, batch processing, offset management, and dead-letter queues.
- Preserved **in-order processing for each parcel while enabling parallel processing across partitions**, with offsets committed after successful batch persistence and failed events isolated for later processing.
- Integrated the streaming pipeline with **multi-region CockroachDB**, using geographically distributed data placement and replication alongside FastAPI services for parcel tracking.
- Performed load and fault-tolerance testing with Prometheus and Grafana, processing **millions of events** and reaching approximately **40K events/minute with zero consumer lag** at the optimal configuration.

**Tech:** Apache Kafka · CockroachDB · FastAPI · Python · Prometheus · Grafana

[View Repository](https://github.com/bharanidharan27/geo-track)

---

## 🧩 Other Projects

### The Unofficial Guide — RAG Housing Assistant for ASU Students
**Jun 2026** · RAG · Semantic Retrieval · Retrieval Evaluation

Built an end-to-end RAG application that makes real housing experiences near ASU searchable across **3,200+ chunks** derived from apartment reviews and Reddit discussions, producing grounded answers with source attribution.

- Designed the retrieval pipeline using recursive chunking, Sentence Transformers, and ChromaDB, with **property-aware metadata reranking** introduced after evaluation exposed apartment-specific retrieval failures.
- Built grounded generation constrained to retrieved evidence, with **programmatic source attribution** and supporting retrieved chunks exposed for transparency and debugging.
- Evaluated retrieval and generation behavior across representative questions, traced answer-quality failures back to retrieval, and identified hybrid retrieval and stronger reranking as next-step improvements.

**Tech:** Python · ChromaDB · Sentence Transformers · Groq · Gradio

[View Repository](https://github.com/vineeth-utd/the-unofficial-guide)

---

## 🛠️ Technical Areas

**Languages:** Python · JavaScript/TypeScript · Clojure · Go · Java

**Backend & Distributed Systems:** REST APIs · FastAPI · Node.js · GraphQL · Apache Kafka · Redis · Distributed Processing

**Data & Databases:** SQL · PostgreSQL · MongoDB · CockroachDB · Qdrant · ChromaDB

**Data Engineering:** ETL/ELT Workflows · Data Pipelines · Data Architecture · Data Modeling · Data Quality & Validation · Query Optimization · Data Transformation · API Integration

**AI Engineering:** Agentic AI · LangGraph · LangChain · RAG · Tool Calling & Orchestration · Semantic Retrieval · Vector Databases · AI Evaluation · AI Guardrails

**Frontend:** React · TypeScript

**Cloud & Infrastructure:** Microsoft Azure (Data Factory · Cosmos DB · Blob Storage · VMs) · Docker · Kubernetes · Jenkins · ArgoCD

**Tools & Platforms:** Git · GitHub · Metabase · DBeaver · Claude Code · Cursor · Antigravity · GitHub Copilot

---

## 🚧 Currently Building

I'm currently expanding the **Customer Intelligence Platform** with merchant and shopper profiles, journeys, segmentation, merchant health, and richer business analytics, building on its completed event-driven and incremental data-processing foundation.

The next layer brings **evidence-grounded AI investigations** through controlled business tools, exact and semantic retrieval, an AI Gateway, and LangGraph-based investigation workflows.

---

## 🤝 Let's Connect

I'm exploring **2027 full-time opportunities** in Software Engineering, Backend & Distributed Systems, Data Engineering, and AI Engineering.

I'm especially interested in building **reliable, scalable systems and AI-powered applications** that solve real-world problems and create meaningful business impact.

[LinkedIn](https://www.linkedin.com/in/vineeth-subramaniam-j/) · [Email](mailto:vineeth.jaisankar@gmail.com)