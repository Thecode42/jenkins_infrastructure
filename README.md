## Acerca del proyecto

`JENKINS_INFRASTUCTURE` Los pasos para generar desde la Infraestructura hasta el despliegue son.
1. Create-infrastructure: 
    Crea la infraestructura desde cero esto incluye vpc,subnet,internet_gateway, route_table, security_group, alb, target_group, launch_template, autoscaling_group.

2. Deploy-project-to-aws:
    Genera el artefacto, genera test, analisis, crea la imagen docker, publica en ECR de AWS y llama a *Deploy-to-aws* para mandar asiganar la imagen al launch templay y desplegar la instancia.
3. Deploy-to-aws:
    Es llamado por el pipeline anterior con el nombre de la imagen y así deplegarla en EC2 de AWS.
---