<div align="center">

# Lucas Gomes

### Backend & AI Integration Engineer

Building production systems at the intersection of backend engineering,  
AI integrations, accounting and public data.

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)](https://www.djangoproject.com/)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)
[![MCP](https://img.shields.io/badge/Model_Context_Protocol-111827?style=flat-square)](https://modelcontextprotocol.io/)

</div>

## Selected work

### [Gesttor Contábil](https://gesttorcontabil.com.br)

A multi-tenant ERP and automation platform for accounting firms, designed around real Brazilian accounting and tax workflows.

Gesttor centralizes client portfolios, fiscal operations, NFS-e issuance, digital certificates, documents, tasks, financial workflows and AI-assisted operations in a single system. The platform is developed from production use cases, with particular attention to data isolation, reliability and regulated workflows.

From an engineering perspective, Gesttor is structured as a monorepo with a Django API, a dedicated web backoffice and an independent client portal. PostgreSQL provides the transactional core, while Celery and Redis support asynchronous workloads, scheduled routines and operational automation.

Key engineering areas include:

- Multi-tenant data isolation and permission-aware modules
- Brazilian NFS-e workflows, including the national service invoice standard
- Background processing with explicit reliability and retry semantics
- Separate staff and client-facing applications sharing the same backend domain
- Digital certificates, document storage and external service integrations
- AI and Model Context Protocol integrations for assisted operations
- Cloud object storage for public and private media
- Sentry error monitoring and performance tracing with sensitive-data filtering
- CI checks for linting, architectural boundaries, migration safety and module contracts
- Expanded automated testing for higher-risk fiscal code paths

The product is currently in controlled rollout at [gesttorcontabil.com.br](https://gesttorcontabil.com.br). The main source repository remains private because it contains proprietary business logic and active production integrations.

### PGMEI Automation API

A production-oriented FastAPI service that turns Brazil's PGMEI web workflow into a structured job API for consulting MEI tax periods and generating DAS documents.

The technically unusual part is the browser architecture. Instead of controlling Chrome through Playwright or CDP, the system runs FastAPI and a real Chromium session in the same container and uses a Manifest V3 browser extension as the automation layer. The extension and API communicate through an authenticated HTTP bridge.

This separation gives each layer a clear responsibility: FastAPI owns jobs and queue state, the extension owns browser state and page interaction, and the container runtime owns the Chromium process.

Key engineering areas include:

- Chromium automation through a browser extension rather than an attached remote-debugging session
- Canonical-tab reconciliation and leader election resilient to Manifest V3 service-worker restarts
- Persistent FIFO job queue with restart-aware recovery semantics
- Explicit distinction between extension liveness and real job progress
- Recovery limits so an unresponsive browser job cannot block the entire queue indefinitely
- Reliable PDF reconciliation even when Chrome download events are missed during service-worker idle cycles
- Structured operational events, stable error codes and health endpoints
- Prometheus metrics for workers, queue depth, job duration, failures, CAPTCHA waits and browser health
- A separate Prometheus and Grafana observability stack with a provisioned PGMEI Operations dashboard
- Automated Python tests for the API, queue and bridge plus JavaScript tests for extension coordination

The service is also designed to be consumed by other applications and AI agents, exposing structured job state instead of requiring callers to understand the underlying browser workflow.

### [ZapMEI](https://zapmei.com.br)

A product layer built for Brazilian microentrepreneurs, using the PGMEI automation infrastructure to turn a complex government workflow into a simpler self-service experience.

ZapMEI combines a public acquisition site with a dedicated MEI consultation experience. Users can arrive through direct or campaign links, identify their CNPJ, consult available DAS periods and continue the delivery flow without interacting directly with the PGMEI portal.

The public application is built with Astro, TypeScript and Tailwind CSS and is deployed as a static frontend backed by the consultation API.

Key product and engineering areas include:

- Dedicated deep-linkable MEI consultation pages instead of a modal-only workflow
- Asynchronous API polling with explicit loading, ready, error and expiration states
- Privacy-aware URLs and analytics, avoiding CNPJ and document data in tracking events
- Responsive flows validated with Playwright across desktop and small mobile viewports
- Technical SEO, sitemap generation and dozens of intent-oriented acquisition pages
- First-touch attribution and UTM preservation across the consultation funnel
- Dockerized static delivery with build-time validation for public API configuration

The source repository is private while the public product evolves at [zapmei.com.br](https://zapmei.com.br).

### [Querido Diário MCP Server](https://github.com/lucaspmgomess/querido-diario-mcp-server)

An open-source, local-first MCP server that gives AI agents structured, read-only access to Brazilian official gazette data through the Querido Diário public API.

- Published on [PyPI](https://pypi.org/project/querido-diario-mcp-server/)
- Published on the [MCP Registry](https://registry.modelcontextprotocol.io/?q=io.github.lucaspmgomess%2Fquerido-diario-mcp-server)
- Async HTTP client with typed Pydantic models
- MCP tools with structured outputs
- Input validation and SSRF-conscious design
- Automated tests, type checking and CI
- No account, API key, telemetry or proprietary backend required

## Open-source contributions

### Open Library | Internet Archive

Contributed to the migration of blocking lending and availability logic from Templetor templates into Python request handlers, improving separation of concerns and supporting the project's FastAPI migration.

- [FastAPI: Move book lending preparation into Python | PR #13495](https://github.com/internetarchive/openlibrary/pull/13495)
- [Hoist list availability lookups into Python handler | PR #13465](https://github.com/internetarchive/openlibrary/pull/13465)

Both changes were reviewed, validated and merged into the upstream project.

Additional merged contributions include cleanup of unused template globals and i18n template globals.

### Langroid

Implemented the original SerpApi Google Search integration for the Langroid agent framework, including mocked tests, environment-based configuration, documentation and integration coverage.

The implementation was carried forward by the maintainer and merged in [PR #1133](https://github.com/langroid/langroid/pull/1133), with the original commit authorship preserved.

### Querido Diário | Open Knowledge Brasil

Reworked the Porto Alegre official gazette scraper after the municipality changed its publishing infrastructure, restoring current collection and extending historical coverage back to March 1995.

The implementation combines two independent data sources into a continuous collection pipeline: the historical PROCEMPA AtoM archive for editions from 1995 to 2011, and the current DOPA API for newer publications. It includes pagination and defensive parsing for historical records, date-range filtering, handling of extra editions, Executive and Legislative metadata mapping, download URL normalization and automated regression coverage for the transition between both sources.

A full validation run collected 15,215 publications and 15,215 files from March 1995 through August 2026 without exhausted retries or discarded items. Additional targeted collections were used to validate historical years, the 2011 source transition and recent publications, with automated tests and CI also passing.

- [Fix Porto Alegre gazette spider | PR #1469, currently in review](https://github.com/okfn-brasil/querido-diario/pull/1469)

## Focus

- Backend architecture and multi-tenant systems
- Browser automation and resilient job processing
- AI agents and MCP integrations
- Public APIs and civic technology
- Reliable automation for regulated workflows
- Testing, observability and data isolation

## Contact

- GitHub: [@lucaspmgomess](https://github.com/lucaspmgomess)
- Email: [lucas.maurer@ufrgs.br](mailto:lucas.maurer@ufrgs.br)
- Location: Porto Alegre, Brazil
