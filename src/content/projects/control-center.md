---
title: "Control Center"
problem: "AI-Workflows, Agenten und n8n-Automatisierungen sind über verschiedene Tools verteilt — kein zentrales Lagebild."
solution: "Self-hosted Dashboard auf eigenem Hetzner-Server: Live-Status aller Agenten, n8n-Workflow-Übersicht, Incident-Tracking."
stack: ["Next.js 15", "FastAPI", "Python", "Docker", "Coolify", "Authentik"]
status: "live"
order: 3
kpi: "Zentrales Ops-Tool für alle laufenden AI-Automatisierungen — intern, hinter SSO."
---

## Was ist das Control Center?

Ein selbst gehostetes Operations-Dashboard für AI-Automatisierung:

- **Agent-Übersicht:** Status aller laufenden und geplanten Agenten
- **n8n-Integration:** Workflow-Status direkt aus n8n
- **Incident Tracking:** Fehler und Alerts an einem Ort
- **Authentik SSO:** Kein öffentlicher Zugang — nur nach Login

## Architektur

```
Browser → Authentik SSO → Next.js Frontend
                               ↓
                         FastAPI Backend
                               ↓
                   n8n API (automation-plus-ki.de)
```

## Hosting

Läuft auf eigenem Hetzner-Server via Coolify. CI/CD über GitHub Actions:
Push → Build Docker Image → Push to GHCR → Coolify Deploy.

Kein lokales Docker nötig — alles über CI/CD.

## Status

Live und in aktiver Nutzung. Intern unter Authentik SSO — nicht öffentlich zugänglich.
