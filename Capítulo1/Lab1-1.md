#  Crea agentes en el Copilot Studio de Teams

## Objetivo de la práctica:
Al finalizar la práctica, serás capaz de:
- Identificar el uso de Copilot Studio en Teams
- Identificar las limitantes en Copilot Studio en Teams
- Identificar las caracteristicas de seguridad de los agentes clásicos de Copilot Studio en Teams

## Diagrama del laboratorio 
El siguiente diagrama resume visualmente lo que realizarás a lo largo de la siguiente práctica. 

![diagrama1](../images/1Capitulo1Intro1.png)

## Duración aproximada:
- 35 minutos.

## Instrucciones 
La creación de agentes clásicos en Microsoft Teams consiste en configurar bots que interactúan con los usuarios mediante mensajes, comandos o tarjetas adaptativas. Estos agentes se desarrollan utilizando herramientas como el Microsoft Bot Framework y se integran a través de Azure Bot Services. Su función principal es automatizar tareas, responder preguntas frecuentes o facilitar procesos dentro del entorno colaborativo de Teams, utilizando flujos de conversación predefinidos y conectores a servicios externos.

En el siguiente ejercicio, diseñarás un agente capaz de interactuar contigo en temas personalizados. Este agente podrá ejecutar acciones automáticamente, como enviar correos electrónicos, lo que te permitirá experimentar cómo se construyen soluciones inteligentes que mejoran la productividad y la comunicación dentro de Teams.


### Tarea 1. Acceder a Copilot Studio en Teams.

**Paso 1.** Ingresar a Teams

