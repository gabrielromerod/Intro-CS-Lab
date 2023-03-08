# Semana 5: Git, GitHub y Terminal
Git es una herramienta que realiza una función del control de versiones de código de forma distribuida.

GitHub es un sitio "social coding". Te permite subir repositorios de código para almacenarlo en el sistema de control de versiones Git. En simples palabra el Facebook de los programadores. :wink:

La terminal o consola es una forma generalizada de llamar a la interfaz de usuario de línea de comandos: una pantalla (generalmente, de color de fondo negro sobre letras blancas) donde escribiendo comandos (secuencias de palabras especiales) ordenamos al sistema realizar acciones concretas. Aunque una interfaz gráfica de usuario (GUI) puede ser más cómoda y agradable para el usuario, las razones para preferir una interfaz de línea de comandos son muchas:

 - Es más rápido crear un programa para línea de comandos.
 - Suele ser más potente en cuanto a personalización de opciones.
 - Permite creación de scripts para automatizar tareas repetitivas.
 - Suele ser una opción más universal entre sistemas.
 - Suele ser instantáneo, al no tener que cargar pantallas gráficas.
 - Acceder a servidores de manera remota.

Antes de aprender como usar git debemos conocer a la terminal, ya que para interactuar con Git vamos a emplear una terminal. Ahora nos preguntamos: ¿Cómo abro la famosa terminal?

