En nuestra cuenta de Amazon AWS podemos utilizar el servicio S3 que es gratuito hasta 5 Gb.  
No admite base de datos.   
Sirve para una web estática pues sólo necesita html, css y javascript.  
Para poder transferir ficheros al servidor vamos a necesitar una herramienta FTP (file transfer protocole).  
El que vamos a utilizar es Cyberduck (otro podría ser Filezilla).  

Para ello hemos de seguir los siguientes pasos:  

###1.- Descargar [Cyberduck](https://cyberduck.io/)  
Elegimos la última versión disponible en la web oficial.  
La descargamos e instalamos.  

![](http://grabilla.com/06503-98e343ea-e1fa-4024-9c02-c3b91b62f04a.png)  

###2.- Crear nuevas credenciales en Amazon AWS  
Para ello vamos a la web de [Amazon AWS](https://aws.amazon.com/es/)  
Entramos en nuestra cuenta y seleccionamos **Credenciales de Seguridad**  

![](http://grabilla.com/06503-3c4399a5-c2d1-4905-883b-34b1b32a022f.png)  

Seleccionamos **Continue to Security Credentials**  
![](http://grabilla.com/06503-46e5cef5-57a8-40cb-bac4-c9787167d65c.png)  

Y ahora **Access keys**  

![](http://grabilla.com/06503-4ce6f083-6cb1-4157-b2f3-8372ea970b2c.png)  


![](http://grabilla.com/06503-2aafaf5f-c81d-449c-915c-c437adfdb5c3.png)

Copiamos la **Access Key ID** y la **Secret Access Key** y las guardamos en un sitio seguro, pues las vamos a necesitar para conectar Cyberduck con el servicio **S3**.  

![](http://grabilla.com/06503-24cc7c99-41e2-4ed0-8581-1c1f0de3c065.png)

###3.- Conectar Cyberduck con las credenciales  

Abrimos Cyberduck y seleccionamos **Nueva Conexión**  

En el primer campo seleccionamos **S3**:  

![](http://grabilla.com/06503-3ef2c66e-580d-4d9c-8550-7ef4e96824f5.png)  

Cumplimentamos los datos de las credenciales.
  

ATENCIÓN: Si **no** queremos que nos guarde la contraseña no seleccionar el campo  
 **Guardar contraseña**  

###4.- Crear index.html con SBT (Sublime Text) y subirlo a S3  

Creamos un archivo desde Sublime Text y lo guardamos en el escritorio.  

![](http://grabilla.com/06503-5bd00fba-e4ff-4b7a-9fe0-78ca665dd2d2.png)  

Seleccionamos la carpeta a la que queremos subir el archivo y click en **subir**  

![](http://grabilla.com/06503-75fdfff6-9bc5-4bc3-96a1-f899c0650f1a.png)  


###5.- Crear un bucket y configurarlo como web  

Vamos a S3 (Amazon AWS) para crear un bucket.  

![](http://grabilla.com/06503-a682fd47-2c68-47ec-92f2-7bdfe469156c.png)  

El nombre que le demos ha de ser único (como si se tratara de un dominio).

Seleccionamos:  

![](http://grabilla.com/06503-0d1d895e-97db-40cc-8761-06a6760ffb24.png)

![](http://grabilla.com/06503-bc0ca59f-5449-4362-8047-ee2a6bf29916.png)  

![](http://grabilla.com/06503-a986acf0-5fa7-4f21-9fa4-1e5bbeb9ac6b.png)  

De este modo hemos configurado nuestro bucket como web.  

Ahora podemos entrar en el nuevo bucket y crear las carpetas:  

docs  
imagenes  
webs  


###6.- Previsualizar nuestra mini-web.  

Para previsualizarlo hemos de ir al bucket y click en la lupa de su izquierda  

![](http://grabilla.com/06503-6524116c-bc02-426f-9ae5-f7ebfa9e6352.png)  

En **Static Website Hosting** tendremos la url en **Endpoint:**

