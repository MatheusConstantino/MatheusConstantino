# Matheus Constantino

**Senior Software Engineer & Tech Lead** | 7+ anos entregando sistemas escaláveis  
São Paulo, Brasil | [LinkedIn](https://linkedin.com/in/matheus-constantino-gomes) | [Email](mailto:matheusconstantino57@gmail.com)

---

## 💻 Stack Técnica

### Backend & APIs
Node.js • PHP/Laravel • C# • Python • REST • GraphQL

### Frontend
React • Vue.js • TypeScript • JavaScript • HTML5 • CSS3

### Databases
PostgreSQL • MySQL • MongoDB • Redis

### Mensageria & Streaming
RabbitMQ • Kafka • Event-Driven Architecture

### Cloud & DevOps
AWS (Lambda, S3, CloudFront, RDS) • Azure • Docker • Kubernetes • CI/CD • GitHub Actions

### Metodologias & Práticas
Clean Architecture • DDD • SOLID • Design Patterns • TDD • Microservices • Scrum • Code Review

---

## 🎯 Experiência Relevante

### Tech Lead @ We are Dvlopers
*Liderança técnica e arquitetura de soluções escaláveis para produtos SaaS*

#### **Migração Monolito → Microservices (LMS Corporativo)**
- Decompôs aplicação PHP monolítica em 8 microservices (Node.js/C#)
- Implementou event bus com **RabbitMQ** para comunicação assíncrona
- **Redis** como cache distribuído + session store
- Reduziu deploy time de 45min → 8min com CI/CD por serviço
- **Impacto:** 94% melhoria no TTFB, escalabilidade horizontal independente

#### **Payment Gateway Resiliente**
- Projetou arquitetura multi-gateway com **circuit breaker pattern**
- Fallback automático entre 5 provedores (Stripe, PayPal, PagSeguro, Mercado Pago)
- **DLQ + retry exponencial** para transações críticas
- PostgreSQL com **ACID garantido** para dados financeiros
- **Resultado:** 99.8% uptime mesmo com indisponibilidade de gateways individuais

#### **Streaming Platform (1K+ concurrent users)**
- CDN híbrida (CloudFront + edge caching) com latência p95 < 200ms
- Adaptive bitrate com **HLS** + transcoding serverless (AWS Lambda)
- **MongoDB** para metadados de vídeo + analytics em tempo real
- **Economia:** 63% em custos de storage com S3 Intelligent-Tiering

#### **FinTech - Open Banking Integration**
- Integrou 15+ APIs bancárias com **adapter pattern** para isolamento
- Pipeline real-time com **Kafka** + PostgreSQL para conciliação financeira
- R$ 100K+ transações/mês com auditoria completa e compliance
- **Microservices** independentes: auth, transactions, reconciliation, reporting

---

## 🧠 Decisões Técnicas de Impacto

**Quando escolher consistência eventual vs. forte?**  
Em sistema de pagamentos, optei por consistência forte (ACID/PostgreSQL) para transações e eventual (Kafka) para notificações - ganho de 40% em throughput sem comprometer integridade financeira.

**Trade-off: Monorepo vs. Polyrepo em microservices**  
Adotei monorepo (Nx) para 8 services - shared libraries centralizadas reduziram duplicação, mas exigiram CI robusto para testes isolados. Valeu a pena pela velocidade de refactoring cross-service.

**Quando não usar cache?**  
Em dashboard financeiro real-time, evitei Redis para dados transacionais - complexidade de invalidação não justificava o ganho vs. leituras otimizadas no PostgreSQL (índices parciais + materialized views).

**RabbitMQ vs. Kafka: qual escolher?**  
Kafka para logs de auditoria (retenção longa, replay) e RabbitMQ para eventos transacionais (confirmação de entrega crítica). Cada ferramenta para seu caso de uso ideal.

---

## 👥 Liderança & Mentoria

- Mentorei **10+ desenvolvedores** (júnior → pleno) com foco em clean code e arquitetura
- Implementei **code review estruturado** (redução de 60% em bugs de produção)
- Defini **padrões arquiteturais** adotados em 5+ projetos simultâneos
- Interface com **stakeholders**: traduzo requisitos de negócio em soluções técnicas viáveis
- Conduzo **tech talks** internas sobre DDD, microservices e boas práticas

---

## 📚 Aprendizado Contínuo

Atualmente expandindo conhecimento em **React Native avançado** e arquiteturas mobile escaláveis (offline-first, complex state management, performance optimization).

---

## 📊 GitHub Stats

<div align="center">
  <img height="180em" src="https://github-readme-stats.vercel.app/api?username=MatheusConstantino&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true"/>
  <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=MatheusConstantino&layout=compact&langs_count=7&theme=tokyonight"/>
</div>

---

**Disponível para:** Consultoria técnica • Arquitetura de sistemas • Liderança de times de engenharia
