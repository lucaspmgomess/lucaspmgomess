<div align="center">

# Lucas Gomes

### Backend & AI Systems Engineer

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)](https://www.djangoproject.com/)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)
[![MCP](https://img.shields.io/badge/Model_Context_Protocol-111827?style=flat-square)](https://modelcontextprotocol.io/)

I design and operate backend platforms, automation infrastructure and AI-enabled systems for operationally complex environments.

`BACKEND SYSTEMS → INTEGRATIONS → AUTOMATION → AI → PRODUCTION`

</div>

## Engineering profile

My work sits at the intersection of backend architecture, workflow automation and AI systems.

I focus on software that has to interact with real operational constraints: multi-tenant data, asynchronous processing, government and third-party services, browser-dependent workflows, human operations and AI agents.

Rather than treating integrations as glue code, I design them as production systems with explicit boundaries, failure handling, observability and recovery paths.

## Current focus

**Backend architecture**  
Multi-tenant applications, API design, domain modeling and data-intensive systems with Python, Django, FastAPI and PostgreSQL.

**Distributed workflows**  
Asynchronous execution, queues, scheduling and resilient job orchestration with Celery, Redis and RabbitMQ.

**AI systems**  
Tool-enabled agents, Model Context Protocol, structured execution and AI integrations connected to real operational systems.

**Automation infrastructure**  
Turning browser-dependent and legacy workflows into API-driven services with explicit state, retries, timeouts and recovery.

**Production engineering**  
Containerized deployment, testing, metrics, health checks and operational visibility with Docker, Prometheus, Grafana and Sentry.

## Selected engineering work

### [Gesttor Contábil](https://gesttorcontabil.com.br)

Multi-tenant ERP and automation platform for accounting firms, designed around real accounting, tax and document workflows.

**Architecture:** Django · PostgreSQL · Celery · Redis · RabbitMQ · React · Docker

Engineering responsibilities include:

- tenant-aware backend architecture and data isolation;
- permission-aware modules and separate staff/client application surfaces;
- asynchronous fiscal, document and scheduled processing;
- NFS-e, digital certificate and external-service integrations;
- AI and MCP interfaces for assisted operational workflows;
- observability, CI gates and automated regression coverage.

The main repository is private because it contains proprietary business logic and active production integrations.

### PGMEI Automation API

Production-oriented automation service that exposes Brazil's PGMEI browser workflow through a structured FastAPI job interface.

**Architecture:** FastAPI · Chromium · Manifest V3 · PostgreSQL · Prometheus · Grafana · Docker

The system isolates browser state from API consumers and treats browser automation as a recoverable execution layer rather than an inline script.

Key engineering concerns include:

- persistent job state and restart-aware recovery;
- authenticated communication between browser automation and API orchestration;
- worker and browser health monitoring;
- stale-session detection and recovery;
- timeout and failure-state handling;
- reliable document download and reconciliation;
- Prometheus metrics and operational dashboards;
- automated Python and JavaScript test suites.

### [ZapMEI](https://zapmei.com.br)

Customer-facing product layer built over the PGMEI automation infrastructure.

**Architecture:** Astro · TypeScript · Tailwind CSS · Playwright · API integrations

The product connects acquisition, consultation flows and backend automation while preserving explicit application states and operational boundaries.

Engineering work includes deep-linkable workflows, asynchronous API states, privacy-aware URLs, technical SEO, attribution and automated browser validation.

### [Querido Diário MCP Server](https://github.com/lucaspmgomess/querido-diario-mcp-server)

Open-source MCP server that gives AI agents structured, read-only access to Brazilian municipal official-gazette data through the Querido Diário public API.

[PyPI](https://pypi.org/project/querido-diario-mcp-server/) · [MCP Registry](https://registry.modelcontextprotocol.io/?q=io.github.lucaspmgomess%2Fquerido-diario-mcp-server) · [Source](https://github.com/lucaspmgomess/querido-diario-mcp-server)

- async HTTP client with typed Pydantic models;
- structured MCP tool outputs and strict validation;
- read-only, SSRF-conscious execution model;
- automated tests and static type checking;
- no proprietary backend or account dependency.

## Open-source engineering

I contribute primarily to backend infrastructure, integrations and maintainability improvements in established open-source projects.

### Internet Archive / Open Library

Contributing to the migration of blocking application logic out of Templetor templates and into Python request handlers.

- **[PR #13495](https://github.com/internetarchive/openlibrary/pull/13495)** — moved lending and availability preparation for work, edition and search pages into Python with regression coverage and manual QA.
- **[PR #13465](https://github.com/internetarchive/openlibrary/pull/13465)** — removed blocking Solr and availability I/O from list templates while preserving routing, pagination and behavior.
- **[PR #13434](https://github.com/internetarchive/openlibrary/pull/13434)** — reduced legacy template-global exposure as part of rendering-layer cleanup.

All three were merged upstream.

### Langroid

Implemented the original SerpApi Google Search integration for the Langroid agent framework in **[PR #1130](https://github.com/langroid/langroid/pull/1130)** with mocked tests, environment-based configuration, documentation and integration coverage.

The implementation was carried forward and merged upstream in **[PR #1133](https://github.com/langroid/langroid/pull/1133)** with the original commit authorship preserved.

### Querido Diário / Open Knowledge Brasil

Reworked the Porto Alegre official-gazette ingestion pipeline after the municipality changed publishing infrastructure.

**[PR #1469](https://github.com/okfn-brasil/querido-diario/pull/1469)** joins the historical PROCEMPA AtoM archive with the current DOPA API into a continuous collection pipeline covering March 1995 onward.

The implementation includes:

- two independent upstream data sources;
- historical pagination and defensive parsing;
- date-range filtering and extra-edition handling;
- Executive and Legislative metadata mapping;
- regression coverage across the source transition;
- validation across 15,215 publications and files.

## Engineering principles

I care about systems that remain understandable under failure.

That usually means:

- explicit domain and tenancy boundaries;
- durable state for asynchronous work;
- idempotent and recoverable integrations;
- observable execution instead of opaque automation;
- controlled interfaces between AI agents and production systems;
- tests around behavior and failure modes, not only happy paths.

## Core technologies

**Backend:** Python · Django · FastAPI · REST APIs · PostgreSQL  
**Async & messaging:** Celery · Redis · RabbitMQ  
**AI systems:** MCP · LLM agents · structured tools  
**Automation:** Chromium · browser automation · Playwright  
**Operations:** Docker · Prometheus · Grafana · Sentry · CI/CD

## Contact

GitHub: [@lucaspmgomess](https://github.com/lucaspmgomess)  
Email: [lucas.maurer@ufrgs.br](mailto:lucas.maurer@ufrgs.br)  
Porto Alegre, Brazil
