# Instalación

Hay muchas maneras de instalar esto, pero para facilidad vamos a usar docker xd

Para instalarlo es conveniente siempre ir a la documentación oficial de docker a través de la documentación de la pagina oficial

https://www.jenkins.io/doc/book/installing/docker/#downloading-and-running-jenkins-in-docker

ya que me encontré muchas versiones de la imagen de jenkins en dockerhub.

Hacemos pull de la imagen recomendada y vamos a la documentación de github donde encontraremos los comandos buenos para que esto corra facilito

https://github.com/jenkinsci/docker/blob/master/README.md

---

Una vez instalado ponemos la contraseña para desbloquear que nos aparece en la consola, seguimos el wizard con las cosas por defecto, llenamos el nombre contraseña etc. Hasta que lleguemos al panel principal.

![jenkins_arch](jenkins_arch.png)

jenkins funciona como una arquitectura maestro-esclavo, donde por defecto tenemos el nodo maestro. Sin embargo, en nuestra organización pueden existir diferentes equipos, desarrolladores, proyectos etc. por lo que el nodo maestro puede verse sobrecargado y tener problemas de conflictos entre paquetes y versiones.

Por eso es que aparece el concepto de nodos esclavos, en donde vamos a correr separadamente los jobs, por lo cual el nodo maestro vamos a destinarlo solo para porpósitos de agendamiento/orquestación.

En el diagrama de la izquerda podemos ver 3 nodos esclavos, en cada uno de ellos tenemos la configuración necesaria para correr los jobs de una app específica. Por ejemplo si estamos trabajando una versión de node específica el nodo1 tendra la versión X de node. El problema aparece cuando hay otro proyecto con una versión diferente.

Entonces al lado derecho vemos una arquitectura mas contemporánea donde los jobs corren en contenedores de docker, ya que con esta tecnología es mas facil gestionar las versiones y requerimientos para correr nuestros jobs.

