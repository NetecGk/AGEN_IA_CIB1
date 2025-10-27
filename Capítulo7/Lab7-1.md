#  Evaluar el comportamiento de un modelo, uso de agentes, acciones y almacenamiento de registros de conversación

## Objetivo de la práctica:
Al finalizar la práctica, serás capaz de:

- Evaluar el comportamiento de un modelo en Azure AI Foundry mediante pruebas manuales y métricas de evaluación.
- Crear y configurar un agente contextualizado que genere archivos con datos estructurados y ejecute acciones (Code Interpreter).
- Revisar y auditar registros de conversación en Threads para asegurar trazabilidad y validar las acciones del agente.

## Diagrama del laboratorio 
El siguiente diagrama resume visualmente lo que realizarás a lo largo de la siguiente práctica. 

![diagrama1](../images/7Capitulo1Intro1.png)

## Duración aproximada:
- 60 minutos.

## Instrucciones 
Medir y evaluar el comportamiento de una aplicación que utiliza modelos de inteligencia artificial es fundamental para garantizar su seguridad, confiabilidad y alineación con los objetivos del negocio. Esto permite detectar desviaciones, sesgos, o comportamientos no deseados que podrían comprometer la integridad del sistema o la experiencia del usuario. Cuando se emplean agentes para ejecutar tareas específicas, la orquestación de múltiples agentes añade una capa de complejidad que debe ser cuidadosamente gestionada para evitar conflictos, redundancias o vulnerabilidades. Una supervisión continua y una evaluación rigurosa son esenciales para mantener el control sobre sistemas autónomos que toman decisiones o interactúan con datos sensibles.

En este laboratorio usarás Azure AI Foundry para probar manualmente un modelo de inteligencia artificial y observar su comportamiento en situaciones específicas. Crearás un agente contextualizado que actuará según los parámetros definidos, lo que garantiza que su respuesta sea coherente y alineada con los objetivos de la tarea. Este agente generará un archivo con los datos necesarios para una solicitud de devolución, asegurando que la información esté bien estructurada. Además, verificarás el registro de actividad en Threads, lo que te permitirá confirmar que el agente ha ejecutado correctamente cada paso y mantener trazabilidad sobre su desempeño.


### Tarea 1. Acceder al entorno del laboratorio.

**Paso 1.** Desde tu equipo accede al servicio de Escritorio remoto. La dirección IP y las credenciales será proporcionadas por tu insturctor. 

![labimage](../images/2Capitulo1Lab1.png)

![labimage](../images/2Capitulo1Lab2.png)

![labimage](../images/2Capitulo1Lab3.png)

---

**Paso 2.** En tu máquina virtual Windows, abre la ventana del navegador y accede a `ai.azure.com`.

![labimage](../images/7Capitulo1Lab1.png)

---

**Paso 3.** Inicia sesión con la cuenta proporcionada por tu instructor.

![labimage](../images/7Capitulo1Lab2.png)

### Tarea 2. Probar el comportamiento de un modelo de inteligencia artificial.

**Paso 1.** En una nueva pestaña del navegador, ingresa al siguiente vínculo. Este, mostrará un documento JSONL. 

Haz clic derecho en cualquier parte del documento en el navegador y selecciona la opción **Save as**.

![labimage](../images/7Capitulo1Lab3.png)

Echale un vistazo al archivo. Contiene entradas y salidas esperadas que probarán el funcionamiento del modelo. Lo saremos para confirmar que efectivamente el modelo conteste de una manera segura. 

---

**Paso 2.** Guarda el archivo en la carpeta **Downloads** con el nombre por defecto.

![labimage](../images/7Capitulo1Lab4.png)

---

**Paso 3.** Regresa a la pestaña del navegador donde tienes abierto Azure AI Foundry. En el menú lateral izquierdo, haz clic en **Evaluation**, en la sección Protect and govern.

