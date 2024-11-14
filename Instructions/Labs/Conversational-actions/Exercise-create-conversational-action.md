# Ejercicio: Creación de una acción conversacional

En este ejercicio, crearás una acción conversacional que proporcionará información sobre un proyecto organizativo ficticio titulado "Project ABC".

Tareas del ejercicio:

- Creación de acciones conversacionales en Copilot Studio
- Publicación de una acción conversacional en Microsoft Copilot
- Prueba de la acción conversacional en Microsoft Copilot

## Tarea 1: (Opcional) Prueba de la experiencia predeterminada

Para empezar, haz una pregunta sobre el proyecto ABC en Microsoft 365 Copilot.

1. Abre **Microsoft Teams** e inicia sesión con una cuenta profesional o educativa.

1. Selecciona **Chat** en la barra lateral.

1. Selecciona **Copilot** en el menú de chat.

1. En el cuadro de redacción del mensaje, escribe `Who should I contact for questions about Project ABC?`

1. Ten en cuenta que Microsoft 365 Copilot no tiene actualmente ninguna información sobre Project ABC.

## Tarea 2: Creación de una nueva acción conversacional

Para empezar, configura el nombre, la solución y el esquema para una nueva acción conversacional en Microsoft Copilot.

1. En el explorador web, ve a [Copilot Studio](https://copilotstudio.microsoft.com) e inicia sesión con una cuenta profesional o educativa, si se te solicita.  Selecciona **Omitir** para omitir los mensajes de bienvenida.

    **Nota:** la primera vez que abras Copilot Studio, puede mostrar una interfaz de chat para crear el primer copiloto. Si esto sucede, selecciona el menú **...** en la parte superior derecha (junto al botón **Crear**), selecciona **Cancelar creación de copiloto** y, después, **salir** para salir de la interfaz de chat y ver la página principal de Copilot Studio.
1. Selecciona **Biblioteca** en el panel de navegación izquierdo. Aquí puedes ver una lista de las acciones y conectores existentes y crear una nueva.
1. Selecciona **Agregar un elemento** en la parte superior.  Un menú muestra 2 opciones para ampliar Copilot para Microsoft 365.
:::image type="content" source="../Media/extend copilot options.png" alt-text="La ventana muestra 2 opciones para ampliar Copilot: crear un copiloto o crear una acción.":::
1. Selecciona **Nueva acción**.

1. Selecciona **Conversación** para crear una acción conversacional.

1. En el campo **nombre**, escribe `Project ABC` y acepta la solución y el esquema predeterminados.

1. Selecciona **Crear** para continuar. Se crea la nueva acción conversacional. Esto tardará varios segundos. Cuando haya terminado, se te colocará en el lienzo de creación para continuar con la configuración de la acción.

## Tarea 3: Configuración del tema

A continuación, configura el nombre y el desencadenador del tema.

1. En el panel de creación de acciones conversacionales, ve a la pestaña **Temas**.

1. Selecciona el cuadro de texto **Nombre de tema** en la parte superior del panel, que tiene como valor predeterminado el nombre `"Untitled"` y escribe `Project ABC info` para asignar un nombre al tema.

1. En el nodo **Desencadenador** del tema, selecciona el cuadro de texto en el texto "Describir lo que hace el tema" y escribe `Answers questions and provides information about Project ABC, including questions about objectives, points of contact, and rollout timeline.`.

## Tarea 4: Envío de un mensaje

A continuación, agrega un nodo al tema para enviar un mensaje sobre Project ABC.

1. En el nodo Desencadenador, selecciona el icono **+** para agregar un nuevo nodo.

1. En el menú que se muestra, selecciona **Enviar un mensaje**.  Se ha creado un nuevo nodo de mensaje.

1. En el nodo de mensaje, selecciona el cuadro de texto y escribe `Project ABC is an initiative aimed at improving the culture and engagement within the company.  Objectives of the project include improved morale, increased employee survey results, and improved culture ratings.  For more information about Project ABC, contact Devon Torres.`.

1. Selecciona **Guardar** encima del lienzo de creación para guardar los cambios.

## Tarea 5: Publicación de la acción

A continuación, publica la acción para usarla en Microsoft 365 Copilot.

1. Selecciona **Publicar** en la parte superior de la página.

1. En la página **Publicar complemento**, selecciona **Publicar**.

1. En la página **¿Publicar contenido más reciente?**, confirma que el complemento Project ABC Info está habilitado y selecciona **Publicar**.  El proceso de publicación puede tardar un par de minutos.  Se mostrará una notificación en la parte superior de la ventana cuando se haya completado la publicación.

## Tarea 6: Habilitación y prueba de la acción

Por último, prueba la acción en Microsoft 365 Copilot.

1. Abre **Microsoft Teams**.

1. Selecciona **Chat** en la barra lateral.

1. Selecciona **Copilot** en el menú de chat.

1. En el área de redacción del mensaje, selecciona el botón **Administrar respuesta de Copilot**.

1. En el control flotante, busca **Copilot Studio** y selecciona **Agregar** para agregar Copilot Studio.
 
2. La acción **Project ABC Info** debe aparecer ahora en el control flotante.  Confirma que **Project ABC Info** está habilitado y cierra el control flotante.

:::image type="content" source="../Media/projectABCInfo-action-enabled.png" alt-text="Captura de pantalla de la acción Project ABC Info que se muestra en "Manage Copilot response" flyout in Teams.":::

3. En el cuadro de redacción del mensaje, escribe `Who should I contact for questions about Project ABC?`

4. Observa que Microsoft 365 Copilot devuelve información sobre Project ABC al invocar la acción conversacional.

Puedes personalizar o expandir esta acción conversacional con nodos adicionales.  Por ejemplo, puedes crear un nuevo nodo **Respuestas generativas** y cargar un archivo, lo que amplía el conocimiento disponible para la acción.

**Nota:** recuerda lo siguiente al probar la acción en Copilot:
- Copilot siempre reescribirá tus respuestas con su propia voz. En esta vista previa no es posible transmitir el contenido sin cambios al usuario final.
- La descripción de la acción conversacional es crítico para determinar la confiabilidad con la que se invocará. La descripción le enseña al orquestador en qué es buena tu acción y qué respuestas puede proporcionar. Asegúrate de utilizar una prosa clara al escribir la descripción y considera experimentar con cambios para obtener el mejor resultado.
- Seguir estos pasos con precisión no garantiza que Copilot devuelva los resultados esperados cada vez.  Copilot determinará cuándo invocar el complemento y cómo devolver los resultados.

## (Opcional) Desafío: ¡Crea tu propio copiloto!

Aplica lo que has aprendido para crear, publicar y probar una nueva acción conversacional para un escenario de tu elección.  Revisa los pasos de este ejercicio según sea necesario.