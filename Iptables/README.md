# Para la instalación se debe hacer lo siguiente:

* Crear un directorio en el root del servidor
	
	mkdir /root/scripts

* Ingresar al directorio

	cd /root/scripts
 
* Descargar los archivos
	
	https://github.com/cags84/Utilidades/archive/master.zip

* Descomprimimos ambos archivos

	unzip master.zip


* Le damos permisos a los archivos

	chmod +x *.sh

* Editamos los archivos y colocamos nuestras propias reglas

	vim /root/scripts/start.sh
	vim /root/scripts/stop.sh

* Cargamos al rc.local, para que arranque con la maquina:

	echo '/root/scripts/start.sh' >> /etc/rc.local

* Como lo arrancamos desde la terminal?

	sh /root/scripts/start.sh

* Como limpiamos las reglas y para el firewall?

	sh /root/scripts/stop.fw
	
* Para ver las reglas

	iptables -L -nv