# Lambda

Ejecutar código sin pensar en servidores.

Vamos a crear nuestra lambda y aparecen diversas opciones, podemos elegir el runtime, crear uno o incluso subir un contenedor. Como siempre elegiremos Python.

Lambda crea un servidor por cada petición que llega. En este tiempo de creación se instala nuestro código y sus dependencias, a este tiempo se le conoce como cold-start.

Amazon optimiza los servidores dejándolos disponibles por unos minutos por si llega otra petición ya esté todo listo, y sea solo cuestión de ejecutar el código sin tener que isntalar todo otra vez (warn-start).

Lambda siempre ejecuta las peticiones en un servidor nuevo, es decir, existe siempre un servidor por llamado.

Por defecto hay un límite de concurrencia para lambda, osea la cantidad de funciones que podremos tender viviendo al mismo tiempo. Si el usuario excede el límite de llamados lambda retornará error 429 tooManyRequests

### Triggers

Son los eventos que disparan la función lambda, y hay muchas opciones. Algunos ejemplos son

- Integrar APiGateway para escuchar llamados HTTP y ejecutar nuestra función a modo de backend
- Integrar S3 para ejecutar nuestra función, para que, al subir una imagen, esta genere versiones comprimidas.
- Integrar Event bridge para ejecutar nuestra función a una hora determinada
- Integrar AWS CodeCommit e invocar nuestra función cuando se crea un rama o un tag nuevo, o cuando se hace push a una rama existente

[Aqui](https://docs.aws.amazon.com/lambda/latest/dg/lambda-services.html) hay mas ejemplos sobre como se puede integrar lambda con los demás servicios de AWS

### Test

En la pestaña de tests podemos seleccionar plantillas según nuestras necesidades. Si por ejemplo estamos integrando lambda con APIGateway, al seleccionar la plantila de ese servicio podremos ver el **event** que recibirá nuestra función, y en base a eso crear nuestro código.

```python
def lambda_handler(event, context):
    return {
        'statusCode': 200,
        'body': json.dumps(event),
    }
```

siendo este el evento

```json
{
  "version": "2.0",
  "routeKey": "POST /likes_counter",
  "rawPath": "/likes_counter",
  "rawQueryString": "",
  "headers": {
    "accept": "*/*",
    "accept-encoding": "gzip, deflate, br",
    "content-length": "0",
    "host": "2zgfeblgz3.execute-api.us-east-1.amazonaws.com",
    "user-agent": "Thunder Client (https://www.thunderclient.com)",
    "x-amzn-trace-id": "Root=1-6523287f-30d8275916a93e223c2cc81b",
    "x-forwarded-for": "45.225.224.116",
    "x-forwarded-port": "443",
    "x-forwarded-proto": "https"
  },
  "requestContext": {
    "accountId": "794976204901",
    "apiId": "2zgfeblgz3",
    "domainName": "2zgfeblgz3.execute-api.us-east-1.amazonaws.com",
    "domainPrefix": "2zgfeblgz3",
    "http": {
      "method": "POST",
      "path": "/likes_counter",
      "protocol": "HTTP/1.1",
      "sourceIp": "45.225.224.116",
      "userAgent": "Thunder Client (https://www.thunderclient.com)"
    },
    "requestId": "MgND5iQGoAMEJ4w=",
    "routeKey": "POST /likes_counter",
    "stage": "$default",
    "time": "08/Oct/2023:22:09:03 +0000",
    "timeEpoch": 1696802943023
  },
  "body": "{\n  \"app\": \"test_app\",\n  \"page\": \"test_page\"\n}",
  "isBase64Encoded": false
}
```

Podemos ver que tenemos el http method, body, headers etc. 

También podemos sacar el evento simplemente retornandolo en la respuesta de la función y trabajar a partir de ahí. Entonces, guardamos y ejecutamos nuestro test.

Importante tener que en cuenta que [**el evento va a cambiar dependiendo del servicio qeu estemos integrando**](https://docs.aws.amazon.com/lambda/latest/dg/lambda-services.html) 

### Settings

Podemos modificar las características de hardware del servidor que utilzia lambda para ejecutar nuestro código. Si vamos a la pestaña de settings podemos ver que pdemos asignar RAM, almacenamiento, red etc.

### Roles

Al crear la función lambda esta crea por defecto con un rol. Es importante tener esto en cuenta ya que al momento de hacer la integración con otros servicios tendremos que configurar la policy de ese rol para evitar el error AccessDenied. Por defecto viene con CloudWatchLogs para escribir en CloudWatch los logs que arroja la lambda. 

### Variables de entorno

podemos acceder a ellas mediante, para el caso de python
```python
os.environ["MY_VAR"]
```
Para otros lenguajes se hace diferente. El caso es que para configurar las variables de entorno 

1. vamos a configuración
2. Variables de entorno
3. Crearlas y disfrutar

### Limitaciones

Este servicio fue pensado para ejcutar tareas pequeñas, por lo tanto tiene limitaciones de tiempo para retornar timeout. El máximo configurable es de 15 minutos, pero hay que recordar que cobran por tiempo de ejecución.

También está limitado el payload del evento a 6MB.

Hay un límite del archivo zip que puede ser subido a almbda, 50MB para subir 250MB para descomprimir

### Lambda desde imagen docker

- [lambda docker](https://docs.aws.amazon.com/lambda/latest/dg/python-image.html#python-image-instructions)