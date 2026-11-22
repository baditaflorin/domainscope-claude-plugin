---
name: market-lookup
description: "Look up country and sector structure with DomainScope: how concentrated a market is, a country's market index and its governance, ICT, city, airport and business-registry context. Use for market sizing, country comparisons or questions like how concentrated are the industries in Poland."
---

# Market and country lookup with DomainScope

1. **List the dimensions first.** Call the dimensions tool (`domainscope_list_market_dimensions`) before the concentration tool. The
   concentration tool refuses a dimension it does not know, and the list shows which dimensions exist, how well each is covered and
   whether it can be measured inside a slice. If the dimension the user needs is missing, say so instead of guessing a name.
2. **Concentration.** Use the market concentration tool (`domainscope_get_market_concentration`) with `dimension`, and optionally
   `within` and `value` together to slice, for example `dimension=industry`, `within=country`, `value=Poland`. Pass a country's full
   English name (`Poland`): it is the safest form. Only dimensions marked sliceable can be sliced. If the answer has no groups or a total
   of zero, report "no data", not "competitive".
3. **Country market index.** Use the market index tool (`domainscope_get_market_index`) with `country` (required). Do not narrow it by
   `industry` or `business_model` unless the user asks: narrower views can be slow and can come back empty, in which case the answer
   explains the empty slice and suggests values to try.
4. **Country context.** Use the country context tool (`domainscope_get_country_context`) with `country` and `aspect`, both required. The
   aspects are `governance`, `corruption`, `ict`, `wikidata`, `cities`, `airports` and `business-registry`. Call it once per aspect the
   user needs. City lists show domain counts per city: if a count looks like zero for a large city, say the count may be incomplete.

## How to report it

- Explain the concentration index (HHI) in one line: higher means a few companies hold most of the market.
- State the dimension, the country and the coverage the tool reported. Coverage varies, so a thin result is a thin result.
- Two tools can report different totals for the same country because they count different sets. Say which tool gave which number.
- Say the figures describe the websites in DomainScope's catalog, not the whole economy of the country.
- Do not extrapolate beyond what the tools returned.
