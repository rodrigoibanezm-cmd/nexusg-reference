# Materialización operacional

## Propósito

La materialización prepara una representación operacional antes de que una interfaz o agente la consuma.

## Flujo

```text
fuente
→ datos crudos
→ normalización
→ métricas y evidencia
→ reglas y señales
→ vista materializada
→ consumo runtime
```

## Principio central

```text
la preparación calcula
el runtime consume
```

Esto reduce latencia, evita recalcular lógica en cada interacción y mantiene una fotografía coherente para distintos consumidores.

## Responsabilidad

La materialización puede:

- consolidar entidades y métricas;
- aplicar políticas versionadas;
- agrupar señales redundantes;
- preparar resúmenes;
- construir vistas por tenant, fecha o propósito;
- registrar origen y fecha de actualización.

## Completitud

Una vista no debe presentarse como completa cuando el universo de entrada está incompleto.

Antes de publicar una materialización, la implementación debe validar las condiciones de completitud definidas para esa fuente y propósito.

Si no se cumplen, debe:

- conservar la materialización anterior cuando sea seguro;
- marcar el resultado como incompleto;
- evitar afirmaciones de cobertura total;
- registrar el motivo.

## Idempotencia

Reprocesar el mismo ámbito y período debe actualizar la representación correspondiente sin crear duplicados innecesarios.

## Historia

Cuando el propósito lo requiera, distintas fechas o versiones deben conservarse para auditoría y comparación.

## Separación runtime/operación

### Operación

- captura;
- persistencia;
- normalización;
- clasificación;
- cálculo;
- reconstrucción de vistas.

### Runtime

- lectura;
- filtrado autorizado;
- entrega de JSON estructurado;
- render o interpretación.

## Fuera de alcance

La referencia no exige una tabla de snapshots, una base de datos o un scheduler concreto.
