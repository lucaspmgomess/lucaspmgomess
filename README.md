<div align="center">

# Lucas Gomes

### Backend & AI Integration Engineer

Python · Django · FastAPI · PostgreSQL · Distributed Systems · AI Agents

Building backend systems, automation infrastructure and AI integrations for complex, integration-heavy workflows.

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)](https://www.djangoproject.com/)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)
[![MCP](https://img.shields.io/badge/Model_Context_Protocol-111827?style=flat-square)](https://modelcontextprotocol.io/)

</div>

## Open-source engineering

### Open Library | Internet Archive

Contributing to Open Library's ongoing migration of blocking application logic out of Templetor templates and into Python request handlers.

- **[PR #13495 — FastAPI: Move book lending preparation into Python](https://github.com/internetarchive/openlibrary/pull/13495)** — merged. Moved lending and availability preparation for work, edition and search pages into Python, with regression coverage and side-by-side manual QA.
- **[PR #13465 — Hoist list availability lookups into Python handler](https://github.com/internetarchive/openlibrary/pull/13465)** — merged. Removed blocking Solr and availability I/O from list templates while preserving routing, pagination and existing behavior.
- **[PR #13434 — Remove unused i18n template globals](https://github.com/internetarchive/openlibrary/pull/13434)** — merged. Reduced legacy template-global exposure as part of the broader rendering-layer cleanup.

The maintainer review for #13495 reproduced the tests, approved the change and highlighted it as the most difficult part of that migration work.

### Langroid

Implemented the original SerpApi Google Search integration for the Langroid agent framework in **[PR #1130](https://github.com/langroid/langroid/pull/1130)**, including mocked tests, environment-based configuration, documentation and integration coverage.

The implementation was carried forward by the maintainer and merged upstream in **[PR #1133](https://github.com/langroid/langroid/pull/1133)** with the original commit authorship preserved.

### Querido Diário | Open Knowledge Brasil

Reworked the Porto Alegre official-gazette scraper after the municipality changed its publishing infrastructure.

**[PR #1469](https://github.com/okfn-brasil/querido-diario/pull/1469)** combines the historical PROCEMPA AtoM archive with the current DOPA API into a continuous collection pipeline covering March 1995 onward.

- Two independent upstream data sources
- Historical pagination and defensive parsing
- Date-range filtering and extra-edition handling
- Executive and Legislative metadata mapping
- Regression coverage across the 2011 source transition
- Full validation run: **15,215 publications and 15,215 files**
- Automated tests and CI passing

The PR is currently under upstream review.

## Public project

### [Querido Diário MCP Server](https://github.com/lucaspmgomess/querido-diario-mcp-server)

Open-source, local-first MCP server that gives AI agents structured, read-only access to Brazilian municipal official-gazette data through the Querido Diário public API.

- Published on [PyPI](https://pypi.org/project/querido-diario-mcp-server/)
- Published on the [MCP Registry](https://registry.modelcontextprotocol.io/?q=io.github.lucaspmgomess%2Fquerido-diario-mcp-server)
- Async HTTP client with typed Pydantic models
- Structured MCP tool outputs and input validation
- SSRF-conscious, read-only design
- Automated tests, static type checking and CI
- No account, API key, telemetry or proprietary backend required

## Production systems

### [Gesttor Contábil](https://gesttorcontabil.com.br)

Multi-tenant ERP and automation platform for accounting firms, built from production accounting and tax workflows.

`Django` · `PostgreSQL` · `Celery` · `Redis` · `React` · `Docker` · `Sentry`

- Multi-tenant data isolation and permission-aware modules
- NFS-e, digital-certificate and external-service integrations
- Async fiscal, document and scheduled processing
- Separate staff and client-facing applications on a shared backend domain
- Sentry monitoring, CI gates and automated testing
- AI and Model Context Protocol integrations for assisted operations

The product is in controlled production rollout. Its main source repository is private because it contains proprietary business logic and active production integrations.

### PGMEI Automation API

Production-oriented FastAPI service that exposes Brazil's PGMEI browser workflow as a structured job API.

`FastAPI` · `Chromium` · `Manifest V3` · `Prometheus` · `Grafana` · `Docker`

- Persistent job queue with restart-aware recovery
- Authenticated bridge between browser automation and API orchestration
- Browser lifecycle and session coordination
- Reliable document download and reconciliation
- Stable job states, health checks and operational events
- Prometheus metrics and provisioned Grafana dashboards
- Python and JavaScript automated tests

### [ZapMEI](https://zapmei.com.br)

Product layer for Brazilian microentrepreneurs built on top of the PGMEI automation infrastructure.

`Astro` · `TypeScript` · `Tailwind CSS` · `Playwright` · `Docker`

- Deep-linkable consultation flows backed by an asynchronous API
- Explicit loading, ready, error and expiration states
- Privacy-aware URLs and analytics
- Responsive flows validated with Playwright
- Technical SEO, sitemap generation and intent-oriented acquisition pages
- First-touch attribution and UTM preservation

## Engineering focus

- Backend architecture and multi-tenant systems
- Integration-heavy and regulated workflows
- Resilient job processing and browser automation
- AI agents, MCP integrations and developer tooling
- Testing, observability and data isolation
- Public APIs and civic technology

## Contact

- GitHub: [@lucaspmgomess](https://github.com/lucaspmgomess)
- Email: [lucas.maurer@ufrgs.br](mailto:lucas.maurer@ufrgs.br)
- Porto Alegre, Brazil
