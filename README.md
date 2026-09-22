# QMoosa Ecosystem Growth & Market Operations

This repository contains market-facing material for **original QMoosa / RDL projects**: grants, partnership outreach, node-operator recruitment, launch messaging, one-pagers, campaign planning, and security-program templates.

## Evidence-first marketing rule

Marketing claims must be narrower than the evidence in the canonical technical repository.

| Project | Canonical technical source | Public positioning |
|---|---|---|
| [PQ-RDL Blockchain](https://github.com/elon00/pq-rdl-blockchain) | `pq-rdl-blockchain` | CI-verified operational devnet/prototype; public mainnet and independently operated public testnet are not claimed |
| [QMoosa Deep Tech AI & Quantum](https://github.com/elon00/qmoosa-deep-tech-ai-quantum-platform) | project README + CI/reality artifacts | Experimental/research/hackathon platform; internal scorecards are not independent certification |
| [QMoosa Nexus](https://github.com/elon00/qmoosa-nexus-platform) | project README + contract/deployment evidence | Multi-chain/account-abstraction research prototype; deployment claims require reproducible explorer evidence |
| [QTON](https://github.com/elon00/qton) | testnet evidence in repository | TON testnet project; not represented as mainnet-live, independently audited, or market-proven |
| [QSui](https://github.com/elon00/QSui) | Move package + project verification | Sui research/testnet-oriented prototype; tokenomics and deployment plans are not market adoption evidence |

Do not describe repository-defined gates, badges, scorecards, simulations, generated receipts, local benchmarks, or CI as third-party certification.

## Repository purpose

```text
rdl-marketing/
├── grants/            grant research and application drafts
├── marketing/         launch copy, one-pagers and campaign material
├── node-recruitment/  permission-based operator recruitment material
├── portfolio/         ecosystem catalog and project mapping
└── bug-bounties/      disclosure and security-program templates
```

## Allowed market claims

A claim is suitable for publication when the referenced evidence exists and supports the exact wording. Examples:

- “ML-DSA-65 integration tests pass in repository CI.”
- “QTON records TON testnet deployment evidence.”
- “PQ-RDL has a CI-verified operational devnet prototype.”
- “The project is recruiting technically capable operators to evaluate a devnet.”
- “The repository includes experimental HotStuff-style consensus and PQC integration work.”

## Claims requiring additional evidence

Do **not** publish these without independent, reproducible support:

- “world's first”, “best”, “leading”, “institutional-grade”, or similar superlatives
- “production-ready”, “mainnet-live”, “fully decentralized”, or “enterprise-ready”
- guaranteed yield, staking rewards, token price, liquidity, exchange listing, or investment return
- specific latency/TPS/throughput claims that were not measured under a documented workload
- user, revenue, TVL, volume, validator-count, partnership, grant-award, or adoption metrics without source evidence
- “audited”, “certified”, “FIPS validated”, “MiCA compliant”, “SEC compliant”, or “legally approved” without the relevant independent authority
- “quantum-safe” for an entire system merely because a PQC primitive is present

See [MARKETING_CLAIM_POLICY.md](MARKETING_CLAIM_POLICY.md).

## Node-operator recruitment

Use only consent-aware, targeted outreach. The canonical operator automation lives in `pq-rdl-blockchain` and is designed to:

- require consent before outreach
- honor opt-outs and do-not-contact state
- throttle repeated contact
- distinguish dry-run from delivered outreach
- avoid guaranteed operator rewards
- describe network status truthfully

Do not scrape contacts or mass-message unrelated developers, communities, or phone numbers.

## Grants and partnerships

Grant documents are working drafts. Before submission:

1. verify the program is still active and eligibility rules are current;
2. verify every technical and deployment statement against the canonical repository;
3. remove unverified performance/adoption metrics;
4. label requested funding as an application/request, not an award;
5. have legal, tax, token, and securities statements reviewed where material.

## Campaign release checklist

Before publishing a campaign asset:

1. identify the canonical implementation repository;
2. link the evidence supporting each material claim;
3. distinguish simulation, local devnet, public testnet, mainnet and production;
4. confirm security/audit language is accurate;
5. confirm incentives are actually funded and governed before advertising them;
6. confirm contact lists have a legitimate outreach basis and opt-out path;
7. archive the final approved copy with a review date.

## Security

Do not commit:

- API keys, seed phrases, wallets or private keys
- operator/customer PII
- private partner correspondence
- unpublished credentials or access tokens

See [SECURITY.md](SECURITY.md).

## Portfolio boundary

This marketing repository is for the user's original QMoosa/RDL projects. It is **not** a marketing umbrella for unrelated forks, mirrors, tutorials, upstream repositories, or reference collections present elsewhere on the GitHub account.

## Current status

**MARKETING OPERATIONS REPOSITORY — NOT A TECHNICAL PRODUCTION CERTIFICATION**

Use the canonical engineering repositories to determine implementation and deployment status.
