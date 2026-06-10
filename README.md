<h1 align="center">Matheus Constantino</h1>

<p align="center">
  Full Stack Engineer &nbsp;·&nbsp; Geospatial &nbsp;·&nbsp; Distributed Systems &nbsp;·&nbsp; AI Integration<br/>
  7 years building products where data volume, spatial precision, and deadlines actually matter
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/matheus-constantino-gomes/">LinkedIn</a>
  &nbsp;·&nbsp;
  <a href="mailto:matheusconstantino57@gmail.com">matheusconstantino57@gmail.com</a>
</p>

---

### What I do

I build systems at the intersection of **high-volume data processing, geospatial engineering, and distributed architecture** — domains where a wrong coordinate, a late batch, or a missed regulatory deadline has real consequences.

---

### Currently: Kaffa Tech — BDGD Pipeline

The BDGD (Base de Dados Geográficos da Distribuidora) is the geospatial database that every electricity distributor in Brazil must validate and deliver to ANEEL. It's ~30 GB of spatial data per release, tables with **30M+ rows**, dozens of validation rules, and hard regulatory deadlines.

The architecture is purpose-built for throughput and correctness:

```
[Angular / NX Monorepo] → [Node.js API] → [RabbitMQ exchange + routing keys] → [.NET processing motor]
                                 ↑                                                        ↓
                          [GeoServer layers]  ←  [PostGIS / SQL Server spatial results]
```

What this looks like in practice:
- Designing **RabbitMQ** exchange/routing-key topologies for async Node.js ↔ .NET communication
- **Batch write strategies** and spatial index tuning on PostGIS and SQL Server (30M+ rows)
- **GeoServer** layer publishing and SRID validation at scale
- **Angular (NX monorepo)** for front end — making geographic validation results understandable to engineers and regulators

Stack: `Angular` `NX Monorepo` `Node.js` `TypeScript` `RabbitMQ` `.NET (processing motors)` `PostGIS` `SQL Server` `GeoServer` `PostgreSQL`

---

### Previously: We Are Dvelopers — 4 Product Verticals

Shipped production features across 4 different domains. Same discipline every time: understand the business constraint, design for it, deliver.

**LMS Platform Migration**
- Decomposed a PHP monolith into microservices (Node.js)
- Event bus with RabbitMQ for async communication
- Reduced deploy time from 45 min → 8 min with per-service CI/CD
- 94% improvement in TTFB, independent horizontal scaling

**Payment Gateway**
- Multi-gateway architecture with circuit breaker pattern
- Automatic fallback across providers (Stripe, PayPal, PagSeguro, Mercado Pago)
- DLQ + exponential retry for critical transactions
- 99.8% uptime even with individual gateway failures

**Streaming Platform (1K+ concurrent users)**
- Hybrid CDN (CloudFront + edge caching), p95 latency < 200ms
- Adaptive bitrate with HLS + serverless transcoding (AWS Lambda)
- 63% reduction in storage costs with S3 Intelligent-Tiering

**FinTech / Open Banking**
- Integrated 15+ banking APIs with adapter pattern for isolation
- Real-time pipeline with PostgreSQL for financial reconciliation
- R$100K+ transactions/month with full audit trail and compliance

Stack: `Node.js` `React` `Vue` `TypeScript` `PostgreSQL` `MongoDB` `Redis` `AWS`

---

### How I use AI in engineering — not just "I use AI tools"

I designed the full development workflow of [`poc-geoserver-sqlserver`](https://github.com/MatheusConstantino/poc-geoserver-sqlserver) around AI agents — and the same philosophy carries into daily work:

- **Spec-first discipline** — every feature starts as a spec, reviewed by a PO agent before a single line of code is written
- **Specialized agents** — PO, QA, Spatial Expert, Infra, and Reviewer agents, each with domain-specific context (`.claude/agents/`)
- **Pre-merge gate** — a Reviewer agent checks security, spatial correctness, and API contracts before any PR lands
- **Runtime AI layer** — Claude API endpoints for benchmark interpretation and geospatial inconsistency triage, with Zod schema validation so output is always machine-readable and typed
- **Custom slash commands** — `/project:benchmark`, `/project:validate`, `/project:qa` — repeatable, documented workflows anyone on the team can run

The philosophy: **AI as a system component with defined responsibilities**, not a chat window you paste code into.

---

### Technical decisions I think about

**Eventual vs. strong consistency?**
In payment systems I kept ACID/PostgreSQL for transactions and eventual consistency for notifications — 40% throughput gain without compromising financial integrity.

**Monorepo vs. polyrepo for microservices?**
Adopted NX monorepo for shared libraries — reduced duplication significantly, but required solid per-service CI. Worth it for cross-service refactoring speed.

**RabbitMQ vs. Kafka — which one?**
RabbitMQ for transactional events where delivery confirmation is critical. Each tool for its actual use case.

**When not to add a spatial index?**
STIntersects on large POLYGON inputs can cause full scans if selectivity is low. For the BDGD pipeline, filtered indexes on known geographic partitions make the difference between a query that runs in 80ms and one that times out.

---

### Full stack, genuinely

```
Frontend  →  Angular (NX monorepo) · React (2022–) · Vue (2018–)
Backend   →  Node.js · TypeScript · Fastify · RabbitMQ · REST
Spatial   →  PostGIS · SQL Server Spatial · GeoServer
Data      →  PostgreSQL · SQL Server · MongoDB · Supabase
AI        →  Claude API · Anthropic SDK · multi-agent workflows
DevOps    →  Docker · Docker Compose · GitHub Actions · AWS
```

---

### Featured projects

| Project | What it demonstrates |
|---------|---------------------|
| [poc-geoserver-sqlserver](https://github.com/MatheusConstantino/poc-geoserver-sqlserver) | SQL Server vs PostGIS spatial benchmark — 15 scenarios, AI-generated insights via Claude API, multi-agent dev workflow, full CI/CD |
| **rebanho** *(private)* | Platform for organizing and managing religious community events — Supabase + TypeScript |

---

### By the numbers

- **30 GB** BDGD processed per release cycle
- **30M+** rows handled in batch with optimized write strategies
- **15** spatial benchmark scenarios automated end-to-end
- **7 years** writing production code across spatial, fintech, media, and education

---

<div align="center">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=MatheusConstantino&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=MatheusConstantino&layout=compact&langs_count=7&theme=tokyonight"/>
</div>
