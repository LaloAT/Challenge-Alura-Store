# 🛍️ Alura Store — Practicando Python para Data Science (Challenge)

Este repositorio contiene mi solución al **Challenge de Data Science – Alura Store**.  
El objetivo del proyecto es **ayudar al Sr. Juan a decidir qué tienda vender** analizando datos históricos de **4 tiendas**.

---

## 🧩 ¿Qué hicimos en el proyecto?

1. **Carga y preparación de datos**
   - Lectura de los 4 CSV de tiendas desde URLs públicas.
   - Conversión de tipos (`Precio`, `Calificación`, `Costo de envío`) a numérico.
   - Parseo de fechas (`Fecha de Compra`) cuando es necesario.
   - Limpieza básica de textos.

2. **5 análisis principales (con visualizaciones)**

   **A. Análisis de facturación (ingresos)**
   - *Qué calculamos:* Ingreso total por tienda (suma de `Precio`).
   - *Gráficos:* **Barras** de ingresos por tienda + **Pastel** de participación.

   **B. Ventas por categoría**
   - *Qué calculamos:* Conteo de ventas por `Categoría del Producto` en cada tienda.
   - *Gráficos:* **Barras agrupadas** por categoría/tienda y versión **100% apilada** para ver el mix.

   **C. Calificación promedio y distribución**
   - *Qué calculamos:* Media de `Calificación` (1–5) por tienda y su distribución.
   - *Gráficos:* **Barras** (promedio), **apiladas 1–5** (distribución porcentual) y **boxplot** por tienda.

   **D. Productos más y menos vendidos**
   - *Qué calculamos:* `Top 5` y `Bottom 5` productos por tienda + Pareto global.
   - *Gráficos:* **Barras horizontales** para Top/Bottom por tienda y **Pareto** (barras + línea acumulada).

   **E. Costo de envío**
   - *Qué calculamos:* `Costo de envío` **promedio** por tienda y su distribución.
   - *Gráficos:* **Barras** (promedio) y **boxplot** (distribución).

3. **Visualizaciones ejecutivas (resumen)**
   - **Bubble chart:** Ingresos vs. Calificación (tamaño = Costo de envío promedio).
   - **Radar de KPIs normalizados:** Ingresos, Calificación, Ventas, Envío (invertido).
   - **Mix de categorías 100%** por tienda.
   - **Ingresos mensuales** por tienda (líneas).
   - *(Opcional)* **Scatter** Precio vs Calificación por tienda.

4. **Informe final (autogenerado)**
   - Se genera `informe_alura_store.md` con:
     - Tabla de **métricas clave** por tienda (ingresos, calificación, envío).
     - **Hallazgos** por tienda (categorías y productos top/bottom).
     - **Visualizaciones clave** (guardadas como PNG y mostradas en el notebook).
     - **Conclusión y recomendación**: qué tienda vender y **por qué**, basada en un **score de ineficiencia**:
       - Ingresos **bajos** (peor),
       - Calificación **baja** (peor),
       - Costo de envío **alto** (peor).
     - Los **pesos** del score son ajustables en el notebook.

---

## 📦 Datos

- Archivos: `tienda_1.csv`, `tienda_2.csv`, `tienda_3.csv`, `tienda_4.csv`
- Columnas relevantes:  
  `Producto`, `Categoría del Producto`, `Precio`, `Costo de envío`, `Calificación`,  
  `Fecha de Compra`, `Lugar de Compra`, `Vendedor`, `Método de pago`, `Cantidad de cuotas`, `lat`, `lon`.

> Los CSV se leen directamente desde las URLs públicas del challenge.

---

## 🧰 Tecnologías y librerías

- **Python 3.9+**
- **pandas** (manipulación de datos)
- **numpy** (cálculo numérico)
- **matplotlib** (visualizaciones)
- **Google Colab / Jupyter** (entorno de ejecución)



## 📌 **Conclusión**

Con base en los ingresos, la satisfacción del cliente (calificación), el mix y desempeño de productos/categorías y el costo de envío, el notebook calcula un score de ineficiencia y recomienda qué tienda vender.
Esta recomendación está respaldada por tablas y visualizaciones, y puede ajustarse modificando los pesos del score si el contexto de negocio lo requiere.
