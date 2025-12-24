# Guía de Configuración de ESP32 para Proyectos de EEZ Studio

Esta guía te ayudará a configurar el IDE de Arduino con soporte para placas ESP32 para usar con proyectos LVGL de EEZ Studio.

## Requisitos Previos

- Arduino IDE 1.8.x o 2.x instalado
- Conexión a Internet

## Instalación del Paquete de Placas ESP32 en Arduino IDE

### Método 1: Usando Arduino IDE 2.x (Recomendado)

1. **Abre Arduino IDE 2.x**

2. **Agrega la URL del Gestor de Placas ESP32:**
   - Ve a `Archivo` → `Preferencias` (o `Arduino IDE` → `Configuración` en macOS)
   - En el campo "URLs Adicionales de Gestor de Placas", agrega:
     ```
     https://espressif.github.io/arduino-esp32/package_esp32_index.json
     ```
   - Haz clic en `Aceptar`

3. **Instala el Paquete de Placas ESP32:**
   - Ve a `Herramientas` → `Placa` → `Gestor de Placas`
   - En el cuadro de búsqueda, escribe `esp32`
   - Encuentra **"esp32 por Espressif Systems"**
   - Selecciona la versión que desees:
     - **Recomendado: Última versión estable (3.0.x o más reciente)**
     - Para compatibilidad con proyectos antiguos: versión 2.0.x
   - Haz clic en `Instalar`
   - Espera a que se complete la instalación

### Método 2: Usando Arduino IDE 1.8.x

1. **Abre Arduino IDE 1.8.x**

2. **Agrega la URL del Gestor de Placas ESP32:**
   - Ve a `Archivo` → `Preferencias`
   - En el campo "URLs Adicionales de Gestor de Placas", agrega:
     ```
     https://espressif.github.io/arduino-esp32/package_esp32_index.json
     ```
   - Haz clic en `Aceptar`

3. **Instala el Paquete de Placas ESP32:**
   - Ve a `Herramientas` → `Placa` → `Gestor de Placas`
   - En el cuadro de búsqueda, escribe `esp32`
   - Encuentra **"esp32 por Espressif Systems"**
   - Selecciona la versión que desees
   - Haz clic en `Instalar`

## Solución de Problemas Comunes

### Problema: Falla la Instalación del Gestor de Placas

**Problema:** La descarga falla o se agota el tiempo al instalar el paquete de placas ESP32

**Soluciones:**

1. **Verifica tu conexión a Internet**
   - Asegúrate de tener una conexión estable a Internet
   - Intenta desactivar VPN o proxy temporalmente

