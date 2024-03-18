# PowerBI&CICD - report

Este proyecto contiene tres pipelines que automatizan tareas relacionadas con el manejo y análisis de archivos PBIX en Power BI utilizando diferentes herramientas y enfoques.

## Pipeline 1: cd-pipelines-build-cloudAgent

### Descripción
Esta pipeline actualiza un informe PBIX en un repositorio Git y despliega los cambios en un servicio de Power BI. Descarga la herramienta PBI-tools para compilar el informe PBIX, lo actualiza en el repositorio Git y luego lo publica en el servicio de Power BI.

### Configuración
- **Desencadenador:** Se activa en cada confirmación en la rama "main".

## Pipeline 2: ci-pipelines-scan

### Descripción
Esta pipeline utiliza PBI-InspectorCli para analizar un informe PBIX en busca de posibles problemas o violaciones de las mejores prácticas. Descarga y configura PBI-InspectorCli, luego genera y muestra un informe de análisis.

### Configuración
- **Desencadenador:** No tiene activación automática.

## Pipeline 3: ci-pipelines-unzip-cloudAgent

### Descripción
Esta pipeline extrae la información de un informe PBIX y la actualiza en un repositorio Git. Descarga la herramienta PBI-tools para extraer la información del informe PBIX, luego actualiza el repositorio Git con los archivos extraídos.

### Configuración
- **Desencadenador:** Se activa en cada confirmación en una rama diferente a "main".
- **Parámetros:**
- **cleanDirectory:** Indica si se debe limpiar el directorio antes de la extracción. Por defecto, se establece en "true".
