# Que es
Cuando creamos una cuenta de amazon esta viene con una VPC por defecto. Por ejemplo al entrar a EC2 podemos ver que en el formulario de creación de las instancias nos pide seleccionar una VPC, una subred, una IP etc.

VPC significa virtual private cloud, es una red propia en la nube. Es importante tener en cuenta que todos los recursos que lanzamos en amazon **viven** en **zonas de disponibilidad**. Las zona de disponibilidad son datacenters que pueden estar dispersos geográficamente en una región.

En la imagen se puede observar que la VPC es una red que abarca toda la region y permite de esta manera que los recursos puedan cominarse entre si a pesar de que vivan en diferentes zonas de disponibilidad. De la misma manera estos recursos necesitan conectarse a internet. Es por eso que por defecto nuestra cuenta viene con una VPC creada.

Las suberedes de la imagen son subredes privadas **dentro** de la VPC, las cuales pueden ser cada zona des disponibilidad. Es como una subred en la subred. La VPC tiene un rango de direcciones que se divide entre las zonas de disponibilidad y luego cada una de ellas hereda un fragmento de ese rango direcciones de la VPC.

Podemos también concluir que las instancias reciben ambas direcciones IP, de la subred y de la VPC. 

Y finalmente toda la comunicación a internet se hace a través del Internet Gateway

![vpc_region](vpc_region.png)

Podemos controlar el acceso a nuestras redes y recursos a través de security groups, los cuales se crean dentro de la VPC, que funcionan básicamente como un firewall. ¿Qué trafico puede entrar a esta red? para eso creamos las NACLs (Network Access Control List) que son listas de control de acceso a la red.

![controlling_access](controlling_access.png)