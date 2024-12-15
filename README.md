# Desafío AWS EC2

Este proyecto consiste en crear una instancia EC2 mediante el uso de GitHub Actions. A continuación, se detallan los pasos realizados:

## Pasos realizados

1. **Configurar las credenciales de AWS**  
   Se establecieron las credenciales necesarias para interactuar con los servicios de AWS desde GitHub Actions.

2. **Crear un grupo de seguridad**  
   - Se creó un grupo de seguridad asociado a una VPC existente.  
   - Se definió una regla de entrada para permitir acceso SSH únicamente desde la dirección IP del autor del proyecto.

3. **Crear una clave SSH**  
   Se generó una clave SSH para habilitar la conexión a la instancia mediante este protocolo.

4. **Definir y crear la instancia EC2**  
   Se configuraron los siguientes parámetros para la instancia:  
   - Nombre de la instancia.  
   - ID de la subnet.  
   - Imagen a utilizar: *Amazon Linux 2 AMI*.  
   - Tipo de instancia: *t2.micro*.  
   - Perfil de instancia: previamente configurado con el rol y permisos necesarios.  
   - Región: *us-east-1*.  
   - Nombre de la llave SSH creada previamente.

5. **Extraer la ID de la instancia**  
   Se obtuvo la ID de la instancia creada para utilizarla en la creación de una AMI.

6. **Crear una AMI**  
   Se creó una *Amazon Machine Image (AMI)* basada en la instancia EC2 creada, para que sea reutilizable en futuros proyectos.

---

## Requisitos previos

- Cuenta de AWS con permisos para crear instancias EC2 y manejar grupos de seguridad.
- Repositorio en GitHub con GitHub Actions habilitado.

---

## Estructura del flujo de trabajo (GitHub Actions)

El flujo de trabajo automatiza todos los pasos necesarios para implementar la solución descrita. Puedes encontrar el archivo `ec2.yml` en el directorio `.github/workflows`.

---

## Recursos utilizados

- **Amazon EC2**: Servicio para ejecutar instancias de máquinas virtuales en la nube.
- **GitHub Actions**: Plataforma de CI/CD para la automatización del flujo de trabajo.

---

## Autor

Este proyecto fue desarrollado por Gerald Opitz, con el objetivo de practicar la automatización de infraestructura en AWS utilizando GitHub Actions.

