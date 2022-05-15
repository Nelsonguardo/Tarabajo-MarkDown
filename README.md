<center> 

![logo](logotecno.png "Tecnologico Comfenalco logo")

 </center>
<center> <h1>VAGRANT </h1> </center>

<center> <h4>PRESENTADO POR: </h4> </center>

<center> <h4>Edinson Contreas Cogollo
        <br>Nelson Guardo Camacho
        <br>Jorge Gamarra
        <br>Dilan Patiño Mendoza
 </h4> </center>

 <center> <h4>DIRIGIDO A: </h4> </center>

  <center> <h4>Ronald Cuello Meza
</h4></center>

<center> <h4>ASIGNATURA:</h4> </center>

<center> <h4>SISTEMAS DISTRIBUIDOS</h4> </center>

 <center> <h4>FUNDACIÓN UNIVERSITARIA TECNOLÓGICO COMFENALCO FACULTAD DE INGENIERÍA
        <br>INGENIERIA DE SISTEMAS SEMESTRE 9
        <br>16/05/2022
 </h4> </center>

---

<center> <h1>VAGRANT </h1> </center>

<center> 

![Vagrant logo](logo.png "Vagrant logo")

>Development Environments Made Easy

 </center>

 ---

## **¿Que es?**

<p style='text-align: justify;'>
Vagrant es una herramienta o aplicación de líneas de comando utilizada en el sector IT, especialmente por desarrolladores. Permite la creación de entornos de desarrollo virtualizados que pueden ser reproducidos y compartidos de una forma muy fácil.</p>

<p style='text-align: justify;'>
Esta herramienta nos permite una serie de comandos y ficheros de configuración que pueden movilizarse de un entorno a otro, y donde podremos desarrollar y hacer las pruebas que nos sean necesarias y eliminarlo cuando hayamos terminado. Vagrant puede utilizar VirtualBox con el objetivo de simplificar la configuración de este software de virtualización.</p>

<p style='text-align: justify;'>
Esta aplicación nos permitirá manejar y configurar máquinas virtuales manteniendo un mismo entorno de trabajo y brindándoles a estas máquinas las diferentes herramientas de gestión de configuración. El mecanismo de Vagrant también facilita el proceso de desarrollo de software cuando este es montado por más de una persona, debido a que evita los problemas de compatibilidad entre sistemas y brinda la posibilidad de compartir sus archivos o también llamados, archivos Vagrantfile, donde se centralizan las configuraciones creadas.</p>

## Simple y potente
 <p style='text-align: justify;'>
HashiCorp Vagrant proporciona el mismo flujo de trabajo fácil, independientemente de su función como desarrollador, operador o diseñador. Aprovecha un archivo de configuración declarativa que describe todos sus requisitos de software, paquetes, configuración del sistema operativo, usuarios y más.</p>

<pre><code>
$ vagrant init hashicorp/bionic64
$ vagrant up
  Bringing machine 'default' up with 'virtualbox' provider...
  ==> default: Importing base box 'hashicorp/bionic64'...
  ==> default: Forwarding ports...
  default: 22 (guest)
  => 2222 (host) (adapter 1)
  ==> default: Waiting for machine to boot...
 
$ vagrant ssh
  vagrant@bionic64:~$ _
</code></pre>

---

## **¿Por qué Vagrant?**

<p style='text-align: justify;'>Vagrant proporciona entornos de trabajo fáciles de configurar, reproducibles y portátiles construidos sobre la tecnología estándar de la industria y controlados por un único flujo de trabajo consistente para ayudar a maximizar la productividad y la flexibilidad de usted y su equipo.</p>

<p style='text-align: justify;'>Para lograr su magia, Vagrant se apoya en los hombros de gigantes. Las máquinas se aprovisionan sobre VirtualBox, VMware, AWS o cualquier otro proveedor. Entonces, estándar de la industria herramientas de aprovisionamiento como scripts de shell, Chef o Puppet, pueden instalar y configurar automáticamente el software en la máquina virtual.</p>

---

## **Características**
- Software libre.
- Escrito en ruby.
- Github.
- Han contribuido cientos de personas.

---

## **Aspectos clave de Vagrant**

<p style='text-align: justify;'>
Vagrant es una herramienta de software open source que simplifica el trabajo de ejecución y de gestión de máquinas virtuales, unificando las diversas plataformas de virtualización que existen en una única interfaz.</p>

---

## **Ventajas**
- Aumenta la flexibilidad.
- Facilita la distribución de entornos virtuales.
- Gran facilidad de uso.
- Aporta la seguridad de duplicar con exactitud un entorno.
- Resulta muy útil en las fases de desarrollo.

---

## **Problema** 

1. Configurar escenarios a mano es tedioso y provoca errores.
2. Un desarrolador debe centrarse en el desarrollo .
3. Los escenarios pueden cambiar .

---

## **Una Solución** 

- Distribuir de forma separada imagenes de OS y la configuracion completa.
    - Muy ligero.
    - Facil de modificar y redistribuir.
    - Facilmente integrable en el flujo de trabajo.
    - Muy util para software libre.

---    

  ## **Limitaciones** 

  1. Configuracion avanzadas depende del provedor.
  2. No adecuados para escenarios complejos.
  3. Recursos limitados para entornos de Cloud Computing.    

---   

## **¿Cómo instalar Vagrant**

1.	Para instalar Vagrant, primero debemos descargarlo desde la página oficial de esta herramienta, eligiendo el sistema que usarás como por ejemplo Windows o Mac y completarás los pasos de instalación.
2.	Será necesario la descarga del proveedor software de visualización que vayamos a utilizar, como puede ser VirtualBox.
3.	Para verificar que Vagrant ya está instalada en nuestros dispositivos, iremos a una terminal (Linux o Mac) o PowerShell (Windows) y escribiremos «vagrant». Si la instalación se realizó correctamente, deberán aparecernos los comandos más comunes como «box», «connect», «login» y otros.


