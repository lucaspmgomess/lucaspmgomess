<div align="center">

# Lucas Gomes

### Backend & Automation Engineer | Python, TypeScript, Browser Automation & AI Integrations

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)](https://www.djangoproject.com/)
[![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)
[![MCP](https://img.shields.io/badge/Model_Context_Protocol-111827?style=flat-square)](https://modelcontextprotocol.io/)

I build backend systems, browser automations, resilient integrations and AI-enabled tools for real operational workflows. Based in Porto Alegre, Brazil.

</div>

## Selected work

- **[Open Library](https://github.com/internetarchive/openlibrary/pulls?q=is%3Apr+author%3Alucaspmgomess+is%3Amerged)**: Four merged pull requests improving Python-side request preparation and removing unused template globals, with regression coverage and behavior preservation.
- **[Querido Diário](https://github.com/okfn-brasil/querido-diario/pull/1469)**: Rebuilt Porto Alegre's official-gazette collection across the historical PROCEMPA archive and the current DOPA API, validating more than 15,000 publications and files from 1995 onward.
- **[Querido Diário MCP Server](https://github.com/lucaspmgomess/querido-diario-mcp-server)**: Published MCP server with typed, read-only tools for Brazilian municipal gazette search.

## Systems I build

### Gesttor Contábil

Multi-tenant accounting ERP used for client, fiscal and document workflows.

**Stack:** Django, PostgreSQL, Celery, Redis, RabbitMQ, React and Docker.

My work includes tenant isolation, permission-aware modules, asynchronous processing, fiscal integrations, MCP interfaces, observability and regression coverage. The production repository is private, so the public profile describes the system without exposing business logic or customer data.

### PGMEI automation

A production browser-automation service for Brazil's PGMEI system. It separates API consumers from browser state and treats automation as a recoverable job workflow rather than a one-off script.

**Stack:** FastAPI, Chromium, Manifest V3 Chrome extension, SQLite, Prometheus, Grafana and Docker.

The browser side manages tab lifecycle, service-worker recovery and downloads, while the backend coordinates jobs through an HTTP bridge and a persistent queue. The production repository is private; I can discuss design decisions and demonstrate sanitized examples without exposing credentials, customer information or production configuration.

### ZapMEI

Customer-facing product built around MEI consultation and guide workflows.

**Stack:** Astro, TypeScript, Tailwind CSS, Playwright and API integrations.

Work includes deep-linked flows, asynchronous UI states, privacy-aware URLs, technical SEO and browser-based validation.

### Querido Diário MCP Server

A local-first MCP server for searching Brazilian municipal official gazettes using the public Querido Diário API.

**Status:** Beta. Published on [PyPI](https://pypi.org/project/querido-diario-mcp-server/) and the [MCP Registry](https://registry.modelcontextprotocol.io/?q=io.github.lucaspmgomess%2Fquerido-diario-mcp-server).

Install and launch with Python 3.12+ and uv:

```bash
uvx querido-diario-mcp-server
```

The server exposes three read-only tools: municipality lookup, municipality details and gazette search. It makes fixed HTTPS requests to the public API and does not accept arbitrary URLs.

The repository documents CI checks for Ruff, formatting, Pyright and pytest with coverage. Tests mock the HTTP boundary and cover successful responses, validation, malformed data, upstream errors, timeouts and MCP tool outputs. See the [README](https://github.com/lucaspmgomess/querido-diario-mcp-server#readme) for client configuration, development commands and current scope.

## Technical focus

**Backend:** Python, Django, FastAPI, REST APIs, PostgreSQL, SQLite  
**Web & browser:** TypeScript, JavaScript, Chrome Extensions (Manifest V3), Playwright, React, Next.js  
**Distributed workflows:** Celery, Redis, RabbitMQ, durable jobs and recovery  
**AI integrations:** MCP, tool-enabled agents and structured outputs  
**Production:** Docker, CI/CD, Prometheus, Grafana, Sentry and automated tests

## Contact

[GitHub](https://github.com/lucaspmgomess) · [Email](mailto:lucas.maurer@ufrgs.br) · Porto Alegre, Brazil
