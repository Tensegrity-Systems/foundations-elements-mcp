---
name: elements-lookup
description: Look up Foundations Elements by name or alias, then fetch specs in batch. Use when building or reviewing UI and you need component definitions, expected behaviors, or best practices from the Elements catalog.
---

# Elements lookup

Remote MCP server: `https://foundations.tensegrity.works/mcp` (OAuth / Foundations account).

## Workflow

1. Call `elements_kinds` first if you need the kind map (0 credits).
2. Call `elements_search` with a name, slug, or alias before guessing a slug. Search returns briefs, never full spec bodies.
3. Call `elements_get` once with `terms` (up to 12) when you need multiple specs. Do not call it once per slug.
4. Use `term` on `elements_get` only for a single spec.
5. `elements_history` is Max entitlement only.

## Do not

- Promise bulk export of the entire library.
- Treat paid HTTP x402 paths (`GET /mcp/elements/search`) as this MCP install — that channel is separate.
