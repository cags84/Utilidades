Para la instalación se debe hacer lo siguiente:

** Crear un directorio en el root del servidor
# mkdir /root/scripts

** Ingresar al directorio
 # cd /root/scripts
 
** Descargar los archivos
# wget http://bash.cyberciti.biz/dl/381.sh.zip
# wget http://bash.cyberciti.biz/dl/151.sh.zip

** Descomprimimos ambos archivos
# unzip 381.sh.zip
# unzip 151.sh.zip

** Cambiamos de nombre los archivos
# mv 381.sh start.fw
# mv 151.sh stop.fw

** Le damos permisos a los archivos
# chmod +x *.fw

** Editamos los archivos y colocamos nuestras propias reglas
# vim /root/scripts/start.fw

** Cargamos al rc.local, para que arranque con la maquina:
# echo '/root/scripts/start.fw' >> /etc/rc.local

** Como lo arrancamos desde la terminal?
# /root/scripts/start.fw

** Como limpiamos las reglas y para el firewall?
# /root/scripts/stop.fw