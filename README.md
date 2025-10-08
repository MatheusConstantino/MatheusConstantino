# Matheus Constantino

**Senior Software Engineer & Tech Lead** | 7+ anos entregando sistemas escaláveis  
São Paulo, Brasil | [LinkedIn](https://linkedin.com/in/matheus-constantino-gomes) | [Email](mailto:matheusconstantino57@gmail.com)

---

## Stack Principal

**Backend:** Node.js • PHP/Laravel • C# • Python  
**Frontend:** React • Vue.js • TypeScript  
**Infra:** AWS • Azure • Docker • Kubernetes • PostgreSQL • Redis • MongoDB  
**Práticas:** Clean Architecture • DDD • Microservices • Event-Driven • TDD

---

## Experiência Relevante

### Tech Lead @ We are Dvlopers
*Liderança técnica e arquitetura de soluções escaláveis para produtos SaaS*

**Migração Monolito → Microservices (LMS Corporativo)**
- Decompôs aplicação PHP monolítica em 8 microservices (Node.js/C#)
- Implementou event bus com RabbitMQ para comunicação assíncrona
- Reduziu deploy time de 45min → 8min com CI/CD por serviço
- Resultado: 94% melhoria no TTFB, escalabilidade horizontal independente

**Payment Gateway Resiliente**
- Projetou arquitetura multi-gateway com circuit breaker pattern
- Fallback automático entre 5 provedores (Stripe, PayPal, PagSeguro, MP)
- DLQ + retry exponencial para transações críticas
- 99.8% uptime mesmo com indisponibilidade de gateways individuais

**Streaming Platform (1K+ concurrent users)**
- CDN híbrida (CloudFront + edge caching) reduzindo latência p95 < 200ms
- Adaptive bitrate com HLS + transcoding serverless (Lambda)
- Otimização de custos: S3 Intelligent-Tiering economizou 63% em storage

**FinTech - Open Banking Integration**
- Integrou 15+ APIs bancárias com padrão adapter para isolamento
- Pipeline real-time de conciliação financeira (Kafka + PostgreSQL)
- R$ 100K+ transações/mês processadas com auditoria completa

---

## Decisões Técnicas de Impacto

**Quando escolher consistência eventual vs. forte?**  
Em um sistema de pagamentos, optei por consistência forte (ACID) para transações e eventual para notificações - ganho de 40% em throughput sem comprometer integridade financeira.

**Trade-off: Monorepo vs. Polyrepo em microservices**  
Adotei monorepo (Nx) para 8 services - shared libraries centralizadas reduziram duplicação de código, mas exigiram CI robusto para testes isolados por serviço.

**Quando não usar cache?**  
Em dashboard financeiro real-time, evitei Redis para dados transacionais - complexidade de invalidação não justificava o ganho vs. leituras otimizadas no PostgreSQL (índices + materialized views).

---

## Mentoria & Liderança

- Mentorei 10+ desenvolvedores (júnior → pleno)
- Implementei code review estruturado (redução de 60% em bugs de produção)
- Defini padrões arquiteturais adotados em 5+ projetos simultâneos
- Interface com stakeholders: traduzo requisitos de negócio em soluções técnicas viáveis

---

## Aprendizado Contínuo

Atualmente expandindo conhecimento em **React Native avançado** e arquiteturas mobile escaláveis (offline-first, state management complexo).

---

**Disponível para:** Consultoria técnica • Arquitetura de sistemas • Liderança de times de engenharia
