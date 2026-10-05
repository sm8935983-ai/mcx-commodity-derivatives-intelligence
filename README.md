# MCX Commodity Derivatives Intelligence

A full-stack analytical platform for evaluating MCX India gold futures contracts using proper price normalization, historical spread analysis, and conservative signal generation.

## Features

- MCX bhavcopy ingestion with CSV upload fallback
- strict validation and data-quality reporting
- configurable contract specification engine
- normalization to equivalent pure-gold price per gram
- spread and z-score analytics
- conservative NO SIGNAL logic
- walk-forward backtesting with transaction costs and slippage
- dashboard for relative value and performance
- demo mode for non-live data

## Stack

- Backend: FastAPI, SQLAlchemy, pandas, numpy, scipy
- Frontend: React + Vite + TypeScript
- Database: SQLite by default, PostgreSQL-ready

## Local run

Backend:

```bash
cd backend
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

Frontend:

```bash
cd frontend
npm install
cp .env.example .env
npm run dev -- --host 0.0.0.0 --port 5173
```

## API examples

- `GET /api/health`
- `GET /api/contracts`
- `GET /api/data`
- `GET /api/normalized-prices`
- `GET /api/spread`
- `GET /api/signals`
- `GET /api/term-structure`
- `POST /api/backtest`
- `GET /api/trades`
- `GET /api/data-quality`

## Important disclaimer

This application is for educational and research purposes only. Signals are statistical indicators, not financial advice.
