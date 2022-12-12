# **Instalar PostgreSQL**

Para la instalación de PostgreSQL ejecutaremos las instrucciones que a continuación se muestran:

### **Instalar PostgreSQL**

```
sudo dnf update -y
sudo dnf install epel-release
sudo dnf install https://download.postgresql.org/pub/repos/yum/reporpms/EL-8-x86_64/pgdg-redhat-repo-latest.noarch.rpm
sudo dnf install postgresql15 postgresql15-server -y
```

### **Iniciar cluster de la base de datos**

```
/usr/pgsql-15/bin/postgresql-15-setup initdb
```

### **Iniciar el servicio de PostgreSQL**

```
systemctl start postgresql-15
```

### **Habilitar el servicio de PostgreSQL**

```
systemctl enable postgresql-15
```
