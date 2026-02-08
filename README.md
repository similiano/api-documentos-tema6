# API Documentos – Tema 6

## Objetivo del proyecto
Este proyecto implementa una **API REST de Documentos** como parte del Tema 6.  
El objetivo es demostrar:
- CRUD completo sobre la entidad Documento.
- Endpoint de salud (`/health`) y métricas (`/metrics`).
- Pipeline CI/CD con gates de calidad.
- Seguridad shift-left (SAST/DAST).
- Observabilidad (logs JSON y métricas Prometheus).
- Documentación de calidad y postmortem.

---

## Stack tecnológico
- **Backend:** Node.js 20 + Express
- **Tests:** Jest + Supertest
- **Lint:** ESLint
- **SAST:** CodeQL
- **DAST:** OWASP ZAP baseline
- **Contenedor:** Docker multi-stage
- **CI/CD:** GitHub Actions
- **BD:** SQLite (local, simple)
- **Logs:** Winston (JSON estructurado con timestamp)
- **Observabilidad:** Prometheus client

---

## Cómo ejecutar local
```bash
npm install
npm run dev

## Entrega final
- Release/tag final: https://github.com/similar/api-documentos-tema6/releases/tag/v1.0.0
