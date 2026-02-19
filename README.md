# securecode README

[**Link**](https://marketplace.visualstudio.com/items?itemName=PawlaDev.securecode)

**Escanea tu código en busca de vulnerabilidades OWASP Top 10 directamente desde VSCode.**

---

## Descripción

**SecureCode** es una extensión para Visual Studio Code que ayuda a detectar posibles vulnerabilidades basadas en OWASP Top 10 en archivos de código fuente (JavaScript, PHP, Python y HTML).  
Se integra en el editor como una vista lateraly permite ejecutar, con un solo clic, un escaneo de patrones inseguros (inyecciones, fallos de control de acceso, configuraciones erróneas, etc.). Todos los hallazgos aparecen resaltados en el editor y agrupados por nivel de riesgo (Grave, Medio, Bajo o Sugerencia).

---

## Características

- **Escaneo rápido en múltiples lenguajes**  
  Analiza código JavaScript, PHP, Python y HTML en busca de patrones inseguros (inyección SQL, XSS, SSRF, etc).

- **Clasificación por niveles de riesgo**  
  Los hallazgos se agrupan automáticamente en:  
  - 🔴 **Grave**  
  - 🟠 **Medio**  
  - 🟡 **Bajo**  
  - 🟢 **Sugerencia**

- **Interfaz visual en la barra lateral**  
  - Muestra el total de vulnerabilidades encontradas.  
  - Permite expandir/contraer cada nivel de riesgo para ver los títulos y líneas afectadas.  
  - Enlaces directos para saltar a la línea exacta en el editor.

- **Panel de detalles**  
  Al hacer clic en “Detalles”, se abre un panel con:  
  - Explicación de la vulnerabilidad  
  - Recomendaciones de mitigación  
  - Enlace a la documentación oficial de OWASP

- **Configuración personalizable**  
  Puedes habilitar o deshabilitar reglas específicas según categoría OWASP (Broken Access Control, Injection, etc.) desde la configuración de VSCode.

---

## Requisitos

- Visual Studio Code **1.90.0** o superior  
- Node.js (solo para compilación/empacado, no necesario en tiempo de ejecución)  
- Permisos de lectura/escritura en el proyecto donde quieras escanear los archivos

---

## Instalación

1. **Tienda de extensiones de VSCode**  
   Busca “SecureCode” en el Marketplace y haz clic en “Instalar”.

2. **Instalación manual (.vsix)**  
   Si ya tienes el paquete `.vsix`, abre una terminal y ejecuta:
   ```bash
   code --install-extension securecode-1.0.0.vsix

---

## Uso

**Abrir el menú principal**
1. En el panel lateral de Visual Studio Code, haz clic en el icono de SecureCode.

![Logo](resources/image.png)

2. Ahí verás el menú principal, donde inicialmente aparece "🐶 0 problemas detectados"

**Ejecutar un análisis**
Dentro del menú principal, haz clic en el botón de analizar (▶️) para iniciar un escaneo del archivo abierto en el editor

**Interpretar los resultados**
- Tras ejecutar el análisis, el menú se actualiza mostrando:
    - Total de problemas detectados
    - Desplegables por nivel de riesgo:
        - 🔴 Grave  
        - 🟠 Medio  
        - 🟡 Bajo  
        - 🟢 Sugerencia
    - Si no se han detectado vulnerabilidades para un nivel, aparecerá un (0) y, al desplegarlo, el mensaje "No se encontraron posibles vulnerabilidades."
    - Dentro de cada sección se incluye un listado con:
        - Título de la vulnerabilidad encontrada
        - Enlace "(línea x)" que lleva directamente al lugar afectado en el editor.
        - Enlace "Detalles" para abrir el panel con información completa.

**Ver detalles de una vulnerabilidad**
1. Haz clic en Detalles, junto a la vulnerabilidad elegida.
2. Se abrirá otro panel a la derecha del editor con:
    - Nombre de la herramienta
    - Título y nivel de riesgo de la vulnerabilidad
    - Línea en la que se encuentra
    - Categoría correspondiende dentro del OWASP Top 10 2021
    - Tres secciones:
        - **Explicación**: Descripción de la vulnerabilidad
        - **Posibles soluciones**: Recomendaciones concretas para su mitigación
        - **Más información**: Enlace a la documentación oficial OWASP


---

## Configuración
En el menú de la herramienta, haz clic en el icono de ajustes (⚙️). Aquí encontraras opciones para habilitar o deshabilitar relgas por categoría OWASP:


---

### 1.0.0 (06-06-2025)

- Primera versión pública.
- Soporte para análisis de JavaScript, PHP, Python y HTML.
- Clasificación por niveles de riesgo y panel de detalles con recomendaciones OWASP.

---

¡Gracias por usar SecureCode! Si tienes dudas, sugerencias o encuentras algún bug, abre un issue en GitHub o contáctame:

GitHub: PawlaDev
