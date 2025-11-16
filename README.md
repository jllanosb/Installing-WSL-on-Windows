# Guia de Instalación de **WSL 2** (Subistema) en Windows
WSL (Windows Subsystem for Linux versión 2) es una implementación completa del kernel de Linux desarrollada por Microsoft que se ejecuta directamente sobre Windows, ofreciendo un rendimiento y una compatibilidad mucho mejores con las aplicaciones Linux.

## Características principales de WSL 2: 

1. **Rendimiento mejorado**: WSL 2 ofrece un rendimiento significativamente superior en operaciones de archivo y una compatibilidad completa con llamadas al sistema de Linux, lo que lo hace ideal para tareas exigentes como desarrollo de software, pruebas y automatización. 

2. **Integración con Windows**: Puedes ejecutar herramientas y aplicaciones de línea de comandos de Linux —como bash, grep, ssh, git, etc.— directamente en Windows, sin necesidad de una máquina virtual tradicional. 

3. **Distribuciones disponibles**: Puedes instalar múltiples distribuciones de Linux desde la Microsoft Store, como Ubuntu, Debian, Fedora, Kali Linux, openSUSE y otras. 

4. **Redes**: WSL 2 tiene su propia dirección IP y soporta plenamente redes, servidores web, bases de datos y otras aplicaciones que requieren conectividad de red. 

5. **Gestión de recursos**: Puedes limitar el uso de CPU y memoria de WSL 2 para optimizar el rendimiento de tu sistema. Esto se hace mediante un archivo de configuración llamado .wslconfig en tu carpeta de usuario (%USERPROFILE%\.wslconfig). 

6. **Acceso a archivos**: Puedes acceder fácilmente a los archivos de Windows desde dentro de WSL 2 (en /mnt/c/, /mnt/d/, etc.) y viceversa, lo que facilita el trabajo híbrido entre ambos sistemas. 

## Requisitos Mínimos

- Tener mínimo **Windows 10 versión 1903** (o posterior) con Build 18362 (o posterior).
- Procesador con soporte de *Virtualización*
- Mínimo *4GB* de RAM (8GB Recomendado)
- Espacio de almacenamiento es Disco SSD o NVME minimo *5GB*

Verificar Virtualización: Abre administrador de tareas (Crtl-Shift-Esc)
Navega: Rendimiento > CPU > Virtualización
![Check Visualizacion](pictures/check-virtualization-enable.png)