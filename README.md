# Evaluación del Rendimiento de las Operaciones de Reserva en un Sistema Hotelero Desarrollado con Java 21 y SQL Server 2022

[![Entrega 1](https://img.shields.io/badge/Entrega-v0.1--perfil-blue.svg)](#estado-del-proyecto)
[![Licencia](https://img.shields.io/badge/Licencia-MIT-green.svg)](LICENSE)
[![Java](https://img.shields.io/badge/Java-21%20LTS-orange.svg)](https://openjdk.org/)
[![Database](https://img.shields.io/badge/SQL%20Server-2022-red.svg)](https://www.microsoft.com/sql-server)

> Proyecto de investigación formativa para la asignatura **Programación 3 (Sección 03)**, Facultad de Informática y Ciencias Aplicadas.

---

## Integrantes del Equipo

| Nº | Carnet | Nombre Completo | Usuario GitHub |
| :-: | :-: | :--- | :--- |
| 1 | 17-0613-2024 | MENJIVAR CHAVEZ RICARDO FABIO | `@Fabio-Menjivar` |
| 2 | 25-4370-2023 | MORENO MEJIA HECTOR ANTONIO | `@hector-more` |
| 3 | 25-0574-2024 | LARA LOPEZ CESAR GONZALO | `@cesarlaralopezlaralopez-prog` |
| 4 | 17-2696-2024 | REYES RODRIGUEZ SILVIA ARELY | `@SilviaReyes05` |
| 5 | 25-4222-2024 | MIRANDA GUZMAN ERICK ARMANDO | `?` |
| 6 | 27-4135-2022 | AGUILAR ASCENCIO DAVID ALEXIS | `@DavidAlexis28` |
| 7 | 25-2531-2022 | AMAYA HERNANDEZ ANGEL OTONIEL | `?` |

* **Docente:** Eliseo Ernesto Hernández Díaz  
* **Institución:** Facultad de Informática y Ciencias Aplicadas  
* **Fecha:** 18 de Septiembre de 2026  

---

## Descripción del Problema Técnico
A medida que el volumen de transacciones escala hacia cientos de miles de registros en sistemas de procesamiento en línea (OLTP), los motores de bases de datos relacionales pueden experimentar degradación severa en sus tiempos de respuesta debido a escaneos completos de tabla (*table scans*), bloqueos concurrentes y saturación de memoria. Actualmente, no se cuenta con evidencia empírica que cuantifique el impacto exacto del incremento en el volumen de datos sobre la latencia de las operaciones críticas (consulta de disponibilidad, inserción, modificación y cancelación de reservas) gestionadas mediante Java 21, JDBC y SQL Server 2022, lo que impide fundamentar decisiones de optimización sobre datos verificables.

---

## Pregunta de Investigación
* **Pregunta principal:** ¿Cómo afecta el aumento del volumen de datos al tiempo de respuesta de las operaciones de reserva en un sistema hotelero desarrollado con Java 21, JDBC y SQL Server 2022?
* **Preguntas secundarias:**
  * ¿Cómo varía el tiempo de respuesta de la consulta de habitaciones disponibles al aumentar el volumen de datos almacenados en SQL Server 2022?
  * ¿Qué diferencias de tiempo de respuesta se presentan entre las operaciones de registro, modificación y cancelación de reservas bajo diferentes volúmenes de datos?
  * ¿Qué operaciones presentan mayor variación y demandan optimizaciones a nivel de consultas SQL o conectividad JDBC?

---

## Objetivos del Proyecto

### Objetivo General
Evaluar el impacto del incremento en el volumen de datos sobre el tiempo de respuesta de las operaciones de reserva en un sistema hotelero desarrollado con Java 21, JDBC y SQL Server 2022, mediante un diseño experimental controlado.

### Objetivos Específicos
1. Construir un banco de pruebas reproducible e instrumentar un prototipo en Java 21 y JDBC que ejecute de forma automatizada las transacciones de reserva sobre SQL Server 2022.
2. Medir empíricamente los tiempos de respuesta (latencia en milisegundos) de las operaciones bajo cuatro volúmenes escalonados de datos: 100, 1.000, 10.000 y 100.000 registros.
3. Comparar estadísticamente el comportamiento temporal de las consultas e identificar cuellos de botella para proponer directrices de indexación y optimización técnica.

---

## Delimitación Tecnológica

| Componente | Tecnología / Especificación | Propósito |
| :--- | :--- | :--- |
| **Lenguaje de programación** | Java 21 (LTS) | Lógica de la aplicación y automatización de pruebas |
| **Persistencia / Conector** | JDBC (`PreparedStatement`) | Comunicación estandarizada con la base de datos |
| **Motor de Base de Datos** | Microsoft SQL Server 2022 | Almacenamiento y procesamiento relacional de reservas |
| **Entorno de Desarrollo** | IntelliJ IDEA | Configuración, compilación y depuración del proyecto |
| **Control de Versiones** | Git 2.x / GitHub | Historial distribuido, ramas, pull requests y issues |
| **Sistema Operativo Base** | Windows 11 (64 bits) | Entorno de ejecución de pruebas |
| **Perfil de Hardware** | 8 GB RAM / CPU 3.00 GHz | Parámetros del entorno para reproducibilidad de pruebas |

---

## Estructura del Repositorio

```text
investigacion-reservas-hotel/
│
├── README.md                               # Portada general, resumen y metadatos del proyecto
├── LICENSE                                 # Licencia de código abierto
├── .gitignore                              # Exclusiones de archivos temporales e IDEs
├── .env.example                            # Plantilla para variables de conexión
│
├── docs/                                   # Documentación y módulos de investigación
│   ├── entrega1-perfil.md                  # Documento consolidado de la Entrega 1
│   ├── entrega1-perfil.pdf                 # Versión compilada para entrega formal
│   ├── bitacora.md                         # Registro de decisiones y acuerdos del equipo
│   ├── objectives.md                       # Objetivos y variables de medición
│   ├── academic-social-justification.md    # Justificación académica (ISO/IEC 25010)
│   ├── social-professional-justification.md# Justificación social y del sector hotelero
│   ├── apa-intext-citations.md             # Normalización de citas en texto según APA 7
│   └── references.md                       # Compilación de referencias técnicas oficiales
│
├── src/                                    # Código fuente del prototipo Java 21
│
├── data/                                   # Datos sintéticos para pruebas
│   ├── raw/
│   └── processed/
│
└── experimentos/                           # Scripts y métricas de rendimiento