---

## Comandos básicos de Vagrant

1. Muestra la versión actual
<pre><code># vagrant --version
Vagrant 2.0.2</code></pre>

2. Enumerar todos los box 
<pre><code>#vagrant box list
iamseth/rhel-7.3 (virtualbox, 1.0.0)</code></pre>

3. Agregar un box

<pre><code>#vagrant box add [options] < name, url, or path > </code></pre>

- Puede ser de https://app.vagrantup.com/boxes/searchDescarga varios archivos de imagen de Vagrant

    <pre><code>#vagrant box add ubuntu/trusty64</code></pre>

-  Agregar box remoto a través de la URL especificada 

    <pre><code>#vagrant box add https://atlas.hashicorp.com/ubuntu/boxes/trusty64</code></pre>

 - Agregue un box local   

  <pre><code># vagrant box add {box_name} {file_path}

   Ejemplos:

  # vagrant box add CentOS7.1 file:///D:/Work/VagrantBoxes/CentOS-7.1.1503-x86_64-netboot.box </code></pre>

4. Inicialice una nueva máquina virtual

<pre><code># vagrant init ubuntu/trustry64</code></pre>

- Este comando creará un archivo de configuración llamado Vagrantfile en el directorio actual. El contenido es aproximadamente el siguiente:

<pre><code>Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
end</code></pre>

- Después de iniciar Vagrant en este directorio, Vagrant descargará el cuadro "ubuntu / trusty64" de Internet al local y lo usará como imagen de VM.



5. Inicialice una nueva máquina virtual

<pre><code># vagrant up</code></pre>

- Si queremos iniciar cualquier VM, primero ingrese al directorio con el archivo de configuración de Vagrantfile, y luego ejecute el comando anterior. La salida de la consola suele ser la siguiente:

<pre><code>Bringing machine 'default' up with 'virtualbox' provider...
==> default: Importing base box 'ubuntu/trusty64'...
==> default: Matching MAC address for NAT networking...
==> default: Checking if box 'ubuntu/trusty64' is up to date...
==> default: Setting the name of the VM: start_default_1518789015107_16928
==> default: Clearing any previously set forwarded ports...
Vagrant is currently configured to create VirtualBox synced folders with
the `SharedFoldersEnableSymlinksCreate` option enabled. If the Vagrant
guest is not trusted, you may want to disable this option. For more
information on this option, please refer to the VirtualBox manual:
 
  https://www.virtualbox.org/manual/ch04.html#sharedfolders
 
This option can be disabled globally with an environment variable:
 
  VAGRANT_DISABLE_VBOXSYMLINKCREATE=1
 
or on a per folder basis within the Vagrantfile:
 
  config.vm.synced_folder '/host/path', '/guest/path', SharedFoldersEnableSymlinksCreate: false
==> default: Clearing any previously set network interfaces...
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
==> default: Forwarding ports...
    default: 22 (guest) => 2222 (host) (adapter 1)
==> default: Booting VM...
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
    default:
    default: Vagrant insecure key detected. Vagrant will automatically replace
    default: this with a newly generated keypair for better security.
    default:
    default: Inserting generated public key within guest...
    default: Removing insecure key from the guest if it's present...
    default: Key inserted! Disconnecting and reconnecting using new SSH key...
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
    default: The guest additions on this VM do not match the installed version of
    default: VirtualBox! In most cases this is fine, but in rare cases it can
    default: prevent things such as shared folders from working properly. If you see
    default: shared folder errors, please make sure the guest additions within the
    default: virtual machine match the version of VirtualBox you have installed on
    default: your host and reload your VM.
    default:
    default: Guest Additions Version: 4.3.36
    default: VirtualBox Version: 5.2
==> default: Mounting shared folders...
    default: /vagrant => /Users/qianlong/DockerProjects/vagrant/start</code></pre>

6. Habilite SSH para iniciar sesión en la VM

- Ingrese al directorio donde se encuentra el archivo de configuración de Vagrantfile y ejecute el siguiente comando:

<pre><code># vagrant ssh</code></pre>

- Si necesita salir de la máquina virtual, escriba directamente en la línea de comando en la máquina virtual exit.

7. Ver el estado actual de la VM

- Ingrese al directorio donde se encuentra el archivo de configuración de Vagrantfile y ejecute el siguiente comando:

<pre><code># vagrant status </code></pre>

- Si la VM se está ejecutando, puede ver la siguiente información en la consola:

<pre><code>Current machine states:
 
default                   running (virtualbox)
 
The VM is running. To stop this VM, you can run `vagrant halt` to
shut it down forcefully, or you can run `vagrant suspend` to simply
suspend the virtual machine. In either case, to restart it again,
simply run `vagrant up`.</code></pre>

8. Apague la VM

- Ingrese al directorio donde se encuentra el archivo de configuración de Vagrantfile y ejecute el siguiente comando:

<pre><code># vagrant halt</code></pre>

9. Destruye la VM

- El formato del comando es el siguiente:

<pre><code>vagrant destory [name|id]</code></pre>

- Los ejemplos son los siguientes:

<pre><code># vagrant destroy ubuntu/trusty64</code></pre>

- Si estamos usando el nombre predeterminado de la máquina virtual "default", entonces podemos ingresar directamente el siguiente comando para destruir la VM

<pre><code># vagrant desotry</code></pre>

- Los resultados son los siguientes:

<pre><code>    default: Are you sure you want to destroy the 'default' VM? [y/N] y
==> default: Forcing shutdown of VM...
==> default: Destroying VM and associated drives...</code></pre>