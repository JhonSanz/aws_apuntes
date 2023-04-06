# Servicios de interés

### Protección a Datos
- Amazon Macie: para descubrir y proteger sus datos sensibles
- AWS Key Management Service: almacena y administra claves de cifrado
- AWS CloudHSM: almacenamiento de claves basado en hardware y el cumplimiento normativo
- AWS Certificate Manager, provisiona, administra e implementa certificados de seguridad TSL y TLS
- AWS Secrets Manager: rotar, gestionar y recuperar secretos como contraseñas
### Protección de la infraestructura
- AWS Shield, para la protección de denegación de servicio
- AWS Web Aplication Firewall, (WAF) filtra el tráfico de sitios web maliciosos
- AWS Firewall Manager, administra las reglas del firewall de forma centralizada
### Detección de amenazas
- Amazon GuarDuty, detecta amenazas automáticamente
- Amazon Inspector, ayuda a analizar la seguridad de la aplicación
- Amazon config, registra y evalúa configuraciones de nuestros recursos
- Amazon CloudTrail, rastrea la actividad del usuario y el uso de las API
### Gestión de identidades
- AWS Identity and Access Management, (IAM) administra de forma segura el acceso a una cuenta, servicios y recursos
- AWS Inicio de sesión único: Implemente el acceso de sesión único (single sign on)
- AWS administra la identidad dentro de las aplicaciones, se puede hacer el inicio de sesiones moviles
- AWS Servicio de Directorio, implementa y administra un Active Directory Service
- AWS Organizaciones, para gobernar y administrar de forma centralizada en un mismo lugar


# Identity and Access Management

Es un servicio que ayuda a administrar quien puede acceder y a que recursos en nuestra cuenta de Aws, podremos crear usuarios y grupos, y establecer permisos para poder denegar o permitir el acceso a los recursos mediante el uso de políticas. Este es un servicio gratuito.

Entre las características principales están los usaurios y los roles:
- Cuando creamos la cuenta, el usuario root va a ser el que pueda acceder a todos los recursos de la cuenta aws. Esta cuenta va a poder crear mas usuarios
- Las políticas generalmente se crean en la consola de IAM mediante un archivo de configuración, por ejemplo:
```json
// Se toma como ejemplo los buckets de s3, servicio para almacenar archivos
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "s3.ListBucket"
            ],
            "Resource": "arn:aws:s3:::bucket-name",
        },
        {
            "Effect": "Allow",
            "Action": [
                "s3.GetObject"
                "s3.PutObject"
            ],
            "Resource": "arn:aws:s3:::bucket-name/*",
        },
    ]
}
```