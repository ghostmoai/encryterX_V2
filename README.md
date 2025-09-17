# EncryptorX

Bienvenido a EncryptorX, una aplicación de escritorio para Windows diseñada para proteger tus archivos mediante un cifrado robusto. Desarrollada en Python, ofrece una solución sencilla y eficaz para asegurar tu información sensible, funcionando tanto con una interfaz gráfica como desde la línea de comandos.

## Características Principales

*   **Cifrado Fuerte:** Utiliza el algoritmo AES-256 para asegurar tus datos.
*   **Interfaz Dual:** Funciona tanto con una interfaz gráfica (GUI) como desde la línea de comandos (CLI).
*   **Instalación Sencilla:** Instala la aplicación con un solo comando desde la terminal.
*   **Actualizaciones Automáticas:** Notifica y permite instalar nuevas versiones directamente.
*   **Código Abierto:** Totalmente de código abierto y disponible en GitHub.

## Instalación

Puedes instalar EncryptorX de dos maneras:

### 1. Instalación Automática (Recomendado)

Este es el método más rápido y fácil. Abre una terminal (PowerShell o CMD) o el diálogo Ejecutar (`Win + R`) y pega el siguiente comando. Descargará e instalará la última versión de forma automática.
```powershell
powershell -command "Invoke-WebRequest -Uri 'https://github.com/ghostmoai/encryterX_V2/releases/latest/download/setup.exe' -OutFile '$env:TEMP\setup.exe'; Start-Process '$env:TEMP\setup.exe' -ArgumentList '-y' -Verb RunAs"
```

**Opción 2: Instalación Manual**
Si ya has descargado `setup.exe`, navega a su ubicación en una terminal y ejecuta `.\setup.exe` para una instalación interactiva, o `.\setup.exe -y` para una instalación silenciosa. Para desinstalar, usa `.\setup.exe --uninstall`.
### Otros Métodos

*   **Instalación Gráfica:** Descarga `setup.exe` desde la página de releases de GitHub, haz doble clic en el archivo y sigue las instrucciones.

*   **Desinstalación:** Puedes desinstalar la aplicación desde "Agregar o quitar programas" en Windows, o ejecutar el siguiente comando en una terminal para una desinstalación silenciosa:
    ```powershell
    powershell -command "& 'C:\Program Files\EncryptorX\setup.exe' --uninstall -y"
    ```

## ¿Cómo Funciona?

EncryptorX toma un archivo y una contraseña proporcionada por el usuario. A partir de la contraseña, genera una clave de cifrado segura y la utiliza para encriptar el contenido del archivo con AES-256. El archivo resultante (`.enc`) contiene los datos cifrados y la información necesaria para su posterior descifrado. Solo con la contraseña original se puede revertir el proceso.

## Uso desde la Terminal

Una vez instalado, puedes usar `EncryptorX` directamente desde cualquier terminal gracias a que el instalador lo añade al PATH del sistema.

*   **Encriptar texto:** `EncryptorX --encryter "mi texto secreto"`
*   **Desencriptar texto:** `EncryptorX --descryter "gAAAAAB..."`
*   **Encriptar un archivo:** `EncryptorX --encryter-arc "C:\ruta\a\mi\archivo.txt"`
*   **Desencriptar un archivo:** `EncryptorX --descryter-arc "C:\ruta\a\mi\archivo.txt.enc"`
*   **Abrir la interfaz gráfica:** `EncryptorX`

## Ejecución Directa desde la Terminal (Avanzado)

Para usuarios avanzados o desarrolladores que deseen ejecutar la aplicación directamente desde el código fuente, pueden hacerlo siguiendo estos pasos en una terminal.

**Requisitos:**
*   Git
*   Python 3 y pip

**Pasos:**

1.  **Descargar el código :**
    ```bash
    git clone https://github.com/ghostmoai/encryterX_V2.git
    ```

2.  **Navegar al directorio:**
    ```bash
    cd encryterX_V2
    ```

3.  **Instalar dependencias:**
    La aplicación necesita algunas bibliotecas para funcionar. Instálalas con el siguiente comando:
    ```bash
    pip install -r requirements.txt
    ```

4.  **Ejecutar:**
    Ahora puedes usar la aplicación como una herramienta de línea de comandos.
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
> Este software se proporciona 'tal cual', sin garantías de ningún tipo, expresas o implícitas. El autor, `ghostmoai`, no se hace responsable de ninguna pérdida de datos o daño que pueda resultar del uso (o mal uso) de esta aplicación.
>
> **¡Es fundamental que realices copias de seguridad de tus archivos importantes antes de cifrarlos!**
