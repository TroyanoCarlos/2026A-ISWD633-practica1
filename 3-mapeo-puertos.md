# Mapeo de puertos
El mapeo de puertos es un mecanismo que permite redirigir el tráfico de red desde un puerto en el host (tu máquina local o servidor) hacia un puerto específico en un contenedor Docker.
Por ejemplo, supongamos que tienes un contenedor que ejecuta un servidor web en el puerto 80 dentro del contenedor, pero quieres acceder a ese servidor desde tu navegador en la máquina host. Puedes usar el mapeo de puertos para redirigir el tráfico del puerto 80 del contenedor al puerto 3000 en el host. De esta manera, cuando accedas a http://localhost:3000 en tu navegador, el tráfico se dirigirá al servidor web dentro del contenedor en el puerto 80.

![mapeo](mapeoPuertos.PNG)

### Para crear un mapeo de puertos (puerto host y puerto contenedor)
El mapeo de puertos se especifica al ejecutar un contenedor Docker utilizando la opción -p o --publish seguida de los puertos que deseas mapear
```
docker run -d --name <nombre contenedor> -p <puerto host>:<puerto contenedor> <nombre imagen>:<tag>

```
Crear un contenedor a partir de la imagen nginx version alpine con el mapeo de puertos del ejemplo gráfico, host 3000 y contenedor 80
<img width="817" height="88" alt="image" src="https://github.com/user-attachments/assets/1d0d392e-7566-4e7c-bf07-c3f82ebc6108" />

# COMPLETAR

# COLOCAR UNA CAPTURA DE PANTALLA  DEL ACCESO http://localhost:3000

<img width="1876" height="968" alt="image" src="https://github.com/user-attachments/assets/3f2a5e70-d6eb-4232-86f5-4cb22b635d5a" />


### Para mapear más de un puerto

```
docker run -d --name <nombre contenedor> -p <puerto host 01>:<puerto contenedor 01> -p <puerto host 02>:<puerto contenedor 02> <nombre imagen>:<tag>
```

Crear un contenedor a partir de la imagen rabbitmq version management-alpine, para este mapeo de puertos usar en el host los mismos puertos del contenedor.

<img width="1013" height="458" alt="image" src="https://github.com/user-attachments/assets/10713a37-511b-42b4-98aa-4533afad4aee" />

# COMPLETAR

### Usando una forma más semántica cuando se especifican puertos

```
docker run -d --name <nombre contenedor> --publish published=<valorPuertoHost>,target=<valor> <nombre imagen>:<tag> 
```
### Publicando todos los puertos
```
docker run -P -d --name <nombre contenedor> <nombre imagen>:<tag> 
```

-P: le indica a Docker que asigne automáticamente puertos aleatorios en tu host para todos los puertos expuestos por el contenedor.

**Recordar**
No puedes mapear puertos a un contenedor existente directamente después de su creación con Docker. El mapeo de puertos debe especificarse en el momento de crear y ejecutar el contenedor.

### Crear contenedor de Jenkins puertos contenedor: 8080 (interface web) y 50000 (comunicación entre nodos) imagen: jenkins/jenkins:alpine3.18-jdk11
# COMPLETAR

# COLOCAR UNA CAPTURA DE PANTALLA  DEL ACCESO http://localhost:8080
<img width="1912" height="955" alt="image" src="https://github.com/user-attachments/assets/486aa0f7-84b5-45a3-82f6-0f7f04cb0d1a" />


### ¿Cómo obtener la contraseña solicitada?
Para obtener la contraseña solicitada es necesario ingresar al contenedor.

![Imagen](jenkins.PNG)


<img width="1140" height="509" alt="image" src="https://github.com/user-attachments/assets/49977872-23e7-4ffb-a315-900d7fe42b36" />

<img width="1730" height="948" alt="image" src="https://github.com/user-attachments/assets/5a568b86-b7c9-45a6-b99f-bedf241fd1eb" />


