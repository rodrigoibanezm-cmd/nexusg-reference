# Contratos públicos

Estos archivos describen formas de intercambio estables. No son código ejecutable ni copias de contratos internos.

## Frontera de confianza

`actor_context` y `tenant_context` forman parte del sobre de ejecución, pero deben ser resueltos o verificados por una capa autenticada. No deben aceptarse como autoridad solo porque un cliente, frontend o LLM los envíe.

El contenido semántico propuesto por un LLM se limita a campos autorizados, normalmente `capability` y `parameters`. El backend conserva la responsabilidad de:

- autenticar al principal;
- resolver tenant y permisos;
- validar el scope efectivo;
- validar el contrato;
- ejecutar la capacidad;
- registrar la traza.

## Versionado

Los ejemplos usan versiones ilustrativas. Una implementación debe versionar contratos, motores y políticas de manera independiente cuando sus cambios puedan alterar el resultado.

## Extensión

Los contratos pueden especializarse por capacidad mediante esquemas adicionales. Una especialización no debe debilitar autenticación, autorización, trazabilidad ni evidencia.