Ingresa en tu navegador a [Mircosoft Teams](https://teams.microsoft.com/) usando el siguiente link: `https://teams.microsoft.com/`, y usa las credenciales otorgadas por el instructor. Si aparece alguna ventana emergente o de bienvenida ciérrala. 

![LabImage](../images/1Capitulo1Lab1.png)

---

**Paso 2.** Instala Copilot Studio

En el panel izquierdo, haz clic en Apps y luego usa la barra de búsqueda para encontrar `Microsoft Copilot Studio`. Al encontrarlo selecciona el botón ***Add***.

![LabImage](../images/1Capitulo1Lab2.png)

---

**Paso 3.** Verifica los permisos
En la ventana emergente ubica la pestaña ***Permisos*** y revisa los permisos listados, una vez hecho esto, haz clic en el botón **Add** y posteriormente en el botón **Open** de la ventana de confirmación de aplicación añadida.

![LabImage](../images/1Capitulo1Lab3.png)

![LabImage](../images/1Capitulo1Lab4.png)

---

**Paso 4.** Verificación de interfaz web

Seguramente recibirás una recomendación para el uso de la app de escritorio, por propósitos de nuestro laboratorio continuaremos en la interfaz web seleccione "Show the app anyway". 

![LabImage](../images/1Capitulo1Lab5.png)

### Tarea 2. Crear un equipo en Teams

**Paso 1.** Para poder crear un asistente en Teams, antes debes elegir o crear un equipo. Regresa a la opción de chat del costado izquierdo, selecciona "See all your teams" vera al centro en la sección **"Your Teams and channels"** un listado de sólo un equipo, después en el apartado superior derecho haz clic en **Create team ▾** y luego seleccionan **create team**.


![LabImage](../images/1Capitulo1Lab8.png)

---

**Paso 2.** Crea un nuevo equipo configurando los siguientes parámetros:

* **Team name:** Netec(xy) **cambie la xy por su número de usuario que se le asigno**
* **First channel name:** General

Y luego haz clic en el botón **Create**.

En este caso, vamos a omitir los miembros al equipo, por lo cual, en la siguiente ventana haz clic en **Skip**.

![LabImage](../images/1Capitulo1Lab9.png)
![LabImage](../images/1Capitulo1Lab10.png)

### Creación del agente


**Paso 1.** Regresa nuevamente a la aplicación **Copilot Studio** que previamente añadiste a Mircosoft Teams.

Abre la interfaz haciendo clic en el botón **Start now**.

Nota: si aparece la ventana emergente  "This app may have issues in the web version of Teams" seleccione "Show the app anyway"


![LabImage](../images/1Capitulo1Lab6.png)

---

**Paso 2.** Verás una ventana que te solicita seleccionar un equipo para iniciar, selecciona el equipo que creaste previamente: **Netec(xy)**. Esto abrirá una ventana donde te dice que se está creando el chatbot de clic al botón **Continue**, después otro clic en **Close**.

![LabImage](../images/1Capitulo1Lab11.png)
![LabImage](../images/1Capitulo1Lab12.png)

---
**Paso 3.** En la interfaz de Microsoft Copilot seleccione la pestaña **Copilots**, después observe en el costado izquierdo debajo de **"My copilots"** debe estar el nombre de su equipo **Netec(xy)**, seleccionado este equipo que creo de clic al boton **+New copilot**.


![LabImage](../images/1Capitulo1Lab13.png)

---

**Paso 4.** Lo primero que vamos a hacer es editar el idioma del agente, haz clic en **Edit language**, y luego busca y selecciona **Spanish (es-ES)**.

![LabImage](../images/1Capitulo1Lab14.png)

---

**Paso 5.** En la sección **Name** ingrese NetecBot(xy) **cambie la xy por su número de usuario que se le asigno** como nombre y de clic al botón **Create**.

![LabImage](../images/1Capitulo1Lab15.png)



**Paso 7.** En la ventana emergente escribe el siguiente mensaje: `Hola`, y presiona Enter. La respuesta generada hace parte de un tema preconfigurado, haz clic sobre la respuesta del agente en la ventana del **Test bot**, esto abrirá el tema del que se devolvió la respuesta, en este caso **¿Qué tal?**.

![LabImage](../images/1Capitulo1Lab17.png)

---

**Paso 8**. Observa que el tema tiene un conjunto de mensajes predefinidos que puedes editar, eliminar o añadir nuevos mensajes.

En la sección del Tema **Message** elimine el mensaje que esta por default después de clic en **+Add**  y seleccione la opción Message variation después cambiarás la respuesta preconfigurada por: ¡Hola! Soy NetecBot, su asistente virtual. Puedo ayudar con preguntas de las políticas de seguridad de la empresa.

finalmente de clic en el botón **Save**.

![LabImage](../images/1Capitulo1Lab18.png)

---

**Paso 9.** Nuevamente escribe `Hola`, y verifica que la respuesta generada sea la misma que configuraste previamente. 

![LabImage](../images/1Capitulo1Lab19.png)

---

**Paso 10.** Ahora vamos a crear un nuevo tema, cierra la ventana del **Test Bot**, selecciona la opción **Topics** del costado izquierdo y haz clic en el botón **+ New topic** > **From blank**.

![LabImage](../images/1Capitulo1Lab20.png)

---

**Paso 11.** Para editar el *Trigger* de clic en **Edit** luego Configure los siguientes parámetros:
* **Add phrases:** políticas de seguridad, seguridad, normas de seguridad, etc.

Luego cierre la ventana de las **Phrases**.

![LabImage](../images/1Capitulo1Lab21.jpg)

---

**Paso 12.** Agrega un nuevo nodo conversacional de **Send a message** y en la sección **Messages**, escribe: `Actualmente le puedo dar apoyo con las siguiente políticas de seguridad`. 

Luego haz clic nuevamente en la cruz **+** y selecciona nuevamente **Send a message**.

![LabImage](../images/1Capitulo1Lab22.png)

---

**Paso 13.** En la sección **Messages**, copie y pegue las siguiente opciones:

```markdown
[Política de Seguridad de la Información](https://aznetecgroup29-my.sharepoint.com/:w:/g/personal/azstudent29_aznetecgroup29_onmicrosoft_com/ESEo-WtwPQ5InbSjhodc08wBBeXHeN1UVLCiJOAcLO_slg?e=Hmo9R0)
[Política de Uso Aceptable de Tecnología](https://aznetecgroup29-my.sharepoint.com/:w:/g/personal/azstudent29_aznetecgroup29_onmicrosoft_com/EawxZNlG-oVNiYFe_dGPSTYBT1miyw1CkvGI-pHoUbuifg?e=mqPvG5)
[Política de Respaldo y Recuperación](https://aznetecgroup29-my.sharepoint.com/:w:/g/personal/azstudent29_aznetecgroup29_onmicrosoft_com/Edawx6RgH29ArSpN2_O0QaIB8Xi58JWgSpvdYBx5HxJQrw?e=OTsr1y)
[Política de Identidad y Acceso](https://aznetecgroup29-my.sharepoint.com/:w:/g/personal/azstudent29_aznetecgroup29_onmicrosoft_com/Ec4T0DMUQWlHtIeyOgljpGkBfj_NLJJjCE2mbD73Dy_05Q?e=wgDI98)
[Política de Concientización y Capacitación en Seguridad](https://aznetecgroup29-my.sharepoint.com/:w:/g/personal/azstudent29_aznetecgroup29_onmicrosoft_com/EdPAfbokR5RIoah6jiGVGGgBRA3w8AP7kZN1jS9H0hebPw?e=hmpft9)
```

 Cada opción, que se agrego tiene un vínculo usando **Markdown**. Los vínculos fueron los siguientes:

 | Opción | Vínculo |
| --- | --- |
| Política de Seguridad de la Información | https://aznetecgroup29-my.sharepoint.com/:w:/g/personal/azstudent29_aznetecgroup29_onmicrosoft_com/ESEo-WtwPQ5InbSjhodc08wBBeXHeN1UVLCiJOAcLO_slg?e=Hmo9R0 |
| Política de Uso Aceptable de Tecnología | https://aznetecgroup29-my.sharepoint.com/:w:/g/personal/azstudent29_aznetecgroup29_onmicrosoft_com/EawxZNlG-oVNiYFe_dGPSTYBT1miyw1CkvGI-pHoUbuifg?e=mqPvG5 |
| Política de Respaldo y Recuperación | https://aznetecgroup29-my.sharepoint.com/:w:/g/personal/azstudent29_aznetecgroup29_onmicrosoft_com/Edawx6RgH29ArSpN2_O0QaIB8Xi58JWgSpvdYBx5HxJQrw?e=OTsr1y |
| Política de Identidad y Acceso | https://aznetecgroup29-my.sharepoint.com/:w:/g/personal/azstudent29_aznetecgroup29_onmicrosoft_com/Ec4T0DMUQWlHtIeyOgljpGkBfj_NLJJjCE2mbD73Dy_05Q?e=wgDI98 |
| Política de Identidad y Acceso | https://aznetecgroup29-my.sharepoint.com/:w:/g/personal/azstudent29_aznetecgroup29_onmicrosoft_com/EdPAfbokR5RIoah6jiGVGGgBRA3w8AP7kZN1jS9H0hebPw?e=hmpft9 |



**Paso 14.** Debajo del mensaje hacemos nuevamente clic en **+** y selecciona **Ask a question**.

![LabImage](../images/1Capitulo1Lab26.png)

---

**Paso 15.** Configura la pregunta con los siguientes parámetros:
* **Enter a message:** ¿Quieres que te envíe las políticas por correo electrónico?
* **Identify** Booleano
* **Save user response as**: Haz clic en el nombre ***Var1***, y luego configura el nombre a `Decisión`, cierra la ventana de **Propiedades de variables**.

![LabImage](../images/1Capitulo1Lab27.png)

---

**Paso 16.** Haz clic en el botón **+** debajo de la pregunta y selecciona **Add a condition**.

![LabImage](../images/1Capitulo1Lab28.png)

---

**Paso 17.** Configura la condición  con los siguientes parámetros:
* Select a Variable: `Decisión`
* Valor lógico **is equal to**
* Enter or select a value: **true**

![LabImage](../images/1Capitulo1Lab29.png)

---

**Paso 18.** En la rama **If true**, haz clic en el botón **+** y selecciona **Ask a question**.

---

**Paso 19.** Configura la pregunta con los siguientes parámetros:
* **Enter a message:** Selecciona la política
* **Identify:** Multiple choice options 
* **Options for user:** de clic en **New option** para ir agregando cada una de estas opciones ir dando Enter cada que agrega una opción; Política de Seguridad de la Información, Política de Concietización y capacitación, Política de Identidad y acceso.
* ***Save user response as:** `Respuesta`, para cambiar este nombre tiene que dar doble clic en *Var1* se abre la ventana emergente y puede ahora si cambiar el nombre, despues de cambiar el nombre cierre la ventana emergente.


**Nota:** ***Para este ejemplo sólo agregaremos esas tres***

![LabImage](../images/1Capitulo1Lab33.png)


**Paso 20.** desplazarse hacia abajo  y debajo de la condición de **Politica de Seguridad de la información** de clic en ***+* para agregar otro nodo
-Una vez agregado el nodo  seleccione **Variable management** luego  seleccione **{X} Set a variable value**.

![LabImage](../images/1Capitulo1Lab33.1.png)

**Paso 19.** Configura  en *set variable value* los siguientes parámetros:
* **Set variable:** seleccione Select a variable se abrira una ventana emergente despues en esa ventana seleccione **Create a new variable**. se creara una variable
 de nombre *Var1* de clic en esta nombre y renombrela a 'respuestaString'
* **To value:**  de clic en los puntos suspensivos para editar **...** despues en la ventana emergente seleccione la pestaña **Formula** e ingrese lo siguiente **Text(Topic.Respuesta)**  despues de colocar la formula seleccione el boton **Insertar** la configuración final de la variable quedara  como se muestra en la imagen.

  ![LabImage](../images/1Capitulo1Lab33.2.png)

**Paso 20.** Agrega un nodo debajo de tipo  **Ask a question** debajo de la variable que secreo en el paso anterior .


**Paso 21.** Configura la pregunta con los siguientes parámetros:

* **Formular una pregunta** Por favor, ingresa tu correo electrónico.
* **Identify** seleccione Email.
* **Save user response as:**: Haz clic  en **Var1** y renombre la variable a `Correo`, cierra la ventana de **Propiedades de variables**.

![LabImage](../images/1Capitulo1Lab33.4.png)

---

**Paso 22.** Agrega un nodo debajo de la  pregunta **Por favor, ingresa tu correo electrónico**.
seleccione **Add a tool** seleccione la pestaña **Tool** despues en la opcion que tiene un icono de un rayo seleccione **Add a tool** Busque y seleccione **Send an email (V2)** nota:este tiene que ser de office 365 Outlook. despues seleccione en **Connection**  Not connected para que se abra la opcion de **Create new connection** seleccione esta opción, despues de clic en **Create**   coloque sus credenciales y de clic **Add to agent**  en **X**.

***Nota**El paso anterior solo es para agregar una conexión este no agregara un nodo.*

**Paso 22.** Ahora si vamos a agregar un nodo debajo de la  pregunta **Por favor, ingresa tu correo electrónico**. seleccione **+** seleccione **Add a tool** seleccione la pestaña **Tool** despues en la opcion  **Send an email (V2)**

**Paso 23.** En el nodo agregado reciente mente configure los siguientes parámetros:
* Seleccione **+Set value**  para agregar  To, Subject y Body para cada uno de estos valores configure los siguiente:
* To: correo
* Subject:respuestaString
* Body: reemplazalo por el siguiente mensaje estático:

>`¡Hola!`
>
>`De acuerdo a tu solicitud, a continuación envío la ruta donde se encuentran las políticas de seguridad, si no tienes acceso no dudes en comunicarte con tu administrador.`
>
>`https://aznetecgroup29-my.sharepoint.com/:f:/g/personal/azstudent29_aznetecgroup29_onmicrosoft_com/EjiYFXC_g45Hg2xzfil_dZwBrJMBhxYS462pMXtWDfE9RQ?e=RDqEpO`
>
>`Saludos`

![LabImage](../images/1Capitulo1Lab33.7.png)

---
* La configuración final debe de quedar como se puestra en la imagen siguiente:


**Paso 20.** Haz clic en el botón **+** debajo de la rama para la opción ***Política de Seguridad de la Información*** y selecciona **Llamar a una herramienta**. Luego, selecciona **Crea un flujo**.

![LabImage](../images/1Capitulo1Lab36.png)

---

**Paso 21.** Esto abrirá un conjunto de plantillas de Power Automate. Tómate un momento para verificar algunas, y luego selecciona **Enviar un mensaje de correo electrónico de Outlook**. Otorga permisos al conector Office 365 Outlook, haciendo clic en **Iniciar sesión**

![LabImage](../images/1Capitulo1Lab37.png)
![LabImage](../images/1Capitulo1Lab382.png)

---

**Paso 22.** El flujo prácticamente está creado, sólo debemos hacer algunos ajustes. Haz clic en la acción: **Send an email (V2)**

![LabImage](../images/1Capitulo1Lab38.png)



**Paso 24.** En la acción **Return value(s) to Power Virtual Agents** Elimina **Boby**

![LabImage](../images/1Capitulo1Lab383.png)

---

**Paso 25.** En el trigger **Power Virtual Agents** Elimina **Boby**.

![LabImage](../images/1Capitulo1Lab384.png)

---

**Paso 26.** Haz clic en el botón **Guardar**, para guardar tu flujo automatizado.

![LabImage](../images/1Capitulo1Lab39.png)

---



**Paso 29.** Ahora sí, haz clic en el botón **+** debajo de la pregunta anterior y selecciona **Llamar a una herramienta**. Luego, selecciona el flujo que acabas de crear.

![LabImage](../images/1Capitulo1Lab43.png)

---

**Paso 30.** En el campo **To**, selecciona la variable `Correo` que creaste en la pregunta anterior. En el campo **Subject**, selecciona la variable `Respuesta` que creaste anteriormente.

![LabImage](../images/1Capitulo1Lab44.png)

---

**Paso 31.** Agrega un nuevo mensaje que contenga el siguiente texto:

`he enviado un correo electrónico con la información de las políticas`

Luego finaliza agregando un nuevo nodo de tipo **Redirigir a otro tema**, y selecciona **Fin de la conversación**

![LabImage](../images/1Capitulo1Lab45.png)
![LabImage](../images/1Capitulo1Lab46.png)

---

**Paso 32.** Vamos a dejarlo así, haz clic en el botón de **Guardar** del costado superior derecho. 

![LabImage](../images/1Capitulo1Lab47.png)

---

**Paso 33.** Ahora haz clic en el botón **Test your chatbot** del costado inferior izquierdo.

![LabImage](../images/1Capitulo1Lab16.png)

---

**Paso 34.** En la ventana emergente escribe el siguiente mensaje: `políticas de seguridad`, y presiona Enter. Prueba el flujo de tu conversación libremente. 

![LabImage](../images/1Capitulo1Lab48.png)

---

**Paso 35.** Haz clic en el botón **Publicar** del costado izquierdo. Y en la ventana que se abre, nuecamente en el botón central **Publicar**

![LabImage](../images/1Capitulo1Lab49.png)
![LabImage](../images/1Capitulo1Lab51.png)

---

**Paso 36.** Haz clic **Opciones de disponibilidad**

![LabImage](../images/1Capitulo1Lab52.png)

---

**Paso 37.** Llevalo al equipo que creaste inicialmente haciendo clic en **Agregar a Netec** y luego en **Agregar**.

![LabImage](../images/1Capitulo1Lab53.png)
![LabImage](../images/1Capitulo1Lab54.png)

---

**Paso 38.** El bot te saludará en un ventana de chat. 

![LabImage](../images/1Capitulo1Lab55.png)

### Resultado esperado

Interactua con el chat desde Teams. Sigue el flujo de conversación, debes recibir toda la información que configuraste previamente, así como el correo electrónico. 

![imagen resultado](../images/1Capitulo1Lab56.png)
![imagen resultado](../images/1Capitulo1Lab50.png)

**Nota:** Si el agente no te contesta en la ventana de chat, intenta buscar la app desde Teams que lleva por nombre **NetecBot**. 



























