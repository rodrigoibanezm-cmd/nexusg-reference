# Principios de arquitectura

## 1. Comprensión sobre sistemas existentes

NexusG agrega una capacidad de lectura y decisión sin reemplazar ERP, CRM, correo, BI, documentos u otras fuentes.

## 2. Contratos antes que prompts

Las capacidades se describen mediante entradas y salidas formales. El lenguaje natural se traduce a contratos; no sustituye su validación.

## 3. Cálculo controlado

Las métricas, reglas, agregaciones y políticas se ejecutan en componentes controlados, auditables y versionables.

## 4. LLM acotado

El LLM interpreta lenguaje y contenido, clasifica semánticamente y genera narrativa. No administra credenciales ni reemplaza controles de acceso, validación o cálculo.

## 5. Evidencia primero

Toda conclusión relevante debe conservar referencias a la información que la sostiene.

## 6. Modalidad epistemológica explícita

El sistema distingue entre:

- hecho registrado;
- declaración de una persona;
- cálculo;
- clasificación semántica;
- inferencia;
- recomendación.

## 7. Recuperación progresiva

Las fuentes extensas o no estructuradas se investigan desde representaciones compactas hacia evidencia detallada solo cuando es necesario.

## 8. Presupuesto de contexto

El contexto entregado al LLM se administra mediante compactación, paginación, selección y límites explícitos.

## 9. Señales persistentes

Una situación operacional posee identidad estable, estado, contexto y evidencia. Puede actualizarse sin duplicarse en cada ejecución.

## 10. Preparación antes del consumo

Cuando una interfaz necesita una fotografía operacional, la carga y los motores la preparan antes del runtime.

```text
la preparación calcula
el runtime consume
```

## 11. Interfaces pasivas

Las interfaces renderizan y facilitan interacción. No deben reconstruir prioridad, evidencia o cálculo ya formalizado.

## 12. Separación de identidad y tenant

El principal autenticado, el usuario, el tenant y sus permisos son conceptos distintos.

## 13. Transportes intercambiables

REST, MCP, aplicaciones conversacionales u otros canales son adaptadores sobre las mismas capacidades.

## 14. Configuración no es arquitectura

Thresholds, pesos, ventanas, límites y taxonomías pueden variar. La arquitectura define dónde viven, cómo se versionan y cómo se auditan.
