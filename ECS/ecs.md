# ECS 

El servicio para poner a correr nuestros lindos contenedores, es básicamente un servicio de orquestación. Para eso primero que todo tenemos que

1. Ir a crear un cluster, al cual le vamos a poner un nombre
2. Y acá viene lo bueno, podemos elegir nuestra infraestructura. Por defecto está seleccionado AWS Fargate, pero podríamos creanos una instancia EC2 para que viva ahí nuestro servicio. Esto tiene implicaciones de pricing etc. Por eso seleccionaremos Fargate
3. Le damos a crear

Nos metemos a nuestro cluster

# Tasks

Es una abstracción sobre como ECS corre nuestro contenedor, practicamente la ejecución de este. Una tarea puede incluir mas de un contenedor, los cuales interactuan (algo similar a lo que pasa con docker-compose), podemos definir puertos por donde se hablen el uno al otro. La idea es tener los servicios separados, cada un en su contenedor. Por ejemplo, no quisiéramos tener en el mismo contenedor nuestra API y la base de datos.

# Servicio

Un servicio se encarga de agrupar las tareas, por ejemplo si tuviéramos una aplicación muy popular y crece el tráfico, es conveniente replicar nuestra infraestructura y utilziar un balanceador de carga. Entocnes lo único que habría que hacer es replicar nuestras tareas dentro del servicio.


---

Vamos a crear la tarea

1. Vamos a tasks definitions y crear una nueva
2. Hay que ponerle un nombre a la tarea
3. Y ahora seleccionamos nuestra infraestructura, podemos elegir SO, CPU, RAM etc. Esto es muy importante porque entre mas cosas le signemos mayor será el cobro. Seleccioné los menores recursos posibles xd
4. Tasks roles nos permitirá comunicar nuestro fargate con otros servicios de AWS, es importante pero no lo voy a hacer ahora. El task execution role se dejar crear automáticamente
5. Ahora como vimos anteriormnente, la tarea nos pedirá que agreguemos los contenedores que queremos correr aqui. Vamos entonces a nuestro ECR (o cualquier repositorio de imágenes público) y copiamos la URI de nuestra imagen.
6. Asignamos el portmapping de nuestro interés, ya que esta es una api, necesitamos el puerto 80 para que podamos comunicarnos a través de HTTP.
7. Asignamos lo límites de nuestro hardware, ya que si esto empieza a necesitar mas recursos los va a escalar y va a cobrar mas. Entonces de acuerdo a las necesidades asignamos una cantidad razonable.
8. Y vemos muchas otras configuraciones que para este ejemplo no son tan relevantes porque tenemos un solo contenedor, luego haré un ejemplo con mas contenedores para utilziar todo eso
9. Le damos a crear. Aqui **no se lanza** ningun contenedor, solamente es la definición del comportamiento que van a tener nuestros contenedores.