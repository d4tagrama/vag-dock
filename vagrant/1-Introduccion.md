# Primera máquina virtual #

En esta actividad se generará una máquina virtual basada en **Ubuntu 18 Bionic Beaver**



### 1. Descargar *box*

Para agregar a la lista de *box* disponinibles ejecutamos el siguiente comando:

```bash
vagrant box add ubuntu/bionic64
```

### 2. Generar Vagrantfile

Aun cuando es posible generar el `Vagrantfile` de manera manual con cualquier editor de texto en este caso se utilizará las herramientas de vagrant para generar dicho archivo ejecutando el siguiente comando: 

```bash
vagrant init ubuntu/bionic64
```

Posterior de ejecutar el comando anterior podemos utilizar el comando `ls` para listar los archivos en el directorio actual donde se debe visualizar un nuevo archivo con el nombre de  *Vagrantfile*.

### 3. Iniciando la máquina virtual
Vagrant permite poner en diferentes estados la máquina virtual  como: **halt**, **up**, **suspended**, entre otros. Para inicializar la máquina virtual es necesario ejecutar el siguiente comando:

```bash
vagrant up
```
El comando anterior genera de manera automática una máquina virtual dependiendo el *provider* seleccionado en nuetro caso es *VirtualBox*.

**Nota:** Se puede seleccionar el proveedor a utilizar utilizando el comando `$ vagrant up --provider=<provider>`
### 4. Accediendo a la máquina virtual

Vagrant al instanciar  el *box* mapea puertos definidos a la instancia o máquina virtual. Vagrant genera una llave publica la cual permitirá acceder vía `ssh` a la máquina virtual sin la necesidad de contraseña.


Para acceder a la máquina virtual ejecutamos el siguiente comando:

```bash
vagrant ssh
```
