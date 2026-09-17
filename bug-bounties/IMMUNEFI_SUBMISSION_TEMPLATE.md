# 🐞 Immunefi Vulnerability Disclosure Submission Template

Use this pre-formatted template when submitting critical findings to Immunefi or protocol teams.

---

### 1. Title & Classification
- **Vulnerability Title:** [Concise description of the flaw, e.g., Signature Replay via Unchecked Nonce in P2P Challenge Frame]
- **Target Protocol:** [Target Project Name]
- **Target Asset:** [Contract Address / Repo Link / Binary Component]
- **Severity Assessment (CVSS v3.1):** 
  - Score: [e.g., 9.8 Critical / 7.5 High]
  - Vector: `CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H`

---

### 2. Executive Vulnerability Summary
[A 2-paragraph overview explaining what the bug is, why it occurs, and the maximum financial/operational impact if exploited by a malicious attacker.]

---

### 3. Technical Vulnerability Details
- **Affected Function/Code:**
  ```rust
  // Insert affected code snippet here
  ```
- **Root Cause Analysis:**
  [Explain the architectural or cryptographic breakdown — e.g. lack of mutual authentication, race condition, or deserialization exploit.]

---

### 4. Proof of Concept (PoC)
```bash
# Step 1: Clone target
git clone [repo_url]
cd [repo_dir]

# Step 2: Run reproduction script
node test/exploit_poc.mjs
```

**PoC Script (`exploit_poc.mjs`):**
```javascript
// Automated deterministic exploit payload
```

---

### 5. Recommended Remediation
[Provide the exact, safe, deterministic diff or code patch to permanently fix the issue.]

```diff
- // Vulnerable logic
+ // Secured logic
```

---

### 6. Payout & Contact Details
- **Recipient Address (USDC / ERC20):** `[Your Public Wallet Address]`
- **PGP Fingerprint:** `[Your PGP Key]`
