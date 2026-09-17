# 🌐 1-Click Node Operator Manual — PQ-RDL Testnet

Welcome to the **PQ-RDL Public Testnet** validator network. Running a node earns operator credentials, testnet incentives, and future mainnet validator whitelisting.

---

## ⚡ Minimum System Requirements
- **CPU:** 2 vCPU (x86_64 or ARM64)
- **RAM:** 4 GB
- **Disk:** 40 GB NVMe / SSD
- **OS:** Ubuntu 22.04 LTS / 24.04 LTS or macOS / Windows with WSL2
- **Network:** Public IP with port `7102` open for P2P/RPC

---

## 🚀 Quickstart (3 Commands)

### Step 1: Clone and Build Binary
```bash
git clone https://github.com/elon00/pq-rdl-blockchain.git
cd pq-rdl-blockchain

# Install Rust & Node prerequisites if missing
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
source "$HOME/.cargo/env"

# Build optimized release binary
cargo build --release --locked --bin rdl-node
```

### Step 2: Generate TLS Credentials
```bash
mkdir -p data
openssl req -x509 -newkey rsa:2048 -keyout data/rdl-tls-key.pem \
  -out data/rdl-tls-cert.pem -days 365 -nodes -subj "/CN=rdl-validator-$(hostname)"
```

### Step 3: Launch Validator & Sync to Public Network
```bash
./target/release/rdl-node --listen "0.0.0.0:7102"
```

To test if your node is synced:
```bash
# Query current block height
./target/release/rdl-node --height "127.0.0.1:7102"

# Query current tip hash
./target/release/rdl-node --tip "127.0.0.1:7102"
```

---

## 🛡️ Running as a System Service (24/7 Autopilot)

Create `/etc/systemd/system/rdl-node.service`:
```ini
[Unit]
Description=PQ-RDL Post-Quantum Validator Node
After=network.target

[Service]
Type=simple
User=ubuntu
WorkingDirectory=/home/ubuntu/pq-rdl-blockchain
ExecStart=/home/ubuntu/pq-rdl-blockchain/target/release/rdl-node --listen 0.0.0.0:7102
Restart=always
RestartSec=3
LimitNOFILE=65535

[Install]
WantedBy=multi-user.target
```

Enable and start:
```bash
sudo systemctl daemon-reload
sudo systemctl enable rdl-node
sudo systemctl start rdl-node
sudo journalctl -u rdl-node -f
```
