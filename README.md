# Implantación de una web estática con Apache

1. Crear los directorios en /var/www
* cd /var/www
	* sudo mkdir iaw2425
	* sudo mkdir doc-iaw2425


2. Copiar el archivo default para modificarlo
* cd /etc/apache2/sites-available
	* cp 000-default.conf iaw2425
	* cp 000-default.conf docu-iaw2425


3. Modificar los archivos que hemos copiado con la información correspondiente de cada uno
* cd /etc/apache2/sites-available
	* sudo nano iaw2425
	* sudo nano docu-iaw2425


4. Crear un enlace simbólico con sites-enable
* cd /etc/apache2/sites-enabled
	* a2ensite iaw2425
	* a2ensite docu-iaw2425



5. Crear los archivos para editarlos
* cd /var/www/iaw2425/
	* sudo nano index.html


* cd /var/www
	* mkdocs new docu-iaw2425
	* cd docu-iaw2425
	* sudo nano ??


