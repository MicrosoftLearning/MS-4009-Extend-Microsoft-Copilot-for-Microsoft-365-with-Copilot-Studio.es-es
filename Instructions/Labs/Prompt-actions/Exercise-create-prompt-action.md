# Ejercicio: Creación de complemento de mensajes

En este ejercicio, aprenderás:

- Cómo escribir un buen mensaje
- Cómo crear la solicitud en Copilot Studio
- Cómo probar el mensaje en el generador de mensajes
- Cómo usar el complemento de mensajes en Microsoft 365 Copilot

## Cómo escribir un buen mensaje

Anteriormente en este módulo, ya has aprendido algunos aspectos básicos de la ingeniería de mensajes. Un buen recurso para obtener más información sobre la ingeniería de mensajes es leer la guía de ingeniería de mensajes del equipo de AI Builder. La guía de ingeniería de mensajes se puede encontrar [aquí](https://aka.ms/learn-ai-builder-prompting-guide).

## Los elementos de un buen mensaje

La guía de ingeniería de mensajes del equipo de AI Builder cuenta con un gran conjunto de elementos que deben formar parte del mensaje.

Como puedes ver, tiene los siguientes elementos:

- **Tarea**: una **instrucción** que indica al modelo de transformador generativo preentrenado (GPT) la tarea que se va a realizar.
- **Contexto**: describe los **datos** en los que se actúa, junto con las **variables** de entrada.
- **Expectativas**: transmitir a GPT los **objetivos** y las **expectativas** sobre la respuesta.
- **Salida**: ayuda a GPT a darle el formato que quieres a la **salida**

![Captura de pantalla de la página de ingredientes del mensaje de la guía de ingeniería de mensajes de AI Builder. Las tareas, el contexto, las expectativas y la salida se resaltan como ingredientes del mensaje.](../Media/4-prompt-engineering-guide.png)

## Tarea 1: Diseño de un mensaje

En esta tarea, diseñarás un mensaje que te ayudará a crear un plan de desarrollo profesional basado en hitos profesionales.

> [!IMPORTANT]
> Al crear un mensaje, no es necesario empezar desde cero. Aunque es muy útil saber cómo escribir un buen mensaje, puede ser útil empezar con algo que ya te lleva a mitad del camino.
> Ya hay ejemplos de mensajes disponibles en la [Galería de soluciones de ejemplo: adopción de Microsoft](https://aka.ms/power-prompts). En este ejercicio usaremos el [ejemplo de mensaje Professional Development Plan](https://adoption.microsoft.com/sample-solution-gallery/sample/pnp-powerplatform-prompts-professional-development/).

Vamos a agregar todos los ingredientes del mensaje:

- **Tarea**: Design a professional development plan.
- **Contexto**: For someone aiming to achieve the following career [milestones].
- **Expectativas**: The plan should include goals and objectives, resources, and tools and a timeline for activities.
- **Salida**: Format the plan to be concise and actionable and present the information in a clear easy-to-follow manner suitable for a junior level employee.

Todo junto, el mensaje sería el siguiente:

*Design a professional development plan for someone aiming to achieve the following career [milestones]. The plan should include goals and objectives, resources, and tools and a timeline for activities. Format the plan to be concise and actionable and present the information in a clear easy-to-follow manner suitable for a junior level employee.*

## Tarea 2: Creación de una acción de mensaje en Copilot Studio

Ahora que has terminado de escribir el mensaje, es el momento de escribirlo en Copilot Studio.

1. En el explorador web, ve a [Copilot Studio](https://copilotstudio.microsoft.com) e inicia sesión con una cuenta profesional o educativa, si se te solicita.  Selecciona **Omitir** para omitir los mensajes de bienvenida.

    **Nota:** la primera vez que abras Copilot Studio, puede mostrar una interfaz de chat para crear el primer copiloto. Si esto sucede, selecciona el menú **...** en la parte superior derecha (junto al botón **Crear**), selecciona **Cancelar creación de copiloto** y, después, **salir** para salir de la interfaz de chat y ver la página principal de Copilot Studio.
1. Selecciona **Biblioteca** en el panel de navegación izquierdo. Aquí puedes ver una lista de las acciones y conectores existentes y crear una nueva.
1. Selecciona **Agregar un elemento** en la parte superior.  Un menú muestra 2 opciones para ampliar Copilot para Microsoft 365.
:::image type="content" source="../Media/extend copilot options.png" alt-text="La ventana muestra 2 opciones para ampliar Copilot: crear un copiloto o crear una acción.":::
1. Selecciona **Nueva acción**.
1. En la pantalla *Nueva acción*, selecciona **Mensaje**. Se abrirá el generador de mensajes de AI Builder.
1. En la página **Detalles de la acción**, escribe "Professional Development Plan" como **nombre de acción**.
1. Escribe la siguiente **descripción**: "Creates an actionable professional development plan based on desired career milestones."
1. Selecciona **Siguiente**.
1. En la sección **Mensaje** de la página **Agregar una acción de mensaje**, escribe "Design a professional development plan for someone aiming to achieve the following career [milestones]. The plan should include goals and objectives, resources and tools and a timeline for activities. Format the plan to be concise and actionable and present the information in a clear easy-to-follow manner suitable for a junior level employee". como **mensaje**.

    > [!NOTE]
    > Observa que hay una barra de información en la parte superior que indica que el mensaje debe tener al menos un valor dinámico.

1. En **Configuración de mensaje** en la barra lateral derecha, abre la sección **Entrada**.
1. Selecciona el botón **Agregar entrada** para agregar una entrada.
1. Escribe `milestones` como nombre para la entrada.
1. Agrega el siguiente texto como datos de ejemplo:

      ```text
      * Become medior in 3 years
      * Have 3 top reviews in a row
      * Become a manager in 10 years
      ```

1. Selecciona **[milestones]** en la sección del mensaje con el cursor.
1. Selecciona **Insertar**.
1. Selecciona **milestones**.

      Esto convertirá **[milestones]** en un valor dinámico.

1. ¡Estamos listos para probar nuestro mensaje!

## Tarea 3: Prueba del mensaje en el generador de mensajes

1. Selecciona **Probar mensaje** debajo de la sección mensaje. Esto probará el mensaje con los datos de ejemplo que agregaste antes.

    > [!NOTE]
    > Esto enviará el mensaje al modelo de IA y mostrará la respuesta en la sección respuesta de IA. Te permite ver cómo responde el LLM y ver si estás satisfecho con los resultados.

1. Cuando estés satisfecho con la respuesta de IA, selecciona **Guardar mensaje personalizado** para guardar el mensaje.

    En la ventana siguiente, puedes revisar la descripción del complemento y la descripción de las entradas.

1. En la página **Seleccionar parámetros de acción**, cambia la descripción de entrada de **milestones** a:

      ```text
      The career milestones that the user wants to achieve
      ```

1. Selecciona **Siguiente**.

1. Selecciona **Publicar** para publicar la acción en Microsoft 365 Copilot.  Esta operación puede tardar unos minutos.

## Tarea 4: Uso del complemento mensaje en Microsoft 365 Copilot

Ahora que has creado la acción del mensaje y la has probado, continúa con la siguiente tarea para acceder a ella en Microsoft 365 Copilot.  El complemento puede tardar 5 minutos o más en aparecer en Microsoft 365 Copilot.

1. Abre [Microsoft Teams](https://teams.microsoft.com).
1. Selecciona el botón **Copilot** en la barra de navegación izquierda.
1. Selecciona el icono **Administrar respuesta de Copilot** en la parte inferior de la pantalla (junto a donde puedes enviar mensajes a Copilot).
1. Busca **Copilot Studio** en el menú flotante que apareció y confirma que está activado para habilitarse.  
1. Selecciona **el icono de símbolo de intercalación** para expandir la lista de acciones en Copilot Studio.

    > [!NOTE]
    > Puede ser que Copilot Studio no está visible. Puede haber dos razones para eso: el administrador no ha implementado la aplicación integrada de Copilot Studio o el complemento aún no se ha indexado, y eso puede significar que deberías esperar un poco más tiempo.

2. Busca la acción con el nombre **Professional Development Plan** en la lista de acciones de la sección Copilot Studio y selecciona el botón de alternancia junto a él para habilitarlo.

    > [!NOTE]
    > Si no ves Professional Development Plan en la lista de complementos en Copilot Studio, puede tardar un poco más en aparecer. Puede tardar un poco más en aparecer en Microsoft 365 Copilot.

3. Después de habilitar la acción Professional Development Plan, puedes usarla en Copilot. **Pruébalo** enviando el siguiente mensaje a Copilot en Teams: "I would like to generate a Professional Development Plan to achieve the following career milestones: 1 - become better at my work as a marketer and 2 - have a better chance at getting promoted to the senior marketer role"

**Sugerencia:** para habilitar el modo de desarrollador en Copilot, escribe `-developer on` en chat.  Esto te permite observar cuándo Copilot usó un complemento para responder en el chat.
