# **Instalar Rundeck**

Para la instalación de Rundeck tendremos que ubicarnos en la terminal de nuestro servidor, en nuestro caso ocupamos [RockyLinux](https://docs.rockylinux.org/).
El sistema operativo debe de estar actualizado, para comprobarlo o actualizarlo ejectua el siguiente comando:

```
sudo yum update
```

_____

Ya actualizado nuestro sistema operativo seguimos los pasos que a coninuación se muestran:

### **Transferimos Rundeck**

```
curl https://raw.githubusercontent.com/rundeck/packaging/main/scripts/rpm-setup.sh 2> /dev/null | bash -s rundeck
```
### **Instalamos rundeck**

```
sudo yum install rundeck
```

### **Instalar dependencias**

Seguir las documentaciones Instalación de [Java](/conocimientos_tecnicos/administracion_sistemas/Rundeck/install_rundeck/docs/installJava/) y [PostgreSQL](/conocimientos_tecnicos/administracion_sistemas/Rundeck/install_rundeck/docs/installPostgres/)

### **Iniciar servicio de Rundeck**

Una vez instaladas las herramientas anteriores hay que iniciar Rundeck
```
sudo systemctl enable rundeckd
```

### **Habilitar servicio de Rundeck**

```
sudo systemctl start rundeckd
```

### **Acceder al inicio de sesión**

[localhost:4440](http://localhost:4440/)
