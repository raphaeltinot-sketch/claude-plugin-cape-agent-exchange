---
name: deal-flow-overview
description: >
  This skill should be used when the user asks "what does the market look like",
  "show me deal flow", "which sectors are active", "how many qualified software
  companies are there", "what is available in Europe", or wants an aggregate
  view of Cape Partners' technology M&A universe rather than a specific mandate.
metadata:
  version: "0.1.0"
---

# Deal-Flow Overview with Cape Partners

Summarize the shape of the market through the Cape `get_deal_flow` tool.

## Call the tool

1. Pass `focus` in the user's own words, and `sector` or `geography` only if the user named them.
2. Set `limit` only if the user asks for more or fewer sector rows (default 20, maximum 50).
3. If the user has a specific mandate in mind, switch to the counterparty-matching skill instead.

## Present results

1. Summarize counts by sector, size bands and the best fit achieved in each sector.
2. Highlight where depth is strongest and where it is thin, using only the returned numbers.
3. A compact table works well for sector, count, size bands and best fit.
4. Mention what the view is: the scored deal universe in aggregate, not a list of companies.

## Hard rules

- The data contains no company names and no individual records. Never speculate about who the companies are.
- Do not extrapolate to the whole market. Describe only Cape's universe.
- If the result is empty, say so plainly.
- Offer a mandate-specific search as a natural next step when the user wants to go deeper.
