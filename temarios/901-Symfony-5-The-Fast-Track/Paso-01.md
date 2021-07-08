# Paso 1 Revisando tu entorno de trabajo

Por favor, no te saltes este paso. O al menos, lee la última sección sobre la CLI de Symfony.

## 1.1 Un ordenador

Necesitas un ordenador. La buena noticia es que Symfony puede funcionar en cualquiera de los sistemas operativos más conocidos:
macOS, Windows o Linux. Symfony y todas las herramientas que vamos a utilizar son compatibles con cada uno de ellos.

### 1.2 Decisiones subjetivas

Quiero ir rápido con las mejores opciones. He tomado decisiones subjetivas para este libro.

**PostgreSQL** va a ser nuestra elección para todo: desde la base de datos hasta las colas, desde la caché hasta el almacenamiento en sesión. Para
la mayoría de los proyectos, PostgreSQL es la mejor solución, tiene gran escalabilidad y permite simplificar la infraestructura administrando solo
un único servicio.

Al final del libro, aprenderemos a gestionar las colas de mensajes con **RabbitMQ** y las sesiones con **Redis**.

### 1.3 IDE

Recomendaría usar **Visual Studio Code** o **PhpStorm** . El primero es gratuito, el segundo no lo es pero tiene una mejor integración con
Symfony (gracias al *plugin de soporte de Symfony* ). Estoy escribiendo este libro en Visual Studio Code.

### 1.4 Terminal

Cambiaremos del IDE a la línea de comandos todo el tiempo. Puedes usar el terminal incorporado de tu IDE, pero yo prefiero usar uno real para
tener más espacio.

Linux viene con un Terminal incorporado. Utiliza **iTerm2** en macOS. En Windows, **Hyper** funciona bien.

### 1.5 Git

Parece que todo el mundo está usando Git ahora. En Windows, instala **Git bash**. Asegúrate de que sabes cómo realizar las operaciones más comunes,
como ejecutar **`git clone`**, **`git log`**, **`git show`**, **`git diff`**, **`git checkout`** ...

### 1.6 PHP

Usaremos **Docker** para los servicios, pero me gusta tener PHP instalado en mi ordenador local por razones de rendimiento, estabilidad y
simplicidad. La combinación de un servicio local de PHP y Docker es la combinación perfecta para mí.

Usa **PHP 8.0** y comprueba que las siguientes extensiones de PHP están instaladas o instálalas ahora: **`intl`** , **`pdo_pgsql`** , **`xsl`** , **`amqp , **`gd , **`openssl y
**`sodium. Opcionalmente también puedes instalar redis, curl y zip.
Puedes comprobar las extensiones habilitadas actualmente usando php
-m.
También necesitamos php-fpm si tu plataforma lo soporta, php-cgi
también sirve.
1.7Composer
Hoy en día, gestionar dependencias lo es todo en un proyecto Symfony.
Descarga la última versión de Composer , la herramienta de gestión de
paquetes para PHP.
Si no estás familiarizado con Composer, tómate un tiempo para leer sobre
él.
33No es necesario que escribas los nombres completos de los comandos:
composer req hace lo mismo que composer require, usa composer rem en
lugar de composer remove…
1.8 NodeJS
No escribiremos mucho código JavaScript, pero usaremos herramientas
JavaScript / NodeJS para administrar nuestros assets. Comprueba que
tienes NodeJS instalado y el gestor de paquetes Yarn.
1.9 Docker y Docker Compose
Gestionaremos los servicios mediante Docker y Docker Compose.
Instálalos e inicia Docker. Si es la primera vez que lo utilizas, familiarízate
con él. Pero no te asustes, lo usaremos de forma muy sencilla. Sin
configuraciones sofisticadas ni complejas.
1.10Symfony CLI
Por último, pero no por ello menos importante, utilizaremos la línea de
comandos (CLI) de symfony para aumentar nuestra productividad. Desde
el servidor web local que proporciona, hasta la integración completa con
Docker y el soporte de SymfonyCloud, nos servirá para ahorrar mucho
tiempo.
Instala Symfony CLI y muévelo a algún lugar dentro de tu $PATH. Crea
una cuenta SymfonyConnect si aún no la tienes e inicia sesión a través de
symfony login.
Para utilizar HTTPS localmente, también necesitamos instalar una
autoridad de certificación (CA) para habilitar el soporte de TLS. Ejecuta el
siguiente comando:
$ symfony server:ca:install
34Comprueba que tu ordenador tiene todos los requisitos necesarios
ejecutando el siguiente comando:
$ symfony book:check-requirements
Si quieres trabajar de forma aún más elegante, también puedes ejecutar el
proxy de Symfony . Es opcional, pero te permite obtener un nombre de
dominio local que termina en .wip para tu proyecto.
Cuando ejecutemos un comando en una terminal, casi siempre le
pondremos el prefijo symfony, por ejemplo symfony composer, en vez de
sólo composer , o symfony console en lugar de ./bin/console.
La razón principal es que la CLI de Symfony establece automáticamente
algunas variables de entorno basadas en los servicios que se ejecutan
en tu máquina a través de Docker. Estas variables de entorno están
disponibles para las peticiones HTTP porque el servidor web local las
inyecta automáticamente. Por lo tanto, el uso de symfony en la CLI
asegura que tengas el mismo comportamiento en todos los componentes
de tu entorno.
Además, la CLI de Symfony selecciona automáticamente la «mejor»
versión posible de PHP para el proyecto.
35
