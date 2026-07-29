# Capacidades y routers

## Capacidad

Una capacidad es una operación formal que NexusG puede ejecutar sobre una fuente o una representación operacional.

Debe definir:

- nombre estable;
- propósito;
- contrato de entrada;
- contrato de salida;
- permisos requeridos;
- errores posibles;
- evidencia producida;
- versión.

## Router

El router recibe una solicitud formal y selecciona el motor correspondiente.

```text
solicitud
→ validación
→ autorización
→ resolución de capacidad
→ ejecución
→ normalización de respuesta
```

## Responsabilidad del router

- comprobar que la capacidad existe;
- normalizar parámetros compatibles;
- seleccionar el motor;
- propagar actor y tenant autorizados;
- aplicar la forma común de respuesta.

## Fuera de alcance

El router no debe:

- consultar directamente fuentes de dominio;
- calcular métricas;
- interpretar evidencia;
- construir narrativa;
- contener reglas específicas de clientes.

## Motores especializados

Cada motor debe poseer una responsabilidad acotada. Ejemplos conceptuales:

- consultar entidades;
- agregar métricas;
- comparar períodos;
- recuperar documentos;
- leer evidencia detallada;
- materializar señales;
- administrar una acción autorizada.

## Composición

Una capacidad compleja puede componer motores menores siempre que conserve:

- contratos explícitos;
- trazabilidad de subejecuciones;
- control de errores;
- límites de acceso;
- evidencia de cada etapa.

## Transportes

Una misma capacidad puede exponerse por:

- REST;
- MCP;
- una aplicación conversacional;
- una interfaz interna;
- un proceso programado.

El transporte adapta el protocolo. No redefine la lógica de dominio.

## Extensión

Agregar una capacidad requiere:

1. definir su contrato;
2. registrar su motor;
3. declarar permisos;
4. especificar evidencia y trazas;
5. probar entradas, salidas y errores;
6. documentar sus límites.
