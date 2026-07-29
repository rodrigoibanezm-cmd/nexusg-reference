# Visión general

## Propósito

NexusG transforma información operacional dispersa en comprensión utilizable, evidencia trazable y señales accionables.

No reemplaza los sistemas de origen. Opera sobre ellos mediante integraciones autorizadas y capacidades formales.

## Arquitectura general

```text
Fuentes estructuradas y no estructuradas
→ integración autorizada
→ normalización
→ capacidades y motores
→ interpretación semántica
→ cálculo controlado y políticas
→ evidencia y trazabilidad
→ señales operacionales
→ Workspace / PressureBoard
```

## Componentes principales

### Integración

Conecta fuentes autorizadas y administra credenciales delegadas sin exponerlas al LLM ni a las interfaces.

### Normalización

Convierte datos heterogéneos en representaciones intermedias consistentes: entidades, métricas, documentos, eventos y evidencia.

### Capacidades

Expone operaciones formales y acotadas. Una capacidad define qué puede pedirse, qué parámetros acepta y qué devuelve.

### Motores

Ejecutan consultas, agregaciones, reglas y políticas controladas. No dependen de una narrativa libre para producir resultados.

### Capa semántica

Interpreta lenguaje, clasifica contenido y genera narrativa dentro de contratos explícitos.

### Persistencia y materialización

Conserva memoria operacional, evidencia, ejecuciones y señales. Cuando corresponde, prepara vistas antes del consumo runtime.

### Workspace

Permite investigar libremente o profundizar una señal existente.

### PressureBoard

Muestra un conjunto reducido de situaciones que requieren atención y explica por qué importan.

## Dos modos de comprensión

```text
Workspace     = investigación
PressureBoard = priorización
```

Ambos consumen las mismas capacidades, señales y evidencias. No son sistemas separados.

## Fuera de alcance

Esta referencia no prescribe:

- proveedor de nube;
- base de datos específica;
- framework frontend;
- modelo LLM concreto;
- thresholds universales;
- taxonomías únicas;
- nombres de endpoints o tablas;
- configuración de clientes.
