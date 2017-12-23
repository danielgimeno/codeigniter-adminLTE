###################
Que es CodeIgniter
###################

CodeIgniter es un framework para desarrollo de aplicaciones web, facil de usar,
facil de instalar sin complicaciones: cada cosa en su sitio. 


*******************
AdminLTE
*******************

AdminLTE es un panel de administración para Bootstrap creado por el estudio Almsaeed. 
Es una solución de código abierto basada en un diseño modular que permite una 
construcción y personalización sencillas. ... AdminLTE está basado en Bootstrap 3. 

**************************
Changelog and New Features
**************************

You can find a list of all changes for each release in the `user
guide change log <https://github.com/bcit-ci/CodeIgniter/blob/develop/user_guide_src/source/changelog.rst>`_.

*******************
Requerimientos de servidor
*******************

PHP version 5.6 o superior

************
Instalacion
************

Git clone https://github.com/danielgimeno/codeigniter-adminLTE
Y Listo

Para la creacion de un virtual host en Apache 2.4

crear una entrada en /etc/apache2/sites-available

configuracion.conf

<VirtualHost *:80>
	ServerAdmin webmaster@localhost

	DocumentRoot <PATH-A-LA-CARPETA-DEL-ROOT>
 	ServerName local.<NOMBRE-DEL-PROYECTO>
	<Directory <PATH-A-LA-CARPETA-DEL-ROOT>>
            AllowOverride All
            Require all granted

	</Directory>

	ErrorLog ${APACHE_LOG_DIR}/error_<MI-PRYECTO>.log

	# Possible values include: debug, info, notice, warn, error, crit,
	# alert, emerg.
	LogLevel warn

	CustomLog ${APACHE_LOG_DIR}/access_<MI-PROYECTO>.log combined


</VirtualHost>

Enlazar la configuracion del archivo:
root@machina:/etc/apache2/sites-enabled#

ln -s ../sites-available/proyecto.conf  proyecto.conf


*******
Configuracion
*******

En Application/config/config.php

modificar la linea 

$config['base_url'] = 'http://local.miproyecto/';

En Application/config/database.php

configurar el acceso a la bbdd:

$db['default'] = array(
	'dsn'	=> '',
	'hostname' => 'localhost',
	'username' => '',
	'password' => '',
	'database' => '',

