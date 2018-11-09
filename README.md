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

![1 iniciarservidorchat](https://user-images.githubusercontent.com/35973932/48267213-abaf8900-e429-11e8-8bb5-221fd9349a2f.png)

2. Una vez Iniciado el Servidor iniciamos la clase ClienteChat, e introducimos un nombre por cada cliente que ejecutemos (Max.10):

![2 creamoscliente1](https://user-images.githubusercontent.com/35973932/48267272-cf72cf00-e429-11e8-857a-f7a7267fdad9.png)

![3 creamoscliente2](https://user-images.githubusercontent.com/35973932/48267274-d13c9280-e429-11e8-916f-37d4bb814137.png)

3. En el servidor nos saldrá el numero de clientes que hay conectados, y una vez creados se podrá enviar mensajes:

![4 conversar](https://user-images.githubusercontent.com/35973932/48267281-d39eec80-e429-11e8-91af-b76aaadfe6d2.png)

4. En el caso de que un usuario salga será notificado:

![5 salircliente](https://user-images.githubusercontent.com/35973932/48267288-d6014680-e429-11e8-9a6e-cfa73f2d576e.png)

5. El servidor al ser quien controla las conexiones, si sale se cierra el chat entero:

![6 salir servidorchat](https://user-images.githubusercontent.com/35973932/48267329-f8935f80-e429-11e8-831c-1b7bcd2cef03.PNG)

