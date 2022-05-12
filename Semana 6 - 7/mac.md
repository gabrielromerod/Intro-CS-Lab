# Instalación Mac - MySQL y Workbench

Tienes que tener [Brew](https://brew.sh/index_es) instalado antes de seguir estos pasos. En la página web que te proporcionamos encontraras el proceso de instalación y si presentas problemas de recomendamos estos videos:
- [How to Install Homebrew on Apple M1 Macs](https://youtu.be/SOjSNB7F2m4) - Just Another Dang How To Channel
- [Cómo instalar Homebrew en Mac OS Big Sur](https://youtu.be/VzFMdJh8Z_I) - El Rincón De Isma - Tutoriales y Tecnología

## Instalación MySQL
1. Abrimos la terminal de Mac y ejecutamos este comando:

``` 
brew install mysql
```
2. Una vez completado en la instalación nos debe aparecer un mensaje como este:
``` 
We've installed your MySQL database without a root password. To secure it run:
    mysql_secure_installation

MySQL is configured to only allow connections from localhost by default

To connect run:
    mysql -uroot

To start mysql:
  brew services start mysql
Or, if you don't want/need a background service you can just run:
  /opt/homebrew/opt/mysql/bin/mysqld_safe --datadir=/opt/homebrew/var/mysql
```
3. Ejecutamos el comando de Start MySQL:
``` 
brew services start mysql
```
4. Nos debe aparecer lo mostrado a continuación:
``` 
Successfully started `mysql` (label: homebrew.mxcl.mysql)
```
5. Ahora nos debemos conectar: 
``` 
mysql -uroot
```
6. En caso obtengas un error comprueba que los comandos escritos sean los correctos. Por otra parte si todo está bien te saldrá lo siguiente:
``` 
MySQL [(none)]>
```
7. Ahora comprueba que todo está correcto pidiendo que nos muestre nuestras bases de datos:
``` 
show databases;
```
8. ¡Has ejecutado tu primera linea de codigo en SQL!
``` 
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sys                |
+--------------------+
4 rows in set (0.007 sec)
```
## Instalación Workbench
1. Abrimos la terminal y ejecutamos:
```
brew install --cask mysqlworkbench
```
2. Abrimos Workbench y le damos click en Local Instance 3306:

![Welcome to MySQL Workbench](https://static.platzi.com/media/user_upload/Captura%20de%20Pantalla%202020-06-19%20a%20la%28s%29%202.10.24-12152bd4-591a-4c13-9eaf-3c66e9baa1da.jpg)

3. Se nos abre el inicio de Workbench y ya podemos comenzar a trabajar:

![MySQL Workbench Working Area](https://static.platzi.com/media/user_upload/Captura%20de%20Pantalla%202020-06-19%20a%20la%28s%29%202.10.38-cb583ff5-1f5b-4093-a41a-f8373a9c41f5.jpg)

### [Completaste el proceso de intalación ya puedes continuar aprendiendo](./Semana6-7.md)