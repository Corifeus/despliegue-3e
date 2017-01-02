

Pasos a seguir:

1- Copie los archivos proporcionados en el repositorio a su lugar de trabajo.

2-Cargue la máquina con un vagrant up

3-Dentro de la máquina creada introduzca los siguientes comandos para solucionar un error de seguridad de MySQL:

mysql -h localhost -u root -proot CREATE USER 'usuario'@'localhost' IDENTIFIED BY 'usuario'; GRANT ALL PRIVILEGES ON . TO 'usuario'@'localhost' WITH GRANT OPTION; CREATE USER 'usuario'@'%' IDENTIFIED BY 'usuario'; GRANT ALL PRIVILEGES ON . TO 'usuario'@'%' WITH GRANT OPTION; exit sudo service mysql restart

4-Una vez hecho esto podrá conectarse a la máquina creada desde el terminal sql de la máquina original con el siguiente comando:

mysql -h localhost -u usuario -pusuario -P 3309