Cambia a la pestaña **Manual evaluations**. Luego, haz clic en el botón **+ New manual evaluation**

![labimage](../images/7Capitulo1Lab5.png)

---

**Paso 4.** En la nueva ventana cambia el mensaje del sistema por: `Ayudar a los usuarios con consultas relacionadas con viajes, ofreciendo sugerencias, consejos y recomendaciones como un agente de viajes experto.`.

![labimage](../images/7Capitulo1Lab6.png)

---

**Paso 5.** En la sección inferior de ***Manual evaluation result***, haz clic en el botón **Import Test Data**.

![labimage](../images/7Capitulo1Lab7.png)

---

**Paso 6.** En la ventana emergente, haz clic en el botón **Upload file**.

![labimage](../images/7Capitulo1Lab8.png)

---

**Paso 7.** Selecciona el archivo JSONL que descargaste previamente y haz clic en **Open**.

![labimage](../images/7Capitulo1Lab9.png)

---

**Paso 8.** Una vez que el archivo se haya cargado, haz clic en el botón **Next**.

![labimage](../images/7Capitulo1Lab10.png)

---

**Paso 9.** Observa cómo se organizaron los datos en preguntas y respuestas esperadas. Baja al constado inferior de la ventana y en **Dataser mapping** configura los siguientes valores:

- Input: **Question**
- Expected response: **ExpectedResponse**.

Luego haz clic en **Add**.

![labimage](../images/7Capitulo1Lab11.png)

---

**Paso 10.** Debieron haberse cargado las preguntas y respuestas esperadas. Haz clic en el botón **Run** para iniciar la respuesta de parte del modelo.

![labimage](../images/7Capitulo1Lab12.png)

---

**Paso 11.** Una vez que el proceso haya finalizado, observa los resultados. Verás junto a la lista de preguntas y respuestas esperadas, las salidas generadas por el modelo.

Las tasas de evaluación aún están en 0%, esto es normal, dado que necesitamos realizar la evaluación manualmente. 

![labimage](../images/7Capitulo1Lab13.png)

---

**Paso 12.** Evalua manualmente la respuesta generada de cada una de las preguntas. Si es correcto, márcalas con el ícono del pulgar arriba.

![labimage](../images/7Capitulo1Lab14.png)

---

**Paso 13.** Si la respuesta generada no es correcta, márcala con el ícono del pulgar abajo.

![labimage](../images/7Capitulo1Lab15.png)

---

**Paso 14.** Una vez que hayas evaluado todas las respuestas, observa cómo las tasas y métricas de evaluación se actualizan automáticamente.

Puedes guardar o exportar los resultados. 

![labimage](../images/7Capitulo1Lab16.png)

### Tarea 3. Crear un agente contextualizado para generar un archivo con datos estructurados.

**Paso 1.** En el menú lateral izquierdo, haz clic en **Playgrounds**. Luego, haz clic en el botón **Try the Agents playground**.

![labimage](../images/7Capitulo1Lab19.png)

---

**Paso 2.** En la nueva ventana, selecciona el recurso que creaste en el laboratorio pasado y luego haz clic en **Let's go**.

![labimage](../images/7Capitulo1Lab20.png)

---

**Paso 3.** En la sección de **Instructions**, define el siguiente mensaje:

`Eres un asistente de IA para gastos corporativos. Respondes preguntas sobre gastos basándote en los datos de la política de gastos. Si un usuario desea presentar una reclamación de gastos, obtienes su dirección de correo electrónico, una descripción de la reclamación y el importe a reclamar, y escribes los detalles de la reclamación en un archivo de texto que el usuario puede descargar.`

Lee con detenimiento las instrucciones que le estás dando, son clave para comprender el propósito del agente en este laboratorio. 

![labimage](../images/7Capitulo1Lab21.png)

---

**Paso 4.** En la parte inferior encontrarás una sección llamada **Knoledge** con un botón **+Add**, haz clic sobre este. 

