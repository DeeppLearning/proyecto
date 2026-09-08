# Sistema de Inteligencia y Observatorio de Contratación Pública TIC (SECOP I & II)

Plataforma analítica empresarial para la auditoría, análisis multidimensional y modelado predictivo de la contratación pública en el sector TIC en Colombia (2015–2025).

---

## Características Principales

- **Motor DuckDB In-Memory**: Consultas analíticas ultrarrápidas sobre más de 213,000 contratos directamente desde archivos Parquet.
- **Flujo Macro -> Micro**: Análisis territorial a nivel nacional (32 departamentos) con enfoque detallado en Antioquia y Bogotá/Cundinamarca.
- **Estudio Multidimensional (OLAP Pivot)**: Agregaciones dinámicas por departamento, entidad, subsector, modalidad y rangos de contratación.
- **Sistema de Comparación Avanzado**: Comparativas de métricas clave, tasas de prórroga y distribución de inversión.
- **Generador de Reportes Ejecutivos en PDF**: Emisión de reportes oficiales de alta fidelidad con ReportLab.
- **Modelos de Machine Learning**: Detección de anomalías de contratación, clustering de proveedores y predicción de prórrogas.

---

## Requisitos y Configuración

### 1. Clonar el repositorio
```bash
git clone <URL_DEL_REPOSITORIO>
cd <CARPETA_DEL_REPOSITORIO>
```

### 2. Instalar dependencias
```bash
pip install -r requirements.txt
```

### 3. Ejecutar la plataforma
```bash
python app_visual/servidor_visual.py
```
Abrir en el navegador: `http://localhost:8050`

---

## Estructura del Repositorio

```text
├── app_visual/
│   ├── servidor_visual.py       # Servidor HTTP, API REST y Frontend SPA integrado
│   ├── calcular_ml_real.py      # Pipelines de evaluación y ML
│   └── generar_guia_pdf.py      # Generador de documentación técnica en PDF
├── data/
│   ├── parquet/                 # Conjuntos de datos procesados (SECOP TIC)
│   └── checkpoints/             # Checkpoints de extracción y normalización
├── acotar_industria_tic.py      # Reglas y filtrado de taxonomía TIC
├── auditar_datos_reales.py      # Auditoría de integridad de valores y contratos
├── normalizar_departamentos.py  # Estandarización geográfica DANE
├── requirements.txt             # Dependencias del proyecto
└── README.md
```

---

## Licencia y Datos
Datos de origen público tomados de la Agencia Nacional de Contratación Pública - Colombia Compra Eficiente (SECOP I y SECOP II vía Datos Abiertos Colombia / Socrata API).
