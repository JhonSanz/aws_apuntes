# AWS Load balancers

Imaginemos que creamos un juego el cual desplegamos en AWS. Nuestra aplicación vive en una instancia de EC2.

![happy_game_1](happy_game_1.png)

Hasta hoy solamente hay 5 jugadores activos, que utilizan los recursos al mismo tiempo. Pero a medidad que pasa el tiempo nuestro juego se vuelve cada vez mas popular, y ahora cientos de usuarios están utilizando los recursos de nuestra instancia.

Aunque son buenas noticias, debemos solucionar algo porque al incrementar la cnatidad de solicitudes nuestro servicio se vuelve cada vez mas deficiente, tiempos de respuesta peores debido a la cantidad de **tráfico**.

Entonces lo que hay que hacer es replicar las instancias de EC2 de nuestra aplicación y poner en frente un balanceador de carga.

![happy_game_2](happy_game_2.png)

Como vemos, los usuarios en lugar de acceder a las isntancias de EC2, acceden al load balancer. Ahora es responsabilidad del balanceador el repartir las requests y el trafico a las instancias.

---

## Tipos de balanceadores

Recordando las clases de redes, sabemos que las comunicaciones se dan a través de protocolos que fluyen a través del modelo OSI, el cual cuenta con 7 capas.

- Aplicación
- Presentación
- Sesión
- Transporte
- Red
- Enlace
- Física

Los balanceadores de carga se enfocan en alguna de ellas. Por ejemplo

- Aplication Load Balancer
- Network Load Balancer
- Gateway Load Balancer

#### Application load balancer

La capa de aplicación se encarga de ofrecer al usuario final una interfaz de comunicación hacia las demás capas, permitiendo ejecutar protocolos de red aquí, tales como HTTP, SMTP, SSL etc.

Es aquí donde se inicia la comunicación, conectando al usuario final mediante un programa con los protocolos y enviando la información a las siguientes capas.



https://www.youtube.com/watch?v=bCS9m5RVPyo