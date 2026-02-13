# 🤖 Smart-Support-Bot-v1: Automatización con Clasificación Dinámica

Este proyecto consiste en un sistema de soporte inteligente desarrollado en **n8n**. El bot no solo recibe consultas, sino que utiliza una API externa para enriquecer los datos del usuario, toma decisiones basadas en el género detectado y gestiona tiempos de respuesta asíncronos para mejorar la experiencia del cliente.

## 🚀 Funcionalidades

* **Recepción vía Formulario:** Captura nombre, email y mensaje del usuario en tiempo real.
* **Enriquecimiento con API:** Conexión con `api.genderize.io` para predecir el género del usuario a partir de su nombre.
* **Lógica de Segmentación (IF):** Clasifica la comunicación en dos ramas (Masculino / Femenino o No Detectado) para personalizar el trato.
* **Gestión de Tiempos (Wait):** Implementación de pausas controladas de 2 minutos antes de ejecutar las acciones finales, simulando un proceso de revisión.
* **Notificaciones Automatizadas:** Envío de correos electrónicos personalizados vía **Gmail** con saludos dinámicos.
* **Base de Datos Organizada:** Registro automático de la consulta en **Google Sheets**, separando a los usuarios en diferentes pestañas según su categoría.

## 🛠️ Stack Tecnológico

* **n8n:** Orquestador principal del workflow.
* **HTTP Request:** Para el consumo de la API REST externa.
* **Gmail & Google Sheets:** Integraciones de productividad para salida de datos.
* **JSON:** Estructura de intercambio de datos entre nodos.

## 📖 Cómo utilizarlo

1. Importa el archivo `.json` en tu instancia de n8n.
2. Configura tus credenciales de Gmail y Google Sheets.
3. Asegúrate de tener habilitadas las APIs de Google Drive y Google Sheets en tu consola de Google Cloud.
4. Ejecuta el trigger y completa el formulario para ver la automatización en acción.

---
> *Proyecto desarrollado para practicar flujos avanzados, integración de APIs y lógica condicional en herramientas No-Code.*
