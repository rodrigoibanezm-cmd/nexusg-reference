# Modelo de datos

## Propósito

NexusG usa un modelo conceptual común para operar sobre fuentes distintas sin imponer una única tecnología de persistencia.

## Entidades principales

### Principal

Identidad autenticada que ejecuta una acción.

### User

Persona o cuenta funcional dentro de un tenant.

### Tenant

Ámbito organizacional que delimita datos, políticas y permisos.

### Source

Sistema o repositorio autorizado del que proviene información.

### Entity

Objeto operacional identificable: cliente, negocio, tienda, oportunidad, mensaje, documento u otro.

### Metric

Valor calculado o registrado asociado a una entidad, dimensión y período.

### Document

Unidad de contenido no estructurado o semiestructurado.

### Evidence

Referencia trazable a la información que sostiene una afirmación, cálculo o señal.

### CapabilityExecution

Registro de una ejecución con actor, tenant, capacidad, versión, parámetros, resultado y estado.

### PressureSignal

Representación persistente de una situación que requiere atención.

### MaterializedView

Representación preparada para consumo runtime.

## Relaciones conceptuales

```text
Tenant
├─ Users
├─ Sources
├─ Entities
├─ Metrics
├─ Documents
├─ Evidence
├─ CapabilityExecutions
├─ PressureSignals
└─ MaterializedViews
```

Una señal puede referenciar múltiples evidencias. Una evidencia puede sostener más de una señal o respuesta, siempre que conserve identidad y contexto.

## Identidad estable

Las entidades, señales y evidencias deben usar claves estables dentro de su ámbito. La recarga o reevaluación no debe crear duplicados innecesarios.

## Versionado

Cuando un resultado depende de una regla, taxonomía, contrato o motor, debe poder registrarse su versión.

## Datos crudos y normalizados

Las implementaciones pueden separar:

```text
raw
→ normalized
→ derived
→ materialized
```

La referencia no obliga a una tabla o base específica, pero sí a conservar trazabilidad entre niveles cuando sea relevante.

## Fuera de alcance

Este documento no prescribe:

- nombres de tablas;
- tipos SQL;
- proveedor de base de datos;
- esquema físico único;
- campos específicos de una industria.
