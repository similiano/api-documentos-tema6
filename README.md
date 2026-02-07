# api-documentos-tema6
API REST de documentos con CI/CD (Tema 6)
Probando GitHub Actions 🚀
Segunda prueba de GitHub Actions 🚀

## CI/CD con GitHub Actions

El workflow de integración continua está configurado en `.github/workflows/ci.yml`.  
Este pipeline ejecuta automáticamente **ESLint** y las **pruebas** en cada `push` o `pull request` a la rama principal.  

> Nota: Debido a que el archivo se creó recientemente, aún no se muestran ejecuciones en la pestaña de *Comportamiento*.  
> Sin embargo, el pipeline está listo para activarse en cuanto se realice un nuevo commit o pull request.

## 📊 Observabilidad

Este proyecto incluye mecanismos de observabilidad para facilitar el monitoreo y diagnóstico de la API:

### Logs estructurados con Winston
- Se utiliza **Winston** para registrar cada petición en formato JSON.
- Los logs se almacenan tanto en consola como en el archivo `logs/app.log`.
- Cada entrada incluye método, URL, cuerpo de la petición y timestamp.

### Métricas con Prometheus
- Se expone un endpoint `/metrics` que devuelve métricas en formato Prometheus.
- Métricas incluidas:
  - Métricas por defecto del sistema (CPU, memoria, event loop).
  - Contador de requests HTTP (`http_requests_total`) con etiquetas: método, ruta y estado.
- Estas métricas pueden integrarse fácilmente con **Prometheus + Grafana** para dashboards de monitoreo.

### Beneficios
- Permite detectar problemas de rendimiento y seguridad en tiempo real.
- Facilita la integración con sistemas de observabilidad estándar.
- Cumple con el requisito de observabilidad del Tema 6.
