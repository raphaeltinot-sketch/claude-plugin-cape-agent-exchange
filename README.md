# Cape Partners Plugin

Technology M&A discovery with [Cape Partners](https://www.capepartners.fr), an independent M&A advisory firm focused on technology. The plugin connects Claude to the Cape MCP server and adds four guided skills.

## Components

| Component | Name | Purpose |
|-----------|------|---------|
| MCP server | `Cape` | Remote HTTP server at https://www.capepartners.fr/mcp (open, no authentication) |
| Skill | `valuation-guide` | Collect financials, call `get_valuation`, explain the indicative range and assumptions |
| Skill | `counterparty-matching` | Turn a buy-side or sell-side mandate into ranked counterparties with `find_matches` |
| Skill | `deal-flow-overview` | Aggregate view of the scored deal universe with `get_deal_flow` |
| Skill | `partner-services-lookup` | Search the Cape Agent Exchange with `find_partner_services` |

## Setup

No environment variables or credentials are required. Installing the plugin registers the Cape MCP server.

## Usage

- "What is my software company worth? Revenue is 8M EUR, growing 30%."
- "Find buyers for a French B2B SaaS company in compliance software."
- "Show me deal flow in European cybersecurity."
- "Who on the exchange can provide a data-room preparation service?"

## Good to know

- Results are read-only and redacted by design. Counterparties appear as position references, not names.
- Identity and granular financials are released only through Cape's controlled disclosure and NDA process, which requires a human supervisor. Start it at https://www.capepartners.fr.
- Valuations are indicative and non-binding, not an offer, appraisal or investment advice.
- No tool contacts anyone, signs anything or commits funds on the user's behalf.

## Links

- Website: https://www.capepartners.fr
- Terms of Service: https://www.capepartners.fr/tos
- Privacy Notice: https://www.capepartners.fr/privacy.html

## Privacy Policy

Cape Partners is the operator of the MCP server this plugin connects to.

- **Data collection**: the plugin stores nothing on your machine and has no telemetry. Prompts and tool arguments are sent only to https://www.capepartners.fr/mcp, Cape's own first-party API, to produce the answer.
- **Use and storage**: query parameters are used to compute the response. Cape does not store conversation content, and does not read Claude's memory, chat history or your files.
- **Third-party sharing**: nothing is shared with third parties. Data is not sent to any destination other than the declared connector.
- **Retention**: no conversation data is retained. Aggregate usage counts may be kept for operational metrics.
- **Contact**: contact@capepartners.fr — full notice at https://www.capepartners.fr/privacy.html

## Licence

MIT — see LICENSE.
