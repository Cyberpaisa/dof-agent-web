# DOF — Deterministic Observability Framework

**Math-verified, blockchain-attested autonomous AI agent governance.**

> Zero trust required — only math and blockchain.

[![Live Demo](https://img.shields.io/badge/Live_Demo-dof--agent--web.vercel.app-8b5cf6?style=for-the-badge)](https://dof-agent-web.vercel.app)
[![ERC-8004](https://img.shields.io/badge/ERC--8004-Certified-22c55e?style=for-the-badge)](https://basescan.org/tx/0x7362ef41605e430aba3998b0888e7886c04d65673ce89aa12e1abdf7cffcada4)
[![On-Chain](https://img.shields.io/badge/Avalanche-48%2B_Attestations-e84142?style=for-the-badge)](https://snowtrace.io/address/0x154a3F49a9d28FeCC1f6Db7573303F4D809A26F6)

**Live Demo:** [https://dof-agent-web.vercel.app](https://dof-agent-web.vercel.app)

**Core Framework:** [Cyberpaisa/deterministic-observability-framework](https://github.com/Cyberpaisa/deterministic-observability-framework)

---

## What is DOF?

The **Deterministic Observability Framework (DOF)** is a governance and verification system for autonomous AI agents. Every agent action is:

1. **Governed** — Checked against a deterministic constitution (zero LLM involvement)
2. **Verified** — Proven correct with Z3 formal proofs (8/8 theorems)
3. **Attested** — Recorded on-chain with keccak256 proof hashes

### Key Metrics

| Metric | Value | Verifiable |
|--------|-------|------------|
| Autonomous Cycles | 238+ | Git commit history |
| On-Chain Attestations | 48+ | [Snowtrace](https://snowtrace.io/address/0x154a3F49a9d28FeCC1f6Db7573303F4D809A26F6) |
| Z3 Formal Proofs | 8/8 PROVEN | `python3 -c "from core.z3_verifier import Z3Verifier; print(Z3Verifier().verify_all())"` |
| Unit Tests | 986 passing | `python3 -m unittest discover tests/` |
| Core Modules | 35 | Source code |
| LLM Providers | 5 (fallback chain) | Cerebras → Groq → Mistral → SambaNova → NVIDIA |
| Governance Rules | 42 deterministic | Zero LLM involvement |
| ERC-8004 Identity | Token #31013 | [Basescan TX](https://basescan.org/tx/0x7362ef41605e430aba3998b0888e7886c04d65673ce89aa12e1abdf7cffcada4) |

---

## Track Pages

### 1. Best Agent on Celo
`/best-agent-celo/` — Governed stablecoin transfers (cUSD, cEUR, cREAL) on Celo. Wallet with chain detection. Auto-running agent terminal with live cycle counter.

### 2. MetaMask Delegations
`/metamask-delegation/` — Delegate governance tokens (ENS, UNI, AAVE, ARB, OP). Address validation. 5-step governance pipeline with MetaMask `personal_sign`.

### 3. Octant Public Goods
`/octant-analysis/` — Real-time ecosystem analytics. Canvas-rendered bar charts, live-updating stats (TVL, users, transactions), public goods funding form, top delegates leaderboard.

### 4. Olas Pearl
`/olas-pearl/` — Deploy specialized agents (Collector, Trader, Analyst, Auditor, Governor) into the Olas network. Start/stop controls. Live cycle counter.

### 5. Locus x402 Payments
`/locus-payments/` — Autonomous HTTP 402 payment protocol. Two agents negotiate, pay, and exchange data in a 7-step flow. **Zero human intervention** — agents pay agents.

### 6. SuperRare Generative Art
`/superrare-art/` — Procedural art via Canvas API with seeded PRNG. 5 styles, 5 palettes. Governance content check. Mint as NFT with MetaMask signature.

### 7. Arkhai Escrow
`/arkhai-escrow/` — Trustless escrow with full state machine (OPEN → FUNDED → SUBMITTED → COMPLETED | REJECTED). localStorage persistence. Stats tracking.

### 8. Private Agents
`/private-agents/` — **Real AES-256-GCM encryption** via Web Crypto API. PBKDF2 key derivation (100K iterations). Privacy Vault. Data never leaves the browser in plaintext.

### 9. Agent Services on Base
`/agent-services-base/` — ERC-8004 proof registry on Base. Submit Z3 verification proofs with 5-step pipeline. Real TX link to Basescan.

### 10. AgentEscrow ERC-8183
`/erc-8183/` — Trustless escrow for agent-to-agent commerce. Job board with state machine. 3 roles (Client, Provider, Evaluator). **Autonomous demo** runs the full escrow lifecycle with zero user input.

---

## Architecture

```
User / MetaMask
    ↓
DOF Agent (Autonomous)
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

| Layer | Technology | Notes |
|-------|-----------|-------|
| Frontend | Vanilla HTML/CSS/JS | Zero external dependencies |
| Wallet | `window.ethereum.request()` | Native MetaMask API, no Web3.js |
| Encryption | Web Crypto API | AES-256-GCM + PBKDF2 (100K iterations) |
| Art Generation | Canvas API | Seeded PRNG for reproducible provenance |
| Charts | Canvas API | Gradient fills, live animation |
| Persistence | localStorage | Offline-capable, no backend required |
| Hosting | Vercel | Static deployment, zero build step |
| On-Chain | Avalanche C-Chain, Base, Celo | Multi-chain attestation |

## Smart Contracts

| Contract | Chain | Address | Explorer |
|----------|-------|---------|----------|
| DOFProofRegistry.sol | Avalanche C-Chain | `0x154a3F49a9d28FeCC1f6Db7573303F4D809A26F6` | [Snowtrace](https://snowtrace.io/address/0x154a3F49a9d28FeCC1f6Db7573303F4D809A26F6) |
| ERC-8004 Identity | Base Mainnet | Token #31013 | [Basescan](https://basescan.org/tx/0x7362ef41605e430aba3998b0888e7886c04d65673ce89aa12e1abdf7cffcada4) |

## Running Locally

```bash
# Option 1: Node.js
npx serve .

# Option 2: Python
python3 -m http.server 8080

# Then visit http://localhost:8080
```

No build step. No npm install. No dependencies. Just serve static files.

## Security

- Zero hardcoded credentials or API keys
- All wallet operations via MetaMask (user-controlled)
- Client-side encryption with Web Crypto API (AES-256-GCM)
- No external CDN dependencies (eliminates supply chain risk)
- localStorage stores only user-encrypted data
- `.env` excluded via `.gitignore`

## License

Apache 2.0

---

Built by **[Cyber Paisa](https://github.com/Cyberpaisa)** for the **Synthesis Hackathon 2026**.

*Deterministic governance. Formal verification. On-chain attestation.*
