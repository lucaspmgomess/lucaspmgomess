<div align="center">

# Lucas Gomes

### Backend & AI Integration Engineer

Building production systems at the intersection of backend engineering,  
AI integrations, accounting and public data.

[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Django](https://img.shields.io/badge/Django-092E20?style=flat-square&logo=django&logoColor=white)](https://www.djangoproject.com/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)
[![MCP](https://img.shields.io/badge/Model_Context_Protocol-111827?style=flat-square)](https://modelcontextprotocol.io/)

</div>

## Selected work

### [Gesttor Contábil](https://gesttorcontabil.com.br)

A multi-tenant software platform for accounting firms, companies, MEIs and service providers, built around real accounting and tax operations in Brazil.

The public product currently focuses on removing repetitive work from NFS-e workflows. Accounting firms can manage a portfolio of CNPJs, issue service invoices individually or in batches, capture and organize XML files, manage digital certificates and deliver documents to clients by email or WhatsApp from a centralized workflow.

For companies and service providers, Gesttor provides a simpler path to issue NFS-e through the national standard, organize PDF and XML documents and automate delivery to customers without relying on municipal portals for each operation.

The broader platform is designed as an operational system for accounting firms, bringing together client data, fiscal workflows, documents, tasks, financial operations, integrations and AI-assisted processes in a shared multi-tenant architecture.

Core technologies include Python, Django, PostgreSQL, Redis, Celery, Docker, React and the Model Context Protocol.

The product is currently in controlled rollout. The main source repository remains private because it contains proprietary business logic and active production integrations.

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

## Focus

- Backend architecture and multi-tenant systems
- AI agents and MCP integrations
- Public APIs and civic technology
- Reliable automation for regulated workflows
- Testing, observability and data isolation

## Contact

- GitHub: [@lucaspmgomess](https://github.com/lucaspmgomess)
- Email: [lucas.maurer@ufrgs.br](mailto:lucas.maurer@ufrgs.br)
- Location: Porto Alegre, Brazil
