### **1. Instalar Python globalmente**
Se debe instalar en el sistema la o las versiones de Python a utiliar para el o los entornos virtuales. Cada entorno virtual está sujeto a una versión de python globalmente instalada.

Primero actualizamos la paquetería apt desde donde descargaremos e instalaremos Python:

```bash
sudo apt update
```

Instalamos Python especificando todas la o las versiones a instalar que luego podrán ser listadas con `python --version` para ver qué versiones tenemos en el sistema.

```bash
sudo apt install python3.8 python3.9
```
---
### **2. Instalar pip**:
Pip es el administrador de paquetes de Python y generalmente se instala automáticamente junto con Python. Sin embargo, si por alguna razón pip no está instalado, puedes instalarlo utilizando el siguiente comando:

```bash
sudo apt install python3-pip
```

Cabe recalcar que en el comando se especifica la versión de `Python (python3)` la cual incluye a las versiones de ejemplo en este apunte `python3.8` y `python3.9`.

---
### **3. Instalar virtualenv (si no está instalado):**
Si aún no tienes `virtualenv` instalado, puedes instalarlo utilizando pip, el administrador de paquetes de Python. Ejecuta el siguiente comando en tu terminal para instalarlo:

```bash
python3 -m pip install virtualenv
```

---
### **4. Crear un nuevo entorno virtual:**
Ve al directorio donde deseas crear tu entorno virtual y ejecuta el siguiente comando para crear un nuevo entorno virtual llamado myenv:

```bash
virtualenv myenv
```

Esto creará un nuevo directorio `myenv` en el directorio actual que contendrá el entorno virtual.

---
### **5. Activar el entorno virtual:**
Una vez que el entorno virtual esté creado, actívalo ejecutando el siguiente comando:

```bash
source myenv/bin/activate
```

Después de ejecutar este comando, verás que el prompt de tu terminal cambiará para mostrar el nombre del entorno virtual, indicando que está activado.

---
### **6. Instalar Python, Pandas, Numpy y Jupyter Notebook, etc:**
Con el entorno virtual activado, puedes instalar las bibliotecas que necesitas utilizando pip. Ejecuta los siguientes comandos para instalar Python, pandas, seaborn, matplotlib, numpy y Jupyter Notebook o lo que requieras:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

---
### **7. Iniciar Jupyter Notebook:**
Una vez que hayas instalado todo, puedes iniciar Jupyter Notebook ejecutando el siguiente comando en tu terminal:

```bash
jupyter notebook
```

Esto abrirá Jupyter Notebook en tu navegador web y podrás empezar a trabajar con Python, pandas, numpy y Jupyter Notebook y demás en tu entorno virtual recién creado.

También puedes ejecutar `code .` esto abrirá Visual Studio Code.

---
### **8. Desactivar el entorno virtual (opcional):**
Cuando hayas terminado de trabajar en tu proyecto y quieras salir del entorno virtual, puedes desactivarlo ejecutando el siguiente comando en tu terminal:

```bash
deactivate
```

Esto restaurará tu entorno de terminal a su estado original. Recuerda que si quieres trabajar en tu proyecto más tarde, necesitarás volver a activar el entorno virtual ejecutando `source myenv/bin/activate`.

---

#################################################################################

__ACLARACIÓN:__

En caso de necesitar crear un proyecto en un entorno virtual que luego deba ser subido a GitHub y posterior a ello otra persona deba descargarlo e instalar las herramientas necesarias con sus versiones correspondientes, se deberá proceder de la siguiente manera:

1- Crear el proyecto en un directorio `mkdir proyecto`, ingresar al directorio usando el comando `cd proyecto`, iniciar el repositorio con `git init`, crear y activar el entorno virtual con `python3 -m venv env` o `virtualenv env` y `source env/bin/activate`, instalar las librerías a utilizar por ejemplo `pip install pandas jupyter`, generar un archivo requierements.txt que contendrá todas las librerías instaladas y sus respectivas versiones el cual servirá para que otra persona pueda ejecutarlo instalando de una sola vez las mismas versiones y herramientas que tenemos nosotros `pip freeze > requierements.txt`, luego de haber instalado todo y haber finalizado los archivos del proyecto se debe ejecutar `git add .` --> `git commit -m 'nombredelcommit'` , crear un repositorio vacío en GitHub y vincular el mismo con `git remote add origin <URL_del_repositorio_en_GitHub>`, asegurar el nombre de la rama con `git branch -M main` (o git branch -M master si estás utilizando la rama master), pushear el proyecto con `git push -u origin main`  # (o master si estás utilizando la rama master) 

Un archivo requirements.txt por dentro se ve así:
```
numpy==1.21.3
jupyter==1.0.0
pandas==1.3.4
```


2- Si la otra persona quiere descargar nuestro proyecto e instalar las librerías del entorno virtual deberá: clonar el repositorio `git clone <URL_del_repositorio_en_GitHub>`, ingresar al proyecto con `cd proyecto`, deberá instalar un entorno virtual y activarlo, luego podrá utilizar el archivo requirements.txt con el comando `pip install -r requirements.txt`. 

Con esto, la persona que descargue el proyecto podrá tenerlo localmente e instalar las herramientas necesarias con un solo archivo. Tener a bien generar un README.md para aclarar el proceder.

