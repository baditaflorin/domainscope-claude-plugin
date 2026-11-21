---
name: market-lookup
description: "Look up country and sector structure with DomainScope: how concentrated a market is, a country's market index and its governance, ICT and city context. Use for market sizing, country comparisons or questions like how concentrated are the industries in Poland."
---

# Market and country lookup with DomainScope

1. **List the dimensions first.** Call the dimensions tool before the concentration tool. The concentration tool refuses a
   dimension it does not know, and the list shows which dimensions exist and how well each is covered. The list can be cut short: if the
   dimension the user needs is missing, say so instead of guessing a name.
2. **Concentration.** Use the market concentration tool for a dimension, for example the industries of one country. To slice by country,
   pass the country's full English name (`Poland`), not a code: a code can come back as an empty, "competitive" answer with zero groups.
   If the answer has no groups or a total of zero, report "no data", not "competitive".
3. **Country market index.** Use the country market index tool with the country's full name or two-letter code. Do not narrow it by
   industry or business model unless the user asks: those narrower views are slow and often come back empty.
4. **Country context.** Use the country context tool for governance, ICT and city context, and pass the country's full English name,
   because a two-letter code can come back as "not available". Read its input schema for the aspects it accepts. City lists can show cities with
   zero domains: treat those counts with care.

## How to report it

- Explain the concentration index (HHI) in one line: higher means a few companies hold most of the market.
- State the dimension, the country and the coverage the tool reported. Coverage varies, so a thin result is a thin result.
- Two tools can report different totals for the same country because they count different sets. Say which tool gave which number.
- Do not extrapolate beyond what the tools returned.
