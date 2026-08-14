# Team Charter — Plataforma Web de Aprendizaje de Prompt Engineering

**Materia:** Taller de Sistemas Inteligentes — LAB_01
**Proyecto:** Plataforma interactiva y gamificada para el aprendizaje de Prompt Engineering (tutor virtual con LLM as a Judge)

## Integrantes y disponibilidad

| Integrante | Responsabilidad inicial | Disponibilidad | Restricción |
|---|---|---|---|
| Leonardo Delgado | Arquitectura / Despliegue | Sábados y domingos | Prácticas preprofesionales + clases toda la semana |
| Samuel Villca | Backend / IA (LLM as a Judge) | Sábados y domingos | Prácticas preprofesionales + clases toda la semana |
| Marvin Mollo (Pepe) | Frontend / Producto | Sábados y domingos | Prácticas preprofesionales + clases toda la semana |

> Los 3 integrantes trabajan también algunos feriados nacionales. Al ser un equipo de 3, cada uno cubre más de una responsabilidad según necesidad (ver tabla de responsabilidades del laboratorio).

## Canales y tiempos de respuesta

- **ClickUp:** tareas, responsables y evidencia.
- **WhatsApp/Discord:** coordinación rápida, no decisiones finales.
- **GitHub Issues:** defectos técnicos y bloqueos reproducibles.
- **Tiempo de respuesta normal:** 24 horas.
- **Bloqueo crítico:** se etiqueta en ClickUp y se notifica al canal del equipo.

## Revisión de PR

- Ningún cambio a `main` sin PR.
- Cada PR debe incluir: objetivo, archivos modificados, prueba ejecutada y evidencia.
- Al menos 1 integrante revisa antes de fusionar.
- No se aprueban PR con secretos, credenciales (API keys de OpenAI/Gemini/Claude, claves de Supabase) o tests fallidos.
- Las decisiones de IA asistida se declaran en el PR.

## Manejo de bloqueos

Formato de registro:
- **Bloqueo:** qué impide avanzar
- **Inicio:** fecha/hora
- **Impacto:** qué entrega está en riesgo
- **Intentos:** qué se intentó
- **Siguiente acción:** qué se hará

Ejemplo:
```
Bloqueo: no se cuenta con crédito/API key para el LLM evaluador.
Inicio: [fecha], [hora].
Impacto: no se puede probar el módulo de "LLM as a Judge".
Intentos: solicitud de acceso al docente, comparación de precios entre Gemini API,
Amazon Bedrock y Grok.
Siguiente acción: usar la opción más económica disponible (Gemini, Bedrock o Grok)
para el prototipo y registrar el riesgo en ClickUp.
```

## Reglas de integridad y uso de IA

- Se permite IA (Claude, ChatGPT, Copilot, etc.) para análisis, diseño, código, pruebas y documentación.
- El LLM evaluador de la plataforma ("LLM as a Judge") se implementará con Gemini API, Amazon Bedrock o Grok, priorizando la opción de menor costo; la decisión final se registra en un ADR.
- No se ingresan datos personales de estudiantes, secretos ni credenciales de API en prompts a herramientas externas.
- Todo prompt o código generado debe revisarse, probarse y entenderse por el equipo antes de integrarse.
- El PR declara qué se generó con IA y qué verificaciones se ejecutaron.
- La responsabilidad final del sistema —incluyendo la lógica de evaluación de prompts que ofrece la plataforma— es del equipo, no de la herramienta.

## Definition of Done inicial

Una tarea se considera terminada cuando:
- Tiene criterio de aceptación cumplido.
- Incluye evidencia enlazada en ClickUp.
- El cambio está en GitHub con commit/PR.
- No introduce secretos ni datos sensibles (API keys, credenciales de Supabase).
- Si modifica código, ejecuta pruebas o justifica por qué no aplican.
- Si usa IA, declara uso y verificación.
