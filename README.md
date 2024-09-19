# Proyecto: Amazon_reviews

## Indice:
1. [Objetivo](#Objetivo)
2. [Contexto](#Contexto)
3. [Metodología](#Metodología)   
    3.1. [Procesamiento y preparación de datos](#Procesamiento-y-preparación-de-datos)   
    3.2. [Análisis técnico](#Análisis-técnico)   
    3.3. [Creación de Dashboard en Looker Studio](#Creación-de-Dashboard-en-Looker-Studio) 
4. [Resultados y Recomendaciones](#Resultados-y-Recomendaciones)
5. [Enlaces de recursos adicionales](#Enlaces-de-recursos-adicionales)  
   
## 1. Objetivo:

Analizar los datos de productos de Amazon (precios, descuentos, calificaciones, número de reseñas y categorías) para identificar patrones y relaciones clave que ayuden a comprender el comportamiento de los productos en función de sus precios y descuentos.

## 2. Contexto: 

Datalab, una empresa líder en análisis de datos, se ha posicionado como un aliado confiable para compañías de diversos sectores gracias a su enfoque único de consultoría. En este proyecto, centrado en las ventas y reseñas de Amazon, se analizan datos de más de 1,000 productos disponibles en la plataforma. Amazon, como gigante del comercio electrónico, ofrece un proceso integral de ventas, desde la fijación de precios hasta la gestión de inventario y servicio al cliente. Este análisis busca aprovechar las habilidades analíticas para explorar cómo los precios, descuentos y calificaciones impactan el rendimiento de los productos en Amazon.

Además, con la información encontrada se espera poder dar respuesta a las siguientes hipótesis propuestas (basados en datos numéricos y categóricos):

- Hi1:"Cuanto mayor sea el descuento, mejor será la calificación del producto(puntuación)."  
SQL: correlación o comparación de promedios agrupados por rangos de descuento.

- Hi2: "Cuanto mayor sea el número de personas que evaluaron el producto (rating count), mejor será la calificación (promedio)."
SQL: cálculo de  promedios ponderados o agrupaciones de productos por el número de reseñas y su calificación promedio.

- Hi3: "Los productos más caros tienen a recibir calificaciones más altas."
SQL: analisis de la relación entre actual_price o discounted_price y la calificación promedio.

- Hi4: "Algunas categorías de productos tienden a recibir mejores calificaciones que otras."
SQL: agrupación de productos por categoría y cálculo de la calificación promedio para cada una.

- Hi5: "Los productos con los mayores descuentos pertenecen a categorías específicas."
SQL: agrupación de productos por categoría y cálculo de los descuentos promedio.

## 3. Metodología

### 3.1. Procesamiento y preparación de datos:

#### a. Herramientas:
* Google Sheets
* BigQuery
* Looker Studio 
* Canva
* Loom

#### b. Lenguajes:
* SQL en BigQuery

#### c. Descripción de las fuentes de datos:

Este conjunto de datos provienen de un repositorio de Kaggle.

**Tabla amazon_product**
- *product_id*: ID del producto
- *product_name*: Nombre del producto
- *category*: Categoría del producto
- *discounted_price*: Precio con descuento del producto
- *actual_price*: Precio real del producto
- *discount_percentage*: porcentaje de descuento del producto
- *about_product*: Descripción sobre el producto

**Tabla amazon_review**
- *user_id*: ID del usuario que escribió la reseña del Producto
- *user_name*: nombre del usuario que escribió la reseña del Producto
- *Review_id*: ID de la reseña del usuario
- *Review_title*: Breve reseña
- *Review_content*: reseña larga
- *Img_link*: Enlace de imagen del producto
- *Product_link*: Enlace al sitio web oficial del producto
- *Product_id*: ID del producto
- *Rating*: Calificación del Producto
- *Rating_count*: número de personas que votaron por la calificación de Amazon


#### c. Limpieza y transformación de datos:

- Datos iniciales: 
    * La tabla *products* contiene 1,469 registros y la tabla *reviews* contiene 1,465 registros.
    * La clave de búsqueda utilizada para la unión es *product_id*.

- Revisión de calidad de datos:
    * En la tabla *reviews, se encontraron 92 productos duplicados, lo que indica múltiples reseñas por *product_id*.
    * En la tabla *products*, se encontraron 96 productos duplicados, lo cual es problemático ya que cada *product_id* debería ser único, podrían afectar las uniones, causando más filas de las esperadas y posibles inconsistencias en los datos.

- Resolución de duplicados:
    * Se eliminaron los duplicados en la tabla *products* y *reviews* utilizando la función `DISTINCT` para garantizar un solo registro por *product_id*.
    * Tras eliminar los duplicados, se redujo la tabla *products* a 1,363 registros únicos. 
    * Se actualizó la variable *discount_percentage*, encontrando 89 tipos de descuentos.
    * No se encontraron caracteres especiales en las variables evaluadas.

- Normalización de datos:
    * Se realizaron conversiones de datos, como la transformación de valores a porcentajes y la actualización de categorías para *discounte_percentage* y *rating*
    * La variable *category* se normalizó, identificando 136 tipos de categorías únicas, las que cuales se dividieron 6 seis niveles, utilizando unicamente 3 de estos para el analisis siguiente.

- Vistas y creación de tablas auxiliares:
    * Se crearon tablas auxiliares sin duplicados y con conversiones adecuadas en los datos de ambas tablas.
    * Se crearon las vistas *product_category*, *product_ready* y *reviews_ready*.

- Unión Final de las Tablas:
    * Se realizó la unión de las tres vistas, utilizando `LEFT JOIN`, resultando en 1,355 registros válidos.

### 3.2. Análisis técnico:


### 3.3. Creación de Dashboard en Looker Studio:

## 4. Resultados y recomendaciones

## 5. Enlaces de recursos adicionales:

- [Dashboard Looker Studio]()
- [PPT Google Slide]()
- [Presentación Loom]()  

**Elaborado por:  
Natalia Alejandro González   
Dulce Carmona  
Septiembre 2024** 
