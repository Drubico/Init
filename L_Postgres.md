********************
*       POSTGRES             *
*********************

sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt buster-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
sudo apt-get update
sudo apt-get install postgresql
&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&
 su postgres
psql
 create user admin with password 'root' createdb;
alter user postgres with password 'postgres';
 \q
exit
/etc/postgresql/11/main/pg_hba.conf
modificar la línea:
local   all         all                               peer
sustituyendo peer por md5, es decir:
local   all         all                               md5
/etc/init.d/postgresql reload

&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&
sudo apt-get update
sudo apt-get install postgresql-12 pgadmin4
apt-get install pgadmin3
&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&&
2) Configuración básica
a) Convertirse en el usuario postgres
              su postgres
b) Entrar al SGBD
                psql 
c) Crear un usuario con contraseña (sentencia SQL) que tenga permiso de creación de bases de datos. Sustituyan lapalabramagica por la contraseña que prefieran.
             create user admin with password 'lapalabramagica' createdb;
d) salir
                \q
f) salir de la sesión como usuario postgres para volver a ser root
                 exit   
g) editar como root el fichero /etc/postgresql/11/main/pg_hba.conf (ojo 11 podría cambiar según la versión que se haya instalado). En línea de comandos puede usar nano (fácil) o vi (avanzado), también puede lanzar un editor que se abra en el entorno gráfico como kate (KDE), gedit (Gnome)...

modificar la línea:

local   all         all                               peer

sustituyendo peer por md5, es decir:

local   all         all                               md5

Guardar el archivo y volver a la línea de comandos.
h) recargar la configuración de postgresql ejecutando
              /etc/init.d/postgresql reload
i) salir del usuario root
                 exit
j) utilizar PostgreSQL como usuario admin (pedirá contraseña)

 psql template1 -U admin

k) utilizar los comandos SQL (ver ayuda con \h) y del cliente (ver ayuda con \?). Por ejemplo:

 create database prueba;

 \c prueba

 create table persona(
  identificacion varchar(10) not null,
  nombre varchar(100) not null,
  nacimiento date,
  constraint pk_persona primary key(identificacion));

 insert into persona values('1234567','Pepe Pérez','1/1/1981');

 \q
 
l) podemos volver a nuestra base de datos de pruebas directamente con

 psql prueba -U admin

***********************