2. **Limpia la caché de Arduino:**
   - Cierra Arduino IDE
   - Elimina la carpeta de caché:
     - **Windows:** `C:\Users\<TuNombreDeUsuario>\AppData\Local\Arduino15\`
     - **macOS:** `~/Library/Arduino15/`
     - **Linux:** `~/.arduino15/`
   - Reinicia Arduino IDE e intenta nuevamente

3. **Usa instalación manual:**
   - Descarga el paquete manualmente desde: https://github.com/espressif/arduino-esp32
   - Sigue las instrucciones de instalación manual en el repositorio

4. **Prueba una versión diferente:**
   - Si la versión 3.3.5 específicamente falla, prueba:
     - Última versión estable (serie 3.0.x)
     - O versión estable 2.0.17
   - Nota: La versión 3.3.5 puede no existir; verifica las versiones disponibles en el Gestor de Placas

5. **Verifica firewall/antivirus:**
   - Desactiva temporalmente el firewall o antivirus
   - Agrega Arduino IDE a la lista de excepciones

### Problema: La Placa No Aparece en el Menú de Herramientas

**Problema:** Después de la instalación, la placa ESP32 no aparece en la lista de placas

**Soluciones:**

1. **Reinicia Arduino IDE**
   - Cierra y vuelve a abrir Arduino IDE completamente

2. **Verifica la instalación:**
   - Revisa `Herramientas` → `Placa` → `ESP32 Arduino`
   - Deberías ver varias opciones de placas ESP32

3. **Reinstala el paquete:**
   - Ve al Gestor de Placas
   - Encuentra el paquete ESP32
   - Haz clic en `Desinstalar`
   - Haz clic en `Instalar` nuevamente

## Versiones Recomendadas del Paquete de Placas ESP32

- **Para proyectos nuevos:** Versión 3.0.x (última estable)
- **Para compatibilidad heredada:** Versión 2.0.17
- **Mínima soportada:** Versión 2.0.0

## Verificación de la Instalación

1. Ve a `Herramientas` → `Placa` → `ESP32 Arduino`
2. Deberías ver opciones de placas como:
   - ESP32 Dev Module
   - ESP32-S2 Dev Module
   - ESP32-S3 Dev Module
   - ESP32-C3 Dev Module
   - Y muchas más...

## Uso de ESP32 con EEZ Studio

Una vez que tengas instalado el soporte para placas ESP32:

1. **Crea o abre un proyecto LVGL de EEZ Studio**
2. **Configura los ajustes de compilación** en EEZ Studio:
   - Establece la carpeta de destino para el código generado
   - Configura la ruta de inclusión de LVGL
3. **Compila el proyecto** en EEZ Studio
4. **Abre el sketch de Arduino generado**
5. **Selecciona tu placa ESP32** en Arduino IDE
6. **Selecciona el puerto COM** para tu ESP32
7. **Sube a tu placa ESP32**

## Proyectos de Ejemplo ESP32

Consulta estos proyectos de ejemplo que usan EEZ Studio con ESP32:

- [Nscreen_32-esp32-eez-flow-demo](https://github.com/eez-open/Nscreen_32-esp32-eez-flow-demo)
- [esp32-lvgl-eez-demo](https://github.com/eez-open/esp32-lvgl-eez-demo)

## Recursos Adicionales

- [Documentación del Núcleo Arduino ESP32](https://docs.espressif.com/projects/arduino-esp32/en/latest/)
- [GitHub del Núcleo Arduino ESP32](https://github.com/espressif/arduino-esp32)
- [Documentación de EEZ Studio](https://github.com/eez-open/studio)
- [Documentación de LVGL](https://docs.lvgl.io/)

## Obtener Ayuda

Si continúas experimentando problemas:

1. Revisa los [Issues de EEZ Studio](https://github.com/eez-open/studio/issues)
2. Visita el [Discord de EEZ Studio](https://discord.gg/q5KAeeenNG)
3. Consulta los [Issues del Núcleo Arduino ESP32](https://github.com/espressif/arduino-esp32/issues)

---

## Nota Importante sobre la Versión 3.3.5

Si estás intentando instalar específicamente la versión **3.3.5** del paquete ESP32 y falla:

**La versión 3.3.5 no existe oficialmente.** Las versiones del paquete ESP32 para Arduino IDE siguen este patrón:
- Serie 1.x: Versiones antiguas (descontinuadas)
- Serie 2.x: 2.0.0 hasta 2.0.17 (estables)
- Serie 3.x: 3.0.0 y superiores (más recientes)

**Versiones recomendadas para usar:**
- **3.0.7** - Última versión estable de la serie 3.x (recomendada para nuevos proyectos)
- **2.0.17** - Última versión estable de la serie 2.x (recomendada para compatibilidad)

**Cómo verificar versiones disponibles:**
1. Abre el Gestor de Placas en Arduino IDE
2. Busca "esp32"
3. Haz clic en el menú desplegable de versiones del paquete "esp32 by Espressif Systems"
4. Verás todas las versiones disponibles para instalar

Si alguien te indicó usar la versión 3.3.5, probablemente se refirió a:
- Versión **3.0.5** (existe)
- O la última versión estable de la serie 3.x
