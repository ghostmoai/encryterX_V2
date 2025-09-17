# EncryptorX

Bienvenido a EncryptorX, una aplicación de escritorio para Windows diseñada para proteger tus archivos mediante un cifrado robusto. Desarrollada en Python, ofrece una solución sencilla y eficaz para asegurar tu información sensible.

## Características Principales

*   **Cifrado Fuerte:** Utiliza el algoritmo AES-256 (a través de la biblioteca `cryptography`), uno de los estándares de cifrado más seguros y utilizados a nivel mundial.
*   **Interfaz Gráfica Sencilla:** Una ventana intuitiva creada con Tkinter que permite cifrar y descifrar archivos fácilmente.
*   **Arrastrar y Soltar (Drag & Drop):** Agiliza el proceso permitiendo arrastrar archivos directamente a la aplicación.
*   **Actualizaciones Automáticas:** El programa verifica si hay nuevas versiones disponibles en el repositorio de GitHub y notifica al usuario.
*   **Código Abierto:** El proyecto es completamente de código abierto, permitiendo su revisión, uso y modificación libremente bajo los términos de su licencia.

## ¿Cómo Funciona?

EncryptorX toma un archivo y una contraseña proporcionada por el usuario. A partir de la contraseña, genera una clave de cifrado segura y la utiliza para encriptar el contenido del archivo con AES-256. El archivo resultante (`.enc`) contiene los datos cifrados y la información necesaria para su posterior descifrado. Solo con la contraseña original se puede revertir el proceso.

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
> Este software se proporciona 'tal cual', sin garantías de ningún tipo, expresas o implícitas. El autor, `el_tio_null`, no se hace responsable de ninguna pérdida de datos o daño que pueda resultar del uso (o mal uso) de esta aplicación.
>
> **¡Es fundamental que realices copias de seguridad de tus archivos importantes antes de cifrarlos!**
