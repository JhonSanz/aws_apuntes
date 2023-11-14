# Instancias

Permite crear maquinas virutales en AWS. EC2 significa Elastic Compute Cloud. Donde el término elástico significa que esta tecnología permite crecer o reducir instantáneamente los recursos basado en los requermientos de una aplición específica. También es posible la replicación de instancias para lograr un efecto similiar, estos dos conceptos serán tratados a profuniddad mas adelante.

Hay varios modelos de pago, uno de los mas populares es basado en el uso por segundo de las isntancias.


Por su puesto existen las configuraciones para firewall (security groups), direccionamiento y subredes, balanceadores de carga etc.

---

### AMI

Para crear una instancia de EC2 es necesario tener una imagen de sistema operativo, esto dentro de amazon se llama AMI (Amazon Machine Image).

### Almacenamiento en EC2

Podemos ir al wizard y entrar al proceso de creación. Algo importante es que las instacias pueden almacenar la información de 2 maneras

Una es con el almacenamiento de la instancia misma, pero al dar de baja a la instancia la información va a perderse. Para esto existe la persistencia de la información por medio de los volúmenes **Elastic Block Store EBS**. Esto permite que la información sea independiente de la existencia de la instnacia.

Podemos crear este tipo de almacenamiento en el menú de la izquerda

1. Seleccionando el tipo de volumen, entre las opciones está SSD, HDD, magnético entre otros.
2. Configuramos tamaño, Throughput , IOPS, availability zone. Podemos también crearlo a partir de un snapshot
3. Click en crear

Tenemos nuestro volumen y ya que queremos tener backups de nuestros datos es posible crear snapshots, así como configurar schedules para hacerlo automáticamente.


# Balanceadores de carga