![labimage](../images/7Capitulo1Lab22.png)

---

**Paso 5.** Hay distintos lugares desde los cuales contextualizar el agente, en nuestro caso usaremos el archivo que descargaste previamente. Para esto haz clic en la opción **Files**.

![labimage](../images/7Capitulo1Lab23.png)

---

**Paso 6.** En la ventana emergente, haz clic en el botón **Select local files**.

![labimage](../images/7Capitulo1Lab24.png)

---

**Paso 7.** Abre otra pestaña en el navegador, y acceder al siguiente link. Allí encontrarás un documento con las políticas de solicitud de devolución de gastos. Échale un vistazo, y luego descargalo haciendo clic en el botón **Download File** del costado superior. 

`https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-agents/main/Labfiles/01-agent-fundamentals/Expenses_Policy.docx`

![labimage](../images/7Capitulo1Lab25.png)

---

**Paso 8.** Regresa a la pestaña del agente en Azure AI Foundry. Selecciona el archivo que acabas de descargar y haz clic en **Open**.

![labimage](../images/7Capitulo1Lab26.png)

---

**Paso 9.** Ahora verás el documento cargado en estatus **Not Started**. Haz clic en **Upload and save** y verás cómo cambia de estatus a **Uploaded**.

![labimage](../images/7Capitulo1Lab27.png)

---

**Paso 10.** Nuevamente, en el menú lateral izquierdo busca la sección **Actions** y haz clic en el botón **+ Add**.

![labimage](../images/7Capitulo1Lab28.png)

---

**Paso 11.** Puedes realizar acciones a partir de código generado por las instrucciones del agente, una API específica o con Azure Logic Apps. 

Si recuerdas, en el paso 3 de la tarea actual, configuraste las instrucciones para que el agente pudiera escribir los detalles de la reclamación en un archivo de texto que el usuario puede descargar. Esto lo hará una función de Python generada por dicha instrucción.

Haz clic en **Code Interpreter**.

![labimage](../images/7Capitulo1Lab29.png)

---

**Paso 12.** En la nueva ventana, simplemente haz clic en **Save**.

![labimage](../images/7Capitulo1Lab30.png)

### Tarea 4. Probar el agente

**Paso 1.** En la parte inferior de la ventana del agente, encontrarás un cuadro de texto para ingresar mensajes.

Ingresa el siguiente mensaje:

`Cuánto es el valor máximo que puedo solicitar en devoluciones?`

![labimage](../images/7Capitulo1Lab31.png)

---

**Paso 2.** Observa cómo el agente responde correctamente basándose en el documento de políticas que le proporcionaste.

Ahora, solicita una devolución. Ingresa el siguiente mensaje:

`Me gustaría presentar un reclamo por una comida.`

![labimage](../images/7Capitulo1Lab32.png)

---

**Paso 3.** El agente te pedirá más detalles para proceder. Responde de la siguiente manera:

`Mi correo es <Tu_correo>, desayuné con un cliente y me costó $20 USD`

![labimage](../images/7Capitulo1Lab33.png)

### Resultado final

El agente activará **code interpreter** y generará un archivo descargable con los datos de la solicitud de devolución.

![labimage](../images/7Capitulo1Lab34.png)

Abre el documento que debió quedar en **Downloads** y observa el resultado. 

![labimage](../images/7Capitulo1Lab35.png)
![labimage](../images/7Capitulo1Lab36.png)

---

Regresa al navegador donde tienens abierto Azure AI Foundry y dirígete a **Agents** del menú lateral izquiero. Allí seleccionarás la pestaña My **threads**

![labimage](../images/7Capitulo1Lab37.png)

En dicha pestaña está el registro de las conversaciones que tus usuarios han cruzado con el agente. Puedes usarlo para investigaciones, auditoria, cumplimiento o cualquier otro requerimiento.

![labimage](../images/7Capitulo1Lab38.png)
