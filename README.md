# FinClust: Financial Behavior Clustering App

# FinClust

An unsupervised machine learning application for financial behavior segmentation. Users upload or generate financial data, and the system clusters it into behavioral segments with interactive visualizations.

## Architecture

```
Frontend (SvelteKit)              Backend (FastAPI)
┌──────────────────┐              ┌──────────────────────────┐
│  Registration    │──────────────│  User auth + DB          │
│  Data upload     │──────────────│  Data generation         │
│  Cluster viz     │◀─────────────│  Clustering engine       │
│  Chart display   │              │  Cluster descriptions    │
└──────────────────┘              └──────────────────────────┘
        Netlify                           FastAPI
```

## Backend Structure

- `main.py` — FastAPI application entry point, CORS configuration
- `routes.py` — API endpoints
- `clustering.py` — Unsupervised ML clustering logic
- `data_generator.py` — Synthetic financial data generation
- `database.py` — Database connection and setup
- `models.py` — Database models
- `schemas.py` — Pydantic request/response validation
- `user_manager.py` — User registration and authentication

## Features

- User registration and authentication
- Financial data generation and upload
- Unsupervised clustering (behavioral segmentation)
- Cluster descriptions and interpretation
- Interactive chart visualizations
- Full-stack deployment (Netlify + FastAPI)

## Tech Stack

- **ML:** scikit-learn (unsupervised clustering)
- **Backend:** Python, FastAPI, Pydantic
- **Frontend:** SvelteKit
- **Database:** SQLite / PostgreSQL
- **Deployment:** Netlify (frontend), Render (backend)
