# DocuAgent — Intelligent Document Processing

A **multi-agent AI system** that autonomously processes business documents end-to-end.

## What It Does

Upload any document (invoice, KYC form, contract, receipt, insurance claim, loan doc, shipping form) and 5 specialized agents collaborate to process it:

| Agent | Task |
|---|---|
| 📥 Ingestion Agent | Validates file, extracts metadata |
| 🔍 Classification Agent | Identifies document type with confidence score |
| 📊 Extraction Agent | Pulls structured fields using AI + regex |
| ✅ Validation Agent | Enforces business rules (required fields, numeric checks) |
| 🚦 Routing Agent | Assigns destination queue, SLA, and next actions |

## Tech Stack

- **Backend:** FastAPI (Python)
- **Frontend:** HTML5 · CSS3 · Vanilla JavaScript
- **Design:** Dark glassmorphism UI with animated agent pipeline

## Getting Started

```bash
# Install dependencies
pip install fastapi uvicorn python-multipart Pillow

# Run the server
python server.py
```

Open **http://localhost:8000** in your browser.

## Deployment

The project ships with a `vercel.json` configuration and a serverless entry point at
`api/index.py`, so it can be deployed to Vercel directly from this repository:

```bash
vercel --prod
```

## Supported Document Types

- 📑 Invoice
- 🪪 KYC Form
- 📝 Contract
- 🧾 Receipt
- 🏥 Insurance Claim
- 🏦 Loan Document
- 📦 Shipping Form

## Project Structure

```
📦 DocuAgent
├── server.py          # FastAPI backend + 5 agents
├── app.py             # Streamlit version (alternative)
├── create_ppt.py      # PPTX report generator
├── requirements.txt   # Python dependencies
├── vercel.json        # Deployment configuration
├── api/
│   └── index.py       # Serverless entry point
└── static/
    ├── index.html     # Frontend UI
    ├── style.css      # Premium dark stylesheet
    └── app.js         # Frontend pipeline logic
```

## Author

**Suman Pogul** — [@Sp4545](https://github.com/Sp4545)
