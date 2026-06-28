# 🛒 Segmentación de Clientes con K-Means (Análisis RFM)

Este proyecto aplica técnicas de **Aprendizaje de Máquina No Supervisado** para agrupar y entender el comportamiento de los clientes de una tienda en línea (Online Retail). Utilizando el modelo **K-Means** y la metodología **RFM (Recency, Frequency, Monetary)**, el objetivo es descubrir el valor oculto en los datos de transacciones para diseñar estrategias de marketing efectivas.

---

## 📖 Descripción del Proyecto

En el competitivo mundo del retail, no todos los clientes son iguales. Este análisis procesa más de 500,000 registros transaccionales para identificar qué clientes son los más leales, cuáles están en riesgo de abandono y cuáles tienen un alto potencial de crecimiento. 

El proyecto consta de la limpieza de datos, la construcción de métricas RFM, la búsqueda del número óptimo de clusters mediante el *Método del Codo (Elbow Method)*, y la clasificación final de los usuarios en 4 segmentos estratégicos.

## 📊 Metodología RFM

El modelo se basa en tres variables fundamentales del comportamiento del consumidor:

* **Recency (Recencia):** Días transcurridos desde la última compra del cliente.
* **Frequency (Frecuencia):** Cantidad de compras o transacciones distintas realizadas por el cliente.
* **Monetary (Monetario):** Monto total de dinero gastado por el cliente en todos sus pedidos históricos.

## 🧠 Algoritmo y Modelado

* **Limpieza de Datos:** Eliminación de valores nulos, registros duplicados y transacciones con cantidades o precios menores o iguales a cero.
* **K-Means Clustering:** Se entrenaron modelos K-Means independientes (con $k=4$) para cada métrica (R, F, M).
* **Ordenamiento de Clusters:** Se creó una función personalizada para ordenar lógicamente las etiquetas de los clusters (donde un número mayor siempre representa un mejor valor para el negocio).
* **Scoring:** Se calculó un `SCORE` global sumando los valores de los clusters RFM para categorizar a los clientes.

## 🎯 Resultados de la Segmentación

Basado en el score calculado, la base de clientes se dividió en los siguientes 4 segmentos de valor:

| Segmento | Características RFM | Acción Estratégica |
| :--- | :--- | :--- |
| **High-Value** 🌟 | Recencia muy baja, Frecuencia alta, Gasto muy alto. | Retención, programas de lealtad, beneficios y ofertas exclusivas. |
| **Potential** 🚀 | Recencia baja, Frecuencia moderada, Gasto alto. | Aumentar frecuencia con ofertas personalizadas, *cross-selling* y *up-selling*. |
| **Average** ⚖️ | Recencia media-alta, Frecuencia baja-media, Gasto medio. | Promociones para cultivar el hábito de compra, descuentos por volumen. |
| **Low-Value** ⚠️ | Recencia alta, Frecuencia muy baja, Gasto muy bajo. | Campañas de reactivación, email marketing automatizado. |

## 🛠️ Herramientas y Tecnologías

El proyecto fue desarrollado en Python utilizando libretas de Jupyter, apoyándose en las siguientes librerías:

* **Manipulación de Datos:** `pandas`, `numpy`
* **Visualización:** `matplotlib`, `seaborn`
* **Machine Learning:** `scikit-learn` (Módulo `cluster.KMeans`)

## 🚀 Cómo ejecutar el proyecto

1.  Descarga el archivo necesario 'Online Retail':
    ```bash
    git clone [https://drive.google.com/drive/folders/1zt40x4ltXP8hcZ-Ispjkeb3NCmQquz_b?usp=sharing)
    ```
2.  Instala las dependencias necesarias:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```
3.  Abre el entorno de Jupyter:
    ```bash
    jupyter notebook
    ```
4.  Ejecuta el archivo `Aprendizaje no Supervisado.ipynb`. *(Asegúrate de tener el archivo `Online Retail.xlsx` en la ruta especificada dentro del código o actualiza la ruta según tu sistema).*

---
**Autor:** Hiram Cruz
