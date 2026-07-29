# Identidad, tenancy y seguridad

## Principio central

La identidad autenticada, el usuario, el tenant y el scope de datos son conceptos distintos.

## Principal autenticado

Entidad que inicia una acción y cuya identidad fue verificada por un mecanismo de autenticación.

## Usuario

Persona o cuenta funcional que opera dentro de uno o más ámbitos autorizados.

## Tenant

Frontera organizacional que separa datos, configuraciones, políticas y artefactos.

## Autorización

Toda ejecución debe resolver:

- quién actúa;
- en nombre de qué tenant;
- sobre qué fuente;
- con qué permisos;
- para qué capacidad;
- dentro de qué scope.

El tenant no debe derivarse únicamente de un parámetro libre enviado por el cliente.

## Credenciales delegadas

Las integraciones pueden utilizar autorización delegada por usuario o tenant.

Las credenciales deben:

- permanecer fuera del contexto del LLM;
- almacenarse de forma protegida;
- renovarse en la capa de integración;
- limitarse al scope necesario;
- poder revocarse;
- asociarse a una identidad y ámbito verificables.

## Separación de privilegios

Las operaciones de captura, materialización y administración pueden requerir privilegios distintos a las consultas runtime.

```text
runtime    = lectura y consumo autorizado
operations = captura, reconstrucción y administración
```

## Evidencia y acceso

Una referencia a evidencia no concede acceso automático. La recuperación del contenido debe volver a verificar autorización.

## Multi-tenant

Toda entidad persistente relevante debe quedar asociada a su tenant o a un ámbito equivalente verificable.

Las consultas deben evitar cruces accidentales entre tenants y registrar el ámbito efectivo de ejecución.

## Logs y errores

Los logs deben permitir diagnóstico sin exponer:

- secretos;
- tokens;
- contenido sensible innecesario;
- datos de otros tenants.

Los errores públicos deben ser estructurados y sanitizados.

## Seguridad semántica

El sistema debe evitar transformar una acusación, interpretación o inferencia en un hecho afirmado. La precisión semántica es también un control de seguridad y reputación.

## Fuera de alcance

Este documento no prescribe un proveedor de identidad, sistema de secretos o mecanismo de cifrado concreto.
