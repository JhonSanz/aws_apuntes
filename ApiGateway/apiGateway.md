# Api Gateway

Application programming interfaces.

Un dispositivo necesita acceso a alguna lógica de negocio, o algún servicio corriendo en AWS. Podemos hacerlo conectando con la apiGateway, ya que esta se conectará con algún servicio backend que hayamos creado.

Permite formatear la informaicón en la request, importar templates como Swagger etc.

![overview](overview.png)

- Reduce la latencia de las requests alrededor del mundo y por region.
- Expone las REST API de forma segura hacia otros servicios dentro de la VPC o por conexión directa.

![schema_rest](schema_rest.png)

# Conexión con Lambda

Un ejemplo típico pero muy util es crear un servicio REST que invoque una función lambda

1. Creamos nuestra función lambda con un nombre y un runtime (python obviamente 😉)
2. Vamos a apiGateway y seleccionamos alguna de las opciones que soporte funciones lambda, HTTP API funcionará para este ejemplo (es la recomendada)
3. Seleccionamos en Integraciones nuestra función lambda, ponemos un nombre y click en siguiente
4. definimos las rutas que va a tener nuestra API, con su respectivo verbo y ruta.
5. siguiente siguiente crear

En este momento ya podremos utilizar la función lambda desde nuestro cliente http favorito. 

Utilizaremos este código para identificar el tipo de petición y realizar una acción específica.

```python
import json

def lambda_handler(event, context):
    if event["requestContext"]["http"]["method"] == "POST":
        # guardar en base de datos xd
        pass
    
    return {
        'statusCode': 200,
        'body': json.dumps(event),
    }
```

En este ejemplo vamos a utilziar DynamoDB (ya que es gratis) para guardar los likes que le den a nuestra app

1. Vamos DynamoDB y creamos una nueva tabla con la configuración predeterminada
2. Le ponemos un nombre y en Partition Key ponemos id
3. crear

Si ejecutamos ahora nuestra lambda no va a funcionar, ya que está intentando conectarse a dynamoDB y para esto requiere permisos, entonces

1. En nuestra lambda vamos a la pestaña de configuración, vemos que al crear la lambda esta también creó un rol, el cual en este momento solo tiene acceso a couldWatch.
2. Entonces vamos a editar el rol dandole click y vamos a la pestaña de permisos.
3. click en agregar permisos y asociar políticas
4. debido al acceso que va a tener esta lambda a nuestra base de datos queremos una política estricta, por lo tanto vamos a crear una nueva. Entonces vamos a crear política
5. seleccionamos el servicio de dynamodb y los permisos GetItem, PutItem y UpdateItem
6. Agregamos el ARN de nuestra lambda y click en siguiente
7. le ponemos un nombre a nuestra política y crear
8. se la asignamos a nuestra lambda