# Índice

Vagrant es una herramienta open source que permite crear entornos virtuales livianos, además de automatizar su creación y gestión. Las máquinas virtuales creadas pueden ser ejecutadas por Virtual-Box, VMWare etc.

# Creación de un Raid5 en Vangrant.

Para esta práctica utilizaré una máquina virtual de Debian 11.

![](Imagenes/maquina_v)

Es necesario instalar Vagrant desde los repositorios de Debian:

``apt install vagrant``

Este paquete también nos instalará el plugin vagrant-libvirt. El cual nos facilitará la tarea.

Es el turno de crear el entorno donde realizaremos la práctica. Vagrant utiliza el término Box para referirse a las imágenes de las máquinas virtuales. Para añadir una imgagen se realiza con la siguiente sentencia:

´´vagrant box add debian/bullseye64''

![](Imagenes/box)

Donde debian/bullseye64 es la imagen que añadimos.

![](Imagenes/raid5)

## Diferencias entre Raid1 y Raid5

El Raid5 utiliza la paridad y la suma de comprobación para mejorar la redundancia y necesita un mínimo de tres discos para repartir la información, puediendo utilizar la totalidad de la memoria. Por otro lado, el Raid1 necesita un mínimo de dos discos, realizando una copia de todo el contenido del primer disco al segundoo disco. Perdiendo así, la mitad de toda la capacidad de memoria total. En cambio, el Raid1 al no tener redundancia, mejora su rendimiento de lectura y escritura en comparación con el Raid5.

# Características Raid5
