# InfraJump for Claude

The public, pre-release plugin repository for connecting Claude to **InfraJump**, a cloud infrastructure investigation and cost-analysis platform.

**Status: under development, not released or approved for the Claude directory.** The private MCP server is not yet publicly available; installing a remote connector will require a future, tested OAuth login flow. No user API keys or cloud provider credentials should be placed in this repository.

## Intended capabilities

The first release will let a signed-in InfraJump user investigate the resources and costs in projects they are already authorized to access. Claude will be able to search discovered AWS, Azure, GCP and DigitalOcean resources, view relevant resource details, compare backend-calculated cost periods and review optimization findings.

The first release is read-only. It will not delete resources, deploy software, alter cloud configurations, create credentials or run unrestricted cloud queries.

## Planned plugin contents

- `.claude-plugin/plugin.json`: plugin name, author, version and description.
- `.mcp.json`: the remote HTTPS MCP server URL, without secrets.
- `skills/investigate-infrastructure/SKILL.md`: trustworthy resource investigation workflow.
- `skills/analyze-cloud-costs/SKILL.md`: period comparisons, cost basis, provenance and completeness.
- `skills/review-optimization-findings/SKILL.md`: explain candidates, assumptions and evidence.

The manifest and connector config will be committed only once they match the implemented server and pass validation.

## Product

Website: https://infrajump.com

The service uses the user's existing InfraJump permissions and subscription. Any future directory listing, supported tools, billing rules and privacy information must accurately match what is shipped.

This repository contains no private InfraJump backend code, customer records, service tokens or cloud credentials.
