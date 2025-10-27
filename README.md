<img src="images/neteclogo.png" alt="logo" width="300"/>

# IA Generativa en Ciberseguridad Avanzada

## Plataforma de laboratorios

Te damos la bienvenida a la **plataforma de laboratorios** del curso **IA Generativa en Ciberseguridad Avanzada**. Aquí podrás explorar diferentes tecnologías a través de prácticas guiadas. ¡Desarrolla tus habilidades y lleva tus conocimientos al siguiente nivel!

## Lista de laboratorios

Cada uno de estos laboratorios está diseñado para ofrecerte una experiencia práctica. Haz clic en los enlaces para comenzar.

### [Práctica 1. Crea agentes en el Copilot Studio de Teams](Capítulo1/Lab1-1.md) 
- **Descripción**: Identificar el uso de Copilot Studio, las limitantes  y las características de seguridad de los agentes clásicos de Copilot Studio en Microsoft Teams.
- ⏱️ **Duración estimada**: 35 min.

### [Práctica 2. Nombre de la práctica](Capítulo1/Lab1-2.md)
  - **Descripción**: Crear y configurar un agente personalizado en Copilot Studio integrando datos empresariales desde SharePoint y ajustando sus respuestas mediante instrucciones específicas. Configurar acciones automatizadas usando conectores, como el envío de correos electrónicos a través de Outlook, y establecer reglas para asegurar el flujo seguro de información.
- ⏱️ **Duración estimada**: 35 min.

### [Práctica 3. Desplegar MCP de referencia local, cargar dataset de ejemplo y ejecutar consultas seguras](Capítulo2/Lab2-1.md)
 - **Descripción**: Desplegar un servidor MCP de referencia local, integrando un modelo de lenguaje desde Azure AI Foundry y configurando el entorno de ejecución en Ubuntu. Implementar políticas de seguridad y autenticación, incluyendo la generación y uso de certificados digitales y una autoridad certificadora local. Ejecutar consultas seguras sobre el dataset cargado, utilizando Postman y verificando la comunicación cifrada mediante mTLS y roles definidos.
- ⏱️**Duración estimada**: 60 min.

### [Práctica 4. Desplegar un LLM Gateway local (proxy), añadir una regla simple de inspección y probar rutas a provider mock](Capítulo3/Lab3-1.md) 
 - **Descripción**: Desplegar un LLM Gateway local que inspeccione prompts, enrute solicitudes a proveedores (Azure y mock) y exponga un endpoint de entrada. Configurar reglas de inspección y ruteo (regex y palabras clave) para bloquear intentos de prompt injection y redirigir prompts según condiciones definidas. Generar y revisar logs de eventos con request ID, simular su envío a un SIEM y validar el comportamiento mediante peticiones curl/jq.
 - ⏱️ **Duración estimada**: 40 min.

### [Práctica 5. Crear workflow de caza de amenazas en n8n](Capítulo4/Lab4-1.md)
- **Descripción**: Configurar un flujo de caza de amenazas en n8n que incluya un Webhook de entrada, nodos HTTP Request, Set y Code para recopilar y enriquecer eventos desde el servidor Ubuntu. Normalizar y evaluar riesgos usando lógica personalizada (nodo Code) y reglas condicionales (nodo IF) para asignar puntajes y clasificar niveles de riesgo. Orquestar acciones automáticas y realizar pruebas: enviar bloqueos al servicio de mitigación (/context/block), registrar eventos (/logs) y validar el flujo con Postman.
- ⏱️ **Duración estimada**: 60 min.

### [Práctica 6. Construir pipeline básico de ingestión → indexación → consulta RAG (usar datasets de prueba y validar sanitización)](Capítulo5/Lab5-1.md)
- **Descripción**: Construir un pipeline de ingestión, indexación y consulta RAG usando Azure AI Foundry y Azure Cognitive Search; subir y vectorizar documentos, crear índices y desplegar modelos de embedding y generación para consultas integradas; y validar la sanitización e integridad de datos mediante algoritmos hash y simular ataques para comprobar detección y bloqueo.
- ⏱️**Duración estimada**: 60 min.

### [Práctica 7. Simulación de un prompt injection y aplicación el playbook de respuesta](Capítulo6/Lab6-1.md) 
 - **Descripción**: Simular un ataque de prompt injection contra una aplicación autenticada por Entra ID y observar su impacto en la interacción con el modelo; configurar filtros de contenido personalizados en Azure AI Foundry (content filters, blocklists y protección PII) para bloquear y controlar prompts y respuestas; y validar el comportamiento de seguridad ejecutando la aplicación, probando prompts maliciosos y legítimos, y verificando el bloqueo y registro de eventos.
 - ⏱️ **Duración estimada**: 60 min.

### [Práctica 8. Evaluar el comportamiento de un modelo, uso de agentes, acciones y almacenamiento de registros de conversación](Capítulo7/Lab7-1.md)
- **Descripción**: Evaluar el comportamiento de un modelo en Azure AI Foundry mediante pruebas manuales y métricas de evaluación, crear y configurar un agente contextualizado capaz de generar archivos con datos estructurados y ejecutar acciones mediante Code Interpreter, y revisar los registros de conversación en Threads para asegurar la trazabilidad y validar que el agente haya actuado correctamente.
- ⏱️ **Duración estimada**: 60 min.

---

## 📬 **Contacto y más información**

Si tienes alguna pregunta o necesitas más detalles, no dudes en [contactarnos](mailto:soporte@netec.com). También puedes encontrar más recursos en nuestra [página](https://netec.com).

---

¡Gracias por visitar nuestra plataforma! No olvides revisar todos los laboratorios y comenzar tu viaje de aprendizaje hoy mismo.
