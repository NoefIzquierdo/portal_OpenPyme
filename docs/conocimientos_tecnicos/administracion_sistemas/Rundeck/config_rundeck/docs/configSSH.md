# **Configurar SSH de Rundeck**

Para comenzar con el uso de Rundeck debemos tomar en cuenta el protocolo SSH, ya que será indispensable.
Realicemos las siguientes configuraciones para tener todo listo para usar Rundeck.


### **SSH Rundeck**

Al instalar Rundeck automáticamente genera unas llaves OpenSSH, es necesario mencionar que para configurar nodos en Rundeck se necesitan llaves RSA y no OpenSSH. Por lo tanto aplicaremos las siguientes instrucciones para reemplazar las llaves actuales.

#### **Reemplazar llaves**

Nos cambiamos al usuario rundeck

```
sudo su rundeck
```

Ejecutamos el comando para reemplazar llaves con el usuario rundeck

```
ssh-keygen -t rsa -b 4096 -m PEM
```

Nos lanzará un wizard para rellenar información

1. Primero nos lanzará una opción para cambiar la ruta de nuestras llaves SSH, la ruta que debe tener por default es **/var/lib/rundeck/.ssh/id_rsa** en este caso solo daremos ++enter++.
En caso contrario agregamos la ruta mencionada anteriormente.

2. Si los archivos ya existen en la ruta nos preguntara si queremos sobreescribir el contenido, colocaremos la y (yes) y un ++enter++.

3. Posteriormente nos pedirá agregar una frase secreta, no agregaremos ninguna solo damos ++enter++ 2 veces.

4. Con esto nuestras llaves han sido creadas correctamente


=== "Wizard SSH"

    ```
        {==rundeck$==} ssh-keygen -t rsa -b 4096 -m PEM
        Generating public/private rsa key pair.
        Enter file in which to save the key (/var/lib/rundeck/.ssh/id_rsa):
        /var/lib/rundeck/.ssh/id_rsa already exists.
        Overwrite (y/n)?
        Enter passphrase (empty for no passphrase): 
        Enter same passphrase again: 
        Your identification has been saved in /var/lib/rundeck/.ssh/id_rsa
        Your public key has been saved in /var/lib/rundeck/.ssh/id_rsa.pub
        The key fingerprint is:
        SHA256:PfYIWfv3rEuCweKBLd+fMTS5T9/r3JPRTUjExh6Tsiw rundeck@blacom
        The key's randomart image is:
        +---[RSA 4096]----+
        |             +.. |
        |            . O  |
        |          .. * + |
        |       o =E.o.o .|
        |      o S B.+  .o|
        |       + * O o .o|
        |        o + B + o|
        |           . X.*o|
        |            o =*O|
        +----[SHA256]-----+
        {==rundeck$==}
    ```
