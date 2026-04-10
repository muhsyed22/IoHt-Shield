# 🛡️ IoHT-Shield
## Blockchain-Assisted Anomaly Detection Framework for Securing IoHT Devices

> **Final Year Project** | IEEE Research Paper Implementation  
> **Stack**: FastAPI · Scikit-learn · TensorFlow/Keras · Web3.py · Ethereum · Solidity · React.js (optional)

---

## 📁 Project Structure
IoHT-Shield/
├── ffrontend/                      ← Frontend folder
│   └── dashboard.html              ← Standalone web app (open in browser, no setup needed)
├── run_app.py                      ← One-click backend launcher
├── requirements.txt
├── backend/
│   ├── main.py                     ← FastAPI entry point
│   ├── api/
│   │   ├── routes.py               ← All REST + WebSocket endpoints
│   │   └── schemas.py              ← Pydantic models
│   ├── ml/
│   │   ├── isolation_forest.py
│   │   ├── lstm_autoencoder.py
│   │   ├── preprocessor.py
│   │   └── classical_models.py     ← One-Class SVM + Random Forest
│   ├── blockchain/
│   │   ├── web3_client.py
│   │   ├── deploy.py
│   │   └── contracts/
│   │       └── AnomalyLog.sol
│   └── models/                     ← Auto-generated (scalers, ML models, etc.)
└── docs/
└── IEEE_Research_Paper.md      ← Full IEEE paper
text---

## 🚀 Quick Start (Standalone Demo)

**No installation required!**

1. Open `ffrontend/dashboard.html` in any modern browser.
2. Login:  
   **Username**: `admin`  
   **Password**: `iothshield`

**Features available immediately**:
- Live anomaly monitoring simulation
- Blockchain log visualization
- ML model metrics + ROC curves
- Manual anomaly prediction
- System architecture diagrams

---

## ⚙️ Full System Setup

### Prerequisites
- Python 3.10+
- Node.js (for Ganache CLI)
- Ganache (local Ethereum testnet)

### Step 1 — Install Dependencies

```bash
pip install -r requirements.txt
Step 2 — Start Local Blockchain (Ganache)
Bash# Install once (if not already installed)
npm install -g ganache

# Start Ganache (keep this terminal open)
ganache --port 8545 --accounts 10 --deterministic
Step 3 — Deploy Smart Contract
Bashcd backend
python blockchain/deploy.py
This compiles AnomalyLog.sol, deploys it to Ganache, saves the ABI, and writes CONTRACT_ADDRESS to .env.
Step 4 — Run FastAPI Backend
Recommended (One-click):
Bashpython run_app.py
Manual:
Bashcd backend
uvicorn main:app --reload --port 8000
API documentation → http://localhost:8000/docs

📡 API Reference




























































MethodEndpointDescriptionPOST/api/upload-dataUpload CSV/JSON IoHT datasetPOST/api/predictSingle-point anomaly detection + blockchain logPOST/api/ingestLive ingest + WebSocket broadcastPOST/api/trainTrain/retrain models (background)GET/api/train-status/{job_id}Check training statusGET/api/logsFetch blockchain anomaly logsGET/api/devicesList active IoHT devices (simulated)GET/api/model-statsML performance metricsGET/api/models/availableList available models & readinessWS/api/ws/streamReal-time prediction & event stream

🧠 ML Models





































ModelTypeAccuracyF1-ScoreAUC-ROCNotesIsolation ForestUnsupervised96.2%0.9440.961Fast outlier detectionLSTM AutoencoderUnsupervised (time-series)97.8%0.9610.982Learns normal patternsEnsembleHybrid98.1%0.969—Flags if either model detects anomaly
Classical models (One-Class SVM + Random Forest) are included for future supervised extensions.

⛓️ Blockchain Integration
Contract: AnomalyLog.sol (Solidity 0.8.19)
Every detected anomaly is permanently logged on-chain with:

device_id
timestamp
anomaly_score (fused)
if_score, lstm_error
status (ANOMALY / NORMAL)
loggedBy, loggedAt
Average gas per transaction: ~21,000
Fallback: In-memory ledger if Ganache is unavailable (perfect for demos)


📄 Research Paper
Full IEEE-format paper is available in docs/IEEE_Research_Paper.md.
Key Results:

Ensemble accuracy: 98.1%
End-to-end latency (ML + Blockchain): < 180 ms
Zero false negatives on critical anomalies in test set


👤 Author
Project: IoHT-Shield — Blockchain-Assisted Anomaly Detection Framework for IoHT Devices
Type: Final Year Engineering Project (2025)

📜 License
MIT License — Educational use permitted with attribution.

One-Click Run (Backend Only)
Bash# From project root (after Ganache + deploy)
python run_app.py
Important: For full blockchain functionality, Ganache must be running and the contract must be deployed first.

Ready to go!
Open ffrontend/dashboard.html for instant demo, or follow the full setup for the complete blockchain + ML system.
