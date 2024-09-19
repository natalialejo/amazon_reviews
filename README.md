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

## 3. Metodología

### 3.1. Procesamiento y preparación de datos:

#### 1. Herramientas:
* Google Sheets
* BigQuery
* Looker Studio 
* Canva
* Loom

#### 2. Lenguajes:
* SQL en BigQuery

#### 3. Descripción de las fuentes de datos:

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


#### 4. Limpieza y transformación de datos:

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
