# 🛢️ Análisis de la producción de petróleo crudo en Estados Unidos

> 📊 Proyecto de análisis de datos sobre la evolución temporal, las diferencias
> regionales y la concentración de la producción petrolera estadounidense,
> utilizando datos públicos de la U.S. Energy Information Administration (EIA).

**Estado:** 🚧 En desarrollo — Fase 1: definición y organización  
**Sector:** 🛢️ Petróleo y gas · Producción de petróleo crudo  
**Cobertura:** 🌎 Estados Unidos  
**Frecuencia:** 📅 Mensual  
**Herramientas:** Excel · Power Query · MySQL · SQL · Power BI · DAX · GitHub

---

## 🎯 Objetivo del proyecto

Analizar **cómo evoluciona la producción de petróleo crudo en Estados Unidos**,
identificar las áreas que contribuyen a su crecimiento o disminución y
evaluar su concentración geográfica.

El proyecto desarrollará un proceso reproducible desde la adquisición
y limpieza de datos hasta su validación en SQL y presentación en Power BI.

## 🏭 Caso de uso

Un equipo de análisis del sector energético necesita comprender
**cuánto cambia la producción, dónde se originan esos cambios y cómo
se distribuye la actividad entre las áreas productoras**.

El análisis permitirá:

- 📈 **Seguir tendencias:** comparar la evolución de la producción.
- 🌎 **Comparar territorios:** identificar diferencias entre áreas productoras.
- 🔎 **Descomponer cambios:** determinar qué áreas aportan al aumento
  o disminución de la producción nacional.
- 🏆 **Examinar rankings:** observar cambios en las posiciones relativas.
- 🛢️ **Evaluar concentración:** medir cuánto aportan las principales áreas.

Los resultados ofrecerán contexto para el seguimiento del sector.
Las explicaciones sobre las causas de los cambios requerirán evidencia
complementaria.

## ❓ Preguntas de análisis

| Eje | Pregunta |
|---|---|
| 📈 Evolución | ¿Cómo cambia la producción a lo largo del tiempo? |
| 📉 Variaciones | ¿Qué áreas presentan los mayores aumentos y disminuciones? |
| 🔎 Contribución | ¿Qué áreas explican el cambio de la producción nacional? |
| 🏆 Posicionamiento | ¿Cómo cambia el ranking de las áreas productoras? |
| 🛢️ Concentración | ¿Qué proporción de la producción reúnen las principales áreas? |

---

## 🌎 Alcance inicial

| Dimensión | Definición |
|---|---|
| **Actividad** | Producción de petróleo crudo |
| **País** | Estados Unidos |
| **Frecuencia** | Mensual |
| **Cobertura geográfica** | Estados y áreas marítimas federales disponibles en la fuente |
| **Agrupación regional** | Distritos petroleros PADD, según la clasificación de la EIA |
| **Período de análisis** | Pendiente de validar la cobertura del archivo fuente |
| **Unidad original** | Pendiente de confirmar en el archivo descargado |
| **Enfoque** | Tendencias, variaciones, contribución, rankings y concentración |

> 📌 La definición del producto y sus inclusiones se documentará según
> las notas oficiales de la serie seleccionada. Esta primera versión
> se centra en petróleo crudo; el gas natural queda fuera del alcance.

## 🗃️ Fuente de datos

**U.S. Energy Information Administration (EIA)**

Organismo de referencia para los datos utilizados en este proyecto.

- 🛢️ [Serie de producción de petróleo crudo](https://www.eia.gov/dnav/pet/pet_crd_crpdn_adc_mbblpd_m.htm)
- 🌐 [Portal de petróleo y otros líquidos](https://www.eia.gov/petroleum/data.php)

Se conservará una **copia del archivo original** y se documentarán:

- Fecha de descarga.
- Cobertura temporal y geográfica.
- Definición del producto y unidades.
- Códigos especiales y valores faltantes.
- Transformaciones realizadas.

---

## ⚙️ Herramientas y proceso analítico

| Herramienta | Función prevista |
|---|---|
| **Excel y Power Query** | Inspección, limpieza y transformación de datos |
| **MySQL Workbench y SQL** | Consultas, controles de calidad y validación de indicadores |
| **Power BI y DAX** | Modelo de datos, medidas y visualizaciones |
| **GitHub** | Control de versiones, documentación y publicación |

### 🧭 Ruta de trabajo

**Fuente EIA → Preparación → SQL → KPIs → Power BI → Validación → Hallazgos**

Cada fase se dividirá en bloques con **resultados esperados y controles
antes de avanzar**.

<details>
<summary><strong>📋 Consultar las ocho fases del proyecto</strong></summary>

1. **Definición y organización:** objetivo, alcance, preguntas y repositorio.
2. **Adquisición y limpieza:** conservación del original, preparación
   y diccionario de datos.
3. **Análisis en SQL:** carga, controles de calidad y exploración.
4. **Definición y validación de KPIs:** fórmulas, unidades y reglas
   de agregación.
5. **Modelo de datos:** tablas, calendario, relaciones y validación
   en Power BI.
6. **Medidas y dashboards:** cálculos DAX, visualizaciones y contraste
   con SQL.
7. **Auditoría de calidad:** consolidación de controles, conciliaciones
   y limitaciones.
8. **Publicación y cierre:** conclusiones, README definitivo, imágenes
   y demostración del informe.

La calidad se comprobará durante todo el proceso; la fase 7 reunirá
la evidencia de esas validaciones.

</details>

## 🧪 Criterios de calidad

| Control | Propósito |
|---|---|
| **Unicidad** | Verificar una observación por período y área en la tabla analítica |
| **Continuidad temporal** | Detectar meses ausentes dentro del período seleccionado |
| **Valores especiales** | Distinguir ceros, datos no disponibles y otros códigos de la fuente |
| **Coherencia geográfica** | Evitar duplicar áreas o sumar componentes junto con sus subtotales |
| **Unidades y agregación** | Diferenciar volúmenes mensuales de tasas promedio diarias |
| **Conciliación** | Contrastar las agregaciones con los totales de referencia |
| **Validación cruzada** | Comparar los indicadores de Power BI con los resultados de SQL |
| **Trazabilidad** | Documentar transformaciones, revisiones y diferencias de redondeo |

> 🔎 Una tasa diaria no se sumará entre meses como si fuera un volumen.
> Las reglas de cálculo se definirán antes de construir los indicadores.

---

## 📦 Entregables previstos

- [ ] Datos originales y datos preparados.
- [ ] Diccionario de datos y registro de transformaciones.
- [ ] Scripts SQL de análisis y validación.
- [ ] Catálogo de indicadores y reglas de cálculo.
- [ ] Modelo de datos y dashboard de Power BI.
- [ ] Auditoría de calidad.
- [ ] Hallazgos, conclusiones y limitaciones.
- [ ] Imágenes de los dashboards y demostración del informe.

## ⚠️ Limitaciones del análisis

- Los datos agregados por área geográfica no permiten evaluar
  el desempeño de **pozos individuales, equipos o empresas**.
- Una caída regional de producción no demuestra por sí sola
  el agotamiento de un yacimiento ni una falla operativa.
- Esta fuente no permite estimar por sí sola **reservas, rentabilidad
  o eficiencia de equipos**.
- Los hallazgos y las recomendaciones se incorporarán después
  de completar y validar el análisis.

## 🚧 Avance del proyecto

**Fase actual:** definición y organización.

El repositorio se actualizará progresivamente con los datos,
los controles, los análisis y los resultados de cada fase.
