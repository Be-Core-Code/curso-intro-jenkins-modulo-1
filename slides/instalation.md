### Instalación

* Usando `.war`
* Linux
* Windows
* MacOS
* Desde docker
* Usando docker inside docker

^^^^^^

#### Instalación usando `.war`

* Descargar el fichero .war
* En una terminal ejecutar el comando:
  ```bash
  > java -jar jenkins.war --httpPort=8080.
  ```
* Abrir el navegador y acceder a `http://localhost:8080`


notes:

([ver documentación](https://jenkins.io/doc/book/installing/#war-file))


^^^^^^
#### Instalación usando `.war`


```
...
...
*************************************************************
*************************************************************

Jenkins initial setup is required. An admin user has been 
created and a password generated.
Please use the following password to proceed to installation:

874ca566f02243eabc92226d921756a8

This may also be found at: /home/theuser/.jenkins/secrets/initialAdminPassword

*************************************************************
*************************************************************
```

^^^^^^
#### Instalación usando `.war`

![Unlock Jenkins](/slides/images/unlock_jenkins.png)<!-- .element: class="plain" -->


^^^^^^
#### Instalación usando `.war`

![Install selected plugins](/slides/images/install_suggested_plugins.png)<!-- .element: class="plain" -->

notes:

Se recomienda la opción para instalar los plugins recomendados. Esta opción instala una batería de plugins
estándar que nos permitirá empezar a trabajar con la herramienta sin demasiado esfuerzo.

Una vez hayas cogido práctica con la herramienta, estarás en mejores condiciones para usar la opción manual
y seleccionar únicamente los plugins que necesites.

^^^^^^
#### Instalación usando `.war`

![Installing plugins](/slides/images/installing_plugins.png)<!-- .element: class="plain" -->

^^^^^^
#### Instalación usando `.war`

![Create admin user](/slides/images/create_first_admin_user.png)<!-- .element: class="plain" -->

^^^^^^
#### Instalación en Linux

Jenkins se puede instalar usando `apt` o `rpm`

^^^^^^
##### Instalación en Debian / Ubuntu


```bash
> wget -q -O - https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
> sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
> sudo apt-get update
> sudo apt-get install jenkins
```

notes:

([ver documentación](https://jenkins.io/doc/book/installing/#debianubuntu))



^^^^^^
##### Instalación en Debian / Ubuntu


* Configura Jenkins para que se levante como un demonio al arranque (ver /etc/init.d/jenkins para más detalles)
* Crea el usuario `jenkins` para ejecutar el servicio
* Direcciona la salida de la consola de log al fichero `/var/log/jenkins/jenkins.log`
* Añade el fichero `/etc/default/jenkins` con los parámetros de arranque de jenkins (JENKINS_HOME, etc)
* Configura Jenkins para escuchar en el puerto 8080

^^^^^^
##### Instalación en Debian / Ubuntu

* Editar el fichero `/etc/default/jenkins` y cambiar el valor de HTTP_PORT si queremos que arranque en otro puerto

^^^^^^
##### Instalación en Fedora

```bash
> sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat/jenkins.repo
> sudo rpm --import https://jenkins-ci.org/redhat/jenkins-ci.org.key
> sudo dnf upgrade && sudo dnf install jenkins java
> sudo service jenkins start
> sudo chkconfig jenkins on
```

notes:

([ver documentación](https://jenkins.io/doc/book/installing/#fedora))


^^^^^^
##### Instalación en Fedora

Utilizar el siguiente comando para verificar que está correctamente instalado:

```bash
> systemctl status jenkins
```

^^^^^^
#### Instalación en Windows

Dispone de un instalador para windows:

* Descartar la [última versión](http://mirrors.jenkins.io/windows/latest)
* Seguir las instrucciones de instalación


^^^^^^
#### Instalación en MacOS

Se recomienda la instalación usando [`Homebrew`](https://brew.sh/)

* Instala la última versión LTS: `brew install jenkins-lts``
* Inicia el servicio de Jenkins: `brew services start jenkins-lts`
* Reinicia el servicio de Jenkins: `brew services restart jenkins-lts`
* Actualiza la versión de Jenkins: `brew upgrade jenkins-lts`

notes:

([ver documentación](https://jenkins.io/download/lts/macos/))
