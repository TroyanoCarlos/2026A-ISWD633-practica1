# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
# COMPLETAR

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
<img width="981" height="283" alt="image" src="https://github.com/user-attachments/assets/b6c71892-0719-4c20-84be-7939fa29200e" />

# COMPLETAR

### Listar los contenedores ejecutándose o no

```
docker ps -a
```
<img width="1421" height="239" alt="image" src="https://github.com/user-attachments/assets/548e7dfa-32c7-4c4a-b266-9ac4c10e4182" />

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web
<img width="452" height="61" alt="image" src="https://github.com/user-attachments/assets/17cbf504-30df-4529-a4fa-dd91aeac2720" />


# COMPLETAR

### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```
<img width="1907" height="119" alt="image" src="https://github.com/user-attachments/assets/da7c7951-815e-47ce-950b-b7bb3dfca6a6" />

### Para detener un contenedor

```
docker stop <nombre contenedor>
```

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine

<img width="1256" height="763" alt="image" src="https://github.com/user-attachments/assets/1dd9bb48-4bdd-40c5-b75e-6b0af3d8f6d0" />

# COMPLETAR

**¿Qué sucede luego de la ejecución del comando?**
La terminal queda ejecutando el proceso de correr el contenedor srv-web2, dejando inhabilitada la entrada de nuevas lineas de comando.
# COMPLETAR  

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
<img width="781" height="118" alt="image" src="https://github.com/user-attachments/assets/1ad3e601-2c63-4d16-ae19-f68a8c493824" />


# COMPLETAR

### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 

# COMPLETAR

Verificar que el contenedor que se eliminó
<img width="1890" height="250" alt="image" src="https://github.com/user-attachments/assets/31cdfef7-2953-4121-bee1-4532888e84e0" />

# COMPLETAR

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 

# COMPLETAR

Verificar que el contenedor que se eliminó
<img width="1910" height="271" alt="image" src="https://github.com/user-attachments/assets/6c25e828-74e0-4c0b-9eef-c4030f9039dc" />

# COMPLETAR

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 

# COMPLETAR
<img width="1915" height="791" alt="image" src="https://github.com/user-attachments/assets/f055048d-ccdc-4c23-a563-acbdcc8faa60" />

