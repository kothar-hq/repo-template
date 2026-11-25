# 0001. Record architecture decisions

- Status: Accepted
- Date: 2026-11-25
- Deciders: kothar-hq
- Related: [docs/adr/README.md](README.md)

## Context

We need a way to record the decisions that shape this project over time.
Without a record, the reasons behind choices are lost and future contributors
either repeat the same analysis or unknowingly break an invariant.

## Decision

We will record every significant architecture decision as a Markdown file
under `docs/adr/` using the MADR (Markdown Architectural Decision Records)
style. Files are numbered sequentially (`0001`, `0002`, …) with no gaps. The
index at `docs/adr/README.md` is updated in the same commit as every new or
changed ADR.

The `adr` Claude Code agent in `.claude/agents/adr.md` is the standard way to
create and update records.

## Consequences

- Future decisions have a home and a discoverable index.
- Contributors must update the index whenever they add or change an ADR's
  status.
- Superseded ADRs are kept in full; only their status line changes.

## Alternatives considered

- **No formal record:** fast to start but loses institutional memory quickly.
- **Wiki pages:** harder to review in pull requests and drift from the code
  they describe.
