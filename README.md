# MediScope AI

Local-first educational prototype for disease-specific risk-assessment research. It combines a React clinical-research interface and a FastAPI/scikit-learn service skeleton.

## Run the interface (Windows PowerShell)

```powershell
npm install
npm run dev
```

Open the local Vite address shown in the terminal (normally `http://localhost:5173`).

## Run the API after installing Python

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install -r backend\requirements.txt
uvicorn backend.main:app --reload --port 8000
```

The API rejects prediction requests until separately trained model artifacts exist in `ml/artifacts/`. This is deliberate: no model score is invented when legitimate source data, training and evaluation have not yet been completed.

See `docs/` for architecture, methodology, ethics, testing and a presentation walkthrough.
