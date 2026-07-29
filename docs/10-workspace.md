# Workspace

## Definición

Workspace es la interfaz de investigación de NexusG.

Permite explorar una pregunta abierta o profundizar una señal existente utilizando capacidades formales y evidencia autorizada.

## Modos de entrada

### Investigación libre

Parte desde una pregunta y determina qué capacidades deben ejecutarse.

### Investigación desde una señal

Parte desde el contexto, la recomendación y las evidencias vinculadas a una PressureSignal.

## Flujo

```text
pregunta o señal
→ interpretación de intención
→ selección de capacidades
→ recuperación progresiva
→ cálculo y evidencia
→ síntesis
→ profundización opcional
```

## Recuperación progresiva

Para fuentes documentales o conversacionales:

```text
búsqueda
→ representación compacta
→ selección
→ lectura detallada
→ evidencia específica
```

Workspace no necesita cargar todo el universo de información para comenzar una investigación.

## Responsabilidades

Workspace debe:

- conservar el contexto de la pregunta;
- usar capacidades autorizadas;
- distinguir datos, inferencias y recomendaciones;
- mostrar evidencia suficiente;
- permitir profundización;
- comunicar límites y ausencia de datos.

## Fuera de alcance

Workspace no debe:

- inventar evidencia;
- omitir controles de acceso;
- tratar resultados semánticos como hechos sin validación;
- reconstruir cálculos que corresponden a motores;
- presentar una consulta parcial como revisión completa.

## Relación con PressureBoard

PressureBoard responde primero dónde mirar. Workspace permite comprender qué ocurrió, por qué importa y qué alternativas existen.

```text
PressureBoard → atención
Workspace     → investigación
```

Ambos deben compartir identidad de señal, contexto y referencias de evidencia.
