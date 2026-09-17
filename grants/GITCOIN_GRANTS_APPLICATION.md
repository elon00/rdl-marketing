# 🏛️ Gitcoin Grants Application — PQ-RDL Blockchain

**Project Name:** Republic of Divine Light (PQ-RDL)  
**Track:** Open Source Software / Web3 Infrastructure & Cryptographic Research  
**Primary Repository:** `https://github.com/elon00/pq-rdl-blockchain`  
**License:** MIT / Open Source  

---

### 1. Project Overview (Short Summary)
PQ-RDL is a post-quantum resilient Layer-1 blockchain engineered to defend decentralized ledgers against "Harvest Now, Decrypt Later" (HNDL) state attacks and quantum Shor/Grover factorization. Unlike legacy ECDSA/Ed25519 chains, PQ-RDL natively implements **NIST FIPS 204 (ML-DSA-65 / Dilithium)** lattice-based digital signatures combined with an asynchronous **HotStuff BFT consensus** engine and verifiable disk persistence under strict machine-audited reality gates.

---

### 2. Problem Statement
99% of current Web3 infrastructure (Bitcoin, Ethereum, Solana) relies on secp256k1 or Ed25519 elliptic curve cryptography. A cryptanalytically relevant quantum computer (CRQC) will break these signatures in minutes, risking hundreds of billions in digital assets. Furthermore, current "post-quantum" promises remain simulated whitepapers without running multi-node state synchronization or crash-recovery verifications.

---

### 3. Solution & Technical Architecture
PQ-RDL provides a working, open-source, reproducible blockchain stack featuring:
1. **Hybrid Cryptography Pipeline:** Native integration of NIST FIPS 204 (ML-DSA-65) lattice signatures with Edwards-curve backwards compatibility.
2. **Pipelined HotStuff BFT Consensus:** 3-phase commit with view-change timeout certificates, equivocation proofs, and safety locks.
3. **Fail-Closed Machine Verification:** Every release undergoes the QMoosa Reality Gate (R1 through R6) guaranteeing physical node separation, tip parity, and crash recovery with machine-verifiable JSON attestations.

---

### 4. Progress & Milestones Achieved
- [x] **Milestone 1:** Rust native node binary (`rdl-node`) with full consensus, mempool, and P2P TLS challenge-auth.
- [x] **Milestone 2:** Official NIST Post-Quantum Cryptographic test vectors verified with 0 failures.
- [x] **Milestone 3:** Public Testnet Gate R6 validated with independent cloud validators and automated crash-recovery tip matching.
- [ ] **Milestone 4 (Grant Target):** Deploying 25 globally distributed physical validator nodes and developing post-quantum browser wallet extensions.

---

### 5. Use of Funds
- **Infrastructure & Node Hosting (40%):** Subsidizing validator nodes across diverse geographic regions and autonomous system numbers (ASNs).
- **Formal Security Audits & Fuzzing (35%):** Contracting third-party smart contract and lattice-cryptography security researchers.
- **Developer Documentation & SDKs (25%):** Building developer kits for TypeScript, Rust, and Go to easily deploy post-quantum decentralized applications.

---

### 6. Team & Background
- **Solo Architect & Lead Developer:** Core engineer specializing in distributed systems, post-quantum lattice primitives, and high-assurance verifiable computing.
