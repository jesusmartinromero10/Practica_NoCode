# Practica_NoCode

# Proyecto de Automatización de Carga de Datos de Eventos Educativos

## Descripción General

Este repositorio contiene los recursos necesarios para la automatización de la carga de datos de eventos educativos desde hojas de cálculo de Google a una base de datos. El proceso se centra en la extracción de datos, mapeo, transformación y carga en un esquema SQL.

## Contenidos

1. **Modelo de Datos SQL:**
   - En la carpeta diagrama y scripts esta el archivo `diagramaBD.png` describe la estructura de la base de datos utilizada para almacenar la información de eventos educativos. Incluye tablas, campos y relaciones.

2. **Script de Carga Inicial:**
   - En la carpeta diagrama y scripts esta el archivo `scripts.sql`, se encuentra el script de Mysql que realiza la carga inicial de datos.

3. **Documentación:**
   - El documento `documentacion.pdf` proporciona una guía detallada sobre la solución propuesta. Incluye un análisis de requisitos, diseño de la solución y detalles sobre el proceso de mapeo y transformaciones.

## Instrucciones

1. **Requisitos Previos:**
   - Asegúrate de tener SQL Workbench o similar instalado en tu entorno de desarrollo.
   

2. **Configuración de Base de Datos:**
   - Ejecuta el script `Scripts.sql` en tu sistema de gestión de bases de datos para crear las tablas necesarias e inyección de los datos.


3. **Revisión y Monitoreo:**
   - Después de la ejecución, verifica la base de datos para asegurarte de que los datos se hayan cargado correctamente.
   - Consulta la consola de SQLworkbench para monitorear cualquier posible error durante el proceso.



## Notas Adicionales
**Propuesta de Mejora en la Normalización de la Base de Datos**

- En el contexto del proyecto identificamos oportunidades para mejorar la normalización de la base de datos, lo que contribuirá a una estructura más eficiente y fácil de mantener. A continuación, se detallan las propuestas de mejora:

1. **Descomposición de Campos Multivaluados:**
   
Situación Actual:
Actualmente, algunos campos contienen información multivaluada, lo que puede dificultar la gestión y el mantenimiento de la base de datos.

Propuesta de Mejora:
Descomponer estos campos en tablas separadas. Por ejemplo, si hay una columna "Participantes" que puede contener múltiples nombres, se podría crear una tabla Participantes con una relación muchos a muchos con la tabla principal de eventos.
Yo en este caso solo he sacado una tabla intermedia pero hubiera sacado alguna más y sería mucho más claro y mejor para su mantenimiento y manejo.

2. **Eliminación de Dependencias Transitivas:**
   
Situación Actual:
Identificamos dependencias transitivas que podrían afectar la integridad de la base de datos a largo plazo.

Propuesta de Mejora:
Refactorizar las tablas para eliminar dependencias transitivas. Esto puede implicar dividir una tabla en dos para eliminar dependencias no directas.
- Asegúrate de leer la documentación para comprender completamente el diseño de la solución y las decisiones tomadas durante el proceso de automatización.
- Para cualquier problema o pregunta, no dudes en abrir un problema en el repositorio o contactar conmigo.

## Beneficios Esperados:
- Reducción de la Redundancia: Al descomponer campos multivaluados y eliminar dependencias transitivas, se reducirá la redundancia de datos, ahorrando espacio y mejorando la eficiencia.

- Facilita el Mantenimiento: Una estructura normalizada facilita la actualización y modificación de datos, así como la incorporación de nuevos requerimientos sin afectar la integridad.

- Mejora del Rendimiento: Al gestionar relaciones de manera eficiente y eliminar redundancias, se espera un rendimiento más óptimo en consultas y operaciones de la base de datos.

- Mayor Flexibilidad: Una base de datos más normalizada proporciona una mayor flexibilidad para adaptarse a cambios en los requisitos y la evolución del sistema.

- Mayor Integridad de Datos: La normalización adecuada mejora la integridad referencial y garantiza que los datos sean coherentes y precisos.



Este README proporciona una visión general y pasos básicos para comenzar con el proyecto.
