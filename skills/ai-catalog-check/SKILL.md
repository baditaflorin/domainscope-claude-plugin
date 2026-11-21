---
name: ai-catalog-check
description: "Check whether a website publishes an AI catalog or MCP servers and find companies that host MCP servers, using DomainScope. Use when the user asks whether a company has an AI catalog or an MCP endpoint, or which companies expose MCP servers."
---

# AI catalog and MCP servers with DomainScope

1. Use the **AI catalog** tool for a domain to see what DomainScope has stored about its AI catalog and MCP servers.
2. To find companies that host MCP servers, use the **MCP server search** tool, with a keyword if the user gave one.

## How to report it

- Say what the record shows and when it was last updated if the answer gives a date. The records are stored, not live.
- An empty or all-zero record means "DomainScope has no record of an AI catalog or MCP server for this domain". It does not prove the
  company has none. Say it that way, and never state "this company has no MCP server".
- This skill does not give a readiness score or check `llms.txt` or bot policy: DomainScope does not offer that here. If the user asks
  for a score, say so and suggest they check the site's own `/llms.txt` and `robots.txt`.
- The MCP server search is not ranked and may list template or placeholder entries and unrelated sites. Present results as "domains
  DomainScope has recorded with an MCP server", not as recommendations, and say which entries look like placeholders.
- Name endpoints exactly as returned. Do not invent endpoints and do not connect to one unless the user asks.
- The domain profile also carries an AI posture line. If it disagrees with the AI catalog tool, report both and say they disagree.
