# PracticaChatTema3
Realización Chat servidor-cliente

Una situación típica de un servidor que atiende a múltiples clientes es un servidor de chat. Vamos a construir
un chat sencillo que pueda atender a varios clientes a la vez, cada cliente será atendido en un hilo de ejecución;
en ese hilo se recibirán sus mensajes y se enviarán al resto. 

El Programa se divide en 3 clases:

### Clase ServidorChat:
Es la encargada de hacer de puente entre los clientes y en el cual se controla el número de conexiones que hay en cada momento. y se mantiene a la escucha en un puerto pactado para las peticiones de conexión de cualquier cliente. Si el servidor se cierra se corta las conexiones entre los clientes.

### Clase ClienteChat:
Simplemente se encarga de crear el socket para conectarse con el Servidor. Y así poder comunicarse con el resto de clientes.

### Clase HiloServidor:
Básicamente se encarga de crear los flujos de entrada y salida que permitan enviar y recibir los mensajes de los clientes. Si un cliente sale se rompe el hilo.

# Funcionamiento
1. Ejecutamos la clase ServidorChat:

2. Una vez Iniciado el Servidor iniciamos la clase ClienteChat, e introducimos un nombre por cada cliente que ejecutemos (Max.10):

3. En el servidor nos saldrá el numero de clientes que hay conectados, y una vez creados se podrá enviar mensajes:

4. En el caso de que un usuario salga será notificado:

5. El servidor al ser quien controla las conexiones, si sale se cierra el chat entero:
