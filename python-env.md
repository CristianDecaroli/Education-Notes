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