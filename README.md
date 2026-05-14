# Sistema de Registro de Producción - Retenes Córdoba

Este repositorio contiene una aplicación de Power Apps diseñada para la gestión y digitalización del registro de producción en la planta de Retenes Córdoba. La solución reemplaza los formularios físicos, permitiendo una carga de datos más ágil y precisa directamente desde la línea de producción.

## 🚀 Funcionalidades Principales

### 1. Generación Automática de Identificadores (NP)
La aplicación genera automáticamente un código de **Nota de Pedido (NP)** único para cada registro, combinando el prefijo "NP-" con la fecha y hora exacta de la carga. Esto garantiza la trazabilidad sin intervención del operario.
- **Lógica:** `If(FormMode.New, "NP-" & Text(Now(), "dd/mm/yyyy HH:mm"), Parent.Default)`
<img width="269" height="443" alt="image" src="https://github.com/user-attachments/assets/efc67b78-1883-4738-832b-8750aaf02e2b" />



### 2. Interfaz de Usuario Optimizada (UX)
- **Diseño Responsivo:** La interfaz utiliza contenedores dinámicos que ajustan los elementos según el dispositivo (tablet o PC).
- **Grilla de Carga Simétrica:** Los campos de datos están organizados en una estructura de dos columnas para facilitar la lectura rápida.
- **Campos Automatizados:** Los campos obligatorios del sistema (como *Title*) funcionan en segundo plano, manteniendo la interfaz limpia de datos técnicos redundantes.
<img width="1903" height="823" alt="image" src="https://github.com/user-attachments/assets/db8935f4-7197-4b40-b745-c0c5b2f59f99" />


### 3. Registro Detallado de Operaciones
El formulario permite capturar toda la información crítica del proceso:
- **Producto y Proceso:** Selección vinculada a la base de datos de SharePoint.
- **Control de Cantidades:** Campos específicos para *Cantidad Producida* y *Cantidad Descarte*.
- **Gestión de Turnos y Operarios:** Identificación del personal y el horario de trabajo.
- **Anotaciones:** Espacio para observaciones adicionales sobre el estado de la producción.
<img width="973" height="531" alt="image" src="https://github.com/user-attachments/assets/a947adf3-e8d4-4dbf-a7bb-a17a282ea911" />


### 4. Integración con SharePoint
Todos los datos se sincronizan en tiempo real con una lista de SharePoint, que actúa como base de datos centralizada, permitiendo:
- Almacenamiento seguro.
- Historial completo de producción.
- Exportación de datos para análisis posterior.
<img width="1603" height="551" alt="image" src="https://github.com/user-attachments/assets/4e13285b-3a56-49c4-863b-436ed62c3068" />
## 🛠️ Tecnologías Utilizadas
- **Microsoft Power Apps:** Desarrollo de la interfaz low-code y lógica de negocio.
- **SharePoint Online:** Motor de base de datos y gestión de listas.
- **Power Fx:** Lenguaje de fórmulas para automatización de propiedades.

## 📋 Requisitos e Instalación
1. Importar el archivo `.msapp` en el entorno de Power Apps.
2. Configurar la conexión a la lista de SharePoint correspondiente.
3. Asegurarse de que el usuario tenga permisos de edición en la lista de origen.

---
*Desarrollado por Oliverio Arce*
