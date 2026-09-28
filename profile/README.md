# Chorust

**Building composable primitives for data, agents, and intelligent systems.**

Chorust is an open-source organization building focused systems, data, and AI infrastructure tools — with Rust at the core.

Each project is designed to stand on its own: small enough to understand, explicit about its boundaries, and composable with the rest of the ecosystem.

**Each a voice, together a chorus.**

[Chinese](README.zh-CN.md)

## Projects

### [Chorust](https://github.com/chorust/chorust)
**Local-first observability and control for coding-agent sessions.**

Chorust observes coding agents through their native, documented interfaces while keeping their logs, prompts, stores, and execution paths read-only. It turns agent activity into observable state and controlled actions with explicit evidence, capability boundaries, and conservative safety defaults.

### [Radiust](https://github.com/chorust/radiust)
**Radar data acquisition and processing infrastructure.**

Radiust provides a unified toolkit for discovering, fetching, decoding, validating, caching, and exporting weather-radar data across multiple providers. Python provides the user-facing data and CLI layer, while Rust powers constrained I/O, caching, temporary storage, and infrastructure components.

### [DuckJeu](https://github.com/chorust/duckjeu)
**Judgment as a SQL primitive.**

DuckJeu is a DuckDB extension that brings JEV-style probabilistic and categorical judgments directly into SQL.

```sql
SELECT jev_bool(message, 'the customer requests a refund')
FROM tickets;
```

Judgments become typed values that can participate in ordinary relational operations — filtering, aggregation, joins, caching, and composition.

### [DuckOMo](https://github.com/chorust/duckomo)
**Query Open-Meteo OM data directly from DuckDB.**

DuckOMo is a planned DuckDB extension that maps SQL projection and spatiotemporal predicates into logical OM array slices. The goal is simple: read only the data a query actually needs, without materializing entire OM files first.

### [Conductorust](https://github.com/chorust/conductorust)
**A spec compiler.**

Early-stage work exploring how structured specifications can become executable or machine-consumable representations.

## Principles

We prefer software that is:

- **Focused** — one clear responsibility before a broad platform
- **Composable** — useful independently, stronger together
- **Explicit** — clear contracts, boundaries, and failure modes
- **Local-first where possible** — keep control and data close to the user
- **Evidence-driven** — distinguish implemented, tested, inferred, and planned behavior
- **Rust at the core** — especially where correctness, performance, and systems integration matter

## Why Chorust?

A chorus is made of independent voices. Each voice has its own role, range, and identity. The result comes from coordination rather than uniformity.

That's how we think software should work too.

**They do not need to become one platform. They just need to work well in concert.**
