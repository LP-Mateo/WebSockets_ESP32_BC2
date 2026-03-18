# Cuestionario de Evaluación: Comunicación por Sockets 📝

**Nombre del Estudiante:** Mateo Loján
**Fecha:** 18/03/2026

*Instrucciones: Responde a las siguientes preguntas basándote en la teoría de redes y en el análisis del código de nuestro proyecto. Sube este archivo con tus respuestas a tu repositorio como evidencia de trabajo.*

1. **¿Qué es una Dirección IP y para qué sirve en nuestro proyecto?**
   > Es el identificador único de cada dispositivo que va a permitir conectarse del dispositivo al ESP32.

2. **¿Qué es un Puerto de red? (Menciona qué puerto estamos usando en el código de la ESP32).**
   > Es el número que identifica el servicio de red, aquí se usa el puerto 80.

3. **Define con tus propias palabras qué es un Servidor en informática.**
   > Es un programa que espera señales y que también puede enviar datos a otros equipos

4. **¿Cuál es la diferencia entre un "Servidor" (Hardware/Software) y un "Servicio" (Service)?**
   > Un servidor es quien ejecuta el sistema y el servicio es la función que realiza.

5. **Investigación: ¿Cuál es la diferencia técnica entre un "Socket TCP" normal y un "WebSocket"?**
   > TCP es una conexión directa de datos y websocket puede ayudar comunicación en tiempo real sobre la web.
   
6. **Analizando nuestro código: ¿Quién actúa como Servidor y quién actúa como Cliente? (Justifica tu respuesta mencionando qué funciones del código lo demuestran, ej. `bind()`, `connect()`).**
   > El ESP32 es el servidor y el cliente el dispositivo porque usa el connect() para poder realizar la conexión.

7. **En el código de la computadora (Python), importamos la librería `threading` (Hilos). ¿Qué pasaría con la ventana de Tkinter si no usáramos hilos para recibir los datos de la red?**
   > Sin los hilos posiblemente se quedaría pausado ya que tiene que esperar por los datos de la red.

8. **¿Por qué es necesario usar bloques `try...except` cuando trabajamos con conexiones de red e Internet?**
   > Porque ayuda a ver errores de conexión y asi que el programa no se cierre.

9. **En la función de encender el LED en Python, enviamos el comando así: `sock.send(b'ON')`. ¿Qué significa esa letra `b` antes de las comillas y por qué no enviamos un texto normal?**
   > la b es que se envian bytes porque los sockets usan datos binarios.

10. **Describe brevemente el flujo de datos: ¿Qué camino recorre la información desde que giras el potenciómetro físicamente hasta que la barra se mueve en la pantalla de la computadora?**
    > El potenciómetro envía un valor al ESP32 esto se manda por red mediante sockets y la computadora lo recibe y actualiza la barra en Tkinter.
