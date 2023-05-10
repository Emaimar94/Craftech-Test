# Prueba 1 - Diagrama de Red

 La arquitectura propuesta para la aplicación web en AWS se basa en soluciones distribuidas que permiten soportar cargas variables y lograr alta disponibilidad (HA). Está compuesta por varios servicios y componentes que trabajan juntos para proporcionar una aplicación web escalable y resistente.

+ Para administrar el tráfico y tener alta disponibilidad se utiliza Aplication Loadbalancer.
+ Para la aplicación se utiliza un enfoque de microservicios (ECS), estos microservicios se ejecutan en múltiples instancias distribuidas en diferentes zonas (AZ) para lograr alta disponibilidad. Además, se configuran políticas de escalado (AWS Auto Scaling) automático basadas en métricas de uso para adaptarse a las cargas variables (ajustar automáticamente la capacidad de las instancias según la demanda).
+ Se crea una VPC para brindar una capa de seguridad, además para que tanto el Loadbalancer y las instancias estén dentro de la misma red.
+ La base de datos backend se divide en dos tipos: una base de datos relacional y una no relacional. Para la base de datos relacional, se utiliza Amazon RDS (Relational Database Service). Esto permite una gestión fácil y escalable de la base de datos relacional, garantizando la disponibilidad y durabilidad de los datos. Para la base de datos no relacional, se utiliza Amazon DynamoDB, un servicio de base de datos NoSQL que proporciona un rendimiento rápido y una replicación automática para soportar cargas variables.

# Descripción de las herramientas:

+ Amazon Application Load Balancer: servicio de balanceo de carga administrado proporcionado por Amazon Web Services (AWS). Se utiliza para distribuir el tráfico de red entrante entre múltiples destinos, como instancias EC2, contenedores o servicios de backend, de manera eficiente y escalable.

+ Amazon VPC: servicio fundamental de redes en la nube de AWS que permite a los usuarios crear redes virtuales privadas y personalizables, controlar el enrutamiento y la seguridad, y conectar su infraestructura en la nube con recursos locales de forma segura. Proporciona un nivel adicional de aislamiento y control sobre la infraestructura de red en el entorno de AWS.

+ Amazon Auto Scaling: servicio de AWS que automatiza el ajuste de la capacidad de recursos según la demanda de la aplicación. Permite mantener un equilibrio óptimo entre rendimiento, disponibilidad y costos al escalar automáticamente la capacidad de instancias EC2 o grupos de instancias en función de las políticas y métricas definidas.

+ Amazon EC2: Amazon Elastic Compute Cloud (Amazon EC2) es un servicio de computación en la nube que permite a los usuarios ejecutar aplicaciones en máquinas virtuales escalables y flexibles en la infraestructura de AWS. 

+ Amazon RDS: Amazon Relational Database Service es un servicio administrado de bases de datos relacionales que simplifica la configuración, operación y escalabilidad de las bases de datos en la nube. 

+ Amazon DynamoDB: Amazon DynamoDB es un servicio de base de datos NoSQL administrado y escalable que ofrece un rendimiento rápido, alta disponibilidad y escalabilidad automática. 

+ Amazon S3: Amazon Simple Storage Service (Amazon S3) es un servicio de almacenamiento en la nube altamente escalable, duradero y seguro. Proporciona una solución confiable para almacenar y acceder a grandes volúmenes de datos desde cualquier lugar, con una alta disponibilidad y opciones avanzadas de seguridad. 

