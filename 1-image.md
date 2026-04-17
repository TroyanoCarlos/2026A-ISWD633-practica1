# Imagen
### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.


```
docker pull <nombre imagen> 
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```

Descargar la imagen **hello-world**
<img width="1010" height="207" alt="image" src="https://github.com/user-attachments/assets/57ea9f1c-d955-4d60-839c-e7ac8368a367" />

# COMPLETAR

**¿Qué es nginx?**

NGINX es un software de servidor web de alto rendimiento que también funciona como proxy inverso, balanceador de carga y servidor de caché. Se utiliza principalmente para gestionar y distribuir solicitudes de usuarios hacia aplicaciones web, mejorando la velocidad, la escalabilidad y la disponibilidad de los sistemas. A diferencia de servidores tradicionales, NGINX maneja múltiples conexiones de manera eficiente mediante un modelo asíncrono basado en eventos, lo que lo hace ideal para aplicaciones modernas con alto tráfico.

# COMPLETAR 

Descargar la imagen  **nginx** en la versión **alpine**
<img width="1025" height="354" alt="image" src="https://github.com/user-attachments/assets/eab32239-5ef3-49cd-9e78-040ccf1ccf3b" />

# COMPLETAR

### Listar imágenes


```
docker images
```

# COLOCAR UNA CAPTURA DE PANTALLA DEL RESULTADO 
<img width="852" height="121" alt="image" src="https://github.com/user-attachments/assets/193ff644-3539-4e0c-8c25-303fc2a4658c" />

**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 
# COMPLETAR
<img width="1177" height="564" alt="image" src="https://github.com/user-attachments/assets/816f5e19-418e-4aca-8920-3b581cbc0feb" />

**¿Con qué algoritmo se está generando el ID de la imagen**
Con el algoritmo de hashing sha256  que convierte cualquier cantidad de datos en una cadena alfanumérica única de longitud fija (256 bits o 64 caracteres hexadecimales).
# COMPLETAR

### Filtrar imágenes

```
docker images | grep <termino a buscar>

```

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```

Eliminar la imagen hello-world 
<img width="973" height="101" alt="image" src="https://github.com/user-attachments/assets/ac522660-9aad-4c59-aeed-031dee9aaa45" />

# COMPLETAR

-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```
