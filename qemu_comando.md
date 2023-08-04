##### KVM es una solución de virtualización para Linux, que es incluido en el Kernel de Linux.
---


## Prerequisitos

### Verificar si el hardware soporta virtualización

##### En el caso de Intel

	`grep -e 'vmx' /proc/cpuinfo`

##### En el caso de AMD

	grep -e 'svm' /proc/cpuinfo

##### Verificar que los módulos KMV estén cargados en el kernel, 'debe estarlo por defecto'

	lsmod | grep kvm

### Instalación e implementación

##### Instalar primero estos paquetes, estos proveen el gestor de imágenes de disco y kvm a nivel de usuario
	
	sudo apt install qemu-kvm qemu-img

##### Instalar herramientas opcionales pero muy útiles para la administración de la plataforma

	sudo apt install virt-manager libvirt libvirt-python libvirt-client 

##### Iniciar y verificar que el demonio 'libvirtd' esté corriendo, este es el que se va a encargar de gestionar la plataforma.

	sudo systemctl status libvirtd

### Creando una VM usando KVM

##### Iniciamos virt-manager

	virt-manager
