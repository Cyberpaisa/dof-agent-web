# DOF — Synthesis Hackathon 2026 Submission

## Project Info

| Field | Value |
|-------|-------|
| **Title** | DOF — Deterministic Observability Framework |
| **Tagline** | Math-verified, blockchain-attested AI agent governance |
| **Live Demo** | https://dof-agent-web.vercel.app |
| **GitHub** | https://github.com/Cyberpaisa/deterministic-observability-framework |
| **Demo Frontend** | https://github.com/Cyberpaisa/dof-agent-web |
| **Contract (Avalanche)** | [0x154a3F49a9d28FeCC1f6Db7573303F4D809A26F6](https://snowtrace.io/address/0x154a3F49a9d28FeCC1f6Db7573303F4D809A26F6) |
| **ERC-8004 (Base)** | [TX 0x7362ef41...](https://basescan.org/tx/0x7362ef41605e430aba3998b0888e7886c04d65673ce89aa12e1abdf7cffcada4) |
| **Builder** | Juan Carlos Quiceno Vasquez (@Cyberpaisa) |

---

## Tracks

### 1. Synthesis Open Track — $28,308

**Why DOF fits:** DOF is a complete governance and verification framework for autonomous AI agents. It solves the trust problem: how do you know an AI agent did what it said it did?

**What we built:**
- 35-module Python framework with deterministic governance (zero LLM in the loop)
- Z3 theorem prover integration — 8/8 formal proofs VERIFIED
- On-chain attestation pipeline — 48+ attestations on Avalanche + Base
- 238+ fully autonomous agent cycles with zero human input
- 986 unit tests passing
- 10 interactive track demos at https://dof-agent-web.vercel.app

**Key innovation:** Every agent action is governed by deterministic rules, verified by mathematical proofs, and recorded immutably on-chain. No trust required — only math and blockchain.

---

### 2. ERC-8004 Agents With Receipts — $4,000

**Demo:** https://dof-agent-web.vercel.app/agent-services-base/

**What we built:** Every DOF agent action produces an on-chain receipt:

```
Input → Governance Check → Z3 Proof → keccak256 Hash → registerProof() on Avalanche
```

- DOFProofRegistry.sol deployed on Avalanche C-Chain
- ERC-8004 Identity Token #31013 on Base Mainnet
- Each receipt contains a mathematical proof hash — the correctness itself is attested on-chain
- Proof types: Z3 Verification, Governance Audit, Privacy Check, Security Scan

**Evidence:**
- [DOFProofRegistry on Snowtrace](https://snowtrace.io/address/0x154a3F49a9d28FeCC1f6Db7573303F4D809A26F6)
- [ERC-8004 TX on Basescan](https://basescan.org/tx/0x7362ef41605e430aba3998b0888e7886c04d65673ce89aa12e1abdf7cffcada4)

---

### 3. Best Agent on Celo — $3,000

**Demo:** https://dof-agent-web.vercel.app/best-agent-celo/

Governed stablecoin transfers (cUSD, cEUR, cREAL) on Celo. Every transfer goes through the DOF governance pipeline:
- Wallet connect with automatic chain detection
- 5-step governance pipeline with Z3 verification
- Auto-running agent terminal with live cycle counter
- Transaction history with governed status

---

### 4. MetaMask Delegations — $3,000

**Demo:** https://dof-agent-web.vercel.app/metamask-delegation/

Delegate governance tokens (ENS, UNI, AAVE, ARB, OP) securely. Every delegation is governed, verified, and signed via MetaMask personal_sign.

---

### 5. Locus x402 Payments — $4,000

**Demo:** https://dof-agent-web.vercel.app/locus-payments/

Autonomous HTTP 402 payment protocol. Two agents discover services, negotiate price, pay, and exchange data — zero human intervention. One-click autonomous 7-step flow.

---

### 6. Private Agents — $5,750

**Demo:** https://dof-agent-web.vercel.app/private-agents/

Real AES-256-GCM encryption via Web Crypto API. PBKDF2 key derivation with 100,000 iterations. Privacy Vault stores encrypted data in localStorage. Data never leaves the browser in plaintext.

---

### 7. Agent Services on Base — $4,000

**Demo:** https://dof-agent-web.vercel.app/agent-services-base/

Submit Z3 verification proofs to DOFProofRegistry.sol. Real ERC-8004 registration TX linked to Basescan. 5-step proof submission pipeline.

---

### 8. AgentEscrow ERC-8183

**Demo:** https://dof-agent-web.vercel.app/erc-8183/

Trustless escrow for agent-to-agent commerce. Full state machine with 3 roles (Client, Provider, Evaluator). Autonomous demo runs the complete lifecycle with zero user input.

---

### 9. Additional Tracks

- **Octant Public Goods** — https://dof-agent-web.vercel.app/octant-analysis/
- **Olas Pearl** — https://dof-agent-web.vercel.app/olas-pearl/
- **SuperRare AI Art** — https://dof-agent-web.vercel.app/superrare-art/
- **Arkhai Escrow** — https://dof-agent-web.vercel.app/arkhai-escrow/

---

## Technical Architecture

```
User / MetaMask
    ↓
DOF Agent (Autonomous)
    ↓
1. ConstitutionEnforcer  → 42 deterministic rules, zero LLM
2. Z3 Formal Verifier    → 8/8 theorems PROVEN
3. keccak256 Proof Hash   → Deterministic hash
4. MetaMask Signature     → personal_sign
5. On-Chain Attestation   → Avalanche / Base / Celo
```

## Tech Stack

- **Frontend:** Vanilla HTML/CSS/JS — zero external dependencies, zero build step
- **Wallet:** Native `window.ethereum.request()` — no Web3.js CDN
- **Encryption:** Web Crypto API (AES-256-GCM + PBKDF2)
- **Art:** Canvas API with seeded PRNG
- **Hosting:** Vercel static deployment
- **On-Chain:** Avalanche C-Chain, Base Mainnet, Celo Mainnet

## What Makes DOF Different

1. **Zero LLM in governance** — All rules are deterministic code. If it violates the constitution, it gets blocked.
2. **Formal verification** — Z3 theorem prover generates actual mathematical proofs, not assertions or unit tests.
3. **On-chain receipts** — Every action produces a keccak256 hash published to Avalanche/Base. Permanently auditable.
4. **Zero external dependencies** — No CDN, no npm packages, no build step. Eliminates supply chain risk.
5. **Fully autonomous** — 238+ cycles executed with zero human input.

---

*Submitted by DOF Agent — Synthesis Hackathon 2026*
