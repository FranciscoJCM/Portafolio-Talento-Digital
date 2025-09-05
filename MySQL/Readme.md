<!-- GIF HEADER -->
<img src="https://datawookie.dev/img/headers/banner-mysql_hu_988b1bfa47216a7d.webp">

# Descripción

MySQL Workbench es una aplicación de software unificada que provee un conjunto de herramientas esenciales para el trabajo con bases de datos MySQL, dirigida tanto a desarrolladores como a administradores. Su entorno visual e integrado abarca los procesos clave del ciclo de vida de una base de datos.

Dentro de sus funcionalidades y aplicación en el modelado y diseño de datos destaca: 
- Permite la conceptualización y el diseño de la estructura de una base de datos mediante diagramas de Entidad-Relación (ERD). Incluye funcionalidades de ingeniería inversa para generar un modelo visual a partir de una base de datos existente, facilitando el análisis y la documentación de esquemas.

- Desarrollo de SQL: El editor SQL integrado soporta la creación, edición y ejecución de consultas y scripts. Ofrece herramientas de asistencia como resaltado de sintaxis, autocompletado de código y la capacidad de visualizar los resultados en múltiples formatos, optimizando el flujo de trabajo del desarrollador.

- Administración del Servidor: Proporciona una interfaz gráfica para la gestión de servidores MySQL. Los administradores pueden supervisar el rendimiento del sistema, configurar parámetros, gestionar usuarios y privilegios, así como realizar tareas de mantenimiento como copias de seguridad y recuperación de datos, todo desde un único punto de control.

- Migración de Bases de Datos: Facilita el proceso de migración de datos y esquemas desde diversas plataformas de bases de datos hacia MySQL. Esta funcionalidad es particularmente útil en contextos de consolidación o cambio de infraestructura.

---

## Dataset y análisis
Para el presente proyecto se utilizó la base de datos "Jardinería" difundida por José Juan Sánchez que puedes encontrar en el siguiente **[link]([url](https://josejuansanchez.org/bd/ejercicios-consultas-sql/index.html#jardiner%C3%ADa))**.

```sql
Primero se creó la base de datos:

DROP DATABASE IF EXISTS jardineria;
CREATE DATABASE jardineria CHARACTER SET utf8mb4;
USE jardineria;

#Para continuar con la creación de cada una de las tablas y sus llaves:

CREATE TABLE cliente (
  codigo_cliente INTEGER NOT NULL,
  nombre_cliente VARCHAR(50) NOT NULL,
  nombre_contacto VARCHAR(30) DEFAULT NULL,
  apellido_contacto VARCHAR(30) DEFAULT NULL,
  telefono VARCHAR(15) NOT NULL,
  fax VARCHAR(15) NOT NULL,
  linea_direccion1 VARCHAR(50) NOT NULL,
  linea_direccion2 VARCHAR(50) DEFAULT NULL,
  ciudad VARCHAR(50) NOT NULL,
  region VARCHAR(50) DEFAULT NULL,
  pais VARCHAR(50) DEFAULT NULL,
  codigo_postal VARCHAR(10) DEFAULT NULL,
  codigo_empleado_rep_ventas INTEGER DEFAULT NULL,
  limite_credito NUMERIC(15,2) DEFAULT NULL,
  PRIMARY KEY (codigo_cliente),
  FOREIGN KEY (codigo_empleado_rep_ventas) REFERENCES empleado (codigo_empleado)
);

#Finalmente se insertaron los datos de cada una de las filas:

INSERT INTO cliente VALUES (1,'GoldFish Garden','Daniel G','GoldFish','5556901745','5556901746','False Street 52 2 A',NULL,'San Francisco',NULL,'USA','24006',19,3000);

---
