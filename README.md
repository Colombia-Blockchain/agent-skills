# Colombia Blockchain Agent Skills

A collection of skills for AI agents. Skills are packaged instructions and scripts that extend agent capabilities.

## Installation

```bash
npx skills add Colombia-Blockchain/agent-skills
```

## Available Skills

| Skill | Type | Description |
|---|---|---|
| **erc8004-avalanche** | Blockchain | Build, deploy, and register AI agents on Avalanche using ERC-8004 (Trustless Agents) |

## erc8004-avalanche

The most comprehensive skill for building ERC-8004 AI agents on Avalanche — from zero to a live, registered agent with interoperability protocols.

**What it covers:**

- **Registration** — Register AI agents on-chain (ERC-721 NFT identity), reputation feedback, validation
- **Interoperability** — Complete implementation guides for A2A, MCP, and x402 protocols
- **Deployment** — Architecture diagrams, Railway hosting, infrastructure setup, cost estimation
- **Best Practices** — Metadata structure, scanner score optimization, capability design, common mistakes
- **Troubleshooting** — Real production issues and solutions from building AvaBuilder Agent (#1686)
- **API Reference** — TypeScript/JavaScript examples with viem and ethers.js

**Documentation:**

| Guide | Description |
|-------|-------------|
| `SKILL.md` | Main skill guide — quick start, registration, concepts |
| `references/a2a-guide.md` | A2A protocol — agent-to-agent communication |
| `references/mcp-guide.md` | MCP protocol — programmatic tool access via JSON-RPC |
| `references/x402-guide.md` | x402 protocol — USDC micropayments on Avalanche |
| `references/best-practices.md` | Metadata, scoring, services, capabilities |
| `references/deployment-guide.md` | Architecture, Railway, infrastructure, costs |
| `references/troubleshooting.md` | Real-world issues and diagnostic commands |
| `references/api-reference.md` | TypeScript API examples (viem + ethers.js) |
| `references/registration-format.md` | registration.json specification |
| `references/contract-addresses.md` | All contract addresses and RPC endpoints |

**Scripts:**

| Script | Description |
|--------|-------------|
| `scripts/register.sh` | Register an agent on-chain (Mainnet or Fuji) |
| `scripts/check-agent.sh` | Check agent registration and metadata |
| `scripts/give-feedback.sh` | Give reputation feedback to an agent |
| `scripts/check-avariskscan.sh` | Verify agent in ERC-8004 scanners |

**Contract Addresses (Avalanche):**

| Chain | Identity Registry | Reputation Registry |
|---|---|---|
| Mainnet (43114) | `0x8004A169FB4a3325136EB29fA0ceB6D2e539a432` | `0x8004BAa17C55a88189AE136b182e5fdA19dE9b63` |
| Fuji (43113) | `0x8004A818BFB912233c491871b3d84c89A494BD9e` | `0x8004B663056A597Dffe9eCcC1965A193B7388713` |

**Links:**
- [ERC-8004 Spec](https://eips.ethereum.org/EIPS/eip-8004)
- [8004.org](https://www.8004.org)
- [8004scan.io](https://8004scan.io)

## Compatibility

Works with 20+ AI agents including:

Claude Code, Cursor, Windsurf, Cline, GitHub Copilot, Gemini CLI, and more.

## License

This project is licensed under the Wolfcito Open / Commercial License (WOCL).
Commercial use requires a separate agreement.
