# How-to-use-Github
In this repository we will learn a few essential things for Github. We are going to do step by step three things. The first one: Create a Repository on Github. Second One: Do a commit. Third One: Sign Commits with a GPG Key. Good Luck 😁
# Uso básico de Git
Se aprenderán las funciones esenciales para dar un desarrollo y desenvolverse de manera óptima en el hámbito de trabajo junto a Nautilus Cyberneering.
## Tareas
    Crear un repo en Github
    Hacer commits
    Firmar commits con clave GPG.


### Crear Repositorio en Github
- Crear cuenta en GitHub.com y comprobar la dirección de correo electrónico.
- Acceder a Inicio
- Clickar en el +
    - New Repository
![Captura de pantalla 2024-03-13 a las 14.42.58](https://hackmd.io/_uploads/BJ92iVkRT.png)
- Rellenar los campos:
        - Repository Name
        - Description (opcional)
        - Pública o Privada
        - Añadir un Readme.md (recomendable)
- Create Repository
![Captura de pantalla 2024-03-13 a las 14.54.12](https://hackmd.io/_uploads/S1bNCVkAa.png)
### Vista final del primer paso(Crear un repositorio.)
![Captura de pantalla 2024-03-13 a las 14.55.11](https://hackmd.io/_uploads/HJX50V1CT.png)


### Hacer Commits
Hay varias maneras de hacer commits, en este caso veremos dos, subiendo el propio archivo arrastrándolo desde la carpeta donde la tengamos hasta Github (eficaz pero poco práctico) y también desde la propia consola o github Desktop en mi caso usaré github Desktop.
#### Desde Github
- Entramos al repositorio
- Clickamos en Add file
        - Upload Files
![Captura de pantalla 2024-03-13 a las 15.39.48](https://hackmd.io/_uploads/BJy-KSk0a.png)
- Arrastramos el archivo a esta zona:
![Captura de pantalla 2024-03-13 a las 16.10.51](https://hackmd.io/_uploads/HJGXl8kA6.png)
- Esperamos a que cargue
- Rellenamos los campos del commit
 ![Captura de pantalla 2024-03-13 a las 16.13.15](https://hackmd.io/_uploads/SJXhgLy0a.png)
- Seleccionamos si queremos que el commit vaya directamente al main o a una rama.(Yo lo haré a una nueva rama y le asignaré el nombre de Primer commit de prueba).
- Clickas en Propose changes
- Seleccionamos create pull request
![Captura de pantalla 2024-03-13 a las 16.24.39](https://hackmd.io/_uploads/B1bYXUyRT.png)
- Finalmente le damos a merge pull request
![Captura de pantalla 2024-03-13 a las 16.26.37](https://hackmd.io/_uploads/HyCCQIyAp.png)
- Y le damos a Confirm merge
Debería aparecer lo siguiente
![Captura de pantalla 2024-03-13 a las 16.27.56](https://hackmd.io/_uploads/BkamEIJRp.png)
#### Desde GitHub Desktop
- Entramos en GitHub Desktop
- Iniciamos sesión con nuestro GitHub que creamos anteriormente
- Seleccionamos el repositorio en el que estamos trabajando
- se vería de la siguiente manera:
![Captura de pantalla 2024-03-13 a las 16.43.04](https://hackmd.io/_uploads/Hy_pwU1Cp.png)
No tenemos ningún cambio hecho para hacer el commit por lo tanto tendremos que añadir algo a nuestro proyecto.
- Una vez hechos los cambios se verá de la siguiente manera:
![Captura de pantalla 2024-03-13 a las 16.50.40](https://hackmd.io/_uploads/ByaKKIJAT.png)
Ya esá todo listo para el siguiente commit
- Debemos rellenar las casillas de abajo para poder realizar el commit
![Captura de pantalla 2024-03-13 a las 16.53.19](https://hackmd.io/_uploads/B1lGcL10T.png)
- Le damos a Commit to main para mandar los cambios y pasarlos a la rama principal
- Clickamos en push origin
![Captura de pantalla 2024-03-13 a las 16.54.26](https://hackmd.io/_uploads/SJ98qIkRa.png)
- Ya estaría el commit realizado.

No hay que olvidar que también se puede hacer con comandos desde la terminal sin embargo GitHub Desktop es mucho más intuitiva y fácil de usar, siendo así más óptimo en tiempo y evitando o disminuyendo considerablemente la posibilidad de cometer errores.

### Firmar Commits con clave GPG
Seguiremos los pasos de este tutorial: https://secure-git.guide/

En mi caso lo instalé en MAC, ahora deberemos continuar con este otro tutorial para configurar las claves GPG mediante este tutorial: https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key
**Comenzamos con la generación de claves y su configuración** 
![Captura de pantalla 2024-03-15 a las 10.51.30](https://hackmd.io/_uploads/H11q8n-R6.png)
    
    Escribimos en consola gpg para comprobar que está instalado.

#### - Creamos un par de claves
>gpg --full-generate-key

Pulsamos enter y se pondrá la elección por defecto
![Captura de pantalla 2024-03-15 a las 12.07.59](https://hackmd.io/_uploads/H1QE92Z0a.png)
Volvemos a pulsar enter y se gardará el tamaño de key por defecto
![Captura de pantalla 2024-03-15 a las 12.08.54](https://hackmd.io/_uploads/r1aDchbAa.png)
Ahora continuaremos eligiendo tiempo de caducidad de la key

    Por seguridad es recomendable ponerle fecha de caducidad
![Captura de pantalla 2024-03-15 a las 12.11.41](https://hackmd.io/_uploads/ryEGohb0a.png)
Le pusimos una fecha de caducidad de 1 año

Nos dirá que tenemos que añadir una id:

    GnuPG needs to construct a user ID to identify your key.
![Captura de pantalla 2024-03-15 a las 12.27.46](https://hackmd.io/_uploads/Bkp0R2bCT.png)

Nos dirá de crear una passphrase (contraseña) de al menos 8 carácteres.

#### - Listar la forma larga de las claves GPG

    gpg --list-secret-keys --keyid-format=long

![Captura de pantalla 2024-03-15 a las 12.35.02](https://hackmd.io/_uploads/HyxcepbRp.png)

    Mi clave en este caso es la larga: 37EF7936C57B357C
- Copiamos el siguiente texto y en lugar de mi clave pone la suya
               
        gpg --armor --export 37EF7936C57B357C 
- Copiamos la clave GPG, empezando por [-----BEGIN PGP PUBLIC KEY BLOCK-----]  y terminando por [-----BEGIN PGP PUBLIC KEY BLOCK-----]

        La parte de consola a estaría terminada
- Entramos en Github
    - Clickamos en nuestra foto de perfil en la parte superior a la derecha
    - ![Captura de pantalla 2024-03-15 a las 12.46.36](https://hackmd.io/_uploads/S1xr7pZCa.png)
    - Settings
    - En la parte de Acces, vamos a SSH and GPG keys.
    - ![Captura de pantalla 2024-03-15 a las 12.50.38](https://hackmd.io/_uploads/rJbN4aZ0p.png)
    - New GPG key
    - ![Captura de pantalla 2024-03-15 a las 12.51.14](https://hackmd.io/_uploads/ByO1rTW06.png)
    - En title ponemos un nombre a nuestra clave GPG
    - EN Key se pone toda la clave pública añadiendo también el texto de begin y end
    - Add GPG key
- Autorizamos la key
- Ya quedaría hecha la key
![Captura de pantalla 2024-03-15 a las 12.58.48](https://hackmd.io/_uploads/HycmIabR6.png)

#### Firma del commit con GPG Key
---
Subimos git global nuestro nombre y correo(este debe ser el mismo que usamos en github).
![Captura de pantalla 2024-03-15 a las 14.08.25](https://hackmd.io/_uploads/Sk2P80ZAT.png)
![Captura de pantalla 2024-03-15 a las 14.12.14](https://hackmd.io/_uploads/SyBUwCWRp.png)
Activamos el gpg a la hora de activarse un commit además de su tag y dreccion de gpg

    Buscamos la ubicación de gpg
![Captura de pantalla 2024-03-15 a las 14.14.11](https://hackmd.io/_uploads/BkNTvCZC6.png)

![Captura de pantalla 2024-03-15 a las 14.14.57](https://hackmd.io/_uploads/SkVluAWRT.png)

Comprobamos el funconamiento

![Captura de pantalla 2024-03-15 a las 14.19.03](https://hackmd.io/_uploads/SyTJt0WAp.png)

Ejecutamos en la terminal de Visual Studio Code los siguientes comandos
![Captura de pantalla 2024-03-15 a las 15.04.20](https://hackmd.io/_uploads/SJi9QyfAa.png)

![Captura de pantalla 2024-03-15 a las 15.05.08](https://hackmd.io/_uploads/H1on71GRa.png)

Entramos en github y comprobamos que esté verificado el cambio
![Captura de pantalla 2024-03-15 a las 15.05.57](https://hackmd.io/_uploads/HJfgVkz06.png)

Eso sería todo.






