- Windows cuenta con dos terminales que no son muy amigables a los programadores, pero que han impactado a la cultura popular.

    1. Windows Command Prompt (CMD): El símbolo del sistema (en inglés, 'Command Prompt', también conocido como cmd.exe o simplemente cmd) es el intérprete de comandos.

    ![Command Prompt Image](https://upload.wikimedia.org/wikipedia/commons/b/b3/Command_Prompt_on_Windows_10_RTM.png)
    
    2. Windows Power Shell: Se considera la evolución del CMD, aumenta la cantidad de funciones y optimiza los procesos previos.

    ![Power Shell Image](https://www.muycomputerpro.com/wp-content/uploads/2019/04/PowerShell7.jpg)

- MAC y Linux cuentan con famoso un shell llamado Unix, dicho shell es más conocido como bash. Dentro de sus principales caracteristicas permite la integracion de herramientas para desarrolladores con facilidad.

    1. Ubuntu Terminal:
    
    ![Ubuntu Terminal Image](https://www.ionos.es/digitalguide/fileadmin/DigitalGuide/Screenshots/ubuntu-bash.png)

    2. Mac OS Terminal:

    ![Mac OS Terminal Image](https://tecno-adictos.com/wp-content/uploads/2021/06/Como-usar-la-terminal-macOS-una-guia-para-principiantes.png)

## Comandos básicos de la terminal:
Como bien sabemos desde los inicios de la computación la terminal
se usaba como medio para interactuar con la computadora para ello existen los famosos comandos. A continuación, te dejo unos comandos elementales con sus equivalentes para Windows, Mac OS y Linux:

```
cd -> Change Directory
ls -> List Files == dir Windows
pwd -> Print Working Directory
mkdir -> Create a Folder
rm -> Remove File
rm -r -> Remove Directory
cat > -> Create file
mv -> Move File or Directory
cd .. -> Volver al repositorio anterior
```

1. cd - Change Directory permite moverse entre directorios una actividad que hacemos a diario en el explorador de archivos:
![Change Directory Image](https://generalassembly.github.io/prework/cl/Graphics/terminal_cd.gif)

2. ls - List Files permite ver las carpetas y archivos:
![List Files Image](https://www.solvetic.com/uploads/monthly_03_2017/tutorials-7463-0-36962500-1489423518.jpg)

3. dir - List Files permite ver las carpetas y archivos en Windows:
![List Files Image](https://www.solvetic.com/uploads/monthly_03_2017/tutorials-7463-0-36962500-1489423518.jpg)

4. pwd - Print Working Directory muestra el directorio actual, para windows cd solo te muestra la ubicación:
![PWD Image](https://generalassembly.github.io/prework/cl/Graphics/terminal_ls.gif)

5. mkdir - Create a Folder crea una carpeta el directorio actual:
![mkdir Image](https://generalassembly.github.io/prework/cl/Graphics/terminal_rm_r.gif)

Ahora ya sabemos unos cuantos comandos básicos que son lo suficiente para usar git y pasar el curso por el momento.

## Pasos para empezar a usar git:
1. Tenemos que instalar git desde la [pagina web oficial](https://git-scm.com/download/win) para el caso de Windows. Por otro lado, en MAC y Linux desde la terminal debemos verificar que tenemos git instalado usando el siguiente comando:
```
git --version
```
- Una vez que tengas instalado Git tienes que identificarte con git para ello ejecutas dos comandos uno para indicar tu nombre de usuario que aparecera cuando te conectes a GitHub y otro para el correo que es el de la misma cuenta de GitHub. 
```
git config --global user.name "Gabriel Romero"
```
```
git config --global user.email "gabriel.romero@utec.edu.pe"
```
2. Tenemos que inciar nuestro repositorio para ello ejecutamos el siguiente comando en el carpeta que vamos a usar en nuestro proyecto:
```
git init
```

3. Git tiene tres estados principales en los que se pueden encontrar tus archivos: confirmado (committed), modificado (modified), y preparado (staged). 

    - Confirmado: significa que los datos están almacenados de manera segura en tu base de datos local. 
    - Modificado: significa que has modificado el archivo pero todavía no lo has confirmado a tu base de datos. 
    - Preparado: significa que has marcado un archivo modificado en su versión actual para que vaya en tu próxima confirmación. 
    
    - Esto nos lleva a las tres secciones principales de un proyecto de Git: El directorio de Git (Git directory), el directorio de trabajo (working directory), y el área de preparación (staging area). El flujo de trabajo básico en Git es algo así:

    1. Modificas una serie de archivos en tu directorio de trabajo.
    2. Preparas los archivos, añadiéndolos a tu área de preparación.
    3. Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación y almacena esa copia instantánea de manera permanente en tu directorio de Git.

![git phases Image](https://static.packt-cdn.com/products/9781782168454/graphics/8454OS_01_4.jpg)

4. Como solamente hemos creado nuestro directorio, tendriamos que comenzar que crear trabajar ahi y una vez terminemos ejecutamos el comando add puedes colocar cada archivo manualmente o usar un punto para agregar todos:
```
git add elnombredetuarhivo.txt
```
```
git add .
```

5. Ahora usamos el famoso commit lo puedes poder con un comentario o sin un comentario.
```
git commit -m "Tu mensaje va aqui"
```

6. Crea una cuenta de [GitHub](https://github.com/signup)

7. Crea un repositorio:

    - En la esquina superior derecha de cualquier página, utiliza el menú desplegable  y selecciona Repositorio:
    ![git create Image](https://docs.github.com/assets/cb-11427/images/help/repository/repo-create.png)
    - Escribe un nombre corto y fácil de recordar para tu repositorio. Por ejemplo: "hola-mundo".
    ![git create Image](https://docs.github.com/assets/cb-25139/images/help/repository/create-repository-name.png)
    - También puedes agregar una descripción de tu repositorio. Por ejemplo, "Mi primer repositorio en GitHub".
    ![git create Image](https://docs.github.com/assets/cb-26377/images/help/repository/create-repository-desc.png)
    - Elige la visibilidad del repositorio. Para obtener más información, consulta la sección "Acerca de los repositorios":
    ![git create Image](https://docs.github.com/assets/cb-20877/images/help/repository/create-repository-public-private.png)
    - Selecciona Inicializar este repositiro con un README:
    ![git create Image](https://docs.github.com/assets/cb-49938/images/help/repository/initialize-with-readme.png)
    - Haz clic en Crear repositorio:
    ![git create Image](https://docs.github.com/assets/cb-19887/images/help/repository/create-repository-button.png)

8. Crear repositorios remotos:
    - Una URL HTTPS como https://github.com/user/repo.git
    - Una URL SSH como git@github.com:user/repo.git
```
git remote add origin  <REMOTE_URL> 
```

9. Subimos el repositorio con push:
```
git push
```

Si quieres ver el nombre y correo de la cuenta:
```
git config -e --global
```
