# Guía para crear una cuenta de GitHub y usar Git en Kali Linux

Esta guía cubre los pasos para crear una cuenta en GitHub, configurar Git en Kali Linux y usarlo para crear repositorios y gestionar claves SSH.

## 1. Crear una cuenta en GitHub

1. Dirígete a [GitHub](https://github.com) y haz clic en el botón **Sign Up**.
2. Completa el formulario con tu **nombre de usuario**, **dirección de correo electrónico** y **contraseña**.
3. Verifica tu dirección de correo electrónico al hacer clic en el enlace de verificación enviado a tu bandeja de entrada.
4. Una vez verificado, completa la configuración inicial en GitHub siguiendo los pasos de su asistente.
![Creación de cuenta](imagenes\Creacion_Cuenta.PNG)

## 2. Instalación de Git en Kali Linux

Si aún no tienes instalado Git en tu máquina Kali Linux, sigue estos pasos:

```bash
sudo apt update
sudo apt install git
```

### 2.1. Verificación de la intalación 

Utilizaremos el siguiente comando para verificar que todo este instalado correctamente.

```bash
git --version
```

## 3. Configuración de Git

Configuraremos la cuenta de Git con los siguientes comandos:

```bash
git config --global user.name "SergioMP04"
git config --global user.email "smoratop02@informatica.iesvalledeljerteplasencia.es"
```

![Configuración de la cuenta ](imagenes\Config_Git.PNG)

### 3.1. Creación de la clave SSH

Genera una clave SSH para usarla en GitHub:

```bash
ssh-keygen -t rsa -b 4096 -C "smoratop02@informatica.iesvalledeljerteplasencia.es"
```

![](imagenes\Generate_Key.PNG)

## 4. Agregar la clave SSH a GitHub

Copia la clave pública SSH al portapapeles:

```bash
cat ~/.ssh/id_rsa.pub
```

Selecciona y copia la salida que aparece.

1. En GitHub, ve a Settings (configuración) desde tu perfil.
2. Dirígete a SSH and GPG keys y haz clic en New SSH key.
3. Pega tu clave pública en el campo correspondiente y asigna un nombre para identificarla, por ejemplo, Kali Linux.
![](imagenes\Configuración_Claves.PNG)

---

## 5. Creación de repositorio en GitHub

### 5.1. Crear un repositorio en GitHub

1. Inicia sesión en tu cuenta de GitHub.
2. Ve a tu perfil y haz clic en el botón **New** para crear un nuevo repositorio.
3. Asigna el nombre de tu repositorio como **PPSActividad3Unidad0SergioMoratoPrieto**.
4. Puedes elegir si hacerlo **público** o **privado**.
5. No marques ninguna casilla en la sección de inicialización (como README, .gitignore, etc.), ya que ya tienes la carpeta preparada.
6. Haz clic en **Create repository**.

## 5.2. Inicializar el repositorio local

1. Abre la terminal en Kali Linux.
2. Navega hasta la carpeta de tu proyecto:

   ```bash
   cd /ruta/a/tu/carpeta/PPSActividad3Unidad0SergioMoratoPrieto
   ```

![Creación del repo](imagenes\Creación_Repo.PNG)

## 5.3 Inicializa el repositorio Git en la carpeta

```bash
    git init
```

## 5.4 Agregar archivos y hacer un commit

Agrega todos los archivos de tu proyecto al repositorio:

```bash
    git add
```

Realiza un commit con un mensaje descriptivo depende de la situación es decir, depende de lo que editemos o subamos:

```bash
    git commit -m "Primer commit con el proyecto PPSActividad3Unidad0SergioMoratoPrieto"
```

## 5.5 Conectar el repositorio local con GitHub

Copia la URL SSH de tu repositorio en GitHub. Para obtenerla, haz clic en el botón Code en la página de tu repositorio y selecciona la opción SSH (<git@github.com>:SergioMP04/PPSActividad3Unidad0SergioMoratoPrieto.git).

Conectaremos nuestro repositorio local con el remoto:

```bash
git remote add origin git@github.com:TuUsuario/PPSActividad3Unidad0SergioMoratoPrieto.git
```

## 5.6 Subir los archivos al repositorio de GitHub

Para subir los archivos al repositorio remoto:

```bash
git push -u origin main
```

---
