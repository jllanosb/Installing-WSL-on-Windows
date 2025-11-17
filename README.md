# Guia de Instalación de **WSL 2** (Subistema) en Windows
WSL 2 (Windows Subsystem for Linux versión 2) es una implementación completa del kernel de Linux desarrollada por Microsoft que se ejecuta directamente sobre Windows, ofreciendo un rendimiento y una compatibilidad mucho mejores con las aplicaciones Linux.

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

# Habilitar Virtualización en Windows
**Verificar Virtualización:** Abre administrador de tareas (Crtl-Shift-Esc)
Navega: *Rendimiento > CPU > Virtualización*
![Check Visualizacion](pictures/check-virtualization-enable.png)

## Habilitar Virtualización
Abrir PowerShell como administrador y habilitar:
```bash
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

# Instalar WSL2 en Windows

Abrir PowerShell como administrador y habilitar WSL:

```bash
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```
Necesario `Reiniciar el equipo`.

## Verificar Instalación y Activar WSL v2
En la terminal ejecutar:
```bash
wsl
```
![Check-WSL](pictures/check-wsl.png)

Establecer WSL2 como versión predeterminada:
```bash
wsl --set-default-version 2
```
Nota: `Si pide actualizar [descargar WSL2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) y ejecuta el instalador de actualización manualmente`

# Comandos básicos con WSL

## Listar las instancias instaladas en Windows
Abre comando en la terminal o PowerShell:

 ```bash
wsl --list --verbose
```
o su versión corta:
```bash
wsl -l -v
```
## Listar instancias en ejecucion
Abre comando en la terminal o PowerShell:

```bash
wsl --list --running
```
## Listar las distribuciones disponibles con:

```bash
wsl --list --online
```

Se mostrará una lista similar a:
```
NAME                            FRIENDLY NAME
AlmaLinux-8                     AlmaLinux OS 8
AlmaLinux-9                     AlmaLinux OS 9
AlmaLinux-Kitten-10             AlmaLinux OS Kitten 10
AlmaLinux-10                    AlmaLinux OS 10
Debian                          Debian GNU/Linux
FedoraLinux-43                  Fedora Linux 43
FedoraLinux-42                  Fedora Linux 42
SUSE-Linux-Enterprise-15-SP7    SUSE Linux Enterprise 15 SP7
SUSE-Linux-Enterprise-16.0      SUSE Linux Enterprise 16.0
Ubuntu                          Ubuntu
Ubuntu-24.04                    Ubuntu 24.04 LTS
archlinux                       Arch Linux
kali-linux                      Kali Linux Rolling
openSUSE-Tumbleweed             openSUSE Tumbleweed
openSUSE-Leap-16.0              openSUSE Leap 16.0
Ubuntu-20.04                    Ubuntu 20.04 LTS
Ubuntu-22.04                    Ubuntu 22.04 LTS
OracleLinux_7_9                 Oracle Linux 7.9
OracleLinux_8_10                Oracle Linux 8.10
OracleLinux_9_5                 Oracle Linux 9.5
openSUSE-Leap-15.6              openSUSE Leap 15.6
SUSE-Linux-Enterprise-15-SP6    SUSE Linux Enterprise 15 SP6
```