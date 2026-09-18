# Internship Viva — Company Brain & UNBIFY Discover

A self-contained web presentation on two systems built during the internship.

**View it:** open `index.html` in any browser, or visit the GitHub Pages URL once Pages is enabled.

## The two systems

**Company Brain** — an organizational memory. Connects to the tools a company already
uses, extracts what is inside them, and answers questions with the source attached.
TypeScript monorepo: Fastify API, Next.js app, Temporal workflows, PostgreSQL + Prisma,
Qdrant, Redis, MinIO.

**UNBIFY Discover** — an evidence-gated opportunity engine. A four-chapter journey builds
an evidence ledger about a person, then routes that evidence to real opportunities, or
abstains and says why. Python: FastAPI modular monolith on PostgreSQL + pgvector, with no
broker of any kind.

## Contents

Ten sections: the two systems, the knowledge-extraction workflow, retrieval ranking, the
action lifecycle, what shipped, the Discover journey, the intelligence core, latency
budgets, and the world-intelligence layer.

Two parts are interactive and meant to be operated while presenting:

- **Section 05 — the executor swap.** Toggle between `openclaw:cli` and `hermes` behind
  the `ExecutionEngine` interface. Only the region below the boundary changes; the
  planner, approval gate, Execution Service and UI are stamped unchanged.
- **Section 08 — the L4 gate.** Two steppers mirroring `role_analysis_allowed()`:
  professional facts (needs 4) and supported features (needs 2). The verdict prints the
  same reason string the function returns.

## Presenting

- `←` `→` or `space` to move between sections; `Home` / `End` to jump.
- The rail on the left jumps to any section.
- The **Theme** button, bottom-left, cycles Auto → Light → Dark. Set it to suit the room
  before you start.
- `F11` for full screen.

## A note on the figures

Every number in the presentation comes from the two codebases rather than from memory:
the retrieval weights from `packages/retrieval/src/rank.ts`, the per-phase latency budgets
from `app/latency.py`, the gate thresholds from `app/thresholds.py`, the action states
from `schema.prisma`, and the measured round-trip figures from the Discover README.

The Cerebras figure in section 02 is an external reference only — an engineering write-up
read while building, with no affiliation.
