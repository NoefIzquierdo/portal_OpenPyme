1.- Abrir una terminal 

2.- Para descargar el portal_OpenPyme del repositorio colocamos:   
```
git clone https://gitlab.openpyme.mx/pyerp/portal_openpyme.git
```
3.- Entramos a la carpeta portal_OpenPyme:   
```
cd portal_openpyme
```
4.- Instalar los requisitos del portal:      
```
pip install -r requirements.txt   
``` 
5.- Construir el proyecto:   
```
mkdocs build
```
6.- Iniciar el portal localmente:   
```
mkdocs serve
```
7.- Ir a [localhost:8000](localhost:8000) o [http://127.0.0.1:8000/](http://127.0.0.1:8000/) para observar la interfaz inicial de MkDocs.