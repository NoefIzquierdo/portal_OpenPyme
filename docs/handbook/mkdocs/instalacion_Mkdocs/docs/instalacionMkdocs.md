Para instalar MkDocs manualmente, se necesita tener el gestor de paquetes PIP en tu sistema. 

1.- Verificar si ya esta instalado Python.       
``` 
python --version
```
2.-También el administrador de paquetes de pip de Python. 
```
pip --version   
```   
3.- En caso de que PIP no esté actualizado, actualizar con el siguiente comando:   
```
pip install --upgrade pip
```    
4.- Para instalar MkDocs se utiliza comando:
```
pip install mkdocs
```  
5.- Comprobar que la instalación se ha realizado con éxito, ejecutando el comando:
```
mkdocs --version
```  
6.- Creamos el proyecto:
```
mkdocs new nombreProyecto
```  
7.- Accedemos al proyecto:
```
cd nombreProyecto
```  
8.- Después procedemos a contruir el sitio:
```
mkdocs build 
```
9.- El siguiente comando es para inicializar un sitio:
```
mkdocs serve
```  
10.- Ir a **localhost:8000** o **http://127.0.0.1:8000/** para observar la interfaz inicial de MkDocs.