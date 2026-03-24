# Proof of Concept - Found-and-Lost Pet Portal

## Scope
- App category: Productivity
- Entity model: Found Lost Task
- Deployable stack: Flask + SQLAlchemy + Gunicorn + Docker + CI

## Dynamic Field Configuration
- Owner: `owner` (text)
- Priority (1-5): `priority` (number)
- Operational Notes: `notes` (textarea)

## Run Evidence Commands
```bash
python app.py
curl http://localhost:5000/api/health
curl http://localhost:5000/api/schema
curl -X POST http://localhost:5000/api/records   -H "Content-Type: application/json"   -d '{"title":"Demo Record","status":"in-progress","payload":{"owner":"Demo value","priority":12,"notes":"seed note"}}'
curl http://localhost:5000/api/metrics
```

## Metadata
- Idea number: 37
- Generated UTC: 2026-03-24T15:52:22.008863+00:00
- Status: Phase-2 complete
