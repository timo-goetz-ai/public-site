---
title: "Core Platform (AIOS)"
problem: "AI-Automatisierung braucht eine gemeinsame Infrastruktur — für Workflows, Daten, APIs und Agenten."
solution: "Monorepo-Plattform mit Admin-Dashboard, Python-APIs und n8n-Layern — komplett self-hosted auf Hetzner."
stack: ["Next.js 14", "Python", "FastAPI", "Docker", "n8n", "Directus", "Coolify"]
status: "live"
order: 4
kpi: "5+ Services im Produktivbetrieb, täglich laufende Research- und Content-Workflows."
---

## Was ist Core Platform?

Die Basis-Infrastruktur für alle AI-Automatisierungen auf automation-plus-ki.de:

- **Admin Dashboard:** Next.js Operations-UI für alle internen Services
- **AIOS Core:** Python-API für Agent-Orchestrierung und Daten-Workflows
- **n8n Layer-Architektur:** 100–500er Layers für INGEST → BRAIN → RESEARCH → CONTENT → HUMAN
- **Directus CMS:** Datenbankschicht für Agents, Workflows, Content und Trends

## n8n Workflows (täglich aktiv)

| Workflow | Zeitplan |
|----------|---------|
| Trend Monitor | täglich 08:00 |
| Sentiment Tracker | Mo. 08:00 |
| Content Opportunity | täglich 09:30 |
| Daily Digest | täglich 08:00 |

## Hosting

Komplett self-hosted auf Hetzner via Coolify. Alle Services hinter Authentik SSO.
CI/CD: GitHub Actions → GHCR → Coolify Auto-Deploy.

## Status

Im Produktivbetrieb. Research-Tabellen füllen sich täglich automatisch.
