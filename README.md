# Dashboard de KPIs Financieros y Comerciales — Excel

> Proyecto de práctica en análisis de datos y seguimiento de objetivos comerciales usando Microsoft Excel avanzado.

---

## Herramienta utilizada: Microsoft Excel

Excel es una de las herramientas más utilizadas en el mundo del análisis de datos y la gestión empresarial. En este proyecto se aprovecharon sus capacidades avanzadas para construir un sistema de control de KPIs (Key Performance Indicators) completamente funcional, sin necesidad de herramientas externas.

**¿Por qué Excel para este proyecto?**
- Permite construir dashboards interactivos con **Tablas Dinámicas** y **segmentadores**
- Soporta fórmulas condicionales para calcular estados de cumplimiento en tiempo real
- Es ampliamente adoptado en entornos empresariales, lo que lo hace ideal para reportes reproducibles
- Facilita la visualización rápida de métricas sin infraestructura adicional

---

## Objetivo del Proyecto

Crear un sistema de seguimiento de KPIs para una empresa del sector de distribución de productos agrícolas/alimentarios, que permita:

- Monitorear el desempeño de vendedores frente a sus objetivos de kilogramos vendidos
- Comparar el rendimiento del año actual vs. el año anterior
- Controlar el cumplimiento de metas por producto
- Visualizar la evolución mensual acumulada de ventas

---

## Estructura del Archivo

El archivo `KPI-Fin.xlsx` está organizado en **2 hojas de trabajo**:

### 1. `Control Objetivos` — Hoja principal del dashboard
Concentra todas las tablas dinámicas y métricas de control. Contiene 4 bloques de análisis:

| Bloque | Descripción |
|--------|-------------|
| **KG por Vendedor vs Objetivo** | Compara los kilogramos vendidos por cada vendedor contra su meta, con indicador de estado |
| **Variación Año Anterior por Vendedor** | Muestra el % de cumplimiento respecto al año anterior para detectar caídas o mejoras |
| **KG por Producto vs Objetivo** | Controla el rendimiento por tipo de producto (Acelga, Berenjena, Fresas, etc.) |
| **Evolución Mensual Acumulada** | Seguimiento mes a mes del acumulado de ventas para ver la progresión anual |

### 2. `Opciones` — Hoja de datos de soporte
Tabla maestra con los **objetivos de kilogramos por producto y año** (2018 y 2019), que alimenta los cálculos dinámicos del dashboard.

---

## Métricas y KPIs Calculados

```
✅ Estado por vendedor     →  Cumple / No cumple / En límite  (valores: 1 / -1 / 0)
📉 % vs Año Anterior       →  Variación porcentual interanual
📦 KG por Producto         →  Real vs Objetivo por categoría
📅 Acumulado Mensual       →  Progresión mes a mes durante el año
```

**Vendedores monitoreados:** Alvarez L. · Asurmendia D. · García P. · López M. · Ochoa A. · Pérez J.

**Productos monitoreados:** Acelga · Albaricoque · Berenjena · Calabacín · Fresas · Mandarina · Melón

---
## ¿Cómo se construyó?

### Paso 1 — Diseño de la estructura de datos
Se definió la hoja `Opciones` como tabla de configuración con objetivos por producto y año. Esto permite actualizar metas sin tocar la lógica del dashboard.

### Paso 2 — Creación de Tablas Dinámicas
Se construyeron **4 Tablas Dinámicas** independientes en la hoja `Control Objetivos`, cada una enfocada en una dimensión de análisis diferente (vendedor, producto, tiempo).

> 📸 **[FOTO: Vista general de la hoja "Control Objetivos" mostrando las 4 tablas dinámicas]**
>
> *Cómo agregarla: Abre el archivo en Excel → toma un screenshot de la hoja completa → guarda la imagen como `dashboard_general.png` en una carpeta `/assets/` dentro de tu repositorio → reemplaza esta línea con:*
> ```markdown
> ![Dashboard General](assets/dashboard_general.png)
> ```

### Paso 3 — Cálculo de estados con lógica condicional
Se implementaron columnas de **"Estado"** usando fórmulas `SI()` y comparaciones contra los objetivos de la hoja `Opciones`. El sistema de semáforo usa:
- `1` → Objetivo cumplido ✅
- `0` → En el límite ⚠️
- `-1` → Por debajo del objetivo ❌

### Paso 4 — Indicadores de comparación interanual
Se creó la columna `% KG Total Año Anterior` para calcular qué porcentaje del volumen anterior se está repitiendo en el año actual, permitiendo detectar caídas de rendimiento por vendedor.

> 📸 **[FOTO: Tabla de variación año anterior con los porcentajes por vendedor]**
>
> *Cómo agregarla: Haz zoom en la tabla de variación interanual → captura la imagen → guárdala como `variacion_interanual.png` en `/assets/` → usa:*
> ```markdown
> ![Variación Interanual](assets/variacion_interanual.png)
> ```

### Paso 5 — Control de evolución mensual
Se incluyó una tabla dinámica de seguimiento mes a mes con **acumulado progresivo**, útil para ver si el ritmo de ventas es suficiente para alcanzar el objetivo anual.

> 📸 **[FOTO: Tabla de evolución mensual acumulada]**
>
> *Cómo agregarla: Captura la tabla mensual → guarda como `evolucion_mensual.png` en `/assets/` → usa:*
> ```markdown
> ![Evolución Mensual](assets/evolucion_mensual.png)
> ```

---

## Habilidades demostradas

| Área | Detalle |
|------|---------|
| **Tablas Dinámicas** | Construcción, agrupación y relación entre hojas |
| **Fórmulas avanzadas** | Lógica condicional `SI()`, cálculos de variación porcentual |
| **Modelado de datos** | Separación entre datos de configuración y datos de análisis |
| **KPI Design** | Definición de métricas relevantes para la toma de decisiones |
| **Reporting** | Organización visual clara por bloques temáticos |

---

## Conclusiones

Este proyecto demuestra cómo Excel, bien estructurado, puede actuar como una herramienta de Business Intelligence básica. El sistema de semáforo, la comparación interanual y el acumulado mensual son patrones clásicos en reportes ejecutivos del mundo real.

---

*Proyecto de práctica — Análisis de datos y reporting con Excel*
