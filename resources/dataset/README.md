# PowerBIDaysMalaga2024 - dataset

Este proyecto consta de dos pipelines destinadas a automatizar tareas relacionadas con la gestión y análisis de modelos de inteligencia empresarial (BIM) en Power BI utilizando la herramienta Tabular Editor y Azure DevOps.

## Pipeline 1: ci-pipelines-scan

### Descripción
Esta pipeline está diseñada para realizar un análisis de mejores prácticas en un archivo BIM utilizando Tabular Editor. Después de descargar e instalar Tabular Editor, el proceso ejecuta el análisis de mejores prácticas en el archivo BIM especificado, generando un informe que se carga en los artefactos de la pipeline.

### Configuración
- **Desencadenador:** Manual (no se activa automáticamente).

</br>

## Pipeline 2: cd-pipelines-build

### Descripción
Esta pipeline se encarga de actualizar un conjunto de datos en Power BI después de realizar cambios en el modelo de inteligencia empresarial. Utiliza Tabular Editor para implementar los cambios en el modelo BIM y luego inicia una actualización del conjunto de datos en Power BI. Esta actualización puede desactivarse según la configuración de los parámetros de la pipeline.

### Configuración
- **Desencadenador:** Se activa en cada confirmación en la rama "main".
- **Parámetros:**
  - **refreshDataset:** Indica si se debe realizar la actualización del conjunto de datos en Power BI. Por defecto, se establece en "true".
