# Señales de presión

## Definición

Una **PressureSignal** representa una situación operacional que requiere atención, seguimiento o decisión.

La señal es el concepto persistente. La tarjeta es solo una posible representación visual.

## Propósito

Una señal comprime evidencia dispersa en una unidad de atención que responde:

- qué ocurre;
- por qué importa;
- qué conviene hacer;
- qué evidencia lo sostiene;
- cuál es su estado.

## Contrato conceptual

Una señal debería poder contener:

- identidad estable;
- tenant;
- dimensión;
- estado;
- prioridad;
- título;
- resumen;
- razón de importancia;
- acción recomendada;
- confianza;
- referencias de evidencia;
- contexto reutilizable;
- versión de política;
- fechas de creación y actualización.

## Identidad e idempotencia

La misma situación no debe convertirse en una señal nueva en cada ejecución. Una clave estable permite actualizar su prioridad, estado, interpretación y evidencia.

## Agrupación

```text
un problema operacional
→ una señal activa
```

Si varios hallazgos conducen a la misma decisión, deben agruparse antes de llegar a la interfaz.

## Estado

Una implementación puede distinguir estados como:

- activa;
- resuelta;
- descartada;
- en seguimiento.

Los nombres exactos son configurables. La transición debe ser trazable.

## Prioridad

La prioridad puede resultar de reglas, políticas, métricas e interpretación semántica. Debe ser explicable y versionable.

No existe un threshold universal de NexusG.

## Evidencia

La señal referencia evidencia; no la sustituye. Workspace debe poder recuperar el detalle autorizado de esa evidencia.

## Recomendación

Una acción recomendada debe presentarse como recomendación, no como hecho ni como mandato irreversible.

## Fuera de alcance

Este documento no define buckets, colores, límites visibles ni taxonomías específicas de industria.
