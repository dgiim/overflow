# Trabajar con Overflow localmente

Para trabajar con el código de dgiimOverflow en local pueden seguirse los 
siguientes pasos:

1. Clonar el repositorio desde [GitHub](https://github.com/dgiim/overflow).
2. Servirlo localmente con un servidor como Apache. Podemos guardar un enlace a la carpeta 
   del repositorio en la carpeta que está sirviendo Apache (normalmente `/var/www/html`), 
   para hacer que muestre directamente nuestro repositorio y los cambios que hagamos en él.
3. Crear una base de datos en `mysql` y un usuario al que cedamos permisos completos sobre 
   esa base de datos. Después, cambiar nombre el fichero `qa-config-example` por `qa-config` y 
   escribir en él el nombre y contraseña de la base de datos y del usuario.
4. Opcionalmente, y si tenemos acceso a una base de datos de **dgiimOverflow**, podemos
   cargarla en nuestra base de datos usando:  
   `mysql -u username -p database_name < file.sql`
   Así, el aspecto será el de la página original, en lugar de la página sin configurar.
   
Los administradores pueden usar además:  
`ssh -C dgiim@tux.ugr.es mysqldump -u dgiim -p QA > backup.sql`
Para acceder al servidor y descargar la última versión de la base de datos.
