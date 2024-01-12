# Code build

Este servicio se encarga del continuous integration, el cual comprende los siguientes pasos o etapas:

1. Check out code
2. Build and UT
3. Code Scan
4. Image Build
5. Image Scan
6. Image Push


Para crear nuestra instancia del servicio codeBuild 

1. Vamos a la consola y a AWS CodeBuild
2. ponemos nombre y descripción
3. Tenemos la opción de limitar o restringir el numero de builds concurrentes que se puieden iniciar. Puede ser conveniente e importante a la hora de controlar costos.
4. Ahora configuramos el repositorio que queremos asignar como Source provider. Podemos elegir AWS CodeCommit, pero puede ser Github u otro de nuestra preferencia.
5. En el caso de seleccionar Github especificamos la ruta del repositorio y conectamos la cuenta mediante OAuth, o podemos seleccionar un repositorio público.
6. El entorno de construcción se refiere a la combinación de sistema operativo, runtime y herramientas que CodeBuild utiliza para realizar sus operaciones. [Explicacion detallada de como funciona aqui](https://docs.aws.amazon.com/codebuild/latest/userguide/concepts.html#concepts-how-it-works). Entonces podemos simplemente seleccionar ubuntu, runtime standard y la imagen latest.
- Si queremos construir imagenes de docker debemos darle permisos ingresando a Additional configuration y activando la casilla Privileged donde dice "Enable this flag if you want to build Docker images or want your builds to get elevated privileges"
7. También debemos seleccionar un rol para que ejecute las acciones. Ya que el servicio necesita los permisos para realizar acciones dentro de nuestra cuenta. Este paso es muy importante, ya que vamos a estar utilizando otro servicio llamado AWS systems manager, y debemos explicitamente asignarle permisos a este rol para que pueda intereactuar con ese servicio.
8. Ahora viene el buildspec file. Aqui es donde describimos el comportamiento de nuestro continuous integration.

```yaml
version: 0.2

env:
  parameter-store:
     DOCKER_REGISTRY_USERNAME: /myaws/parameterstore/username 
     DOCKER_REGISTRY_PASSWORD: /myaws/parameterstore/password
     DOCKER_REGISTRY_URL: /myaws/parameterstore/url 
phases:
  # aqui decimos que clase de runtime necesitamos
  install:
    runtime-versions:
      # entonces aqui tenemos una imagen de ubuntu con python disponible, dado que nuestro ejemplo es una app simple de flask 
      python: 3.11

  # las acciones pre_build se requieren cuando hay cosas por hacer antes de contruir la aplicación, por ejemplo instalar las dependencias
  pre_build:
    commands:
      - pip install -r myapp/requirements.txt

  build:
    commands:
      - cd myapp
      - echo "Building docker image"
      - echo "$DOCKER_REGISTRY_PASSWORD" | docker login -u "$DOCKER_REGISTRY_USERNAME" --password-stdin "$DOCKER_REGISTRY_URL"
      - docker build -t "$DOCKER_REGISTRY_URL/$DOCKER_REGISTRY_USERNAME/myawsomeapp:latest" .
      - docker push "$DOCKER_REGISTRY_URL/$DOCKER_REGISTRY_USERNAME/myawsomeapp:latest"

  post_build:
    commands:
      - echo "Build successful"

```
9. Hay otras configuraciones pero por ahora se puede dejar asi jeje
10. Un paso importante aqui es que podemos agregarle seguridad a nuestra aplicación con la sección de variables de entorno, utilizando servicios como AWS systems manager. Podemos ver esto en la sección env, primero creamos todas las variables en systems manager y luego las instanciamos.
