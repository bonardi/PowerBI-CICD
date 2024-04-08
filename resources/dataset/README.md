# PowerBI&CICD - dataset

Este proyecto contiene 2 pipelines que automatizan tareas relacionadas con el manejo y análisis de archivos PBIX en Power BI utilizando diferentes herramientas y enfoques.

## Pipeline 1: ci-pipelines-scan

### Descripción
Esta pipeline utiliza TabularEditor para analizar el dataset en busca de posibles problemas o violaciones de las mejores prácticas. Descarga y configura TabularEditor, luego genera y muestra un informe de análisis.

### Configuración
- **Desencadenador:** No tiene activación automática.

## Pipeline 2: cd-deployment

### Descripción
Esta pipeline actualiza nuestro dataset en el servicio de Power BI. Descarga la herramienta TabularEditor para subir nuestro dataset al servicio y utiliza PowerBIActions para realizar el refresco.

### Configuración
- **Desencadenador:** Se activa en cada confirmación en la rama "main".
- **Refresh**: Se refrescara los datos del dataset para tenerlos actualizados con el nuevo despliegue.
