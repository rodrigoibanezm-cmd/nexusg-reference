# Evidencia y trazabilidad

## Principio central

La narrativa no es la evidencia. NexusG conserva la evidencia como un objeto independiente y trazable.

## Modelo mínimo de evidencia

Una evidencia debería poder identificar:

- tipo de fuente;
- identidad de la fuente;
- entidad o documento relacionado;
- título o descripción;
- extracto o valor observado;
- metadata relevante;
- momento de observación;
- ámbito de acceso.

## Linaje

Cuando una respuesta o señal depende de transformaciones, el sistema debe poder reconstruir:

```text
fuente
→ dato o documento
→ normalización
→ cálculo o clasificación
→ regla o política
→ resultado
→ narrativa o señal
```

## Modalidad epistemológica

Cada afirmación debe conservar su naturaleza.

### Hecho registrado

Información observada directamente en una fuente autorizada.

### Declaración

Contenido expresado por una persona o documento. No equivale necesariamente a un hecho verificado.

### Cálculo

Resultado producido por una fórmula, agregación o regla controlada.

### Clasificación semántica

Interpretación producida por un modelo bajo una taxonomía y contrato definidos.

### Inferencia

Conclusión razonada que excede lo explícitamente registrado.

### Recomendación

Acción propuesta a partir de datos, reglas y contexto.

## Requisitos de trazabilidad

Una ejecución relevante debería registrar, según corresponda:

- actor;
- tenant;
- capacidad;
- parámetros efectivos;
- versión del contrato;
- versión del motor o política;
- fuentes consultadas;
- evidencias seleccionadas;
- advertencias;
- fecha y estado de ejecución.

## Evidencia insuficiente

Cuando la evidencia no alcanza para responder con certeza, el sistema debe indicarlo. No debe completar vacíos con una narrativa convincente.

## Evidencia y privacidad

Una referencia de evidencia no autoriza por sí misma su exposición. La recuperación debe volver a comprobar permisos y ámbito.

## Presentación

Las interfaces pueden mostrar una evidencia mínima y permitir profundización posterior. La compresión visual no debe eliminar la posibilidad de auditoría.
