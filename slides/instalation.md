### Instalación

* Usando `.war`
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

([ver documentación](https://jenkins.io/doc/pipeline/tour/getting-started/))


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

