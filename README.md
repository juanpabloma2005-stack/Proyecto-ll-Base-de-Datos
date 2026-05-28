# E-Commerce Database Project - Final Phase

Este repositorio contiene el diseño, la implementación y la documentación del sistema de bases de datos para una plataforma de comercio electrónico (**E-Commerce**). El proyecto adopta un enfoque de **arquitectura de base de datos híbrida**, combinando la robustez de un modelo relacional para la gestión transaccional con la flexibilidad y velocidad de un modelo NoSQL para el análisis de comportamiento y logs en tiempo real.

---

## Arquitectura del Sistema

El proyecto está dividido en dos componentes principales de almacenamiento:

1. **Componente Relacional (SQL):** Encargado de la persistencia de datos críticos, transacciones, gestión de usuarios, inventarios y compras estructuradas.
2. **Componente NoSQL (Documental):** Diseñado para el almacenamiento masivo de interacciones rápidas, auditorías, logs del sistema y motores de recomendación basados en el comportamiento del usuario.

---

## Estructura del Proyecto

A continuación se detallan los archivos clave que integran este repositorio:

* **`Script_SQL_E-Commerce_Proyecto ll.txt`**  
  Script principal en lenguaje SQL (diseñado para PostgreSQL). Contiene la definición del esquema relacional completo (DDL) incluyendo tablas como usuarios, productos, órdenes de compra y detalles de transacciones, junto con restricciones de integridad y llaves foráneas.
* **`Consultas_Documentadas.txt`**  
  Repositorio de consultas avanzadas y scripts de optimización. Incluye operaciones de agregación, uniones complejas (*joins*), y queries optimizadas para la generación de reportes de negocio.
* **Carpeta `ecommerce_nosql/`**  
  Colección de documentos en formato JSON que simulan e implementan la capa NoSQL orientada a documentos para el análisis de Big Data:
  * `.logs.json`: Historial de eventos del sistema, errores y auditorías de seguridad.
  * `.product_views.json`: Registro de interacciones y visualizaciones de productos por parte de los clientes.
  * `.recommendations.json`: Estructuras de datos destinadas a alimentar el motor de sugerencias personalizadas de la tienda.
  * `.user_activity.json`: Rastreo detallado de sesiones, clics y rutas de navegación de los usuarios dentro de la plataforma.

---

## Instrucciones de Despliegue

### 1. Base de Datos Relacional (SQL)
Para montar el esquema relacional, asegúrate de tener una instancia de base de datos activa (ej. PostgreSQL) y ejecuta el script principal:

```bash
# Ejemplo de ejecución mediante psql (PostgreSQL)
psql -U tu_usuario -d tu_base_datos -f "Script_SQL_E-Commerce_Proyecto ll.txt"