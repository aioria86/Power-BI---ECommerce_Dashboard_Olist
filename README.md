## 📊 Visión General del Proyecto
Este repositorio contiene una demostración técnica de un dashboard de alto nivel para E-commerce. El diseño y la arquitectura de datos fueron originalmente desarrollados para un entorno real de WooCommerce (WordPress) y han sido adaptados exitosamente utilizando el conocido dataset público de **Brazilian E-Commerce Public Dataset by Olist** para fines de demostración pública.

El objetivo es demostrar capacidades avanzadas en Power BI, superando las visualizaciones nativas para crear una experiencia de usuario (UX) personalizada y profesional, orientada a la toma de decisiones gerenciales.

## Características Clave

Este no es un reporte estándar. Implementa técnicas avanzadas de visualización y modelado:

* **UX/UI Avanzado (Layering):** Tarjetas de KPI compuestas mediante la superposición de formas, métricas y sparklines para contexto histórico inmediato.
* **Inteligencia de Tiempo Dinámica:** Medidas DAX complejas (usando tablas desconectadas y `SWITCH`) para permitir alternar periodos (ej. 3 Meses vs Histórico) sin afectar el resto del reporte.
* **Análisis Comparativo (MoM):** Indicadores visuales (badges) que muestran la variación porcentual automática.
* **Visuales Compuestos de Ranking:** Fusión de gráficos de barras y áreas para visualizar ranking y tendencia simultáneamente.

## Origen de Datos (Importante)
Debido a las restricciones de tamaño de archivo de GitHub, **los datasets CSV originales no se incluyen en este repositorio**.

Para interactuar con el modelo o refrescar los datos, debes descargar el dataset oficial desde Kaggle:
**[Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)**

*Instrucciones: Descarga los archivos y asegúrate de que la ruta de origen en el archivo `.pbix` apunte a tu carpeta local de descargas.*

## Estructura del Repositorio

* `*.pbix`: El archivo de proyecto de Power BI con las visualizaciones demo (Tarjetas KPI y Top Ranking).
* `Imagen de referencia.png`: Captura del resultado visual esperado.
* `README.md`: Documentación técnica del proyecto.

## Stack Tecnológico

* **Herramienta:** Microsoft Power BI Desktop.
* **Lenguaje:** DAX Avanzado (Time Intelligence, `DIVIDE/ALL`, Tablas Virtuales).
* **Modelado:** Esquema Estrella (Star Schema).
* **Transformación:** Power Query (M).

## Nota sobre el Dataset
El dataset de Olist anonimiza los nombres de productos usando IDs. Los visuales de detalle reflejarán estos IDs (ej. `aca2eb7d...`) como comportamiento esperado.
