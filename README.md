## ¿Cómo arranco / instalo el proyecto en mi máquina?


#### Provisionamiento:

#### Instalar las siguientes dependencias, en un sistema basado en Debian (como Ubuntu), se puede hacer:

    ```
        $ sudo apt-get install git python-pip python-dev virtualenv postgresql pgadmin3
    ```

#### Crear y activar un nuevo [virtualenv](https://virtualenv.pypa.io/en/stable/). Recomiendo usar [virtualenvwrapper](https://virtualenvwrapper.readthedocs.io/en/latest/). Se puede instalar así:

    $ sudo pip install virtualenvwrapper

    Y luego agregando la siguiente línea al final del archivo `.bashrc`:

        [[ -s "/usr/local/bin/virtualenvwrapper.sh" ]] && source "/usr/local/bin/virtualenvwrapper.sh"

    Para crear y activar nuestro virtualenv:

        $ mkvirtualenv --system-site-packages --python=/usr/bin/python3 refugio

#### Clonar el repositorio:

    ```
        $ git clone https://github.com/marioferreyra/Curso_Django_CodigoFacilito.git
    ```

#### Instalarlo:

    ```
        $ cd Curso_Django_CodigoFacilito
        $ pip install -r requirements.txt
    ```

#### Activar el entorno virtual:

      ```
          $ workon refugio
      ```

#### Generar y llenar la base de datos:

      ```
          $ python manage.py migrate
      ```


#### Activar el server local:

      ```
          $ python manage.py runserver
      ```

#### Luego en el navegador podras acceder a FotoLink:

      ```
          http://127.0.0.1:8000/
          ó
          http://localhost:8000/
      ```

#### Desactivar el entorno virtual

      ```
          $ deactivate
      ```
