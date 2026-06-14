# M42 Labs | Orion Platform

**M42 Labs** is an engineering lab focused on building **Orion Platform** — a staged backend reliability platform for service ownership, authentication, routing, observability, event-driven workflows, background automation, and infrastructure orchestration.

The goal is not to build a random set of microservices.

The goal is to build a clean, reusable, production-minded backend system that demonstrates how distributed services can be designed, connected, observed, and operated.

---

## Current Status

Orion Platform is currently in the **V1 skeleton stage**.

This means the repositories are being structured first:

* clear service ownership
* clean repository boundaries
* basic application skeletons
* local development foundation
* Docker and CI foundations
* initial API and domain models

Advanced production features such as full security hardening, service mesh, distributed tracing, transactional outbox, deployment automation, and scaling patterns will be added gradually.

---

## Platform Overview

Orion is organized as a multi-repository backend system.

Each repository has a specific responsibility.

| Repository | Role |
|---|---|
| [`orion-platform`](https://github.com/shaig-m42-labs/orion-platform) | Main architecture and documentation hub |
| [`m42-infra`](https://github.com/shaig-m42-labs/m42-infra) | Local infrastructure, Docker Compose, orchestration, and shared environment setup |
| [`rigel-gateway`](https://github.com/shaig-m42-labs/rigel-gateway) | API gateway and public entrypoint |
| [`bellatrix-auth`](https://github.com/shaig-m42-labs/bellatrix-auth) | Authentication and authorization service |
| [`betelgeuse-core`](https://github.com/shaig-m42-labs/betelgeuse-core) | Core reliability domain service |
| [`alnitak-events`](https://github.com/shaig-m42-labs/alnitak-events) | Event-driven messaging and async integration service |
| [`mintaka-observe`](https://github.com/shaig-m42-labs/mintaka-observe) | Observability service for metrics, logs, traces, and health monitoring |
| [`saiph-worker`](https://github.com/shaig-m42-labs/saiph-worker) | Background worker service for scheduled and async tasks |
| [`m42-spring-service-template`](https://github.com/shaig-m42-labs/m42-spring-service-template) | Spring Boot service starter template |
| [`m42-go-service-template`](https://github.com/shaig-m42-labs/m42-go-service-template) | Go service starter template |

---

## Core Idea

Orion Platform is designed around a simple operational question:

> What does a backend system need in order to be understandable, observable, recoverable, and maintainable?

The platform explores that question through practical backend components:

* service catalog
* user and identity management
* API gateway routing
* service-to-service communication
* health checks
* incident lifecycle
* metrics and logs
* async workers
* event-driven integrations
* local infrastructure setup
* reusable service templates

---

## Main Services

### Rigel Gateway

`rigel-gateway` acts as the public entrypoint of the platform.

Its responsibilities will include:

* request routing
* gateway-level validation
* authentication boundary
* forwarding trusted identity headers
* public API exposure
* future rate limiting and gateway observability

---

### Bellatrix Auth

`bellatrix-auth` owns identity and access control.

Its responsibilities will include:

* user registration
* login
* JWT-based authentication
* role and permission foundations
* token validation
* future service-to-service authorization support

---

### Betelgeuse Core

`betelgeuse-core` is the core reliability domain service.

Its responsibilities will include:

* organizations
* teams
* services
* environments
* health-check configurations
* incidents
* incident timeline
* operational workflows

This service acts as the main source of truth for platform reliability data.

---

### Alnitak Events

`alnitak-events` focuses on event-driven communication.

Its responsibilities will include:

* async event publishing
* event consumption
* integration workflows
* message processing patterns
* future dead-letter and retry handling

---

### Mintaka Observe

`mintaka-observe` focuses on observability.

Its responsibilities will include:

* metrics
* logs
* traces
* service health visibility
* Prometheus integration
* monitoring dashboards in later stages

---

### Saiph Worker

`saiph-worker` handles background processing.

Its responsibilities will include:

* scheduled jobs
* cleanup tasks
* async workflows
* health-check execution
* automation tasks
* future retry and backoff workflows

---

## Engineering Principles

Orion Platform follows these principles:

* build small, clear services
* avoid overengineering in early stages
* prefer explicit service boundaries
* document responsibilities before adding complexity
* keep local development reproducible
* use simple, practical infrastructure first
* add reliability patterns gradually
* make every repository understandable on its own
* treat observability as a core feature, not an afterthought

---

## Tech Stack

The platform mainly uses:

* Java 21
* Spring Boot
* Go
* PostgreSQL
* Redis
* Docker
* Docker Compose
* GitHub Actions
* OpenAPI / Swagger
* Prometheus
* NATS or event-driven messaging foundations

The stack may evolve as the platform matures.

---

## V1 Goals

The first version focuses on building a clean foundation.

### V1 should include:

* basic service skeletons
* local infrastructure setup
* core API endpoints
* authentication foundation
* gateway foundation
* service catalog foundation
* incident lifecycle foundation
* health-check configuration foundation
* event messaging foundation
* basic observability setup
* CI build and test workflows

### V1 does not aim to include yet:

* full production deployment
* Kubernetes
* service mesh
* advanced distributed tracing
* full RBAC policy engine
* complex event sourcing
* high-availability infrastructure
* enterprise-grade security hardening

Those may come in later stages.

---

## Repository Maturity

Most repositories are currently in early development.

| Stage | Meaning |
|---|---|
| Skeleton | Initial structure, README, basic app setup |
| Foundation | Basic working endpoints and local development support |
| Integration | Connected to other Orion services |
| Hardening | Tests, validation, security, observability, reliability improvements |
| Production-minded | Ready for serious demo or controlled deployment |

Current focus: **Skeleton → Foundation**.

---

## Why This Exists

Orion Platform is built as a portfolio-grade backend system to practice and demonstrate:

* backend architecture
* distributed system boundaries
* Spring Boot service design
* Go service design
* Docker-based local environments
* API gateway patterns
* authentication flows
* async communication
* observability
* incident management
* reliability engineering fundamentals

The project is intentionally built in stages so every part can be understood, improved, and reused.

---

## Start Here

Recommended reading order:

1. [`orion-platform`](https://github.com/shaig-m42-labs/orion-platform)
2. [`m42-infra`](https://github.com/shaig-m42-labs/m42-infra)
3. [`betelgeuse-core`](https://github.com/shaig-m42-labs/betelgeuse-core)
4. [`bellatrix-auth`](https://github.com/shaig-m42-labs/bellatrix-auth)
5. [`rigel-gateway`](https://github.com/shaig-m42-labs/rigel-gateway)

---

## Project Philosophy

Orion is not trying to be perfect from day one.

It is built like a real backend platform should be built:

1. define boundaries
2. create skeletons
3. build the core flows
4. connect services
5. add tests
6. improve reliability
7. add observability
8. harden security
9. document decisions
10. iterate

Small, clear, reliable steps.
