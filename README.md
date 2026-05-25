# Frontend - Innovatech Chile 🇨🇱

Este repositorio contiene la aplicación cliente (Frontend) del sistema de gestión de despachos.

## 🛠️ Especificaciones Técnicas
- **Tecnología Base:** Node.js (SPA)
- **Servidor de Producción:** Nginx (Imagen ultra ligera Alpine)
- **Seguridad (IE2):** Configurado con usuario **No-Root** (`USER nginx`) en el puerto interno `8080` para mitigar riesgos de elevación de privilegios.
- **Optimización (IE1):** Implementación de **Multi-stage build** para separar el entorno de desarrollo del código compilado final en producción.

## 🚀 Pipeline de Despliegue (IE4)
Cualquier cambio sobre la rama `deploy` gatilla un flujo automatizado en GitHub Actions que compila la imagen, la sube a Docker Hub y actualiza de forma transparente el servicio en la instancia AWS EC2.