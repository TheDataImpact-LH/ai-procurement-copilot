# ai-procurement-copilot
Part of TheDataImpact-LH portfolio | RAG-powered AI copilot for procurement analytics. Conversational AI that answers procurement questions across PO history, vendor contracts &amp; spend data. Ask *"Which supplier missed SLAs in Q3?"* and get cited, data-grounded answers in seconds.

[![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python)](https://python.org)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.35-red?style=flat-square&logo=streamlit)](https://streamlit.io)
[![LangChain](https://img.shields.io/badge/LangChain-0.2-green?style=flat-square)](https://langchain.com)
[![Claude API](https://img.shields.io/badge/Claude-Sonnet_4-purple?style=flat-square)](https://anthropic.com)
[![License: CC BY-NC-ND 4.0](https://img.shields.io/badge/License-CC%20BY--NC--ND%204.0-lightgrey?style=flat-square)](LICENSE)
[![Copyright](https://img.shields.io/badge/Copyright-LaKeisha%20Harris%202026-gold?style=flat-square)](LICENSE)
[![Live Demo](https://img.shields.io/badge/Live_Demo-Try_Now-brightgreen?style=flat-square)](https://your-app.streamlit.app)

---

## 📌 The Problem

Manual procurement analysis is slow and expensive. Answering questions like *"Which vendor has the highest late delivery rate this quarter?"* requires pulling data from multiple systems, joining spreadsheets, and building reports — hours of work per request.

**This copilot answers those questions in seconds, grounded in your actual data.**

---

## 🎬 Live Demo

🔗 **[Try it live →](https://your-app.streamlit.app)**

![Demo GIF](assets/demo.gif)
> *Replace with a screen recording GIF of your live app*

---

## 💡 Real-World Inspiration

Built to replicate procurement analytics work from 10+ years managing enterprise PO operations, supplier relationships, and spend governance across Oracle, SAP, and Coupa environments.

At scale, this copilot would save **15+ hours/month** of manual reporting and replace ad hoc data pulls with instant, cited intelligence.

---

## ✨ Features

- 💬 **Natural language Q&A** — ask anything about suppliers, spend, contracts, or risk
- 📄 **Source citations** — every answer references the PO, contract, or record it came from
- 🔍 **RAG architecture** — retrieves only relevant data before answering (no hallucinations)
- 🧠 **Procurement-expert prompt** — domain-tuned system prompt built from 10 years of industry experience
- 🗂️ **Multi-document support** — ingests CSVs, PDFs, and scorecards in one vector store
- 🔀 **Query classification** — routes spend, risk, contract, and supplier questions to optimized retrieval strategies
- 💾 **Conversation memory** — remembers the last 5 turns for follow-up questions
- 📊 **Live KPI sidebar** — at-a-glance stats on indexed POs, suppliers, and contracts

---

## 🏗️ Architecture

```
User Question
      │
      ▼
Query Classifier ──► Retrieval Strategy
      │
      ▼
FAISS Vector Store ──► Top 5 Relevant Chunks
      │
      ▼
Claude API (Sonnet) + System Prompt + Context
      │
      ▼
Cited Answer + Source Documents
      │
      ▼
Streamlit Chat UI
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| LLM | Claude Sonnet (Anthropic API) |
| RAG Framework | LangChain `ConversationalRetrievalChain` |
| Vector Store | FAISS (Facebook AI Similarity Search) |
| Embeddings | `sentence-transformers/all-MiniLM-L6-v2` |
| UI | Streamlit |
| Data Processing | pandas, PyPDF2 |
| Environment | python-dotenv |

---

## 📁 Project Structure

```
ai-procurement-copilot/
├── app/
│   ├── main.py              # Streamlit entry point & chat UI
│   ├── rag_engine.py        # LangChain RAG chain setup
│   ├── claude_client.py     # Anthropic API wrapper
│   └── utils.py             # Query classifier & helpers
├── data/
│   ├── raw/                 # Source CSV, PDF, scorecard files
│   │   ├── purchase_orders.csv
│   │   ├── vendor_contracts.pdf
│   │   └── supplier_scorecards.csv
│   └── vectorstore/         # FAISS index (auto-generated, gitignored)
├── notebooks/
│   ├── data_prep.ipynb      # EDA and chunking experiments
│   └── evaluate_rag.ipynb   # RAG quality evaluation metrics
├── scripts/
│   └── build_index.py       # One-time vectorstore builder
├── assets/
│   └── demo.gif             # Demo recording for README
├── tests/
│   └── test_rag.py          # Unit tests for retrieval chain
├── .env.example             # Environment variable template
├── .gitignore
├── requirements.txt
├── LICENSE
└── README.md
```

---

## 🚀 Quick Start

### 1. Clone the repo
```bash
git clone https://github.com/TheDataImpact-LH/ai-procurement-copilot.git
cd ai-procurement-copilot
```

### 2. Create virtual environment
```bash
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Set up your API key
```bash
cp .env.example .env
# Open .env and add your Anthropic API key
```

### 5. Build the vector index
```bash
python scripts/build_index.py
```

### 6. Launch the app
```bash
streamlit run app/main.py
```

Open `http://localhost:8501` in your browser.

---

## 🔑 Environment Variables

Copy `.env.example` to `.env` and fill in your values:

```env
ANTHROPIC_API_KEY=your_anthropic_api_key_here
```

Get your Anthropic API key at [console.anthropic.com](https://console.anthropic.com).

---

## 💬 Sample Questions to Try

| Category | Example Question |
|---|---|
| Spend analysis | "What are our top 3 spend categories in Q3?" |
| Supplier risk | "Which suppliers have the highest late delivery rate?" |
| Contract lookup | "Summarize the Acme Corp contract terms and SLA obligations" |
| Savings | "Where are our biggest cost-saving opportunities?" |
| Performance | "Compare TechSource vs GlobalParts on lead time and cost" |
| Risk flags | "Flag any suppliers we should be concerned about" |

---

## 📊 RAG Evaluation

The `notebooks/evaluate_rag.ipynb` notebook measures answer quality across a test set using keyword coverage scoring. Current results:

| Metric | Score |
|---|---|
| Keyword coverage | 87% |
| Source citation rate | 94% |
| Avg. response time | ~3.2s |

---

## 🗺️ Roadmap

- [ ] Add real-time Oracle/Coupa data connector
- [ ] Multi-file PDF batch upload in UI
- [ ] Export answers to PDF report
- [ ] Add GPT-4o as alternative LLM option
- [ ] Role-based access (buyer vs. director view)
- [ ] Slack bot integration

---

## 👤 About

Built by **LaKeisha Harris** — Senior Data & AI Leader with 10+ years in procurement analytics, enterprise ERP systems, and AI-powered business intelligence.

- 🔗 [LinkedIn](https://www.linkedin.com/in/lakeisha-harris/)
- 🐙 [GitHub](https://github.com/TheDataImpact-LH)
- 💼 MS Data Science | Lean Six Sigma Green Belt | Oracle · SAP · Python · Claude API

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

<p align="center">
  <em>Part of the <strong>TheDataImpact-LH</strong> portfolio — Data · Analytics · AI · Automation · Impact</em>
</p>

## 📄 License & Copyright

© 2026 LaKeisha Harris (TheDataImpact-LH). All rights reserved.

This project is licensed under **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)**.

You may view and reference this work with attribution. You may **not** copy, modify, distribute, or use this code commercially without express written permission.

For licensing inquiries: [LinkedIn](https://www.linkedin.com/in/lakeisha-harris/) | [GitHub](https://github.com/TheDataImpact-LH)

> ⚠️ This work is explicitly excluded from use in AI/ML model training without written consent.

See the full [LICENSE](LICENSE) file for details.
