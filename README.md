# Foundations Elements MCP

Public install package for the **Foundations Elements** remote MCP server.

- **MCP URL:** https://foundations.tensegrity.works/mcp  
- **Product / waitlist:** https://tensegrity.company/elements  
- **Docs:** https://foundations.tensegrity.works/docs  
- **Privacy:** https://tensegrity.company/privacy  
- **Terms:** https://tensegrity.company/terms  
- **Support:** support@tensegrity.company  

This repository is the free plugin / registry metadata. The Worker implementation stays private. Access to catalog tools requires a Foundations account (OAuth via https://auth.tensegrity.works).

**Publisher (marketplaces):** GitHub org [`Tensegrity-Systems`](https://github.com/Tensegrity-Systems). Canonical repo: https://github.com/Tensegrity-Systems/foundations-elements-mcp (GitLab remains a staging mirror).

## What you get

Cursor / Agent plugin that points at the remote MCP endpoint, plus `server.json` for the official MCP Registry.

Tools include search, kind lists, and spec fetch (`elements_search`, `elements_list`, `elements_get`, and related). See server instructions after connect.

## Install

### Cursor

1. Install this plugin from the Marketplace when published, or load the repo as a local plugin.
2. Complete OAuth when Cursor prompts for Foundations sign-in.
3. Request access at https://tensegrity.company/elements if you do not have an account.

`mcp.json` already points at:

```text
https://foundations.tensegrity.works/mcp
```

### Claude

Add a custom connector with the same HTTPS URL, then sign in with OAuth. Directory listing will use this package’s branding and docs links.

### VS Code / Copilot

Configure an HTTP MCP server with the URL above (after Official / GitHub MCP Registry publication).

## Official MCP Registry

`server.json` declares a remote Streamable HTTP server. Preferred registry name (after domain ownership proof on `tensegrity.works`):

```text
works.tensegrity/foundations-elements
```

## Privacy

Foundations account sign-in and MCP usage are covered by the company privacy policy:

https://tensegrity.company/privacy

This install package does not collect data on its own; it only points clients at the remote MCP URL. Support: support@tensegrity.company.

## License

MIT for this install package. Foundations Elements content and API remain proprietary; see https://tensegrity.company/terms and https://foundations.tensegrity.works/terms.

## Channel note

Paid HTTP (x402) lookups use `GET /mcp/elements/search`. That is a separate agent-catalog path, not this IDE MCP plugin.
