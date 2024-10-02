# Implantación de una web estática con Apache

1. Añadir los puertos que vamos a usar
* cd /etc/apache
	* sudo nano ports.conf 


2. Crear los directorios en /var/www
* cd /var/www
	* sudo mkdir iaw2425
	* sudo mkdir doc-iaw2425


3. Asignar la propiedad del directorio y dar permisos
* sudo chown -R $USER:$USER /var/www/iaw2425
* sudo chown -R $USER:$USER /var/www/doc-iaw2425

* sudo chmod -R 755 /var/www/iaw2425
* sudo chmod -R 755 /var/www/doc-iaw2425


4.  Crear un archivo nuevo para cada host virtual, para que sea mas rapido copio el archivo
default para modificarlo
* cd /etc/apache2/sites-available
	* cp 000-default.conf iaw2425.conf
	* cp 000-default.conf docu-iaw2425.conf


5. Modificar los archivos que hemos copiado con la información correspondiente de cada uno
* cd /etc/apache2/sites-available
	* sudo nano iaw2425.conf
	* sudo nano docu-iaw2425.conf


6. Habilitar los archivos creados y deshabilitar el predeterminado
* cd /etc/apache2/sites-available
	* a2ensite iaw2425.conf
	* a2ensite docu-iaw2425.conf
	* a2dissite 000-default.conf



7. Crear los archivos para editarlos
* cd /var/www/iaw2425/
	* sudo nano index.html


* cd /var/www/doc-iaw2425
	* mkdocs new documentacio-iaw2425
	* cd documentacio-iaw24245
	* sudo nano mkdocs.yml



8. Contruir y subir la pagina de mkdocs a GitHub
* cd /var/www/doc-iaw2425/documentacion-iaw2425
	* mkdocs build
	* mkdocs gh-deploy



