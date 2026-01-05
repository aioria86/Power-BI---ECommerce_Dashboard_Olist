# Dashboard E-commerce Olist - Power BI

## 📊 Visión General del Proyecto

Este repositorio contiene una demostración técnica de un dashboard de alto nivel para E-commerce. El diseño y la arquitectura de datos fueron desarrollados adaptando el conocido dataset público de **Brazilian E-Commerce Public Dataset by Olist**.

El objetivo es demostrar capacidades avanzadas en Power BI, superando las visualizaciones nativas para crear una experiencia de usuario (UX) personalizada y profesional, orientada a la toma de decisiones gerenciales.

> **Nota Técnica:** Este proyecto se distribuye como una **Plantilla de Power BI (.pbit)** para optimizar el almacenamiento en GitHub y facilitar la reutilización de la estructura.

## 🚀 Características Clave

Este no es un reporte estándar. Implementa técnicas avanzadas de visualización, modelado y segmentación geoespacial:

* **UX/UI Avanzado (Layering):** Tarjetas de KPI compuestas mediante la superposición de formas, métricas y sparklines para contexto histórico inmediato.
* **Análisis Geoespacial Estratégico:** Uso de **Shape Maps (TopoJSON)** personalizados para visualizar Brasil sin ruido cartográfico.
* **Segmentación Comercial Personalizada:** Agrupación de los 27 estados brasileños en 4 clusters estratégicos (Sudeste, Sur, Nordeste y Centro-Norte) para equilibrar el análisis de densidad de ventas.
* **Tooltips Avanzados (Page-level):** Fichas contextuales que aparecen al pasar el cursor sobre regiones específicas, mostrando micro-tendencias y clientes top sin saturar la vista principal.
* **Inteligencia de Tiempo Dinámica:** Medidas DAX complejas (usando tablas desconectadas y `SWITCH`) para permitir alternar periodos (ej. 3 Meses vs Histórico) sin afectar el resto del reporte.
* **Visuales Compuestos de Ranking:** Fusión de gráficos de barras y áreas para visualizar ranking y tendencia simultáneamente.
  
## 📂 Estructura del Repositorio

Actualmente, el repositorio cuenta con dos versiones del archivo para facilitar su acceso:

* `*.pbit` (**Recomendado**): Archivo de **Plantilla**. Es el más ligero, contiene toda la estructura y medidas pero requiere cargar los datos de origen al abrirlo.
* `*.pbix`: Archivo de **Power BI completo**. Contiene los datos ya importados.
    * *Nota:* Para hacer posible la subida de este archivo a GitHub, se ha realizado un proceso de optimización reduciendo su tamaño considerablemente.
* `Imagen de referencia.png`: Captura del resultado visual esperado.

## ⚙️ Optimización y Limpieza de Datos

Con el objetivo de mejorar el rendimiento del reporte y reducir el peso del archivo `.pbix` para su distribución, se aplicaron técnicas de **depuración del modelo**:

* **Eliminación de Columnas:** Se han eliminado del modelo todas las columnas de las tablas originales que no eran estrictamente necesarias para los cálculos o visualizaciones actuales.
* **Beneficio:** Esto permite tiempos de carga más rápidos y un archivo final lo suficientemente ligero para ser compartido, manteniendo la integridad de los cálculos DAX y las relaciones del esquema estrella.

## 📝 Nota sobre el Dataset

El dataset de Olist anonimiza los nombres de productos usando IDs. Los visuales de detalle reflejarán estos IDs (ej. `aca2eb7d...`) como comportamiento esperado.

## 🛠 Stack Tecnológico

* **Herramienta:** Microsoft Power BI Desktop.
* **Lenguaje:** DAX Avanzado (Time Intelligence, `DIVIDE/ALL`, Tablas Virtuales).
* **Modelado:** Esquema Estrella (Star Schema).
* **Transformación:** Power Query (M).
* **Geoespacial:** TopoJSON para mapas de forma personalizados.

## ⚙️ Instrucciones de Uso (Importante)

Debido a que el archivo es una plantilla (`.pbit`), necesitas los datos originales para visualizar el reporte. Sigue estos pasos:

1.  **Descargar Datos:** Descarga el dataset oficial desde Kaggle: [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/olistbr/brazilian-ecommerce).
2.  **Abrir Plantilla:** Al abrir el archivo `.pbit` en Power BI Desktop, se abrirá una ventana emergente.
3.  **Cargar Rutas:** Si se solicitan parámetros, ingresa la ruta de tu carpeta local donde guardaste los archivos CSV/Excel o simplemente acepta la carga para que Power BI busque los orígenes.
    * *Nota: Asegúrate de que los nombres de los archivos CSV coincidan con los esperados por el modelo.*
4.  **Actualizar:** Una vez cargado, dale al botón "Actualizar" para poblar los gráficos.

## 📝 Nota sobre el Dataset

El dataset de Olist anonimiza los nombres de productos usando IDs. Los visuales de detalle reflejarán estos IDs (ej. `aca2eb7d...`) como comportamiento esperado.
