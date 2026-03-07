# 📡 TelecomX Challenge - Análisis de Churn de Clientes

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0+-green.svg)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**Desafío Alura LatAm** - Análisis predictivo de cancelación de servicios (churn) en una empresa de telecomunicaciones.

---

## 📋 Tabla de Contenidos

- [Objetivo](#-objetivo)
- [Contexto del Negocio](#-contexto-del-negocio)
- [Metodología](#-metodología)
- [Instalación](#-instalación)
- [Uso](#-uso)
- [Resultados Clave](#-resultados-clave)
- [Tecnologías](#-tecnologías)
- [Autor](#-autor)
- [Licencia](#-licencia)

---

## 🎯 Objetivo

Identificar los factores que más influyen en la cancelación de servicios de telecomunicaciones y desarrollar un análisis exploratorio que permita:

- **Comprender** la distribución del churn entre los clientes
- **Identificar** las variables con mayor impacto predictivo
- **Proveer** insights accionables para estrategias de retención
- **Reducir** la tasa de cancelación del 26.6% actual

---

## 🏢 Contexto del Negocio

**TelecomX** enfrenta una tasa de cancelación del **26.6%**, lo que representa un desafío significativo para la retención de clientes y la rentabilidad del negocio.

**Problema:** De cada 100 clientes, aproximadamente 27 cancelan el servicio, generando pérdidas económicas y afectando el crecimiento sostenible.

**Solución:** Análisis de datos para identificar patrones de comportamiento y factores de riesgo que permitan intervenciones proactivas.

---

## 🔬 Metodología

### 1️⃣ **Preparación y Estandarización de Datos**
- Traducción de columnas y valores al español
- Normalización de categorías (Sí/No, Femenino/Masculino, etc.)
- Limpieza de valores nulos y vacíos
- Conversión de tipos de datos

### 2️⃣ **Análisis de Impacto de Variables**

**Para variables categóricas:**
```
Impacto = Tasa de churn MÁS ALTA − Tasa de churn MÁS BAJA
```

**Para variables numéricas:**
```
Impacto = |Correlación con churn| × 100
```

### 3️⃣ **Visualización y Segmentación**
- Gráficos de barras con degradado de colores
- Distribución de cancelaciones por categoría
- Identificación de segmentos de alto riesgo

### 4️⃣ **Generación de Insights Accionables**
- Ranking de variables por impacto
- Recomendaciones estratégicas por segmento
- Plan de acción priorizado

---

## 📦 Instalación

### Requisitos previos
- Python 3.8 o superior
- pip (gestor de paquetes de Python)

### Pasos

1. **Clonar el repositorio:**
```bash
git clone https://github.com/NULLPX-a/TelecomX_Challenge_Alura_latam.git
cd TelecomX_Challenge_Alura_latam
```

2. **Instalar dependencias:**
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

3. **Ejecutar el notebook:**
```bash
jupyter notebook TelecomX_challenge_2.ipynb
```

---

## 🚀 Uso

### Análisis Rápido

El notebook está estructurado en celdas modulares que pueden ejecutarse secuencialmente:

1. **Imports y configuración** - Carga de librerías
2. **Carga y limpieza de datos** - Preparación del dataset
3. **Estandarización** - Traducción y normalización
4. **Cálculo de impacto** - Ranking de variables
5. **Visualizaciones** - Gráficos y análisis
6. **Conclusiones** - Insights y recomendaciones

### Personalización

Para analizar variables específicas:

```python
# Modificar la lista de variables
variables_categoricas = ['tipo_contrato', 'servicio_internet', ...]
variables_numericas = ['meses_contrato', 'cargo_mensual', ...]

# Ejecutar análisis
df_impactos = calcular_impacto_variable(df, variables_categoricas)
```

---

## 📊 Resultados Clave

### Tasa Global de Churn
**26.6%** - Porcentaje de clientes que cancelan el servicio

### Top 5 Variables con Mayor Impacto

| Rank | Variable | Impacto | Tipo |
|------|----------|---------|------|
| 1 | **tipo_contrato** | 39.9 | Diferencia % |
| 2 | **meses_contrato** | 35.4 | Correlación % |
| 3 | **servicio_internet** | 34.5 | Diferencia % |
| 4 | **seguridad_online** | 34.3 | Diferencia % |
| 5 | **soporte_tecnico** | 34.2 | Diferencia % |

### Hallazgos Principales

🔴 **Alto Riesgo:**
- Clientes con contrato **Mensual** tienen 40pp más de probabilidad de cancelar vs. Bianual
- Primeros **3 meses** de contrato son críticos (52% de churn)
- Servicio de **Fibra Óptica** sin servicios adicionales tiene mayor churn

🟢 **Factores Protectores:**
- Contratos de **largo plazo** (Bianual) → 5% churn
- Servicios adicionales (**seguridad, backup, soporte**) reducen cancelación
- **Autopago** muestra menor tasa de cancelación

---

## 🛠 Tecnologías

| Herramienta | Versión | Propósito |
|-------------|---------|-----------|
| **Python** | 3.8+ | Lenguaje de programación |
| **Pandas** | 2.0+ | Manipulación y análisis de datos |
| **NumPy** | 1.24+ | Cálculo numérico |
| **Matplotlib** | 3.7+ | Visualización de datos |
| **Seaborn** | 0.12+ | Gráficos estadísticos avanzados |
| **Jupyter** | 1.0+ | Entorno interactivo |

---

## 👨‍ Autor

**NULLPX-a**  
[GitHub](https://github.com/NULLPX-a)

**Desafío:** Alura LatAm - TelecomX Challenge

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.


---
