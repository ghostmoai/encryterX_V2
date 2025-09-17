# EncryptorX

Bienvenido a EncryptorX, una aplicación de escritorio para Windows diseñada para proteger tus archivos mediante un cifrado robusto. Desarrollada en Python, ofrece una solución sencilla y eficaz para asegurar tu información sensible.

## Características Principales

*   **Cifrado Fuerte:** Utiliza el algoritmo AES-256 (a través de la biblioteca `cryptography`), uno de los estándares de cifrado más seguros y utilizados a nivel mundial.
*   **Interfaz Gráfica Sencilla:** Una ventana intuitiva creada con Tkinter que permite cifrar y descifrar archivos fácilmente.
*   **Arrastrar y Soltar (Drag & Drop):** Agiliza el proceso permitiendo arrastrar archivos directamente a la aplicación.
*   **Actualizaciones Automáticas:** El programa verifica si hay nuevas versiones disponibles en el repositorio de GitHub y notifica al usuario.
*   **Código Abierto:** El proyecto es completamente de código abierto, permitiendo su revisión, uso y modificación libremente bajo los términos de su licencia.

## Instalación

Puedes instalar EncryptorX usando el ejecutable `setup.exe` que se encuentra en la carpeta `dist` después de la compilación.

### Instalación Gráfica

Simplemente haz doble clic en `setup.exe` y sigue las instrucciones. El instalador solicitará permisos de administrador para copiar los archivos en `C:\Program Files` y registrar la aplicación.

### Instalación desde la Terminal

El instalador también puede ser ejecutado desde la línea de comandos.
1.  Abre una terminal (CMD o PowerShell).
2.  Navega hasta el directorio donde se encuentra `setup.exe`.
3.  Ejecuta `.\setup.exe` para una instalación interactiva o `.\setup.exe -y` para una **instalación silenciosa** que acepta la licencia automáticamente.
4.  Para desinstalar, usa `.\setup.exe --uninstall` (o `.\setup.exe --uninstall -y` para que no pida confirmación al final).

## ¿Cómo Funciona?

EncryptorX toma un archivo y una contraseña proporcionada por el usuario. A partir de la contraseña, genera una clave de cifrado segura y la utiliza para encriptar el contenido del archivo con AES-256. El archivo resultante (`.enc`) contiene los datos cifrados y la información necesaria para su posterior descifrado. Solo con la contraseña original se puede revertir el proceso.

## Uso desde la Terminal

Una vez instalado, puedes usar `EncryptorX` directamente desde cualquier terminal gracias a que el instalador lo añade al PATH del sistema.

*   **Encriptar texto:** `EncryptorX --encryter "mi texto secreto"`
*   **Desencriptar texto:** `EncryptorX --descryter "gAAAAAB..."`
*   **Encriptar un archivo:** `EncryptorX --encryter-arc "C:\ruta\a\mi\archivo.txt"`
*   **Desencriptar un archivo:** `EncryptorX --descryter-arc "C:\ruta\a\mi\archivo.txt.enc"`
*   **Abrir la interfaz gráfica:** `EncryptorX`

## Instalación desde el Código Fuente (para Desarrolladores)

Si prefieres no usar el instalador o quieres ejecutar la última versión directamente desde el código, puedes clonar el repositorio. Esto es ideal para usuarios de Linux, macOS o desarrolladores en Windows.

**Requisitos:**
*   Git
*   Python 3 y pip

**Pasos:**

1.  **Clonar el repositorio:**
    Abre una terminal y ejecuta el siguiente comando para descargar el código fuente.
    ```bash
    git clone https://github.com/tio-radio/encryterX_V2.git
    ```

2.  **Navegar al directorio del proyecto:**
    ```bash
    cd EncryptorX
    ```

3.  **Instalar las dependencias:**
    La aplicación necesita algunas bibliotecas de Python para funcionar. Instálalas usando pip y el archivo `requirements.txt` incluido.
    ```bash
    pip install -r requirements.txt
    ```

4.  **Ejecutar la aplicación:**
    Ahora puedes usar `EncryptorX` como una herramienta de línea de comandos. Por defecto, se ejecutará en modo terminal.
    ```bash
    python EncryptorX.py --help
    ```

## Compilación

El proyecto incluye un script (`copilador_V2.py`) que automatiza todo el proceso de compilación usando **PyInstaller**. Este script se encarga de:
1.  Compilar la aplicación principal (`EncryptorX.py`) en un ejecutable (`EncryptorX.exe`).
2.  Compilar el script del instalador (`installer.py`) en su propio ejecutable (`setup.exe`).
3.  Empaquetar los archivos necesarios, como la licencia, en una carpeta `dist` lista para su distribución.

## Licencia

Este proyecto se distribuye bajo la licencia especificada en el archivo `Licencia Pública – EncryptorX.txt`.

---

> **Descargo de Responsabilidad**
>
> Este software se proporciona 'tal cual', sin garantías de ningún tipo, expresas o implícitas. El autor, `tio radio`, no se hace responsable de ninguna pérdida de datos o daño que pueda resultar del uso (o mal uso) de esta aplicación.
>
> **¡Es fundamental que realices copias de seguridad de tus archivos importantes antes de cifrarlos!**
