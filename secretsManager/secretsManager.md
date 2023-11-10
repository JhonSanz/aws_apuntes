# Secrets Manager

Es un servicio gestionado por aws que permite almacenar de forma **encriptada** texto plano. Es util sobre todo para contraseñas, token de acceso, credenciales etc. ya que no es seguro guardarlo en variables de entorno ni quemar esa información directamente en el código.

Este servicio controla el acceso a los secretos mediante IAM.

Es posible habilitar la configuración de rotación de contraseñas. Esto hace que cada cierto tiempo las contraseñas cambien para tener un mayor nivel de seguridad. SM tiene integración directa con servicios como RDS o Redshift lo cual hace totalmente trasnparente cuando cambia el valor de los secretos.

Entonces

1. Vamos a secrets manager y le damos en crear
2. seleccionamos la fuente, ya que existen integraciones por defecto. Pero en este caso seleccionamos Other type of secret
3. En el formulario ponemos la clave y el valor
4. Seleccionamos el KSM que sirve para encriptar, podríamos crear un pero vamos a dejar el por defecto
5. siguiente y vemos la configuración de rotación, la cual podemos cambiar y habilitar
6. siguiente y crear

Una vez creado y configurado todo simplemente es cuestión de llamar la API con boto3 y el cliente de secrets manager como muestra el ejemplo.


--- 

Esto es genial pero es bastante caro, cobran por secreto almacenado, con recargo de llamados que se hagan.