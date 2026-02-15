# ERC-8004 Agent — Starter Template

Create your own AI agent on Avalanche in 5 minutes.

## Quick Start

```bash
# 1. Install dependencies
npm install

# 2. Run locally
npm run dev

# 3. Open in browser
open http://localhost:3000
```

Your agent is running! You should see the dashboard.

## Test Your Endpoints

```bash
# Dashboard (visual page)
curl http://localhost:3000/

# Health check
curl http://localhost:3000/api/health

# Registration metadata
curl http://localhost:3000/registration.json

# MCP — list available tools
curl -X POST http://localhost:3000/mcp \
  -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","method":"tools/list","id":1}'

# MCP — call a tool
curl -X POST http://localhost:3000/mcp \
  -H "Content-Type: application/json" \
  -d '{"jsonrpc":"2.0","method":"tools/call","id":2,"params":{"name":"ping","arguments":{"message":"hello"}}}'
```

## Customize Your Agent

1. Edit `registration.json` — change name, description, capabilities
2. Edit `src/server.ts` — add your own MCP tools and API endpoints
3. Replace `public/agent.png` with your agent's image
4. Edit `dashboard.html` to customize the visual page

## Deploy to Railway

1. Push your code to GitHub
2. Go to [railway.app](https://railway.app) → New Project → Deploy from GitHub
3. Railway auto-detects the Dockerfile and deploys
4. Get your public URL (e.g., `https://my-agent-production.up.railway.app`)
5. Update all `YOUR-DOMAIN` in `registration.json` with your Railway URL

## Register On-Chain

After deploying, register your agent on Avalanche:

```bash
# Install Foundry (if you don't have it)
curl -L https://foundry.paradigm.xyz | bash && foundryup

# Get test AVAX from faucet
# Visit: https://faucet.avax.network

# Register on Fuji testnet
export PRIVATE_KEY="your-private-key"
cast send 0x8004A818BFB912233c491871b3d84c89A494BD9e \
  "register(string)" \
  "https://YOUR-RAILWAY-URL/registration.json" \
  --rpc-url https://api.avax-test.network/ext/bc/C/rpc \
  --private-key $PRIVATE_KEY
```

After registering, update `registration.json` with your `agentId` and redeploy.

## Project Structure

```
├── src/server.ts          # Your agent's code (endpoints + MCP)
├── registration.json      # ERC-8004 metadata (name, services, capabilities)
├── dashboard.html         # Visual page shown at /
├── public/agent.png       # Your agent's image
├── package.json           # Dependencies
├── tsconfig.json          # TypeScript config
├── Dockerfile             # Railway deployment
├── railway.toml           # Railway settings
├── .env.example           # Environment variables template
└── .well-known/           # Domain verification
```

## Learn More

- [ERC-8004 Spec](https://eips.ethereum.org/EIPS/eip-8004)
- [8004.org](https://www.8004.org)
- [8004scan.io](https://8004scan.io)
- [Colombia-Blockchain/agent-skills](https://github.com/Colombia-Blockchain/agent-skills)
