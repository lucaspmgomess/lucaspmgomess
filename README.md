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

## Open-source contributions

### Open Library | Internet Archive

Contributed to the migration of blocking lending and availability logic from Templetor templates into Python request handlers, improving separation of concerns and supporting the project's FastAPI migration.

- [FastAPI: Move book lending preparation into Python | PR #13495](https://github.com/internetarchive/openlibrary/pull/13495)
- [Hoist list availability lookups into Python handler | PR #13465](https://github.com/internetarchive/openlibrary/pull/13465)

Both changes were validated by maintainers against the project's testing environment and incorporated into the upstream project.

### Langroid

Implemented a SerpApi Google Search integration for the Langroid agent framework, including mocked tests, environment-based configuration and integration coverage.

- [Add SerpApi Google search tool | PR #1130](https://github.com/langroid/langroid/pull/1130)

The implementation was carried forward by the maintainer and merged in [PR #1133](https://github.com/langroid/langroid/pull/1133), with the original commit authorship preserved.

### Querido Diário | Open Knowledge Brasil

Working on the Porto Alegre official gazette scraper, combining the historical PROCEMPA archive with the current DOPA API and expanding coverage back to 1995.

- [Fix Porto Alegre gazette spider | PR #1469](https://github.com/okfn-brasil/querido-diario/pull/1469)

The contribution includes defensive API parsing, historical data collection, automated regression tests and smoke testing against the live source.

## Featured project

### [Querido Diário MCP Server](https://github.com/lucaspmgomess/querido-diario-mcp-server)

An open-source, local-first MCP server that gives AI agents structured, read-only access to Brazilian official gazette data through the Querido Diário public API.

- Published on [PyPI](https://pypi.org/project/querido-diario-mcp-server/)
- Published on the [MCP Registry](https://registry.modelcontextprotocol.io/?q=io.github.lucaspmgomess%2Fquerido-diario-mcp-server)
- Async HTTP client with typed Pydantic models
- MCP tools with structured outputs
- Input validation and SSRF-conscious design
- Automated tests, type checking and CI
- No account, API key, telemetry or proprietary backend required

## Currently building

### Gesttor Contábil

A production-oriented, multi-tenant ERP and automation platform for accounting firms.

The platform brings together client management, workflows, financial operations, Brazilian electronic service invoices, document handling and AI-assisted operations.

Core technologies include Python, Django, PostgreSQL, Redis, Celery, Docker, React and the Model Context Protocol.

The main source repository is currently private because it contains proprietary business logic and active production integrations.

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
