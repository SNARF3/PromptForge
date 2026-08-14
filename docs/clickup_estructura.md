# Estructura de ClickUp — Plataforma Web de Aprendizaje de Prompt Engineering

**Materia:** Taller de Sistemas Inteligentes — LAB_01
**Proyecto:** Plataforma interactiva y gamificada para el aprendizaje de Prompt Engineering (tutor virtual con LLM as a Judge)

## Listas

| Lista | Uso típico en este proyecto |
|---|---|
| **Discovery** | Definición del problema, Product Goal, priorización de retos (Zero-Shot, Few-Shot, Chain of Thought, Role-Playing) |
| **Data** | Datasets de ejemplo por reto, "resultados ideales" de referencia para comparación semántica, licencias y sensibilidad |
| **Architecture** | Diagramas de arquitectura (React + Node.js/Express + Supabase), ADRs, decisión de proveedor de LLM (Gemini API vs Amazon Bedrock vs Grok) y de nube de despliegue (Azure vs AWS) |
| **Build** | Implementación del Playground, API de evaluación, integración del LLM as a Judge, dashboard del docente |
| **QA** | Pruebas del evaluador de prompts, pruebas de la API, pruebas de autenticación y persistencia de progreso |
| **Deploy** | Despliegue en Azure o AWS (según ADR), configuración de Supabase en producción |
| **Risk** | Costos/límites de la API del LLM elegido (Gemini/Bedrock/Grok), precisión del evaluador, bloqueos de acceso a datos o credenciales, disponibilidad limitada del equipo (fines de semana + feriados) |

> Cada tarea se crea o se mueve en la lista que corresponde, pero siempre debe tener dueño, sprint, criterio de aceptación y enlace a evidencia.

## Campos obligatorios en cada tarea

- Sprint
- Dueño
- Criterio de aceptación
- Enlace a evidencia (commit/PR/documento)
- Riesgo asociado
- Estado de bloqueo

## Ejemplo de tarea

```
Título: Implementar evaluador LLM as a Judge para retos Zero-Shot
Lista: Build
Sprint: Sprint 1
Dueño: [Nombre]
Criterio de aceptación: la API recibe el prompt del estudiante, lo envía al LLM
evaluador y devuelve una puntuación de eficiencia junto con sugerencias de mejora,
con pruebas automatizadas pasando.
Evidencia: https://github.com/[equipo]/[repo]/blob/main/docs/evaluator.md
Riesgo asociado: costo y latencia de las llamadas a la API del LLM externo
```

**Regla:** una tarea sin criterio de aceptación es solo una intención.
