# Curso PROXMOX VE
Curso sobre Proxmox VE para el CEP.

## Contenidos

1. Introducción a la virtualización con Proxmox VE
    * ¿Qué es la virtualización?
    * Tipos de virtualización
    * Introducción a KVM/Qemu
    * Introducción a LXC
    * ¿Qué es Proxmox VE?
    * ¿Qué nos ofrece Proxmox VE?

2. Instalación Proxmox VE
    * [Escenarios para la instalación de Proxmox VE](modulo2/escenarios.md)
    * [Instalación de Proxmox VE](modulo2/instalacion.md)
    * [Acceso a la GUI de Proxmox VE](modulo2/acceso.md)
    * [Vista general de la GUI de Proxmox VE](modulo2/vista_general.md)
    * [Introducción al cluster Proxmox VE](modulo2/introduccion_cluster.md)
    * [Almacenamiento y redes disponibles](modulo2/almacenamiento_redes.md)
        * [Actividad 2.1: Instalación y acceso a Proxmox VE (OBLIGATORIA)](modulo2/actividad1.md)

3. Instalación de máquinas virtuales
    * [Gestión de imágenes ISO](modulo3/iso.md)
    * [Dispositivos paravirtualizados](modulo3/paravirtualizados.md)
    * [Creación de máquinas virtuales Linux](modulo3/creacion_linux.md)
    * [Gestión de máquinas virtuales](modulo3/gestion.md)
    * [Características y hardware de las máquinas virtuales](modulo3/caracteristicas.md)
    * [Creación de máquinas virtuales Windows](modulo3/creacion_windows.md)
        * [Actividad 3.1: Creación de una máquina virtual Linux (OBLIGATORIA)](modulo3/actividad1.md)
        * [Actividad 3.2: Creación de una máquina virtual Windows (OBLIGATORIA)](modulo3/actividad2.md)
        * Actividad 3.3: Creación de un escenario  de trabajo (1ª parte) (VOLUNTARIA)

4. Gestionando el almacenamiento
    * [Introducción al almacenamiento en Proxmox VE](modulo4/almacenamiento.md)
    * [Creación de un pool de almacenamiento tipo Directory](modulo4/directory.md)
    * [Añadir nuevos discos a una máquina virtual](modulo4/nuevo_almacenamiento.md)
    * [Gestión de los discos de una máquina virtual](modulo4/gestion_almacenamiento.md)
        * Actividad 4.1: Creación de un pool de almacenamiento para trabajar con imágenes de discos (OBLIGATORIA)
        * Actividad 4.2: Añadir nuevos discos a una máquina virtual (OBLIGATORIA)

5. Gestionando redes virtuales
    * Introducción a la redes virtuales en Proxmox VE
    * Cortafuegos en Proxmox VE
    * Creación de una red interna
        * Actividad 5.1: Creación de un red interna (OBLIGATORIA)

6. Clonación, instantáneas y copias de seguridad
    * [Clonación de máquinas virtuales](modulo6/clonacion.md)
    * [Convirtiendo máquinas virtuales en plantillas](modulo6/plantillas.md)
    * [Snapshots de máquinas virtuales](modulo6/snapshot.md)
    * [Copias de seguridad de máquinas virtuales](modulo6/backup.md)
        * Actividad 6.1: Clonación, instantáneas y copias de seguridad
        * Actividad 6.2: Creación de un escenario  de trabajo (2ª parte) (VOLUNTARIA)

7. Trabajando con Linux Containers
    * Gestionando plantillas de contenedores
    * Creación de contenedores Linux
    * Gestión de contenedores Linux
        * Actividad 7.1: Creación de un contenedor linux (OBLIGATORIA)
        * Actividad 7.2: Creación de un escenario  de trabajo (3ª parte) (VOLUNTARIA)

8. Gestión de usuarios en Proxmox VE
    * Usuarios y Grupos
    * Pools de recursos
    * Permisos
        * Actividad 8.1: Gestión de usuarios y grupos (OBLIGATORIA)

9. Aspectos avanzados

    * Trabajar con imágenes qcow2 ya existentes
    * Configuración de máquinas virtuales con cloud-init

    





Las tareas VOLUNTARIAS nos van a permitir la construcción de un escenario de trabajo:

* Módulo 3: Presentación de las tareas voluntarias. Se instala una máquina linux debian (en el pool local-pve).
* Módulo 6: A partir de la máquina que instalamos en el módulo 3 se crea una plantilla desde la que se van a crear dos nuevas máquinas: router y cliente. Una se puede crear sobre local-pve, y otra sobre el pool creada en el módulo anterior. La máquina router estará conecta a la red pública y a la red privada, la máquina cliente a la red interna. Se configura la máquina router para que haga de enrutador, y de esta manera la máquina cliente tendrá acceso a internet. Todas las configuraciones de red con configuración estática.
* Módulo 7: Se crea un contenedor conectado a la red interna donde se configura un servidor DHCP, por lo que podemos cambiar la configuración de red del cliente para que se configure de forma dinámica.
for