# **Configurar PostgreSQL**

Los siguientes pasos se tendran que realizar con el usuario postgres de la siguiente manera

### **Cambiar a usuario postgres**

```
su postgres
```

### **Usar la base de datos postgres**

```
psql
```

### **En la base de datos**

#### **Crear base de datos rundeck**

```
create database rundeck;
```

#### **Crear usuario y contraseña rundeck**

```
create user rundeckuser with password 'rundeckpassword';
```

#### **Asignar privilegios**

Al usuario rundeckuser se le asignan todos los privlegios para la base de datos rundeck

```
grant ALL privileges on database rundeck to rundeckuser;
ALTER DATABASE rundeck OWNER TO rundeckuser;
GRANT ALL PRIVILEGES ON ALL SEQUENCES IN SCHEMA public TO rundeckuser;
GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA public TO rundeckuser;
```
