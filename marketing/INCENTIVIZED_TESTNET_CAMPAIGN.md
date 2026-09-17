# 🛡️ "Project Quantum Shield" — Incentivized Testnet Campaign Blueprint

> A gamified point-and-reputation program designed to onboard 500+ independent, geographically decentralized node operators and validators.

---

## 🎯 Campaign Objectives
1. Scale from 3 local nodes to **100+ globally distributed physical validators** across 20+ countries and independent ASNs.
2. Stress-test network partition resilience, HotStuff BFT view changes, and peer gossip under heavy load.
3. Build an engaged, organic developer and operator community.

---

## 🏆 Operator Points & Rewards Matrix

| Quest / Action | Point Reward | Verification Evidence |
| :--- | :--- | :--- |
| **Node Launch & Initial Peer Handshake** | **500 pts** | Valid TLS fingerprint & `/rpc/tip` response |
| **24/7 Node Uptime (Weekly)** | **1,000 pts / week** | Automated health ping check ($>99.5\%$ uptime) |
| **Crash-Recovery Drill Participant** | **750 pts / drill** | Successful restart with identical pre/post tip hash |
| **Submit State Transition Transaction** | **200 pts / tx** | Verified in published block ledger |
| **Report Valid Bug / Peer Anomaly** | **2,500 – 10,000 pts**| GitHub issue with reproduction script |
| **Share Node Setup Guide / Social Post** | **300 pts** | Link to tweet, article, or video demo |

---

## 🎖️ Operator Tiers & Badges

1. **Genesis Sentinel (Top 50 Operators):**
   - Mainnet Genesis Validator whitelist.
   - Exclusive "Post-Quantum Cryptographic Pioneer" NFT badge.
   - Priority allocation in future foundation developer grants.
2. **Lattice Guardian (Top 51–200 Operators):**
   - Testnet rewards pool allocation.
   - Direct access to core development Discord channel.
3. **Network Node Operator (All Validated Operators):**
   - Public attestation certificate recorded in `evidence/`.

---

## 📊 Live Leaderboard Architecture
Operators submit their node telemetry endpoint:
```bash
curl -X POST https://api.rdl.network/testnet/register \
  -H "Content-Type: application/json" \
  -d '{"operator": "alice", "public_endpoint": "198.51.100.24:7102", "tls_fingerprint": "..."}'
```

An automated cron job verifies:
- Reachability & block synchronization.
- Points increment automatically.
- Leaderboard renders live on the web interface.
