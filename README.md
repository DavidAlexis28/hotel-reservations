<<<<<<< HEAD
# hotel-reservations
=======
hotel-reservations

**Justificación técnica:** 
 Esta investigación permitirá conocer cómo funciona el sistema de reservas del hotel desarrollado con Java 21, JDBC y SQL Server 2022 especialmente cuando aumenta la cantidad de datos almacenados. 
No solo se comprobará que las operaciones funcionen correctamente, sino también cuánto tiempo tardan en ejecutarse, por eso se realizarán pruebas con diferentes cantidades de datos y se registrarán los tiempos de respuesta. 
Los resultados permitirán identificar qué operaciones tardan más cuando aumenta la información y si es necesario realizar mejoras en las consultas SQL los índices o la comunicación entre Java y SQL Server mediante JDBC, así veremos las posibles mejoras del sistema asi se podrán realizar basándose en los resultados obtenidos en las pruebas y no solamente en suposiciones. 
La optimización de las consultas SQL y el uso adecuado de JDBC son importantes para mejorar el tiempo de respuesta del sistema de automatización hotelera, una buena gestión de las consultas y de las conexiones con SQL Server 2022 puede ayudar a que operaciones como registrar clientes, consultar habitaciones y gestionar reservas se realicen de manera más rápida y eficiente.

**Pregunta principal:** 
¿Cómo afecta el aumento del volumen de datos al tiempo de respuesta de las operaciones de reserva en un sistema hotelero desarrollado con Java 21, JDBC y SQL Server 2022? 

**Preguntas secundarias:** 
¿Cómo varía el tiempo de respuesta de la consulta de habitaciones disponibles al aumentar el volumen de datos almacenados en SQL Server 2022? 
¿Qué diferencias de tiempo de respuesta se presentan entre las operaciones de registro, modificación y cancelación de reservas bajo diferentes volúmenes de datos? 

**Delimitación teórica**
El proyecto se enfocará en los conceptos relacionados con la gestión de reservas de hotel, específicamente en el registro y administración de clientes, habitaciones, reservas y pagos.

**Delimitación espacial/contexto**
El sistema estará orientado a la gestión de reservas de un establecimiento hotelero, considerando las operaciones relacionadas con clientes, habitaciones, reservas y pagos dentro de un contexto académico.

**Delimitación temporal**
El desarrollo del sistema se realizará durante el período académico establecido para el proyecto, comprendiendo las etapas de planificación, desarrollo, pruebas y presentación final.

**Delimitación tecnológica**
El sistema será desarrollado utilizando Java 21 como lenguaje de programación, IntelliJ IDEA 2026.2 como entorno de desarrollo y GitHub Desktop junto con GitHub.com para el control y gestión del código fuente. El desarrollo se realizará en un equipo con Windows 11 de 64 bits, 8 GB de memoria RAM y un procesador de 3.00 GHz.
