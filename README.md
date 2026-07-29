# NexusG Reference

Referencia arquitectónica pública de NexusG.

Este repositorio describe conceptos estables de la plataforma: responsabilidades, contratos, flujos, límites, evidencia, trazabilidad, materialización operacional, seguridad y extensibilidad.

No contiene código productivo, secretos, configuración de clientes, thresholds, estado actual, roadmap, deuda técnica ni detalles de despliegue.

## Qué es NexusG

NexusG es una capa de comprensión operacional entre los sistemas de una organización y las personas que deben decidir.

Integra fuentes estructuradas y no estructuradas, normaliza información, ejecuta capacidades controladas, conserva evidencia y expone dos interfaces principales:

- **Workspace** para investigar preguntas y situaciones con profundidad.
- **PressureBoard** para priorizar las señales que requieren atención.

## Flujo general

```text
Fuentes autorizadas
→ integración y normalización
→ capacidades y motores
→ interpretación semántica controlada
→ cálculo y reglas versionadas
→ evidencia y trazabilidad
→ señales operacionales
→ Workspace / PressureBoard
```

## Principios

- El LLM interpreta lenguaje y contexto; no reemplaza el cálculo controlado.
- Los motores ejecutan reglas determinísticas y políticas formalizadas.
- Toda afirmación relevante debe poder vincularse con evidencia.
- Las fuentes no estructuradas se investigan mediante recuperación progresiva.
- Las señales tienen identidad estable, estado y trazabilidad.
- La preparación operacional ocurre antes del consumo runtime cuando corresponde.
- Las interfaces no reconstruyen inteligencia que ya fue calculada.
- La identidad, el tenant y la autorización son conceptos separados.
- REST, MCP u otros canales son transportes sobre las mismas capacidades.

## Documentación

1. [Visión general](docs/00-overview.md)
2. [Principios](docs/01-principles.md)
3. [Límites del sistema](docs/02-system-boundaries.md)
4. [Flujo runtime](docs/03-runtime-flow.md)
5. [Frontera LLM/backend](docs/04-llm-backend-boundary.md)
6. [Capacidades y routers](docs/05-capabilities-and-routers.md)
7. [Modelo de datos](docs/06-data-model.md)
8. [Evidencia y trazabilidad](docs/07-evidence-and-traceability.md)
9. [Materialización operacional](docs/08-operational-materialization.md)
10. [Señales de presión](docs/09-pressure-signals.md)
11. [Workspace](docs/10-workspace.md)
12. [PressureBoard](docs/11-pressureboard.md)
13. [Identidad, tenancy y seguridad](docs/12-identity-tenancy-security.md)
14. [Glosario](glossary.md)

## Alcance

Esta referencia es conceptual y normativa. Las implementaciones concretas pueden variar en tecnologías, nombres de tablas, endpoints, límites y estrategias de despliegue, siempre que respeten los principios y contratos aquí definidos.
