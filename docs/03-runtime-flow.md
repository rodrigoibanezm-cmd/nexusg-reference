# Flujo runtime

## Propósito

El runtime convierte una pregunta o una acción de interfaz en una ejecución controlada y trazable.

## Flujo de consulta

```text
pregunta o acción
→ interpretación de intención
→ solicitud formal de capacidad
→ validación
→ autorización
→ router
→ motor especializado
→ resultado estructurado
→ evidencia y trazas
→ interpretación narrativa
→ respuesta o actualización de señal
```

## Entrada semántica

El lenguaje natural puede expresar una intención abierta. Antes de ejecutar, esa intención debe convertirse en una solicitud formal con:

- capacidad;
- actor;
- tenant autorizado;
- parámetros;
- modo de salida;
- contexto permitido.

## Ejecución

El router selecciona un motor registrado. El motor consulta fuentes o representaciones normalizadas, ejecuta reglas y devuelve datos estructurados.

## Salida

Una respuesta de capacidad puede incluir:

- datos;
- métricas;
- evidencia;
- advertencias;
- trazas de ejecución;
- información de versión.

La narrativa se genera después de obtener el resultado estructurado.

## Modos de salida

### Compacto

Optimizado para consumo eficiente por el LLM o una interfaz.

### Detallado

Incluye estructuras adicionales para auditoría, desarrollo o investigación profunda.

La existencia de ambos modos no cambia el cálculo; cambia la representación entregada.

## Investigación progresiva

Para fuentes extensas:

```text
búsqueda amplia
→ resumen estructurado
→ selección de elementos relevantes
→ lectura detallada
→ evidencia específica
```

## Escritura de señales

Cuando una interpretación debe persistir:

```text
evidencia recuperada
→ interpretación semántica
→ validación del contrato de señal
→ aplicación de política
→ escritura idempotente
→ vínculo con evidencia
```

## Errores

Los errores deben distinguir al menos:

- autenticación;
- autorización;
- contrato inválido;
- capacidad no soportada;
- fuente no disponible;
- universo incompleto;
- evidencia insuficiente;
- error interno.

Un error no debe transformarse en una conclusión narrativa aparentemente válida.
