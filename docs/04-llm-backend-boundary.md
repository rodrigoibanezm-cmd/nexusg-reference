# Frontera entre LLM y backend

## Principio central

NexusG separa interpretación semántica de ejecución controlada.

```text
LLM      = lenguaje, contexto, clasificación y narrativa
Backend  = autenticación, autorización, contratos, datos, cálculo, reglas, persistencia y evidencia
```

## Responsabilidades del LLM

El LLM puede:

- interpretar preguntas;
- proponer una capacidad formal;
- clasificar contenido dentro de una taxonomía permitida;
- resumir evidencia;
- relacionar contexto;
- redactar una respuesta;
- explicar resultados ya calculados.

## Responsabilidades del backend

El backend debe:

- autenticar al principal;
- resolver tenant y permisos;
- validar contratos;
- acceder a fuentes autorizadas;
- ejecutar consultas y cálculos;
- aplicar reglas y políticas versionadas;
- normalizar resultados;
- persistir señales y evidencia;
- registrar trazas;
- devolver errores estructurados.

## Qué no debe hacer el LLM

- administrar credenciales;
- decidir acceso a datos;
- inventar evidencia;
- modificar libremente el scope;
- reemplazar cálculos determinísticos;
- presentar inferencias como hechos;
- ejecutar escrituras fuera de contratos autorizados.

## Qué no debe hacer el backend

El backend no debe improvisar semántica abierta ni generar conclusiones narrativas no sustentadas.

Sí puede priorizar, recomendar o clasificar cuando esas decisiones están formalizadas mediante reglas, contratos y versiones controladas.

## Clasificación semántica

Cuando una fuente requiere interpretación cualitativa:

```text
contenido
→ contrato de clasificación
→ LLM
→ salida cerrada
→ validación backend
→ normalización
→ reglas derivadas
→ persistencia
```

La salida semántica puede conservarse para auditoría, pero no se considera válida hasta superar la validación del backend.

## Modalidad epistemológica

La narrativa debe conservar la naturaleza de cada afirmación:

- “el sistema registró” para hechos de fuente;
- “el cálculo indica” para resultados derivados;
- “una persona reporta” para declaraciones;
- “la clasificación interpreta” para lectura semántica;
- “se infiere” para inferencias;
- “se recomienda” para acciones propuestas.

## Regla final

El LLM amplía comprensión. No elimina las fronteras de control.
