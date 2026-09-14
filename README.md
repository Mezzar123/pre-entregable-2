# Entregable 2 - Hardening Inicial

## Introducción

En este trabajo se realizó un proceso básico de hardening sobre una máquina virtual utilizando VirtualBox y Kali Linux.

El objetivo fue aplicar algunas medidas de seguridad básicas, como configurar la red, utilizar un usuario con permisos limitados, mantener el sistema actualizado y crear un snapshot para poder recuperar el estado de la máquina en caso de algún problema.

---

## 1. Configuración de red - Modo NAT

Antes de iniciar la máquina virtual, se ingresó a Configuración → Red de VirtualBox y se configuró el adaptador de red en modo NAT (Network Address Translation).

### Captura

![Configuración de red](Red.png)

### Importancia para la seguridad

El modo NAT permite que la máquina virtual tenga acceso a Internet utilizando la conexión del equipo anfitrión, sin quedar directamente expuesta a la red externa.

Esto proporciona cierto aislamiento y reduce la posibilidad de que otros dispositivos puedan iniciar conexiones directamente hacia la máquina virtual.

---

## 2. Usuario con permisos limitados

Dentro de Kali Linux se creó un usuario con permisos limitados, evitando utilizar una cuenta con privilegios administrativos para las tareas normales.

### Captura

![Usuarios del sistema](usuarios%20privilegios.png)

### Importancia para la seguridad

Esto aplica el principio de menor privilegio, que consiste en otorgar a cada usuario solamente los permisos necesarios para realizar sus tareas.

De esta manera, si la cuenta fuera comprometida, el atacante tendría menos posibilidades de modificar archivos importantes, instalar programas o realizar cambios en el sistema.

---

## 3. Sistema actualizado

Se ejecutó el comando `apt upgrade` para comprobar y aplicar las actualizaciones disponibles del sistema.

### Captura

![Sistema actualizado](sistema%20actualizado.png)

### Importancia para la seguridad

Mantener el sistema actualizado es importante porque las actualizaciones pueden incluir correcciones para vulnerabilidades de seguridad.

Si una vulnerabilidad conocida no se corrige, podría ser aprovechada por un atacante. Por eso, mantener los paquetes actualizados ayuda a reducir los riesgos del sistema.

---

## 4. Snapshot - Hardening Inicial

Después de apagar la máquina virtual, se creó un snapshot llamado **Hardening Inicial**.

### Captura

![Snapshot Hardening Inicial](snapshot.png)

### Importancia para la seguridad

Un snapshot permite guardar el estado de una máquina virtual en un momento determinado.

En este caso, funciona como un punto de recuperación. Si posteriormente se realiza una configuración incorrecta o se produce algún problema durante las prácticas, se puede volver al estado guardado.

---

## Conclusión

Con este trabajo se aplicaron diferentes medidas básicas de seguridad sobre una máquina virtual.

La configuración de NAT proporciona cierto aislamiento, el uso de un usuario con permisos limitados aplica el principio de menor privilegio, las actualizaciones ayudan a corregir vulnerabilidades conocidas y el snapshot permite contar con un punto de recuperación.

Estas medidas forman parte de un proceso básico de hardening, cuyo objetivo es reducir los riesgos y mejorar la seguridad del sistema.
