# Preseed Debian 13

**Historial de commits:**

**Preseed inicial**  
Se ha creado y rellenado un archivo `preseed.cfg` lo más completo posible del que partiremos inicialmente.

**Nombre de usuario y nomenclatura de disco modificados**  
Se cambia de `debianASO` a `debianaso` el nombre de usuario, y se modifica de `sda` a `vda` el disco en el que se va a escribir.

**Firewalld**  
Paquete `firewalld` añadido e iniciado con el sistema.

Ahora mismo, funciona en BIOS y UEFI pero sigue preguntándome qué teclado español quiero.  

**Desactivando la instalación de GNOME se soluciona el anterior error**  
Se han desactivado todos los comandos `preseed\late`.

**Primer boot automatizado**  
Se han modificado algunas líneas de tasksel y variables de teclado.

**Mejora particionado V1**  
El particionado se ha mejorado y ampliado valores, aún así me pregunta si quiero crear particion swap.

**Mejora particionado V2**  
Se ha añadido swap y recalculado el tamaño de las particiones.

**Entrega**  
Si bien solo instala en discos de nomenclatura `vda`, he conseguido que el particionado se haga de forma dinámica, repartiéndose un 41,5% a las particiones `/` y `/home`, y un 17% a `/var`. Estos porcentajes toman efecto sobre el espacio libre en disco tras la creación de las particiones `boot`, `/boot/efi` y `/swap`.  
Además, se han incluido archivos de configuración de la ISO para que la instalación se inicie de forma completamente automática.
