SAMPATI V2
SAMPATI V2 is a web-based UPI fraud intelligence and investigation platform.
The website is designed to help analysts monitor suspicious UPI transactions, understand why a transaction was flagged, identify possible mule-account networks, and investigate fraud patterns in real time.
What the Website Does
SAMPATI combines multiple fraud-detection layers instead of relying on a single score:
- Rule-based detection for patterns such as velocity spikes, fan-in/fan-out activity, structuring, dormant-to-active behavior, suspicious device/IP signals, and known trap accounts.
- Isolation Forest for detecting unusual or previously unseen transaction behavior.
- Random Forest for supervised fraud classification.
- Graph analysis using NetworkX to identify linked accounts, suspicious transaction chains, hubs, and mule networks.
- Threat intelligence to connect suspicious messages, VPAs, phone numbers, URLs, and fraud campaigns with transaction activity.
- Real-time monitoring through WebSockets so new transaction and investigation data can appear on the dashboard without manual refresh.
- AI-assisted investigation using Gemini to help summarize cases and explain fraud signals.
Main Website Sections
The platform includes pages for:
- Overview dashboard
- Live transaction monitoring
- Fraud cases and investigations
- Threat intelligence
- Fraud-network topology
- Geographic activity
- Analytics and risk metrics
How It Works
UPI Transaction
      ↓
Fraud Rules
      ↓
Isolation Forest
      ↓
Random Forest
      ↓
Threat Intelligence + Fraud Graph
      ↓
Risk Aggregation
      ↓
ALLOW / HOLD / BLOCK
      ↓
Investigator Dashboard
The final result is not just a fraud score. The website also shows the signals and relationships behind the decision so an investigator can understand what happened.
Tech Stack
Frontend
- React
- Vite
- Tailwind CSS
- Recharts
- WebSockets
Backend
- FastAPI
- Python
- Pydantic
- SQLAlchemy
- AsyncPG
Machine Learning & Intelligence
- NumPy
- Isolation Forest
- Random Forest
- NetworkX
- Google Gemini
Data / Infrastructure
- PostgreSQL
- Redis
- Docker
Important Note
SAMPATI is a prototype and demonstration platform.
External institutional integrations such as NPCI, DPIP, PSP/bank signals, and some notification services are simulated or mocked for the demo. The project does not connect to real production UPI or banking systems.
