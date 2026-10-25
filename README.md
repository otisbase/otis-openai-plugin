# Otis for ChatGPT and Codex

Free business records through your AI: clients, work, expenses, invoices, payments, timers, business settings, tax settings and export.

[Otisbase](https://otisbase.com) is a free MCP server for client billing, built for consultants and small agencies. There is no app or dashboard: your AI assistant is the interface. You tell it what happened, it records the work, expenses and payments in Otis, and Otis issues the invoices you approve. Otis stores the records and enforces the rules, such as invoice numbering, totals and exact-total approval. Issued invoices cannot be rewritten.

This is the Otis plugin for ChatGPT and Codex. It bundles the remote Otis MCP connection with a menu skill and nine workflow skills, so the assistant knows how to run each job step by step. It runs no local backend, model inference, hooks or shell scripts; records stay in the Otis service, stored in the EU on Cloudflare.

## Install

### Codex

```bash
codex plugin marketplace add otisbase/otis-openai-plugin
codex plugin add otis@otis
```

Or run `codex /plugins`, or use the Plugins tab in the ChatGPT desktop app. Start a new session, then type `$otis:` to pick a skill.

### ChatGPT

Otis is submitted to OpenAI's plugin directory and is not listed yet. Until it is, connect the MCP URL below as a custom connector.

Full steps for every assistant are on [How to install](https://otisbase.com/connect). Sign-in uses an email code in your browser.

## Connect without a plugin

The plugin is optional. Any assistant that supports remote MCP servers can add Otis directly with this URL:

```
https://mcp.otisbase.com/mcp
```

Sign-in uses OAuth with an email code, so there is no API key to copy. Use a single Otis connection in each client: if you already connected Otis directly, check that connection before enabling the plugin's copy.

## Skills

| Skill | Purpose |
| --- | --- |
| menu | Open the menu |
| create-invoice | Create invoice |
| record-work | Record work |
| add-expense | Add expense |
| clients | Clients |
| invoices | Invoices |
| payments | Payments |
| business-settings | Business settings |
| tax-settings | Tax settings |
| export | Export |

Choosing a skill never approves an action: issuing an invoice still needs your exact total. Payments are reported facts. Tax guidance is not automatic tax determination. Details are on [otisbase.com/skills](https://otisbase.com/skills).

## Other agents

| Agent | Repository |
| --- | --- |
| Claude, Cowork and Claude Code | [otisbase/otis-claude-plugin](https://github.com/otisbase/otis-claude-plugin) |
| ChatGPT and Codex | [otisbase/otis-openai-plugin](https://github.com/otisbase/otis-openai-plugin) |
| Grok Bot, Grok Build and Cursor | [otisbase/otis-grok-plugin](https://github.com/otisbase/otis-grok-plugin) |
| GitHub Copilot, VS Code, Kiro, Perplexity and other agents that read Agent Plugins 1.0 or Agent Skills | [otisbase/otis-agent-plugin](https://github.com/otisbase/otis-agent-plugin) |

## Links

- [Otisbase](https://otisbase.com)
- [How to install](https://otisbase.com/connect)
- [MCP docs](https://otisbase.com/docs): the endpoint, the rules and every tool
- [Privacy Policy](https://otisbase.com/privacy) and [Terms of Service](https://otisbase.com/terms)
- Support: [support@otisbase.com](mailto:support@otisbase.com)

## License

Released under the [MIT License](LICENSE). Otisbase is operated by Boon IT SRL.

This repository is generated from the Otis workflow catalog by `npm run plugins:build` in the Otis source project. Do not edit it by hand.
