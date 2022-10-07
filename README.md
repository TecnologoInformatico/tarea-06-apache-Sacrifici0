# apache

Reemplace `$ALUMNO` por el nombre de su nombre de usuario en www.tecnologoinformatico.com

EJ: `dmascheroni`

1. Cree el directorio ~/repositorios y dentro clone el
repositorio: `https://github.com/TecnologoInformatico/AdmInf-web.git`
2. Actualice el repositorio de la lista de paquetes.
    `apt update`
3. Instalar el servidor Apache mediante apt.
4. Cree el directorio /var/www/$ALUMNO
5. Asigne como propietario del directorio su usuario.
6. Configure un nuevo Virtual host. (copiando el archivo de configuración por defecto)
  6.1. ServerName $ALUMNO.tecnologoinformatico.com
  6.2. Correo de contacto con el administrador.
  6.3. El root de la aplicación. (/var/www/$ALUMNO)
7. Modifique el archivo /etc/hosts de modo que el ServerName coincida con este equipo `127.0.0.1`.
8. Reinicie el servidor apache para que los cambios tengan efecto.
9. Copie el contenido del directorio ~/repositorios/AdmInf-web a /var/www/$ALUMNO, de tal modo que el contenido del repositorio antes clonado se encuentre en el root de la aplicación.
10. Verifique que el servidor funcione correctamente.
11. Ingrese la IP del servidor y el servername a continuación:

```json
{
    "serverName": "",
    "ip": ""
}
```
---------------------------------------------------
ENTREGA:

1. Cree el directorio ~/repositorios y dentro clone el
repositorio: `https://github.com/TecnologoInformatico/AdmInf-web.git`
	```bash
	mkdir ~/repositorios
	git clone https://github.com/TecnologoInformatico/AdmInf-web.git
	```

2. Actualice el repositorio de la lista de paquetes.
	`sudo apt update`

3. Instalar el servidor Apache mediante apt.
	`sudo apt install apache2`

4. Cree el directorio /var/www/$ALUMNO
	`sudo mkdir /var/www/mecheverria`

5. Asigne como propietario del directorio su usuario.
	`sudo chown ubuntu ruta al archivo o directorio`

6. Configure un nuevo Virtual host. (copiando el archivo de configuración por defecto)
	`sudo cp 000-default.conf mecheverria.conf` -> copio el archivo de configuracion
	`sudo nano mecheverria.conf` -> abro el archivo y lo configuro como dice en los siguientes pasos.
  6.1. ServerName $ALUMNO.tecnologoinformatico.com
  6.2. Correo de contacto con el administrador. -> aca elegi poner mi correo de UTEC.
  6.3. El root de la aplicación. (/var/www/$ALUMNO)


7. Modifique el archivo /etc/hosts de modo que el ServerName coincida con este equipo `127.0.0.1`.
	`sudo nano /etc/hosts` 
8. Reinicie el servidor apache para que los cambios tengan efecto.
	`sudo systemctl restart apache2`
9. Copie el contenido del directorio ~/repositorios/AdmInf-web a /var/www/$ALUMNO, de tal modo que el contenido del repositorio antes clonado se encuentre en el root de la aplicación.
	` cp -r ~/repositorio/AdmInf-web/* /var/www/mecheverria/` -> el /* hace que copie el contenido de la carpeta y no la carpeta en si.
10. Verifique que el servidor funcione correctamente.
	144.22.192.9 en un navegador.
11. Ingrese la IP del servidor y el servername a continuación:

```json
{
    "serverName": "mecheverria.tecnologoinformatico.com",
    "ip": "144.22.192.9"
}
```

