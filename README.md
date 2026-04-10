<FILE filename="README.txt">
# 🛡️ IoHT-Shield
## Blockchain-Assisted Anomaly Detection Framework for Securing IoHT Devices
Final Year Project | IEEE Research Paper Implementation
Built with FastAPI, Scikit-learn, TensorFlow, Web3.py, Solidity & Ethereum

📁 Project Structure
textIoHT-Shield/
├── ffrontend/                      ← Frontend folder
│   └── dashboard.html              ← Standalone web dashboard (zero setup)
├── run_app.py                      ← One-click backend starter
├── requirements.txt
├── backend/
│   ├── main.py
│   ├── api/
│   │   ├── routes.py
│   │   └── schemas.py
│   ├── ml/
│   │   ├── isolation_forest.py
│   │   ├── lstm_autoencoder.py
│   │   ├── preprocessor.py
│   │   └── classical_models.py
│   ├── blockchain/
│   │   ├── web3_client.py
│   │   ├── deploy.py
│   │   └── contracts/
│   │       └── AnomalyLog.sol
│   └── models/                     ← (auto-created)
└── docs/
    └── IEEE_Research_Paper.md

🚀 Quick Start (No Setup Needed)

Just open ffrontend/dashboard.html in any browser.
Login with:
Username: admin
Password: iothshield

You’ll instantly get:

Live anomaly simulation
Blockchain logs
ML metrics & charts
Manual prediction tester


⚙️ Full Setup (Backend + Blockchain)
Prerequisites

Python 3.10+
Node.js (for Ganache)

Step 1: Install Python packages
Bashpip install -r requirements.txt
Step 2: Start Ganache (Local Ethereum)
Bash# Run this in a separate terminal
ganache --port 8545 --accounts 10 --deterministic
Step 3: Deploy Smart Contract
Bashcd backend
python blockchain/deploy.py
Step 4: Run the Backend
Easiest way:
Bashpython run_app.py
Or manually:
Bashcd backend
uvicorn main:app --reload --port 8000
API docs will be at: http://localhost:8000/docs

📡 Main API Endpoints

MethodEndpointWhat it doesPOST/api/predictDetect anomaly + log to blockchainPOST/api/ingestLive data ingest + WebSocket broadcastPOST/api/upload-dataUpload your dataset (CSV/JSON)POST/api/trainRetrain models in backgroundGET/api/logsGet all blockchain entriesWS/api/ws/streamReal-time updates

🧠 ML Models Used

Isolation Forest – 96.2% accuracy
LSTM Autoencoder – 97.8% accuracy
Ensemble (both models) – 98.1% accuracy

All models are unsupervised. Classical models (SVM + Random Forest) are also included for future use.

⛓️ Blockchain Part
Smart contract: AnomalyLog.sol
Every anomaly is saved on-chain (Ganache).
Average gas cost: ~21,000 per transaction.
If Ganache is not running, it gracefully falls back to in-memory logs.

📄 Research Paper
Full IEEE paper is inside docs/IEEE_Research_Paper.md
Key results:

Ensemble accuracy: 98.1%
End-to-end latency: < 180 ms


👤 Author
IoHT-Shield – Final Year Engineering Project (2025)

📜 License
MIT License

One-Click Backend Run
Bashpython run_app.py
(Make sure Ganache is running and contract is deployed first)

Ready to test?
Open the dashboard and try it out. Any issues or suggestions? Just open an issue.
</FILE>
✅ How to use this file:

Copy everything from <FILE filename="README.txt"> to </FILE> (including the tags).
Paste it into a new file on your computer.
Save the file as README.txt (or rename it to README.md if you want GitHub to render it nicely).

You now have a clean, ready-to-upload text file. Just drag it into your GitHub repo. Let me know if you want any last tweaks!1.2scant u give me downlaodable txt file containing all 0of thsi<FILE filename="README.txt">
# 🛡️ IoHT-Shield
## Blockchain-Assisted Anomaly Detection Framework for Securing IoHT Devices
Final Year Project | IEEE Research Paper Implementation
Built with FastAPI, Scikit-learn, TensorFlow, Web3.py, Solidity & Ethereum

📁 Project Structure
textIoHT-Shield/
├── ffrontend/                      ← Frontend folder
│   └── dashboard.html              ← Standalone web dashboard (zero setup)
├── run_app.py                      ← One-click backend starter
├── requirements.txt
├── backend/
│   ├── main.py
│   ├── api/
│   │   ├── routes.py
│   │   └── schemas.py
│   ├── ml/
│   │   ├── isolation_forest.py
│   │   ├── lstm_autoencoder.py
│   │   ├── preprocessor.py
│   │   └── classical_models.py
│   ├── blockchain/
│   │   ├── web3_client.py
│   │   ├── deploy.py
│   │   └── contracts/
│   │       └── AnomalyLog.sol
│   └── models/                     ← (auto-created)
└── docs/
    └── IEEE_Research_Paper.md

🚀 Quick Start (No Setup Needed)

Just open ffrontend/dashboard.html in any browser.
Login with:
Username: admin
Password: iothshield

You’ll instantly get:

Live anomaly simulation
Blockchain logs
ML metrics & charts
Manual prediction tester


⚙️ Full Setup (Backend + Blockchain)
Prerequisites

Python 3.10+
Node.js (for Ganache)

Step 1: Install Python packages
Bashpip install -r requirements.txt
Step 2: Start Ganache (Local Ethereum)
Bash# Run this in a separate terminal
ganache --port 8545 --accounts 10 --deterministic
Step 3: Deploy Smart Contract
Bashcd backend
python blockchain/deploy.py
Step 4: Run the Backend
Easiest way:
Bashpython run_app.py
Or manually:
Bashcd backend
uvicorn main:app --reload --port 8000
API docs will be at: http://localhost:8000/docs

📡 Main API Endpoints

MethodEndpointWhat it doesPOST/api/predictDetect anomaly + log to blockchainPOST/api/ingestLive data ingest + WebSocket broadcastPOST/api/upload-dataUpload your dataset (CSV/JSON)POST/api/trainRetrain models in backgroundGET/api/logsGet all blockchain entriesWS/api/ws/streamReal-time updates

🧠 ML Models Used

Isolation Forest – 96.2% accuracy
LSTM Autoencoder – 97.8% accuracy
Ensemble (both models) – 98.1% accuracy

All models are unsupervised. Classical models (SVM + Random Forest) are also included for future use.

⛓️ Blockchain Part
Smart contract: AnomalyLog.sol
Every anomaly is saved on-chain (Ganache).
Average gas cost: ~21,000 per transaction.
If Ganache is not running, it gracefully falls back to in-memory logs.

📄 Research Paper
Full IEEE paper is inside docs/IEEE_Research_Paper.md
Key results:

Ensemble accuracy: 98.1%
End-to-end latency: < 180 ms


👤 Author
IoHT-Shield – Final Year Engineering Project (2025)

📜 License
MIT License

One-Click Backend Run
Bashpython run_app.py
(Make sure Ganache is running and contract is deployed first)

Ready to test?
Open the dashboard and try it out. Any issues or suggestions? Just open an issue.
</FILE>
