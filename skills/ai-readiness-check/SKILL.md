---
name: ai-readiness-check
description: "Check whether a website publishes an AI catalog or MCP servers, get an AI readiness summary for a domain and find companies that host MCP servers, using DomainScope. Use when the user asks whether a company has an AI catalog or an MCP endpoint, how AI-ready a site is, or which companies expose MCP servers."
---

# AI catalog, AI readiness and MCP servers with DomainScope

1. Use the **AI catalog** tool (`domainscope_get_ai_catalog`) for a domain to see what DomainScope has stored about its AI catalog,
   MCP servers, AI artifacts and where they were discovered.
2. Use the **AI readiness** tool (`domainscope_check_ai_readiness`) for a domain when the user asks how AI-ready a site is. It gives a
   summary (AI catalog, MCP servers, AI artifacts) and a readiness score, with what was and was not checked and the date.
3. To find companies that host MCP servers, use the **MCP server search** tool (`domainscope_search_mcp_servers`), with a keyword or brand
   name if the user gave one (up to 50 results, default 20).

The tools accept a domain such as `stripe.com`. If the user gave only a company name, find the domain first with the identify tool
(`domainscope_identify_domain`, parameter `query`) and check the candidate before using it.

## How to report it

- Say what the record shows and, if the answer gives a date, when it was checked. The records are stored, not live.
- Give the readiness score together with what it covers and what it did not check, exactly as the answer states them. A score is a
  summary of stored records, not a guarantee of how the site behaves.
- An empty or all-zero record means "DomainScope has no record of an AI catalog or MCP server for this domain". It does not prove the
  company has none. Say it that way, and never state "this company has no MCP server".
- If the answer says something was not checked, say that plainly instead of reading it as "no". For anything the tools do not
  cover, suggest the user check the site's own `/llms.txt` and `robots.txt`.
- The MCP server search is not ranked and may list template or placeholder entries and unrelated sites. Present results as "domains
  DomainScope has recorded with an MCP server", not as recommendations, and say which entries look like placeholders.
- Name endpoints exactly as returned. Do not invent endpoints and do not connect to one unless the user asks.
- The domain profile also carries an AI posture line. If it disagrees with the AI catalog or readiness answer, report both and say they
  disagree.
