# Alex Chang

**Backend & Distributed Systems Engineer**

I build backend and infrastructure systems where correctness, failure handling, and operational behavior matter.

My recent work focuses on Go, distributed systems, real-time/event-driven architectures, reliability, lifecycle semantics, and systems that must remain understandable when things partially fail.

I enjoy working close to the implementation: tracing unfamiliar codebases, defining invariants, investigating failure modes, and turning ambiguous requirements into systems with explicit behavior.

## Selected Projects

### [Prods](https://github.com/herefindalex/prods)

A self-hosted product catalog and RFQ platform for manufacturers and distributors.

Built as a Go application with SQLite, server-rendered public pages, and a React-based Admin console. The project explores architecture for product data, publishing semantics, search and filtering, durable background jobs, backup/recovery, idempotent RFQs, multilingual content, and deterministic machine-readable outputs.

**Focus:** Go · SQLite · React · Search & indexing · Correctness · Self-hosted systems

---

### [VenueWire](https://github.com/herefindalex/venuewire)

A multi-venue trading connectivity and execution prototype integrating Bybit and Deribit Testnets.

The interesting part is not placing an order—it is handling what happens when the result is uncertain. VenueWire models durable trade intents, idempotency, reconciliation, WebSocket state, freshness, exact decimal amounts, and failure isolation between venues.

**Focus:** Go · REST · JSON-RPC · WebSocket · FIX 4.4 · Reconciliation · Idempotency

---

### [Guarded Agent Runner](https://github.com/herefindalex/guarded-agent-runner)

A local-first control plane for letting an AI agent inspect infrastructure and propose narrowly scoped changes without giving the agent approval authority or unrestricted execution access.

The design separates proposal, evidence, approval, authority, and execution, with capability-scoped access and fail-closed behavior.

**Focus:** Go · MCP · Agent safety · Capability boundaries · Approval workflows · Auditability

---

## Open Source

I contribute fixes and investigations to infrastructure and distributed-systems projects, especially around lifecycle behavior, concurrency, failure handling, and correctness.

Selected work:

- [LiveKit psrpc — typed subscription shutdown safety](https://github.com/livekit/psrpc/pull/138)
- [LiveKit psrpc — pending RPC lifecycle during client shutdown](https://github.com/livekit/psrpc/pull/139)
- [LiveKit psrpc — avoid exposing panic details to RPC callers](https://github.com/livekit/psrpc/pull/142)

I am particularly interested in bugs where the difficult question is not simply *“does this code work?”*, but:

> What does this operation actually guarantee when shutdown, concurrency, retries, partial failure, or ambiguous outcomes are involved?

## Systems I Like Working On

- Distributed and event-driven systems
- High-throughput Go services
- Real-time data pipelines
- Backpressure, replay, and graceful degradation
- Idempotency and reconciliation
- Lifecycle and shutdown correctness
- Financial and transactional correctness
- Search, indexing, and deterministic retrieval
- Infrastructure and developer tooling
- AI systems with explicit authority and safety boundaries

One of my personal real-time systems processes roughly **10 million one-second market events per trading day**, with Go services, Redis Streams, Kafka, ClickHouse, MySQL, and WebSocket delivery.

## Engineering Principles

A few themes repeatedly show up in my work:

**Unknown is a state.**  
A timeout does not necessarily mean an operation failed.

**Processed is not a sufficient contract.**  
A system should define exactly which effects have completed and which guarantees now hold.

**An index is not the source of truth.**  
Fast candidate discovery and authoritative state often have different responsibilities.

**A balance is not enough.**  
For money and transactional systems, provenance, invariants, rounding, retries, and reconciliation matter as much as the final number.

**Shutdown is part of the API.**  
Lifecycle behavior deserves the same design attention as the happy path.

## Writing

I write about distributed systems, Go, correctness, real-time architectures, and engineering investigations.

Recent themes include:

- lifecycle contracts in Go
- shutdown behavior in unfamiliar codebases
- partial failure, backpressure, and replay
- ambiguous outcomes in distributed workflows
- completion semantics in event-driven systems
- money correctness and provenance
- trading-system abstractions
- search and indexing architecture

→ [Linkedin](https://www.linkedin.com/in/alexchang-tw/recent-activity/articles/)

## Technologies

**Primary:** Go

**Backend & Data:** Python · PHP · MySQL · SQLite · ClickHouse · Redis · Kafka

**Infrastructure:** AWS · Kubernetes · Docker · Linux

**Frontend:** React · Vue.js

**Systems:** REST · WebSocket · NATS · FIX · Event-driven architectures

I care more about understanding the guarantees and trade-offs of a technology than accumulating a long list of tools.

## Connect

- [LinkedIn](https://www.linkedin.com/in/alexchang-tw/)
- [GitHub](https://github.com/herefindalex)
- Email: herefindalex@gmail.com
