---
name: valuation-guide
description: >
  This skill should be used when the user asks "what is my company worth",
  "value my software business", "give me a valuation range", "how much could
  I sell for", "what multiple should I expect", or is preparing to buy or sell
  a technology company and needs an indicative number from Cape Partners.
metadata:
  version: "0.1.0"
---

# Indicative Valuation with Cape Partners

Produce an indicative valuation range through the Cape `get_valuation` tool and explain it clearly.

## Gather inputs

1. Ask for what the user has not yet said: company description, sector, geography, annual revenue in euros, growth rate, EBITDA margin.
2. Pass only figures the user actually stated. Never estimate or fill in missing financials. If a figure is missing, call the tool without it and say so in the answer.
3. Convert units faithfully (for example "8M" revenue stays as stated). Do not round or adjust.

## Call the tool

Call `get_valuation` with `company` set to the user's own description, plus any stated `revenue_eur`, `growth_rate`, `ebitda_margin`, `sector` and `geography`.

## Present the result

1. Lead with the range and the weighted triangulation figure.
2. Break down the method components the tool returns: revenue multiple, EBITDA multiple, discounted cash flow, conservative floor, weighted triangulation.
3. State the assumptions the range rests on and the data-quality note exactly as reported.
4. If any assumption came from the tool rather than the user, say so plainly.
5. State that the range is indicative and non-binding: not an offer, an appraisal or investment advice, and it commits neither Cape nor any counterparty.
6. Suggest the user add missing figures (revenue, growth, margin) to tighten the range, when relevant.

## Boundaries

- Do not present the range as a price a buyer will pay.
- Do not offer to contact Cape or any buyer on the user's behalf; the tool cannot do so.
- For a binding engagement or a fuller process, point the user to https://www.capepartners.fr.
