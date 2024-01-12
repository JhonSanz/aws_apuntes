# CodePipeline

AWS CodePipeline no es mas que un orquestador para las operaciones de CI/CD. Este se encarga de instanciar los servicios CodeBuild y CodeDeploy.

Entonces el flujo es que cuando un desarrollador hace push a una rama en específico, el pipeline invocará los demás servicios para que realicen las operaciones pertinentes.