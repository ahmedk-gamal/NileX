
# 🌾🧠 NILEX.AI

### Smart Green Agricultural Export Ecosystem

[![Status](https://img.shields.io/badge/Status-MVP_Prototype-00C853?style=for-the-badge)](https://github.com/ahmedk-gamal/NileX)
[![AI Engine](https://img.shields.io/badge/AI-Powered-2962FF?style=for-the-badge)](https://github.com/ahmedk-gamal/NileX)
[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![FastAPI](https://img.shields.io/badge/Backend-FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![React](https://img.shields.io/badge/Frontend-React-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactjs.org)
[![MIT License](https://img.shields.io/badge/License-MIT-FFB300?style=for-the-badge)](LICENSE)

---

## 📌 Overview

**NILEX.AI** is an integrated AI‑driven platform that connects Egyptian farmers, exporters, global buyers, and financial institutions into a single intelligent ecosystem.

*   **Advanced Technology**: Deep Learning & Computer Vision for quality grading, Agentic AI for autonomous decision-making, and FinTech credit scoring.
*   **Sustainable Impact**: Reduces post‑harvest losses, lowers water usage and carbon footprint, ensures compliance with international standards.

> 🎯 **Vision** – Transform Egypt into a global agricultural export powerhouse through intelligent, sustainable, and inclusive digital infrastructure, aligned with **Egypt Vision 2030**.

---

## ❗ Problem Statement

*   **Fragmented Supply Chain**: Lack of traceability and coordination.
*   **Limited AI Adoption**: Decisions based on intuition, not data.
*   **Poor Financial Access**: 80%+ of smallholder farmers have no formal credit.
*   **High Post‑Harvest Losses**: 20–30% waste between farm and port.

---

## ⚙️ Core Modules

| Module | Technology Stack | Business Value |
|--------|------------------|----------------|
| **🧠 AI Forecasting** | LSTM, Transformers, RL | Demand prediction, price optimization |
| **👁️ Computer Vision** | CNN (ResNet, EfficientNet), OpenCV | Quality grading, disease detection |
| **🏦 FinTech Scoring** | XGBoost, alternative data | Farmer digital identity, microloans |
| **🛒 Smart Marketplace** | Graph matching, NLP | Direct farmer–exporter connection |
| **🌱 Green Intelligence** | Carbon accounting, water models | Carbon footprint, sustainability reports |

---

## 🏗️ System Architecture

```
[React Dashboard] → [FastAPI Backend] → [Agentic AI Layer]
                           │
         ┌─────────────────┼─────────────────┐
         ▼                 ▼                 ▼
   AI Engine          CV Models        FinTech Scoring
         │                 │                 │
         └─────────┬───────┴───────┬─────────┘
                   ▼               ▼
            Data Lake         Satellite APIs
         (PostgreSQL+MinIO)   (NASA, ESA, Weather)
```

---

## 🛠️ Tech Stack

| Layer | Technologies |
|-------|--------------|
| Frontend | React 18, TailwindCSS, Recharts, PWA |
| Backend | FastAPI, Celery, Redis |
| AI/ML | PyTorch, TensorFlow, HuggingFace, OpenCV |
| Database | PostgreSQL (TimescaleDB), MongoDB |
| Storage | MinIO |
| DevOps | Docker, GitHub Actions, Prometheus+Grafana |

---

## 📊 Economic Impact

| KPI | Improvement |
|-----|-------------|
| Export efficiency | ⬆ +40% |
| Farmer net income | ⬆ +35% |
| Post‑harvest waste | ⬇ -30% |
| Market connectivity | ⬆ +50% |
| Credit access | ⬆ from 15% to 65% |

---

## 🚀 Getting Started

### Prerequisites
- Python 3.10+, Node.js 18+, Docker

```bash
git clone https://github.com/ahmedk-gamal/NileX.git
cd NileX
```

#### Backend
```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
# Edit .env with your API keys
uvicorn main:app --reload --port 8000
```

#### Frontend
```bash
cd frontend
npm install
npm start
```

#### AI Models
```bash
cd ai_models
python train_forecast.py --crop oranges --region egypt
python run_cv_pipeline.py --input data/sample_oranges.jpg
```

#### Docker (Full Stack)
```bash
docker-compose up --build
```

---

## 🔌 API Documentation

- Swagger UI: `http://localhost:8000/docs`
- ReDoc: `http://localhost:8000/redoc`

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/v1/forecast/demand` | POST | Demand & price forecast |
| `/api/v1/cv/grade` | POST | Quality grading from image |
| `/api/v1/credit/score` | POST | Farmer credit score |
| `/api/v1/market/match` | POST | Match farmer with exporter |
| `/api/v1/sustainability/carbon` | GET | Shipment carbon footprint |

---

## 📁 Project Structure

```
NileX/
├── backend/
│   ├── app/{api, core, models, schemas, services}
│   ├── requirements.txt
│   └── Dockerfile
├── frontend/
│   ├── src/{components, pages, services}
│   ├── package.json
│   └── Dockerfile
├── ai_models/
│   ├── forecasting/, computer_vision/, credit_scoring/
│   └── requirements_ai.txt
├── data/{raw, processed, external}
├── docker-compose.yml
├── .env.example
├── LICENSE
├── CONTRIBUTING.md
└── README.md
```

---

## 📡 Data Sources

| Source | Use Case |
|--------|----------|
| NASA FIRMS | Crop health, harvest timing |
| ESA Sentinel Hub | NDVI, soil moisture |
| OpenWeather | Frost, rain forecasting |
| FAO Market Monitor | Global price prediction |
| CBE (future) | Credit scoring API |

---

## 🔒 Security & Privacy

- AES-256 encryption at rest, TLS 1.3 in transit
- Explicit farmer consent for credit scoring
- Role-based access control (Farmer, Exporter, Banker, Admin)
- Compliant with Egyptian Law 151/2020 & GDPR
- Explainable AI (SHAP values)

---

## 🧪 CI/CD (GitHub Actions)

```yaml
name: CI
on: [push, pull_request]
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Backend tests
        run: cd backend && pip install -r requirements.txt && pytest
      - name: Frontend tests
        run: cd frontend && npm install && npm test
```

---

## 🗺️ Roadmap

**Phase 1 (Q3 2025 – MVP)**  
✅ Oranges (Egypt → EU), demand forecasting, basic CV grading, farmer registration.

**Phase 2 (Q4 2025 – Scale)**  
🔄 All major crops, full FinTech integration with banks, Agentic AI for logistics.

**Phase 3 (2026 – Global)**  
🌍 10+ import countries, blockchain traceability, carbon credits marketplace.

---

## 🤝 Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on bug reports, feature requests, and pull requests.

---

## 🌍 Egypt Vision 2030 Alignment

| Pillar | Contribution |
|--------|--------------|
| Economic Development | +25% agricultural exports |
| Digital Transformation | AI backbone for food supply chain |
| Financial Inclusion | 2M+ farmers into formal banking |
| Environmental Sustainability | -15% water use via AI irrigation |

---

## 👥 Team

**Ahmed Khaled** – Project Owner & Lead AI Developer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/ahmedkhaled)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat&logo=github&logoColor=white)](https://github.com/ahmedk-gamal)

---

## 📄 License

MIT License – see [LICENSE](LICENSE) file.

---

## 📬 Contact

- Email: ahmedk.hossam@gmail.com
- Twitter: [@NILEX_AI](https://twitter.com/NILEX_AI)
- Issues: [GitHub Issues](https://github.com/ahmedk-gamal/NileX/issues)

---

## 🌟 Acknowledgments

NASA, ESA, FAO, PyTorch, HuggingFace, FastAPI, and Egypt’s Agritech Incubator.

---



ل `# 🌾🧠 NILEX.AI` لآخر سطر.
4. اعمل **Commit changes**.

كدا بقى **احترافي وجاهز** 👌
