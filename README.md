# 🌐 Daraflow

**A Prompt to AI File Semantic Parser**  
Daraflow te permite transformar *Prompts* en **APIs listas para usar**, capaces de recibir documentos y devolver salidas estructuradas en JSON, sin necesidad de programar nada.  

🔓 Proyecto OSS liberado bajo **AGPLv3** para asegurar que siempre permanezca libre y que cualquier uso en SaaS deba compartir sus mejoras con la comunidad.  

---

## ✨ Características principales
- 📝 **Prompt → API**: define un prompt y Daraflow lo convierte en un endpoint REST.  
- 📂 **Entrada flexible**: envía documentos (PDF, TXT, DOCX, CSV, JSON, etc.).  
- 🤖 **Interpretación semántica** mediante LLM (ej. Gemini, OpenAI, OSS models).  
- 📊 **Salida estructurada en JSON** lista para consumir en tu app o sistema.  
- 🐳 **Docker Ready**: despliegue rápido en cualquier entorno.  
- 🎨 **UI Gráfica**: interfaz simple para crear, probar y gestionar tus APIs.  

---

## 🚀 Instalación

### Opción 1: Docker
```bash
docker run -d \
  --name daraflow \
  -p 8080:8080 \
  ghcr.io/daraflow/daraflow:latest
