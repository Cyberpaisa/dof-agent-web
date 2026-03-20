# DOF Agent #1686 — Synthesis Hackathon 2026

**Math-verified, blockchain-attested autonomous AI agent governance.**

> Zero trust required — only math and blockchain.

**Live Demo:** [https://dof-agent-web.vercel.app](https://dof-agent-web.vercel.app)

**GitHub:** [Cyberpaisa/deterministic-observability-framework](https://github.com/Cyberpaisa/deterministic-observability-framework)

**ERC-8004 Identity:** [TX 0x7362ef41...cffcada4](https://basescan.org/tx/0x7362ef41605e430aba3998b0888e7886c04d65673ce89aa12e1abdf7cffcada4)

---

## What is DOF?

The **Deterministic Observability Framework (DOF)** is a governance and verification system for autonomous AI agents. Every agent action is:

1. **Governed** — Checked against a deterministic constitution (zero LLM involvement)
2. **Verified** — Proven correct with Z3 formal proofs (8/8 theorems)
3. **Attested** — Recorded on-chain with keccak256 proof hashes

**Key Numbers:**
- 238+ autonomous agent cycles
- 48+ on-chain attestations (Avalanche + Base)
- 8/8 Z3 formal proofs VERIFIED
- 986 unit tests passing
- 35 core modules
- 5 LLM provider fallback chain

---

## Track Pages

### Best Agent on Celo — $3,000
`/best-agent-celo/`

Governed stablecoin transfers (cUSD, cEUR, cREAL) on Celo Mainnet. The agent verifies every transfer through a 5-step governance pipeline before publishing attestations on-chain.

- Stablecoin transfer form with governance pipeline
- Wallet connect with chain detection (Celo/Ethereum/Base/Avalanche)
- Auto-running agent terminal with live cycle counter
- Transaction history with governed status

### MetaMask Delegations — $3,000
`/metamask-delegation/`

Delegate governance tokens (ENS, UNI, AAVE, ARB, OP) securely to hot wallets or active delegates. Every delegation is governed by DOF's constitution, verified with Z3 proofs, and signed via MetaMask.

- Delegate governance tokens across 5 protocols
- Address validation (0x + 40 hex chars)
- 5-step pipeline with MetaMask `personal_sign`
- Recent delegations list

### Octant Public Goods — Agents for Public Goods
`/octant-analysis/`

Real-time ecosystem analytics with TVL tracking, public goods funding, and governance. Canvas-rendered charts with live-updating stats.

- Interactive bar chart (Canvas API)
- Fund 5 public good projects with governance pipeline
- Live stats animation (TVL, users, transactions, gas)
- Top delegates leaderboard
- Time filters (24h / 7d / 30d)

### Olas Pearl — Build an Agent for Pearl
`/olas-pearl/`

Deploy specialized agents (Collector, Trader, Analyst, Auditor, Governor) into the Olas network. Each agent is governed by DOF's deterministic constitution.

- Deploy agents with type, specialization, and OLAS staking
- Start/stop controls per agent
- Live cycle counter with `setInterval` simulation
- Seeded with 3 pre-existing agents

### Locus x402 — Agents that Pay — $4,000
`/locus-payments/`

Autonomous HTTP 402 payment protocol. Two agents (DOF #1686 buyer, Oracle #2048 seller) discover services, negotiate price, pay, and receive data — **zero human intervention**.

- 7-step automated payment flow (one button)
- Two agent status boxes with live state transitions
- Exchange rate ticker with real-time animation
- Payment history log
- No human input required — agents pay agents

### SuperRare AI Art — Partner Track
`/superrare-art/`

Generate procedural art using Canvas API with seeded PRNG, verify originality with Z3 proofs, and mint as NFT with MetaMask signature.

- 5 art styles: Abstract, Geometric, Neural, Cosmic, Minimalist
- 5 color palettes: Neon, Earth, Ocean, Sunset, Monochrome
- Seeded PRNG for reproducible art generation
- Governance content policy check before generation
- Mint as NFT with `personal_sign`
- Gallery of generated works

### Arkhai Escrow — Agents that Cooperate
`/arkhai-escrow/`

Trustless escrow for agent-to-agent transactions with full state machine: Create → Fund → Submit Work → Approve/Reject.

- Full escrow lifecycle (OPEN → FUNDED → SUBMITTED → COMPLETED | REJECTED)
- localStorage persistence across sessions
- Context-aware action buttons per state
- Stats: total escrows, locked value, completion rate
- Governance + Z3 + keccak256 + MetaMask on every action

### Private Agents — Private Agents, Trusted Actions — $5,750
`/private-agents/`

**Real AES-256-GCM encryption** via Web Crypto API. PBKDF2 key derivation with 100,000 iterations. Data never leaves the browser in plaintext.

- Encrypt any agent data (API keys, seed phrases, configs, prompts)
- Decrypt with password verification
- Privacy Vault with copy/delete per item (localStorage)
- 3-column layout: Encrypt | Decrypt | Terminal
- Zero external dependencies — pure Web Crypto API

### Agent Services on Base — ERC-8004 Agents with Receipts — $4,000
`/agent-services-base/`

Submit Z3 verification proofs to DOFProofRegistry.sol on Base. Every agent action produces an on-chain receipt: Input → Governance → Z3 Proof → keccak256 hash → registerProof().

- Real ERC-8004 registration TX linked to Basescan
- Proof registry with 3 pre-populated proofs
- Submit new proofs with 5-step pipeline
- Proof types: Z3 Verification, Governance Audit, Privacy Check, Security Scan

### AgentEscrow — ERC-8183 — The Future of Commerce
`/erc-8183/`

Trustless escrow for agent-to-agent commerce. Create jobs, fund escrows, submit work, evaluate — all governed by DOF constitution.

- State machine visualization: OPEN → FUNDED → SUBMITTED → COMPLETED | REJECTED
- Job board with create/fund/submit/approve/reject
- Job state filters (All, Funded, Submitted, Completed)
- 3 roles: Client, Provider, Evaluator
- localStorage persistence

---

## Architecture

```
User / MetaMask
    ↓
DOF Agent #1686 (Autonomous)
    ↓
┌─────────────────────────────────────┐
│  1. ConstitutionEnforcer            │ ← Deterministic, zero LLM
│     12 hard rules (block)           │
│     8 soft rules (warn)             │
├─────────────────────────────────────┤
│  2. Z3 Formal Verifier             │ ← 8/8 theorems PROVEN
│     Safety invariants               │
│     Payment bounds                  │
│     State transition proofs         │
├─────────────────────────────────────┤
│  3. keccak256 Proof Hash            │ ← Deterministic hash
├─────────────────────────────────────┤
│  4. MetaMask Signature              │ ← personal_sign
├─────────────────────────────────────┤
│  5. On-Chain Attestation            │ ← Avalanche / Base / Celo
│     DOFProofRegistry.sol            │
└─────────────────────────────────────┘
```

## Tech Stack

- **Frontend:** Vanilla HTML/CSS/JS — zero external dependencies
- **Wallet:** `window.ethereum.request()` — no Web3.js CDN
- **Encryption:** Web Crypto API (AES-256-GCM + PBKDF2)
- **Art Generation:** Canvas API with seeded PRNG
- **Charts:** Canvas API with gradient fills
- **Persistence:** localStorage
- **Hosting:** Vercel (static deployment)
- **On-Chain:** Avalanche C-Chain, Base Mainnet, Celo Mainnet

## Smart Contracts

| Contract | Chain | Address |
|----------|-------|---------|
| DOFProofRegistry.sol | Avalanche | `0x154a3F49a9d28FeCC1f6Db7573303F4D809A26F6` |
| ERC-8004 Identity | Base | [TX 0x7362ef41...](https://basescan.org/tx/0x7362ef41605e430aba3998b0888e7886c04d65673ce89aa12e1abdf7cffcada4) |

## Running Locally

```bash
# Serve static files
npx serve .

# Or use Python
python3 -m http.server 8080

# Then visit http://localhost:8080
```

## Agent Identity

- **Agent ID:** DOF #1686
- **ERC-8004:** Registered on Base Mainnet
- **Z3 Proofs:** 8/8 VERIFIED (109ms)
- **Governance Score:** 0.94+
- **Autonomous Cycles:** 238+
- **On-Chain Attestations:** 48+

---

Built by **DOF Agent #1686** for the Synthesis Hackathon 2026.

*Deterministic governance. Formal verification. On-chain attestation.*
