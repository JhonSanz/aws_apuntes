# Instancias

Permite crear maquinas virutales en AWS. EC2 significa Elastic Compute Cloud. Donde el término elástico significa que esta tecnología permite crecer o reducir instantáneamente los recursos basado en los requermientos de una aplición específica. También es posible la replicación de instancias para lograr un efecto similiar, estos dos conceptos serán tratados a profuniddad mas adelante.

Por su puesto existen las configuraciones para firewall (security groups), direccionamiento y subredes, balanceadores de carga etc.

---

## Modelos de pago


#### On demand

Renta las instancias y se cobra por hora o segundo (mínimo 60 segundos). Tiene la ventaja de evitar comprometerse a largo plazo, evitar complejidades de planificación. Sin embargo, este es el método mas caro, ya que con las otras opciones amazon hace descuentos.

Aquí simplemente **se cobra por el tiempo de uso**.

https://aws.amazon.com/es/ec2/pricing/on-demand/

#### Reserved instances

Hablando de planificar el uso de instancias a largo plazo, esta es la mejor opción. 

Se pueden adquirir para plazos de 1 o 3 años. AWS ofrece un descuesto hasta del 72% en comparación con las instancias bajo demanda. Es mucho mas barato pero tiene la desventaja de comprometerse a largo plazo.

Para esta modalidad es posible hacer un pago total o parcial anticipado, y de esta manera se calcula el descuento recibido.

https://aws.amazon.com/es/ec2/pricing/reserved-instances/pricing/

#### Spot

Este método es interesante pero mas complejo. Se trata de instancias On demand pero con la característica de que amazon puede prescindir de ellas cuando las necesite, generando una interrupción de nuestros servicios. 

En este caso, estamos utilizando procesamiento marginal de AWS, cuando sea necesario, nos llegará una alerta 2 minutos diciendo que ya no podremos utilziar mas este espacio, pasado este tiempo se interrumpirá el servicio.

Este método genera un ahorro 65%-70%, similar a reserved instances pero sin hacer ningún compromiso a largo plazo, y con la ventaja de on demand, pero tendremos que lidiar con las interrupciones. Es decir, son casos de uso bien planificados y específicos (spot friendly)

---

## Tenancy

Esto también afecta los pagos y la seguridad. Se refiere a la configuración a nivel de hardware, de como queremos que se lance nuestra instancia. hay tres tipos

- Shared: Cuentas de diferentes personas comparten el mismo hardware
- Dedicated: La instancia corre en un single-tenant hardware (un hardware arrendado individual)
- Dedicated host: La isntancia corre en un servidor fisico aislado con capacidad dedicada full para nuestro uso.

Como vemos, entre mas personalizado esté el software tendremos ventajas de seguridad pero al mismo tiempo mas costos.

---

## Direccionamiento IP

Nuestras instancias EC2 al tratarse de hardware tienen asiganda una dirección ip. Esta dirección tiene las siguientes características 

- Al crearse se le asigna una dirección privada, la cual no cambia si detenemos la instancia.
- Al correr la instancia esta recibe una dirección pública, la cual cambia cada vez que "apagamos" y reiniciamos la instancia.
- Para evitar que se renueve la dirección publica existe lo que se llama Elastic IP, la cual auqneu tiene costo adicional, permite que nuestra instancia tenga siempre la misma dirección pública. Este cobro se realiza cuando la instancia está **apagada** de lo contrario Elastic Ip no tiene costo.

---

## AMI

Para crear una instancia de EC2 es necesario tener una imagen de sistema operativo, esto dentro de amazon se llama AMI (Amazon Machine Image).

---

## Almacenamiento en EC2

Podemos ir al wizard y entrar al proceso de creación. Algo importante es que las instacias pueden almacenar la información de 2 maneras

Una es con el almacenamiento de la instancia misma, pero al dar de baja a la instancia la información va a perderse. Para esto existe la persistencia de la información por medio de los volúmenes **Elastic Block Store EBS**. Esto permite que la información sea independiente de la existencia de la instnacia.

Podemos crear este tipo de almacenamiento en el menú de la izquerda

1. Seleccionando el tipo de volumen, entre las opciones está SSD, HDD, magnético entre otros.
2. Configuramos tamaño, Throughput , IOPS, availability zone. Podemos también crearlo a partir de un snapshot
3. Click en crear

Tenemos nuestro volumen y ya que queremos tener backups de nuestros datos es posible crear snapshots, así como configurar schedules para hacerlo automáticamente.

---

## Monitoring

Mediante cloudwatch podemos acceder a varias métricas que generan nuestras instancias de EC2, tales como 

- CPU usage
- Network in/out
- Packets in/out
- Disk read/write

---

## Permissions

Por defecto las instancias no tienen acceso a otros recursos de AWS. Por lo cual estas permiten la asignación de roles de IAM con las policies adecuadas.

Esto es muy importante ya que si desplegamos una aplicación que necesite acceder a otros servicios puede presentar errores debido a falta de permisos.


# Load balancers

# AutoScalling