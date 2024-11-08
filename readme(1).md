# Informe Técnico: Uso de Git

### Actividad 3 - Unidad 0: Uso de Git

## Introducción

El objetivo de esta actividad es aprender a utilizar Git a través de la creación y configuración de un repositorio en GitHub. Se desarrollarán distintas fases, que incluyen la instalación y configuración de Git, la creación de archivos y documentación, y el uso básico de comandos Git para gestionar un repositorio. También se explorará cómo crear un contenedor con una instancia de GitLab utilizando Docker.

## Pasos a Realizar

### 1. Creación de una cuenta en GitHub

El primer paso es abrir una cuenta en [GitHub](https://github.com) utilizando una dirección de correo del centro `@informatica.iesvalledeljerteplasencia.es`.
![](imagenes\Creacion_Cuenta.PNG)
### 2. Instalación de Git y PHP

Se deben instalar Git y PHP en el equipo local. Esto se realiza a través de los siguientes comandos en sistemas basados en Debian/Ubuntu:

```bash
sudo apt update
sudo apt install git php
```
![](imagenes\Install_Git_PHP.PNG)
### 3.Configuración de Git
Configuraremos la cuenta de Git con los siguientes comandos:
```bash
git config --global user.name "SergioMP04"
git config --global user.email "smoratop02@informatica.iesvalledeljerteplasencia.es"
```
### 4.Creación de la clave SSH
Genera una clave SSH para usarla en GitHub:
```bash
ssh-keygen -t rsa -b 4096 -C "smoratop02@informatica.iesvalledeljerteplasencia.es"
```
![](imagenes\Generate_Key.PNG)

