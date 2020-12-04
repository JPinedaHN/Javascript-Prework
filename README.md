# Prework Configuración de Entorno de Desarrollo

Instalar todas las herramientas necesarias para desarrollar sin inconvenientes. En Windows trabajan las cosas pero se pueden encontrar errores, por lo que es necesario instalar Windows Subsystem for Linux.

## Navegador

Herramienta que nos sirve en el desarrollo web. Funcionan por el protocolo _Hyper Text Transfer Protocol_ o _Protocolo de Transferencia de Hyper Texto_ que define como es la transferencia de imágenes o textos, para tener un estándar en cada uno de los navegadores y que no muestren cosas diferentes.

Javascript es un lenguaje de programación que permite la interactividad de los sitios web, combinados con el HTML y CSS hacen funcionar estos sitios.

Google Chrome y sus DevTools, tiene varias versiones:

1. Canary
2. Dev
3. Stable

Firefox Dev, una versión para desarrollo igual que el Chrome Dev, que nos permiten tener features que saldrán en la versión Stable. Existe también el Microsoft Edge.

Instalación: Microsoft Edge. Es necesario instalar la Dev Tools desde la Microsoft Store.
Chrome: Ctrl+Shift+I para entrar directamente a la consola.

## Editor de Texto

Las opciones recomendadas:

- Web Storm
- Atom
- Visual Studio Code

### Extensiones de VSCode

Instalación de Extensiones Recomendadas:

- Prettier
- Color Highligth
- Live Server
- Path Intellisense
- Auto Rename Tag
- Material Icon Theme

## Uso de Live Server en proyectos reales

Creamos un nuevo proyecto para ejemplo: **/EjemploLiveServer/**
Y algunos archivos: **/index.html** **/index.css** **/assets/**

Iniciamos a escribir y le damos click derecho y Abrir con live server

## Instalación de Windows Subsystem for Linux

Podemos seguir esta guía muy importante: [Installing Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

Necesitamos verificar la versión de Windows: `WIN + R` y luego ingresamos el comando `winver`. Debe ser mayor o igual a la version _19041_

Abrir Windows Powershell como Administrador y continuamos con los pasos de la guia:

    1. Copiamos el siguiente código en la consola:

    ```bash
    dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
    ```

    2. Actualizamos a la versión correcta
    3. Activamos la funcionalidad de máquina virtual

    ```bash
    dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
    ```

    4. Activamos WSL 2
    ```bash
    wsl --set-default-version 2
    ```

    5. Instalamos la versión de Linux en la Microsoft store, recomendado Ubuntu

### Configuración de ubuntu en WSL

Instalamos Windows Terminal desde la Microsoft Store

Terminamos de Configurar Ubuntu WSL, creación de Usuario y contraseña.

Las instalaciones debemos hacerlas dentro del Ubuntu WSL incluido nuestro VSCode. Correr ubuntu con persmios de administrador.

#### Instalamos Node JS

La opción recomendada es instalar NVM:

```bash
sudo apt install curl
curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash

source ~/.profile

nvm -v
```

Ahora vamos con Node Usando NVM:

```bash
nvm install node
```

para verificar la instalación

```bash
node -v
```
