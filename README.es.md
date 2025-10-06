# Repositorio de aprendizaje de Agentic Workflows

Este repositorio acompaña el programa "Introduction to Agentic Workflows with Python and OpenAI". Reúne demostraciones ejecutables en Python y material de apoyo que muestran diferentes patrones de agentic workflows, desde encadenamientos simples hasta orquestación con LLMs.

La mayoría de los ejemplos usan el SDK `openai` y esperan un archivo `.env` con `OPENAI_API_KEY` (y opcionalmente `OPENAI_BASE_URL`). Puedes instalar las dependencias compartidas con:

```powershell
pip install -r requirements.txt
```

## Guía carpeta por carpeta

### `Welcome to Introduction to Agentic Workflows with Python and OpenAI`

**Scripts de Python**
- `main.py` &mdash; Compara una base de conocimiento hardcoded con un agente impulsado por OpenAI para preguntas de program management, resaltando cómo los LLMs pueden aumentar la lógica tradicional.
- `demo.py` &mdash; Muestra los paralelos entre funciones basadas en palabras clave y agentes de OpenAI al responder consultas de ejemplo con ambos enfoques.

**Notebooks**
- _No hay notebooks en esta carpeta._

### `Introduction to Implementing Agentic Workflows with Python`

**Scripts de Python**
- `main.py` &mdash; Conecta agentes reutilizables para obtener y procesar datos simulados de usuarios, ilustrando cómo construir un workflow sencillo de estilo productivo.
- `demo.py` &mdash; Ejecuta un workflow de "information processing" (research → fact check → summarize) usando agentes ligeros de demostración.
- `fastchecker.py` &mdash; Extiende el workflow anterior con flagging de palabras clave para mostrar cómo pueden evolucionar las responsabilidades de un agente.

**Módulos**
- `workflow_agents/agent_definitions.py` &mdash; Define la clase base `Agent` y las implementaciones `DataFetchingAgent` y `DataProcessingAgent` usadas por `main.py`.
- `workflow_agents/__init__.py` &mdash; Marcador vacío del paquete para el módulo auxiliar.

**Notebooks**
- _No hay notebooks en esta carpeta._

### `AI Agents and Agentic Workflows`

**Scripts de Python**
- `main.py` &mdash; Compara reglas deterministas de planificación de workouts con un agente basado en LLM que razona sobre perfiles de usuario y produce schedules en JSON.
- `demo-no-llm.py` &mdash; Ejemplos base de procesamiento determinista vs. agentic de tareas sin llamadas a LLM.
- `demo-llm.py` &mdash; Amplía la base con un LLM "strategy advisor" que elige entre ejecución por prioridad o por eficiencia.

**Notebooks**
- _No hay notebooks en esta carpeta._

### `Prompt Chaining Workflow`

**Scripts de Python**
- `main.py` &mdash; Construye una cadena de cuatro agentes para optimización de refinería (analysis → planning → market research → production optimization) impulsada por chat completions de OpenAI.
- `demo.py` &mdash; Cadena mínima researcher → writer que muestra cómo las salidas intermedias moldean los prompts posteriores.

**Notebooks**
- _No hay notebooks en esta carpeta._

## Recursos adicionales

Las demás carpetas de nivel superior contienen principalmente lecciones en video y archivos de subtítulos (zip) que acompañan a los ejemplos en Python. Actualmente el repositorio no incluye notebooks de Jupyter.

## Ejecución de los ejemplos

1. Crea un entorno virtual (opcional) e instala las dependencias con `pip install -r requirements.txt`.
2. Agrega un archivo `.env` en la raíz del proyecto con tu `OPENAI_API_KEY` (y un `OPENAI_BASE_URL` si usas un endpoint personalizado).
3. Ejecuta el script que necesites con `python ruta\al\script.py`. Los scripts que llaman al OpenAI API te avisarán si la API key falta.

¡Disfruta explorando los diferentes patrones para construir agentic workflows!
