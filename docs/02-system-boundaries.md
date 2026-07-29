# Límites del sistema

## Capas y responsabilidades

### Integración

**Responsabilidad:** conectar fuentes autorizadas y obtener datos.

**No debe:** interpretar semánticamente, priorizar ni exponer credenciales.

### Normalización

**Responsabilidad:** convertir formatos heterogéneos en estructuras consistentes.

**No debe:** generar narrativa ni decisiones ejecutivas.

### Capacidades

**Responsabilidad:** definir operaciones formales disponibles para el sistema.

**No debe:** contener lógica de transporte o presentación.

### Router

**Responsabilidad:** validar la intención formal, seleccionar una capacidad y orquestar su ejecución.

**No debe:** implementar lógica de dominio.

### Motores

**Responsabilidad:** ejecutar consultas, cálculos, reglas y políticas formalizadas.

**No debe:** depender de instrucciones narrativas ambiguas.

### Capa semántica

**Responsabilidad:** interpretar lenguaje, clasificar contenido y redactar respuestas.

**No debe:** autenticar, autorizar, administrar secretos o alterar datos fuera de contratos permitidos.

### Persistencia

**Responsabilidad:** conservar datos normalizados, evidencia, ejecuciones, señales y vistas materializadas.

**No debe:** confundirse con la lógica que produce esos artefactos.

### Materialización

**Responsabilidad:** preparar representaciones operacionales completas y consistentes para consumo posterior.

**No debe:** publicar una fotografía como completa cuando su universo de entrada está incompleto.

### Workspace

**Responsabilidad:** investigar preguntas o señales mediante capacidades y evidencia.

**No debe:** inventar evidencia ni saltarse controles de acceso.

### PressureBoard

**Responsabilidad:** mostrar señales priorizadas y facilitar su comprensión inicial.

**No debe:** recalcular prioridad, deduplicar señales o reconstruir inteligencia en el frontend.

## Fronteras críticas

```text
LLM ≠ motor de cálculo
router ≠ lógica de dominio
frontend ≠ motor de prioridad
persistencia ≠ decisión
transporte ≠ capacidad
```

## Resultado esperado

Cada componente debe poder explicarse mediante:

- entrada;
- responsabilidad;
- salida;
- evidencia producida o consumida;
- controles aplicados;
- fuera de alcance.
