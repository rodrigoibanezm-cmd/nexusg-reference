# PressureBoard

## Definición

PressureBoard es la interfaz de priorización de NexusG.

Muestra un conjunto reducido de situaciones que requieren atención y permite comprender rápidamente por qué importan.

## Objetivo

PressureBoard no existe para explorar todos los datos. Existe para reducir tiempo a comprensión y orientar la atención ejecutiva.

## Invariantes

PressureBoard:

- no calcula métricas;
- no clasifica contenido;
- no reconstruye prioridades;
- no deduplica señales;
- no inventa recomendaciones;
- no sustituye la evidencia;
- no funciona como un dashboard BI general.

Consume señales ya preparadas y autorizadas.

## Flujo

```text
PressureSignals activas
→ filtro autorizado
→ orden y agrupación preparados
→ representación visual
→ apertura de contexto
→ Workspace
```

## Contenido mínimo de una señal

La interfaz debería permitir reconocer:

- qué ocurre;
- por qué importa;
- nivel o tipo de atención;
- acción recomendada;
- evidencia mínima;
- acceso a investigación detallada.

## Compresión

El motor debe reducir ruido antes del render.

```text
múltiples hallazgos relacionados
→ una situación operacional
→ una señal activa
```

La interfaz no debe resolver redundancias que pertenecen a la capa de preparación.

## Relación con Workspace

Cada señal debe poder convertirse en contexto de investigación sin perder identidad ni evidencia.

PressureBoard prioriza. Workspace profundiza.

## Fuera de alcance

La referencia no define:

- número máximo de señales;
- colores;
- layout;
- buckets concretos;
- plataforma de frontend;
- comportamiento específico por dispositivo.
