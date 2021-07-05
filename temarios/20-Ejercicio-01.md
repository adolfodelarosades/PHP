# Ejercicio 01 Creación de CRUD para la Gestión de Fondos.

https://carherco.es/ejercicio-2021-07-02/public/

Para realizar este proyecto se siguierón los siguientes pasos:

* 01 Creación del Proyecto
* 02 Añadirlo GIT al Proyecto
* 03 Cargar el Proyecto en VSC
* 04 Ejecutar el Proyecto
* 05 Crear Controlador `Home`
* 06 Crear BD en MySQL llamada `sepe_ejercicio_01`
* 07 Modificar Configuración de la BD en `.env`
* 08 Añadir BootsStrap a la Aplicación
* 09 Modificar Página Home
* 10 Separar Menú y Footer de la Página Home
* 11 Crear Controlador `About`
* 12 Crear Controlador `Login`
* 13 Asociar en el menú las acciones `About` y `Login` 
* 14 Crear Controlador `Fondos`
* 15 Crear Controlador `Editoriales`
* 16 Crear Controlador `Autores`
* 17 Crear Menú para las Opciones de `Fondos`, `Editoriales` y `Autores`


## ✅ 01 Creación del Proyecto

Nos colocamos en el directorio donde deseamos crear el proyecto que llamaremos "ejercicio-01"

![image](https://user-images.githubusercontent.com/23094588/124347228-c7bc5600-dbe3-11eb-9134-ee7e7821380c.png)

Pulsamos el comando:

```sh
composer create-project symfony/website-skeleton ejercicio-01
```

![image](https://user-images.githubusercontent.com/23094588/124347259-ede1f600-dbe3-11eb-8d6e-465eddd9ce2d.png)

El proyecto se empieza a crear.

![image](https://user-images.githubusercontent.com/23094588/124347297-3f8a8080-dbe4-11eb-93cb-9c8da4f6b123.png)

![image](https://user-images.githubusercontent.com/23094588/124347319-60eb6c80-dbe4-11eb-8b8f-9b1b86a3313c.png)

![image](https://user-images.githubusercontent.com/23094588/124347367-a314ae00-dbe4-11eb-947b-0d403f63b88b.png)

Cuando finaliza podemos ver el contenido y comprobar que el proyecto se ha creado.

![image](https://user-images.githubusercontent.com/23094588/124347392-d8b99700-dbe4-11eb-92e6-7045e9b3e9f5.png)

## ✅ 02 Añadirlo GIT al Proyecto

Entramos a la carpeta del proyecto:

![image](https://user-images.githubusercontent.com/23094588/124347589-b4aa8580-dbe5-11eb-8125-1ebdbd277a4d.png)

### Añadir GIT localmente.

Y pulsamos los siguientes comandos git:

```sh
git init

git status

git add .

git status

git commit -m "Commit Inicial"

git status
```

![image](https://user-images.githubusercontent.com/23094588/124347738-5b8f2180-dbe6-11eb-9d5c-07cbd5230023.png)

![image](https://user-images.githubusercontent.com/23094588/124347781-9ee99000-dbe6-11eb-8c3b-b520afa59970.png)

![image](https://user-images.githubusercontent.com/23094588/124347844-ef60ed80-dbe6-11eb-9b4f-00cf3f579650.png)

![image](https://user-images.githubusercontent.com/23094588/124347856-01429080-dbe7-11eb-98ff-525f140e2fe4.png)

![image](https://user-images.githubusercontent.com/23094588/124347951-74e49d80-dbe7-11eb-9ddd-08c24a9cbf2d.png)


### Añadir GitHub

Entrar a nuestra Cuenta de GitHub.

![image](https://user-images.githubusercontent.com/23094588/124348956-1f12f400-dbed-11eb-82ff-c5424c1aced2.png)

![image](https://user-images.githubusercontent.com/23094588/124348984-3b169580-dbed-11eb-956e-7afe982190ad.png)

Vamos a crear un nuevo repositorio llamado `COD-Symphony-5-Ejercicio-01`.

![image](https://user-images.githubusercontent.com/23094588/124351514-23460e00-dbfb-11eb-8711-24ecf2bcc91a.png)

Lo hemos creado totalmente vacío para que nos indique las instrucciones que debemos seguir para ligarlo con el repositorio local.

![image](https://user-images.githubusercontent.com/23094588/124351752-81272580-dbfc-11eb-95aa-688564cb12d0.png)


Nos indica dos grupos de instrucciones, una para cuando no se ha creado el repositorio local:

#### …or create a new repository on the command line

```sh
echo "# COD-Symphony-5-Ejercicio-01" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/adolfodelarosades/COD-Symphony-5-Ejercicio-01.git
git push -u origin main
```

Otro para cuando ya tenemos el repositorio local, que es nuestro caso:

#### …or push an existing repository from the command line

```sh
git remote add origin https://github.com/adolfodelarosades/COD-Symphony-5-Ejercicio-01.git
git branch -M main
git push -u origin main
```

Volviendo a la carpeta del proyecto vamos a hacer algo parecido a la segunda opción:

Vamos a ejecutar el comando que nos suguiere:

```sh
git remote add origin https://github.com/adolfodelarosades/COD-Symphony-5-Ejercicio-01.git
```

![image](https://user-images.githubusercontent.com/23094588/124352027-2b537d00-dbfe-11eb-9d59-4fcc620ee96b.png)

Con esto ya tenemos "likado" el repositorio local con el remoto.

Lo siguiente es hacer un:

```sh
git push
```

![image](https://user-images.githubusercontent.com/23094588/124352104-92713180-dbfe-11eb-80a2-61b6f530a928.png)


Para el primer PUSH debemos ejecutar el comando que nos indica:

```sh
git push --set-upstream origin master
```

Nos pide las claves de nuestra cuenta GitHub.

![image](https://user-images.githubusercontent.com/23094588/124352238-8fc30c00-dbff-11eb-969e-2c8c20b2c9f7.png)

Una vez ingresadas se ha hecho el volcado del repositorio local al remoto, al refrescar el repositorio en GitHub vemos el proyecto subido.

![image](https://user-images.githubusercontent.com/23094588/124352299-de70a600-dbff-11eb-90c0-17e278b2bc86.png)

A partir de aquí los siguientes PUSH serán simplemente con:

```sh
git push
```

## ✅ 03 Cargar el Proyecto en VSC

![image](https://user-images.githubusercontent.com/23094588/124352564-48d61600-dc01-11eb-9d6f-c6f91e212887.png)

La estructura del proyecto la tenemos a la izquierda de VSC:

![image](https://user-images.githubusercontent.com/23094588/124352591-6f944c80-dc01-11eb-9bab-4f3f46abbb38.png)


## ✅ 04 Ejecutar el Proyecto

Para ejecutar el proyecto creado ejecutamos el comando:

```sh
php -S localhost:8000 -t public/
```

Es recomendable abrir una nueva terminal para ejecutar este comando ya que se quedará bloqueada mostrando el LOG del Servidor.

Esto ejecuta el proyecto en un Server que viene incluido con PHP en el puerto 8000:

![image](https://user-images.githubusercontent.com/23094588/124352722-78d1e900-dc02-11eb-9a0d-80cb6e0fc773.png)

Como vemos nos indica que abramos el enlace `http://localhost:8000` en el navegador.

![image](https://user-images.githubusercontent.com/23094588/124352792-ed0c8c80-dc02-11eb-80c8-a01efe14dd98.png)

Los enlaces que nos suguiere son:

https://symfony.com/doc/current/index.html

https://symfony.com/doc/current/page_creation.html

https://symfony.com/community


## ✅ 05 Crear Controlador `Home`

Vamos a comenzar por crear la página Home de la APP, creando el controlador `Home` con la siguiete instrucción:

```sh
php bin/console make:controller
```

![image](https://user-images.githubusercontent.com/23094588/124357848-e3dce900-dc1d-11eb-9079-824b1160c602.png)

Con esto se han creado dos archivos `HomeController.php` e `index.html.twig` en las rutas que nos indica. 

![image](https://user-images.githubusercontent.com/23094588/124357930-3fa77200-dc1e-11eb-8ab6-3d6acbeaf717.png)


Podemos invocar a la ruta `http://localhost:8000/home` para ver la plantilla asociada al Controlador `Home`.

![image](https://user-images.githubusercontent.com/23094588/124358012-9ad96480-dc1e-11eb-9125-b12816246114.png)

Pero como podemos ver nos presenta una excepción, esto se debe a que necesita información sobre la BD.

:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git status
git commit -m "Crear Controlador Home"
git status
git push

```

![image](https://user-images.githubusercontent.com/23094588/124358244-b6913a80-dc1f-11eb-8c83-395fdace2f2a.png)

![image](https://user-images.githubusercontent.com/23094588/124358298-fb1cd600-dc1f-11eb-8dd5-c53676fd3cbc.png)

![image](https://user-images.githubusercontent.com/23094588/124358365-3ae3bd80-dc20-11eb-9758-f582d1388a09.png)



## ✅ 06 Crear BD en MySQL llamada `sepe_ejercicio_01`

![image](https://user-images.githubusercontent.com/23094588/124358094-ff94bf00-dc1e-11eb-8d74-9360c7099d94.png)

## ✅ 07 Modificar Configuración de la BD en `.env`

En el archivo `.env` insertamos la siguiente línea de código:

```sh
DATABASE_URL="mysql://root:root@127.0.0.1:3306/sepe_ejercicio_01?serverVersion=5.7"
```

![image](https://user-images.githubusercontent.com/23094588/124358566-38359800-dc21-11eb-99e6-b545c43a210d.png)

Cargamos nuevamente la ruta `http://localhost:8000/home` y el error desaparece mostrando lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/124358612-66b37300-dc21-11eb-80ee-a740613ff35f.png)


:eight_pointed_black_star: Subir a GIT

## ✅ 08 Añadir BootsStrap a la Aplicación

En la carpeta `public` del proyecto creamos las carpetas `css` y `js`.

![image](https://user-images.githubusercontent.com/23094588/124358787-27d1ed00-dc22-11eb-8802-42e417cd24df.png)

Dentro colocamos los archivos `bootstrap.min.css` y `bootstrap.min.js` en su carpeta correspondiente.

![image](https://user-images.githubusercontent.com/23094588/124358869-93b45580-dc22-11eb-8db0-6bab60699f19.png)


### Modificar el archivo `base.html.twig` para aplicar Bootstrap.

El código en esta plantilla debe ser el siguiente:

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <title>{% block title %}Welcome!{% endblock %}</title>
        {# Run `composer require symfony/webpack-encore-bundle`
           and uncomment the following Encore helpers to start using Symfony UX #}
        {% block stylesheets %}
            <link rel="stylesheet" type="text/css" href="/css/bootstrap.min.css">
        {% endblock %}

    </head>
    <body>
        {% block body %}{% endblock %}

        {% block javascripts %}
            <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
            <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
            <script src="/js/bootstrap.min.js"></script>
        {% endblock %}
    </body>
</html>
```

Si cargamos nuevamente la ruta `http://localhost:8000/home` notamos un ligero cambio debido a que ya se esta aplicando Bootstrap a nuestra plantilla.

![image](https://user-images.githubusercontent.com/23094588/124358955-fc033700-dc22-11eb-9e5a-9e7cac2886dc.png)


:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Añadir Bootstrap"
```

## ✅ 09 Modificar Página Home

Para modificar la página Home debemos modificar la plantilla `templates/home/index.html.twig` con el contenido deseado.

```html
{% extends 'base.html.twig' %}

{% block title %}Fondos{% endblock %}

{% block stylesheets %}
  {{ parent() }}
  <link rel="stylesheet" type="text/css" href="/css/styles.css">
{% endblock %}

{% block body %}
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <a class="navbar-brand" href="#">FONDOS</a>
  <ul class="navbar-nav mr-auto">
    <li class="nav-item">
        <a class="nav-link" href="">¿Quienes Somos?</a>
    </li>
  </ul>
  <form class="form-inline">
    <button class="btn btn-outline-secondary my-2 my-sm-0" type="submit">Login</button>
  </form>
</nav>
<main class="container">
  <div class="starter-template text-center py-5 px-3">
    <h1>Gestión de Fondos</h1>
    <p class="lead">Libros, Revistas, Documentales, Videos, Películas CDs, ...</p>
    <img src="images/libros.jpg" class="img-fluid rounded-circle" width="60%" height="60%" alt="...">
  </div>
</main>
<footer class="footer bg-dark rounded-top text-center">
  <div class="container py-2">
    <p class="text-white my-2">
      &copy; Adolfo de la Rosa
    </p>
  </div>
</footer>

{% endblock %}
```

Como la plantilla necesita la imagen `images/libros.jpg` dentro de la carpeta `public` creamos la carpeta `images` y colocamos el archivo `libros.jpg`.

Si cargamos la ruta `http://localhost:8000/home` lo que vemos es:

![image](https://user-images.githubusercontent.com/23094588/124359491-9a909780-dc25-11eb-8787-17ab92c0e8d9.png)

Como vemos el `footer` no esta bien colocado. En el `footer` tenemos la etiqueta `<footer class="footer bg-dark rounded-top text-center">`, la clase `footer` es inventada y es allí donde vamos a poner el estilo para que el `footer` aparezca donde debe ser.

En la carpeta `public\css` añadimos el archivo `styles.css` cón el siguiente código:

```css
.footer {
  position:fixed;
  left:0px;
  bottom:0px;
  height:60px;
  width:100%;
}
```

Si cargamos nuevamente la ruta `http://localhost:8000/home` vemos:

![image](https://user-images.githubusercontent.com/23094588/124359762-a92b7e80-dc26-11eb-8866-7f474340cbcb.png)

Además de invocar esta página con `http://localhost:8000/home` queremos que se llame también con `http://localhost:8000/`, por lo que debemos modificar el archivo `src/Controller/HomeController.php` añadiendo la ruta adicional:

```html
@Route("/", name="root")
```

![image](https://user-images.githubusercontent.com/23094588/124360044-e04e5f80-dc27-11eb-8c77-4a93da9e3bcb.png)

Al invocar la ruta `http://localhost:8000` o `http://localhost:8000/` tenemos:

![image](https://user-images.githubusercontent.com/23094588/124359906-37a00000-dc27-11eb-89b7-257137380dfb.png)

EXISTEN DOS RUTAS PARA UNA MISMA ACCIÓN.


:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Modificar Página Home"
```

![image](https://user-images.githubusercontent.com/23094588/124360084-155ab200-dc28-11eb-912e-c6c845105a18.png)

![image](https://user-images.githubusercontent.com/23094588/124360106-36230780-dc28-11eb-9837-66185def6e14.png)

![image](https://user-images.githubusercontent.com/23094588/124360115-3d4a1580-dc28-11eb-8ac1-607d0ba41d6c.png)


## ✅ 10 Separar Menú y Footer de la Página Home

Para poder reutilizar el Menú y Footer en las páginas `Login` y `About` vamos a separarlos de la página `Home`.

Crear en `template` la carpeta `comunes` y crear los archivos `_menu_inicial.html.twig` y `_footer_inicial.html.twig`

![image](https://user-images.githubusercontent.com/23094588/124363758-6e811080-dc3d-11eb-8cc0-4ad4d616e7a4.png)

De la página `templates/home/index.html.twig` vamos a cortar el siguiente código para colocarlo en `_menu_inicial.html.twig`


```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <a class="navbar-brand" href="#">FONDOS</a>
  <ul class="navbar-nav mr-auto">
    <li class="nav-item">
        <a class="nav-link" href="">¿Quienes Somos?</a>
    </li>
  </ul>
  <form class="form-inline">
    <button class="btn btn-outline-secondary my-2 my-sm-0" type="submit">Login</button>
  </form>
</nav>
```

Y en su lugar colocamos:

```html
{{ include('_menu_inicial.html.twig') }}
```

También de la página `templates/home/index.html.twig` vamos a cortar el siguiente código para colocarlo en `_footer_inicial.html.twig`

```html
<footer class="footer bg-dark rounded-top text-center">
  <div class="container py-2">
    <p class="text-white my-2">
      &copy; Adolfo de la Rosa
    </p>
  </div>
</footer>
```


Y en su lugar colocamos:

```html
{{ include('_footer_inicial.html.twig') }}
```

La plantilla `templates/home/index.html.twig` queda así:

![image](https://user-images.githubusercontent.com/23094588/124364079-72159700-dc3f-11eb-8b3b-b1d8ea560e6b.png)

Si cargamos el link `http://localhost:8000/home` vemos exactamente lo mismo, pero lo hemos estructurado mejor para poder reutilizar el código:

![image](https://user-images.githubusercontent.com/23094588/124364050-501c1480-dc3f-11eb-921c-5150872d515f.png)


:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Separar Menú y Footer de la Página Home"
```

![image](https://user-images.githubusercontent.com/23094588/124364124-b3a64200-dc3f-11eb-911f-370599676de1.png)


## ✅ 11 Crear Controlador `About`

Vamos a crear el controlador `About` que corresponde a la sección **Quiénes somos** con la instrucción:

```sh
php bin/console make:controller
```

![image](https://user-images.githubusercontent.com/23094588/124364324-0e8c6900-dc41-11eb-81e8-78dfd19ec4ae.png)


Se han creado dos archivos `src/Controller/AboutController.php` e `templates/about/index.html.twig`. 


Al invocar la ruta `http://localhost:8000/about` vemos lo que nos ha creado Symphony.

![image](https://user-images.githubusercontent.com/23094588/124364414-b99d2280-dc41-11eb-9fbb-e011dffe2ec7.png)

Vamos a hacer algunos cambios para obtener la página personalizada.


En `src/Controller/AboutController.php` vamos a cambiar 

```html
@Route("/about", name="about")
```

por

```html
@Route("/quienes-somos", name="about")
```

En `templates/about/index.html.twig` colocamos el siguinete código:

```html
{% extends 'base.html.twig' %}

{% block title %}Quiénes somos{% endblock %}

{% block stylesheets %}
  {{ parent() }}
  <link rel="stylesheet" type="text/css" href="/css/styles.css">
{% endblock %}

{% block body %}
{{ include('comunes/_menu_inicial.html.twig') }}
<main class="container my-4">
  
  <h1>Quiénes somos</h1>

  <h3>Libros, Revistas, Documentales, Videos, Películas CDs, ...</h3>
  
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin malesuada egestas risus hendrerit tincidunt. Nunc eu semper justo, non ultricies nibh. Sed a viverra lorem. Donec sed porttitor turpis, eu cursus tellus. Proin dignissim lorem et eros aliquam faucibus. Suspendisse fermentum, erat et vulputate dapibus, augue purus maximus dolor, vitae gravida eros ex vehicula felis. Vestibulum feugiat nibh urna, fringilla ultrices eros bibendum id. In mollis eleifend pulvinar. Nulla porttitor quis felis at ultricies. Integer sed mi sit amet est feugiat tempor. Phasellus a velit non ligula placerat maximus non sit amet orci. In a imperdiet felis.</p>

  <p>Quisque tempor nunc in turpis molestie laoreet. Donec faucibus, urna sed sodales sagittis, magna libero fermentum tortor, et faucibus nunc enim a lectus. Donec magna velit, viverra vitae eros sit amet, pretium gravida quam. Duis orci lorem, lacinia non tellus ac, maximus dictum tellus. Donec id euismod metus. Integer aliquam enim nunc, at hendrerit ipsum convallis et. Suspendisse vehicula metus mi, eget ullamcorper orci faucibus ac. Quisque a gravida felis, vitae sagittis purus. In blandit viverra ultricies. Sed viverra orci ligula, id condimentum elit elementum vitae. Quisque luctus pulvinar tincidunt. Maecenas vitae nisi ex. Morbi at aliquet tellus, at ullamcorper dui. Mauris faucibus porttitor placerat. Nulla porttitor metus non leo maximus ornare. Maecenas rhoncus gravida convallis.</p>

  <p>Donec tincidunt iaculis malesuada. Donec in semper lorem, eget fringilla lorem. Curabitur vel nisl sollicitudin, auctor lacus a, varius diam. Suspendisse facilisis et orci sed semper. Curabitur sit amet elementum nulla. Suspendisse potenti. Nunc dignissim nec leo at pellentesque. Vivamus gravida ex ex, id egestas nisl scelerisque rhoncus.</p>

  <p>Mauris rutrum nibh dolor, non lacinia erat pellentesque nec. Duis faucibus ultrices purus, id placerat dolor malesuada vel. Duis semper facilisis consectetur. In iaculis metus in libero elementum mattis. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras pulvinar erat nec massa porttitor efficitur. Mauris eget orci id erat sodales imperdiet. Nunc ante enim, tincidunt in metus eget, semper lobortis sapien. Nullam non feugiat ipsum.</p>

  <p>Fusce quis bibendum leo, sit amet aliquam ligula. Cras fringilla est non quam facilisis porta. Proin in dolor ullamcorper, volutpat lorem id, molestie risus. Nulla maximus dignissim massa sit amet suscipit. Nulla lacus nisi, congue eu lorem in, bibendum placerat est. Sed gravida pulvinar dignissim. In ex turpis, pretium sed augue nec, condimentum ultricies elit. Curabitur ut pulvinar mauris, et laoreet purus. Vestibulum eleifend vestibulum sollicitudin. Donec quis fringilla ipsum. Interdum et malesuada fames ac ante ipsum primis in faucibus. Aliquam porttitor ut lacus at posuere. Interdum et malesuada fames ac ante ipsum primis in faucibus. Donec luctus lectus nulla, ut dignissim odio semper vel.</p>

</main>
{{ include('comunes/_footer_inicial.html.twig') }}
{% endblock %}
```

Al llamar al URL `http://localhost:8000/quienes-somos` tenemos:

![image](https://user-images.githubusercontent.com/23094588/124364962-53b29a00-dc45-11eb-8f44-899b9a52d2ae.png)

:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Crear Controlador About"
```

![image](https://user-images.githubusercontent.com/23094588/124365027-a8561500-dc45-11eb-81f6-318f2174a54b.png)


## ✅ 12 Crear Controlador `Login`

Vamos a crear el controlador `Login` que corresponde a la sección **Iniciar Sesión** con la instrucción:

```sh
php bin/console make:controller
```

![image](https://user-images.githubusercontent.com/23094588/124365076-fec35380-dc45-11eb-873b-53be8b64b74e.png)


Se han creado dos archivos `src/Controller/LoginController.php` e `templates/login/index.html.twig`. 

Vamos a hacer algunos cambios para obtener la página personalizada.

En `templates/login/index.html.twig` vamos a colocar el siguiente código:

```html
{% extends 'base.html.twig' %}

{% block title %}Login{% endblock %}

{% block stylesheets %}
  {{ parent() }}
  <link rel="stylesheet" type="text/css" href="css/styles.css">
  <link rel="stylesheet" type="text/css" href="css/styles-login.css">
{% endblock %}

{% block body %}
{{ include('comunes/_menu_inicial.html.twig') }}
<main class="container my-4">
  
    <div class="row justify-content-center">
        <div class="col-lg-5">
            <div class="card shadow-lg border-0 rounded-lg mt-5">
                <div class="card-header"><h3 class="text-center font-weight-light my-4">Login</h3></div>
                <div class="card-body">
                    <form>
                        <div class="form-group">
                            <label class="small mb-1" for="inputEmailAddress">Email</label>
                            <input class="form-control py-4" id="inputEmailAddress" type="email" placeholder="Introduzca email" />
                        </div>
                        <div class="form-group">
                            <label class="small mb-1" for="inputPassword">Password</label>
                            <input class="form-control py-4" id="inputPassword" type="password" placeholder="Introduzca password" />
                        </div>
                        <div class="form-group">
                            <div class="custom-control custom-checkbox">
                                <input class="custom-control-input" id="rememberPasswordCheck" type="checkbox" />
                                <label class="custom-control-label" for="rememberPasswordCheck">Recordar contraseña</label>
                            </div>
                        </div>
                        <div class="form-group d-flex align-items-center justify-content-between mt-4 mb-0">
                            <a class="small" href="password.html">¿Has olvidado tu contraseña?</a>
                            <a class="btn btn-secondary" href="index.html">Login</a>
                        </div>
                    </form>
                </div>
                <div class="card-footer text-center">
                    <div class="small"><a href="#">¿Necesito una cuenta? ¡Inscribirse!</a></div>
                </div>
            </div>
        </div>
    </div>
</main>
{{ include('comunes/_footer_inicial.html.twig') }}
{% endblock %}
```

Vamos a añadir en `public/css` la hoja de estilos `styles-plantilla.css` la cual es una hoja de estilos de la plantilla. Esta hoja de estilos se puede depurar para que solo tenga lo correspondiente al login.

Al llamar al URL `http://localhost:8000/login` tenemos:

![image](https://user-images.githubusercontent.com/23094588/124368019-faeefb80-dc5c-11eb-9d57-02cf5127cadf.png)

:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Crear Controlador Login"
```

![image](https://user-images.githubusercontent.com/23094588/124368042-21149b80-dc5d-11eb-858d-808cdced169b.png)

## ✅ 13 Asociar en el menú las acciones `About` y `Login` 


En la plantlla `_menu_inicial.html.twig` vamos a usar `{{path('nombre acción')}}` para linkar las opciones del menú a las acciones.

```html
<nav class="navbar navbar-expand-lg navbar-dark bg-dark">
  <a class="navbar-brand" href="#">FONDOS</a>
  <ul class="navbar-nav mr-auto">
    <li class="nav-item">
        <a class="nav-link" href="{{path('about')}}">Quiénes somos</a>
    </li>
  </ul>
  <form class="form-inline" action="{{path('login')}}">
    <button class="btn btn-outline-secondary my-2 my-sm-0" type="submit">Login</button>
  </form>
</nav>
```


![image](https://user-images.githubusercontent.com/23094588/124368139-887f1b00-dc5e-11eb-8556-b04da2ef7217.png)


Al pulsar en `Quiénes somos` nos presenta:

![image](https://user-images.githubusercontent.com/23094588/124368151-aba9ca80-dc5e-11eb-9f67-5ae4657c2670.png)


Y al presionar sobre el botón `Login` nos presenta:

![image](https://user-images.githubusercontent.com/23094588/124368178-cda34d00-dc5e-11eb-94be-b4cf1bb2a9ed.png)


:x: FALTA QUE RESALTE LAS OPCIONES SELECCIONADAS.


:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Asociar en el menú las acciones About y Login"
```

![image](https://user-images.githubusercontent.com/23094588/124368212-207d0480-dc5f-11eb-9776-e317f4bb3cd3.png)

## ✅ 14 Crear Controlador `Fondos`

Vamos a crear el controlador `Fondos` con la siguiete instrucción:

```sh
php bin/console make:controller
```

![image](https://user-images.githubusercontent.com/23094588/124375321-e84ae580-dca1-11eb-83c9-0f7843807a62.png)


Crea los archivos `src/Controller/FondosController.php` y `templates/fondos/index.html.twig`.

En `templates/fondos/index.html.twig` colocamos el siguiente código:

```html
{% extends 'base.html.twig' %}

{% block title %}Fondos{% endblock %}

{% block body %}
  <main class="container py-4">
    <h1 class="text-center">Fondos</h1>
  </main>
{% endblock %}
```

Al invocar el URL http://localhost:8000/fondos nos pinta:

![image](https://user-images.githubusercontent.com/23094588/124375668-ac188480-dca3-11eb-9532-7c651ae28e13.png)


:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Crear Controlador Fondos"
```

![image](https://user-images.githubusercontent.com/23094588/124375735-031e5980-dca4-11eb-90d0-8e8ebd288a97.png)


## ✅ 15 Crear Controlador `Editoriales`

Vamos a crear el controlador `Editoriales` con la siguiete instrucción:

```sh
php bin/console make:controller
```

![image](https://user-images.githubusercontent.com/23094588/124375835-64dec380-dca4-11eb-8752-9706d78f96e3.png)

Crea los archivos `src/Controller/EditorialesController.php` y `templates/editoriales/index.html.twig`.

En `templates/editoriales/index.html.twig` colocamos el siguiente código:

```html
{% extends 'base.html.twig' %}

{% block title %}Editoriales{% endblock %}

{% block body %}
  <main class="container py-4">
    <h1 class="text-center">Editoriales</h1>
  </main>
{% endblock %}
```

Al invocar el URL http://localhost:8000/editoriales nos pinta:

![image](https://user-images.githubusercontent.com/23094588/124375922-ca32b480-dca4-11eb-8a9e-8f4c146e045c.png)

:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Editoriales"
```

![image](https://user-images.githubusercontent.com/23094588/124375945-ecc4cd80-dca4-11eb-88cb-2627a281bb5f.png)

## ✅ 16 Crear Controlador `Autores`

Vamos a crear el controlador `Autores` con la siguiete instrucción:

```sh
php bin/console make:controller
```

![image](https://user-images.githubusercontent.com/23094588/124375982-10881380-dca5-11eb-8ff0-3eac1e05d291.png)


Crea los archivos `src/Controller/AutoresController.php` y `templates/autores/index.html.twig`.

En `templates/autores/index.html.twig` colocamos el siguiente código:

```html
{% extends 'base.html.twig' %}

{% block title %}Autores{% endblock %}

{% block body %}
  <main class="container py-4">
    <h1 class="text-center">Autores</h1>
  </main>
{% endblock %}
```

Al invocar el URL http://localhost:8000/autores nos pinta:

![image](https://user-images.githubusercontent.com/23094588/124376050-580e9f80-dca5-11eb-8bc9-d91a2b6ce04d.png)


:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Crear Controlador Autores"
```

![image](https://user-images.githubusercontent.com/23094588/124376092-91dfa600-dca5-11eb-8da3-a047fbcdf292.png)


## ✅ 17 Crear Menú para las Opciones de `Fondos`, `Editoriales` y `Autores`

* En la carpeta `templates/comunes` crear la plantilla `_menu.html.twig` con el siguiente código:

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <img src="{{ asset('images/fondos-01.png')}}" width="50px"/><a class="navbar-brand" href="{{ path('fondos')}}"> F O N D O S</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarSupportedContent">
    <ul class="navbar-nav mr-auto">
      <li class="nav-item">
        <a class="nav-link" href="{{ path('fondos')}}">Fondos</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="{{ path('editoriales')}}">Editoriales</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="{{ path('autores')}}">Autores</a>
      </li>
    </ul>
    <form class="form-inline" action="{{path('root')}}">
      <button class="btn btn-outline-secondary my-2 my-sm-0" type="submit">Logout</button>
  </form>
  </div>
</nav>
```

* Añadir en `public/images` la imagen `fondos-01.png` 

* Añadir en las plantilla de Fondos, Editoriales y Autores la llamada a  `_menu.html.twig` con:

```html
{{ include('comunes/_menu.html.twig') }}  
```

* Añadir en el Login la llamada a Fondos a presionar el botón. (Aún no validamos los valores introducidos)

   ```html
   ...
   <a class="btn btn-secondary" href="{{ path('fondos')}}">Login</a>
   ...
   ```

* Probar todo el flujo de los menús en  http://localhost:8000/ 

   
![image](https://user-images.githubusercontent.com/23094588/124377228-429c7400-dcab-11eb-9926-3e80827f8fa8.png)

![image](https://user-images.githubusercontent.com/23094588/124377240-53e58080-dcab-11eb-9438-7422f7a6c760.png)

![image](https://user-images.githubusercontent.com/23094588/124377273-77103000-dcab-11eb-9139-f1f583de1a88.png)

![image](https://user-images.githubusercontent.com/23094588/124377287-87c0a600-dcab-11eb-8381-f686a42fca73.png)

![image](https://user-images.githubusercontent.com/23094588/124377306-9c9d3980-dcab-11eb-8c52-2f9068cf5a1d.png)

![image](https://user-images.githubusercontent.com/23094588/124377318-af177300-dcab-11eb-95d4-43cbd20473d7.png)

![image](https://user-images.githubusercontent.com/23094588/124377341-c35b7000-dcab-11eb-866b-c8302a8ca30f.png)

:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Crear Menú para las Opciones de Fondos, Editoriales, Autores y Logout"
```

![image](https://user-images.githubusercontent.com/23094588/124377367-dec67b00-dcab-11eb-9ced-15b24657c913.png)

![image](https://user-images.githubusercontent.com/23094588/124377391-00bffd80-dcac-11eb-9a42-5d7199e27f71.png)

![image](https://user-images.githubusercontent.com/23094588/124377457-4f6d9780-dcac-11eb-9438-7e3febc6eada.png)

## ✅ 18 Explicación de BD necesaria

Nuestra aplicacíon va a usar las siguientes tablas con las relaciones que se indican.

### Tablas

* **Tabla Fondo** (titulo, isbn, edicion, publicacion, categoria)
* **Tabla Autor** (nombre, tipo)
* **Tabla Editorial** (nombre)

### Relaciones

* 1 fondo tiene 1 editorial
* 1 editorial tiene N fondos     Relación 1 - N (One To Many)

* 1 fondo tiene N autores
* 1 autor ha escrito N fondos    Relación N - N (Many To Many)

**DOCTRINE**

* DOCTRINE es un **ORM** - Object Relational Mapper
* Mapea objeto de PHP con tablas de la BD.
* DOCTRINE Propone que las tablas no se creen a mano.
* DOCTRINE nos dice que NO debemos pensar en las tablas, por que condicionamos nuestra programación a las tablas creadas.
* DOCTRINE nos dice piensa en las clases que deseas tener, por ejemplo:
* DOCTRINE nos dice diseña las clases que yo me encargare de crear una BD capaz de persistir o representar a esas clases que has diseñado. (CUESTA MUCHO)
* Es bueno crear un Diagrama UML de Clases para ver la representación de las clases involucradas.
* DOCTRINE llama a estas clases **ENTIDADES** **ENTITY**, las cuales se van a almacenar en la carpeta `Entity` de nuestra APP que por ahora se mantiene vacía.
* Para crear Entidades se usa el comando `php bin/console make:entity`


```php
class Editorial {
   
   private int $id
   private string $nombre;
   
   public function getNombre() {
      return $this->nombre;
   }`

  public function setNombre($nombre) {
      $this->nombre = nombre;
   }
   
}
```

```php
class Autor {
   
   private int $id
   private string $tipo;
   private string $nombre;
   
   private $fondos //array de fondos
   
   public function getFondos();
   
   //Todos los getters y setters
   
}
```

Con esto podríamos recuperar todos los fondos de un Autor con:

```php
...
$fondosDelAutor = $autor->getFondos();
...
```

```php
class Fondo {
   
   private int $id
   private string $titulo;
   private string $isbn;
   private int edicion;
   private int publicacion;
   private string categoria
   
   private Editorial $editorial;
   private Autores[] $autores //array de autores
   
   
   //Todos los getters y setters
   
}
```

Podemos desear tener :

```php
...
$fondo->getTitulo();
$fondo->getAutores();
$miEditorial = $fondo->getEditorial();
$nombreEditorial = $fondo->getEditorial()->getNombre();
...
```


## ✅ 19 Crear Entity  `Autor`

Vamos a usar el comando `php bin/console make:entity`:

![image](https://user-images.githubusercontent.com/23094588/124381401-a54d3a00-dcc2-11eb-9e4c-e60d634d39ce.png)

Lo primero que nos pregunta es el nombre de la entidad, en este caso es `Autor`.

En este momento ya se crear los archivos `src/Entity/Autor.php` y `src/Repository/AutorRepository.php`.

![image](https://user-images.githubusercontent.com/23094588/124381468-096ffe00-dcc3-11eb-8f04-993a281e0804.png)

Por un lado nos crea la Entidad `src/Entity/Autor.php` a la cual ya le pone por defecto el campo `$id`:

![image](https://user-images.githubusercontent.com/23094588/124381538-64a1f080-dcc3-11eb-8b23-28445de0fa79.png)


Pero el comando no ha terminado, nos permite añadir los campos que necesitemos:

```sh
Entity generated! Now let's add some fields!
You can always add more fields later manually or by re-running this command.
```

Podemos seguir añadiendo algunos campos ahora mismo o si lo preferimos podemos añadirlos manualmente(expertos) o volver a ejecutar el comando `php bin/console make:entity` para editar la entidad existente mediante el asistente. En este caso vamos a añadir los campos que habíamos definido para la Entidad `Autor`, empezamos por `tipo`:

![image](https://user-images.githubusercontent.com/23094588/124381980-6e2c5800-dcc5-11eb-957b-ea12c03f75cd.png)

Nos pide **nombre de la propiedad**, **tipo** sino lo conocemos podemos pulsar **`?`** para que nos indique todos los tipos posibles, **tamaño** y si es **nulable**. Nos suguiere las opciones y si estamos de acuerdo basta dar Enter o podemos cambiarla por la que deseemos. Una vez contestadas estas cuatro preguntas se acttualiza la Entidad `updated: src/Entity/Autor.php`

![image](https://user-images.githubusercontent.com/23094588/124382115-14785d80-dcc6-11eb-813a-b8e980cfc4cc.png)

Pero el comando aún no termina, nos pregunta que otra propiedad queremos ingresar. Empezamos de nuevo para añadir `nombre`.

![image](https://user-images.githubusercontent.com/23094588/124382193-7afd7b80-dcc6-11eb-9763-cba439c9aa8a.png)

Como ya no queremos añadir nada mas simplemente pulsamos Enter.

![image](https://user-images.githubusercontent.com/23094588/124382225-9e282b00-dcc6-11eb-9008-7902ee6f56ea.png)


Ahora si el comando termina.

Y por ahora ya tenemos nuestra entidad `Autor`.

![image](https://user-images.githubusercontent.com/23094588/124382284-e9423e00-dcc6-11eb-85fe-9db68af2eaf6.png)

**NOTA**

Nos suguiere ejecutar el comando `php bin/console make:migration` para crear la tabla en la BD, pero vamos a esperar a crear las demás entidades para ejecutarlo.


:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Crear Entity Autor"
```

![image](https://user-images.githubusercontent.com/23094588/124382355-4d650200-dcc7-11eb-8a43-6f8bf7c0a14a.png)


## ✅ 20 Crear Entity  `Editorial`

Usamos el comando `php bin/console make:entity`

![image](https://user-images.githubusercontent.com/23094588/124382929-278d2c80-dcca-11eb-8de2-3a731896a967.png)

![image](https://user-images.githubusercontent.com/23094588/124382946-3bd12980-dcca-11eb-9a10-e6e9c5f6aaac.png)

Hemos creado la Entidad `Editorial`

![image](https://user-images.githubusercontent.com/23094588/124382980-63c08d00-dcca-11eb-8504-d083836d4162.png)


![image](https://user-images.githubusercontent.com/23094588/124382993-7b981100-dcca-11eb-8897-e5d0113bef15.png)

:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Crear Entity Editorial"
```

![image](https://user-images.githubusercontent.com/23094588/124383081-e1849880-dcca-11eb-9ee9-94362be2bb88.png)

## ✅ 21 Crear Entity  `Fondo`

Usamos el comando `php bin/console make:entity`

![image](https://user-images.githubusercontent.com/23094588/124383183-493ae380-dccb-11eb-9f4b-b7d53959a8d6.png)

![image](https://user-images.githubusercontent.com/23094588/124383223-98811400-dccb-11eb-85ae-f2a3aac89039.png)

![image](https://user-images.githubusercontent.com/23094588/124383273-ea299e80-dccb-11eb-90e4-5505a0bb117f.png)

![image](https://user-images.githubusercontent.com/23094588/124383307-19401000-dccc-11eb-940e-012e02cf0ac6.png)

Hemos creado la Entidad `Fondo`

![image](https://user-images.githubusercontent.com/23094588/124383342-47255480-dccc-11eb-8eea-c128f1ecbcf4.png)

![image](https://user-images.githubusercontent.com/23094588/124383383-7340d580-dccc-11eb-8993-74162fd5cd67.png)

![image](https://user-images.githubusercontent.com/23094588/124383405-8eabe080-dccc-11eb-9896-535dbdb2aa0a.png)

:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Crear Entity Fondo"
```

![image](https://user-images.githubusercontent.com/23094588/124383439-ba2ecb00-dccc-11eb-8ef0-bac6038c1d69.png)

## ✅ 22 Crear las Relaciones dentro de la Entity `Fondo` con `Editorial` y `Autor`

Para editar la Entity `Fondo` también usamos el comando `php bin/console make:entity`

Empezamos añadiendo la Propiedad `Editorial`

![image](https://user-images.githubusercontent.com/23094588/124383604-a768c600-dccd-11eb-8bb9-3b9e103623c8.png)

![image](https://user-images.githubusercontent.com/23094588/124383615-b3548800-dccd-11eb-9ceb-8a332dab7cc6.png)

![image](https://user-images.githubusercontent.com/23094588/124383722-4db4cb80-dcce-11eb-8492-f729430c0485.png)

![image](https://user-images.githubusercontent.com/23094588/124383770-89e82c00-dcce-11eb-9da5-d1accaf180c0.png)

![image](https://user-images.githubusercontent.com/23094588/124383842-dc294d00-dcce-11eb-8e6e-fe85965246e0.png)

En `Fondo.php` se ha añadido lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/124383888-1a267100-dccf-11eb-91b8-92560e6382b5.png)

![image](https://user-images.githubusercontent.com/23094588/124383898-290d2380-dccf-11eb-9c0d-87ea0c2f7f3d.png)

Y en `Editorial.php` se ha añadido lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/124383958-8b662400-dccf-11eb-9900-0362154a2884.png)

![image](https://user-images.githubusercontent.com/23094588/124383991-a8025c00-dccf-11eb-9618-ae59db1c5656.png)



Ahora vamos a añadir la propiedad `autores`

![image](https://user-images.githubusercontent.com/23094588/124384112-2bbc4880-dcd0-11eb-9eec-6aa55383ef4a.png)

![image](https://user-images.githubusercontent.com/23094588/124384127-34148380-dcd0-11eb-9bbe-4fdb41c3ac9f.png)

![image](https://user-images.githubusercontent.com/23094588/124384210-750c9800-dcd0-11eb-8fc1-803d56b966c6.png)

![image](https://user-images.githubusercontent.com/23094588/124384243-9b323800-dcd0-11eb-8dba-c6bbf4676d0f.png)

En `Fondo.php` se ha añadido lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/124384301-d2084e00-dcd0-11eb-8e6d-c8d09dc7949e.png)

![image](https://user-images.githubusercontent.com/23094588/124384325-ea786880-dcd0-11eb-803d-cec4bd93650e.png)

Vemos que Doctrine genera un pequeño error al intentar generar el singular solo quita la `s` pero para español esto no funciona hay que hacer el arreglo manualmente.

![image](https://user-images.githubusercontent.com/23094588/124384421-683c7400-dcd1-11eb-916c-dba7548b3c09.png)

Estos dos métodos `addAutor` y `removeAutor` nos permite añadir o eliminar un Autor a Fondos.

En `Autor.php` se ha añadido lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/124384560-206a1c80-dcd2-11eb-96e5-5c3a5e1da13d.png)

![image](https://user-images.githubusercontent.com/23094588/124384574-3c6dbe00-dcd2-11eb-81bc-4517180369ce.png)

Aqui tambien modificamos manualmente la llamada a `addAutor` y `removeAutor` para que tengan el nombre correcto.

:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Crear las Relaciones dentro de la Entity Fondo con Editorial y Autor"
```

![image](https://user-images.githubusercontent.com/23094588/124384610-7048e380-dcd2-11eb-9a23-289e0bfed045.png)


## ✅ 23 Realizar las Migration para crear la BD en base a las Entidades existentes

Una vez que ya tenemos las entidades debemos ejecutar el comando:

```sh
php bin/console make:migration
```

![image](https://user-images.githubusercontent.com/23094588/124395807-8bcde180-dd06-11eb-9838-7d4568453dc6.png)

Este comando nos crea el archivo `migrations/Version20210704182911.php` 

![image](https://user-images.githubusercontent.com/23094588/124395849-c0419d80-dd06-11eb-84fc-531b3aed369e.png)

el cual contiene el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/124395880-ec5d1e80-dd06-11eb-91ae-3095f9729755.png)
![image](https://user-images.githubusercontent.com/23094588/124395896-fe3ec180-dd06-11eb-917c-c229cbf33221.png)

Como podemos observar tiene dos métodos o funciones:

* `public function up(Schema $schema): void`: Contiene las instrucciones SQL que se ejecutar al realizar el comando para crear o modificar la BD.
* `public function down(Schema $schema): void`: Contiene las instrucciones SQL que se ejecutar para desacer los cambios si ejecutamos el método anterior.


Como vemos en la consola para continuar nos suguiere ejecutar el comando:


```sh
php bin/console doctrine:migrations:migrate
```

![image](https://user-images.githubusercontent.com/23094588/124396047-af455c00-dd07-11eb-95fc-df883eef537c.png)

Nos advierte que si ejecutamos el comando los datos existentes se pueden perder, como no tenemos nada lo ejecutamos.

Este comando hace el mapeo de las Entidades que tenemos a tablas de la BD, si revisamos la BD tenemos:

![image](https://user-images.githubusercontent.com/23094588/124396105-fd5a5f80-dd07-11eb-8925-89199ef17299.png)

![image](https://user-images.githubusercontent.com/23094588/124396180-532f0780-dd08-11eb-8af4-1a2d8c88dbb0.png)

![image](https://user-images.githubusercontent.com/23094588/124396233-912c2b80-dd08-11eb-89a7-4246c1e625e8.png)

![image](https://user-images.githubusercontent.com/23094588/124396247-a99c4600-dd08-11eb-9207-faf594a1de2a.png)

![image](https://user-images.githubusercontent.com/23094588/124396195-6215ba00-dd08-11eb-9f71-e6d9043a775b.png)

![image](https://user-images.githubusercontent.com/23094588/124396201-735ec680-dd08-11eb-8800-06b6602849e7.png)

![image](https://user-images.githubusercontent.com/23094588/124396224-82de0f80-dd08-11eb-8e33-8bbfbf0201b9.png)

:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Realizar las Migration para crear la BD en base a las Entidades existentes"
```

![image](https://user-images.githubusercontent.com/23094588/124396307-026bde80-dd09-11eb-817d-27441eee0260.png)


## ✅ 24 Diseñar la Página de las Editoriales

### Meter Manualmente un Registro en la Tabla `editorial`

Lo primero que vamos a hacer es manualmente insertar un registro en la tabla `editorial`.

![image](https://user-images.githubusercontent.com/23094588/124396398-8faf3300-dd09-11eb-8e58-2f4753dd41e5.png)

```sql
INSERT INTO `sepe_ejercicio_01`.`editorial` (`id`, `nombre`) VALUES ('1', 'Alfaguara');
```

![image](https://user-images.githubusercontent.com/23094588/124396430-cedd8400-dd09-11eb-90db-29ada6d0ebba.png)

### Recuperar Editoriales de la BD y pasarlas a la Plantilla

Vamos a modificar el controlador `EditorialesController.php`.

![image](https://user-images.githubusercontent.com/23094588/124397071-e585da00-dd0d-11eb-8198-15a821db6358.png)

* Hemos inyectado el Repositorio `EditorialRepository` para poder usar sus métodos, importante la clausula `use App\Repository\EditorialRepository;` para poder usarlo.
* `$editoriales = $editorialRepository->findAll();` recuperamos todas las editoriales existentes usando el método `findAll()` y las almacenamos en `$editoriales`.
* Mandamos `'editoriales' => $editoriales` a nuestra plantilla `editoriales/index.html.twig`.

### Diseñar la Página de las Editoriales

En la plantilla `editoriales/index.html.twig` poner el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/124397168-a015dc80-dd0e-11eb-8b47-8e608bef9614.png)

Revisamos lo que llega el `editoriales` sacandolo a consola.

Si todo va bien creamos una tabla para mostrar los datos de las entidades.

### Revisar la Salida

![image](https://user-images.githubusercontent.com/23094588/124397234-0d297200-dd0f-11eb-9976-51c4dc2173e2.png)

:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Diseñar la Página de las Editoriales"
```

![image](https://user-images.githubusercontent.com/23094588/124397278-55489480-dd0f-11eb-83ff-504b98eab484.png)


## ✅ 25 Diseñar la Página de los Autores

### Meter Manualmente un Registro en la Tabla `autor`


![image](https://user-images.githubusercontent.com/23094588/124397413-f33c5f00-dd0f-11eb-82c0-dd08278f9ea2.png)

```sql
INSERT INTO `sepe_ejercicio_01`.`autor` (`id`, `tipo`, `nombre`) VALUES ('1', 'Persona', 'Pérez-Reverte, Arturo');
```

![image](https://user-images.githubusercontent.com/23094588/124397439-16670e80-dd10-11eb-975f-f41fd6f6224f.png)

### Recuperar Autores de la BD y pasarlas a la Plantilla

Vamos a modificar el controlador `AutoresController.php`.

![image](https://user-images.githubusercontent.com/23094588/124397622-41059700-dd11-11eb-97d1-8712c04053b6.png)


### Diseñar la Página de las Editoriales

En la plantilla `autores/index.html.twig` poner el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/124397641-6c888180-dd11-11eb-989e-d060923332dd.png)

### Revisar la Salida

![image](https://user-images.githubusercontent.com/23094588/124397655-7f9b5180-dd11-11eb-9648-7dd106482d24.png)

:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Diseñar la Página de las Autores"
```

![image](https://user-images.githubusercontent.com/23094588/124397680-b2454a00-dd11-11eb-983a-42ac71498868.png)


## ✅ 26 Diseñar la Página de los Fondos

### Meter Manualmente un Registro en la Tabla `fondo` y `fondo_autor` 

#### Tabla `fondo`

![image](https://user-images.githubusercontent.com/23094588/124397761-22ec6680-dd12-11eb-9311-aa9002609551.png)

```sql
INSERT INTO `sepe_ejercicio_01`.`fondo` (`id`, `editorial_id`, `titulo`, `isbn`, `edicion`, `publicacion`, `categoria`) VALUES ('1', '1', 'El sol de Breda', '84-204-8312-5', '1998', '1998', 'Novela');
```

![image](https://user-images.githubusercontent.com/23094588/124397801-59c27c80-dd12-11eb-8ac1-09bb4e6a009f.png)

#### Tabla `fondo_autor`

![image](https://user-images.githubusercontent.com/23094588/124397850-a9a14380-dd12-11eb-8104-5579298c5814.png)

```sql
INSERT INTO `sepe_ejercicio_01`.`fondo_autor` (`fondo_id`, `autor_id`) VALUES ('1', '1');
```

![image](https://user-images.githubusercontent.com/23094588/124397872-e40ae080-dd12-11eb-99cc-cdc76600682a.png)

### Recuperar Fondos de la BD y pasarlas a la Plantilla

Vamos a modificar el controlador `FondosController.php`.

![image](https://user-images.githubusercontent.com/23094588/124398233-e53d0d00-dd14-11eb-9cb3-90dfcfb4cc01.png)


### Diseñar la Página de las Editoriales

En la plantilla `fondos/index.html.twig` poner el siguiente código:

![image](https://user-images.githubusercontent.com/23094588/124398261-10276100-dd15-11eb-88d1-24ee1df92dcf.png)

***Observese como se recuperan los autores al ser un array y la editorial.***

### Revisar la Salida

![image](https://user-images.githubusercontent.com/23094588/124398285-3f3dd280-dd15-11eb-9f0e-4383ddbc788b.png)

:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Diseñar la Página de las Fondos"
git push
```

![image](https://user-images.githubusercontent.com/23094588/124398328-77451580-dd15-11eb-834e-10f5f0b11742.png)

![image](https://user-images.githubusercontent.com/23094588/124398359-a3609680-dd15-11eb-844a-24792067a819.png)



## ✅ 27 Crear Detalle de Editoriales


### Modificar Controlador

Modificamos el Controlador `src/Controller/EditorialesController.php` para añadir una nueva acción para que pinte el detalle de la Editorial seleccionada.

![image](https://user-images.githubusercontent.com/23094588/124403026-3c9ea580-dd34-11eb-9298-5a78eb65b976.png)


```php
    /**
     * @Route("/editoriales/{id}", name="editorial_detalle")
     */
    public function ver($id, EditorialRepository $editorialRepository): Response
    {
        $editorial = $editorialRepository->find($id);
        
        if(!$editorial) {
            return $this->render('comunes/recurso-no-encontrado.html.twig', [
                'mensaje' => 'Esta Editorial no existe.'
            ]);
        }

        return $this->render('editoriales/detalle.html.twig', [
            'editorial' => $editorial
        ]);
    }
```

### Añadir Font Awesome

En la plantilla `templates/base.html.twig` vamos a añadir Font Awesome

![image](https://user-images.githubusercontent.com/23094588/124403076-acad2b80-dd34-11eb-92b8-c5fbb1247f0a.png)

Añadimos la línea:

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
```

### Añadir Icono para llamar al Detalle de la Editorial

Modificamos `templates/editoriales/index.html.twig`

![image](https://user-images.githubusercontent.com/23094588/124403126-0c0b3b80-dd35-11eb-8f52-d656c1836c35.png)

La línea con el icono es:

```html
<td><a class="nav-link" href="{{ path('editorial_detalle', {id: editorial.id}) }}"><i class="fa fa-search" style="font-size:24px;color:grey;"></i></a></td>
```

Estamos llamando a la acción `editorial_detalle` definida en el controlador pasandole el parámetro `editorial.id`.

### Crear la nueva plantilla `editoriales/detalle.html.twig`


![image](https://user-images.githubusercontent.com/23094588/124403233-95227280-dd35-11eb-8dfa-41aa02befff8.png)

### Crear la nueva plantilla `comunes/recurso-no-encontrado.html.twig`


![image](https://user-images.githubusercontent.com/23094588/124403486-fdbe1f00-dd36-11eb-91bc-93974d808ec2.png)

### Probar el Flujo de Editoriales

![image](https://user-images.githubusercontent.com/23094588/124403501-162e3980-dd37-11eb-8e11-c3dcd40f82fe.png)

![image](https://user-images.githubusercontent.com/23094588/124403510-28a87300-dd37-11eb-8099-73717d0b193f.png)

![image](https://user-images.githubusercontent.com/23094588/124403563-60afb600-dd37-11eb-93a4-d788d890a55c.png)

:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Crear Detalle de Editoriales"
```

![image](https://user-images.githubusercontent.com/23094588/124403633-ac625f80-dd37-11eb-9c99-ea43cdfd8fd3.png)


## ✅ 28 Eliminar una Editorial

### Modificar el Controlador `src/Controller/EditorialesController.php`.


![image](https://user-images.githubusercontent.com/23094588/124473103-3396ee00-dd9f-11eb-9606-4cd2b4516561.png)

También cambiamos el nombre de un método 

![image](https://user-images.githubusercontent.com/23094588/124473226-5923f780-dd9f-11eb-8e26-b47a0ef39845.png)

### Modificar la Plantlla `templates/editoriales/index.html.twig`

Añadimos la opción de Eliminar llamando a la Acción correspondiente:

![image](https://user-images.githubusercontent.com/23094588/124473510-b5871700-dd9f-11eb-8eb1-13c34023e23b.png)


### Prueba de la Salida

![image](https://user-images.githubusercontent.com/23094588/124473786-0434b100-dda0-11eb-861a-f4c3e6803511.png)

![image](https://user-images.githubusercontent.com/23094588/124473834-14e52700-dda0-11eb-9c57-35ffef054e1d.png)

![image](https://user-images.githubusercontent.com/23094588/124473896-275f6080-dda0-11eb-90c6-2fbc10fc7f99.png)

Y si llamo al URL manualmente por ejemplo `http://localhost:8000/editoriales/2/borrar` tengo:

![image](https://user-images.githubusercontent.com/23094588/124474018-4d850080-dda0-11eb-931e-7f5ae212df4a.png)

:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Eliminar una Editorial"
```

![image](https://user-images.githubusercontent.com/23094588/124481544-ad7fa500-dda8-11eb-9961-711c098dc39a.png)



## ✅ 29 Crear una Nueva Editorial

Para crear una nueva Editorial seguimos los siguientes pasos.

### Modificar el Controlador `src/Controller/EditorialesController.php`

Añadimos los siguientes métodos:

![image](https://user-images.githubusercontent.com/23094588/124494237-e161c700-ddb6-11eb-8b33-ad7c1d47bdc6.png)

![image](https://user-images.githubusercontent.com/23094588/124494363-09512a80-ddb7-11eb-9977-fc73600401f8.png)

**EL ORDEN EN QUE COLOCAMOS LAS ACCIONES IMPORTA** En este caso si estas dos rutas las ponemos después de:

![image](https://user-images.githubusercontent.com/23094588/124494513-369dd880-ddb7-11eb-92d9-be2d31ce2afc.png)

Nunca entraran en NUEVA o CREATE por que la estructura de la ruta es la misma.

### Modificar la plantilla `templates/editoriales/index.html.twig`

![image](https://user-images.githubusercontent.com/23094588/124494783-81b7eb80-ddb7-11eb-9b68-338f52cac0cd.png)


### Crear la Nueva Plantilla `templates/editoriales/nueva.html.twig`

![image](https://user-images.githubusercontent.com/23094588/124494882-ab711280-ddb7-11eb-8a54-8b9855f5f844.png)


### Salida de Pantallas

![image](https://user-images.githubusercontent.com/23094588/124495098-f5f28f00-ddb7-11eb-8fb6-7b1626e3b1da.png)


![image](https://user-images.githubusercontent.com/23094588/124495150-0acf2280-ddb8-11eb-8221-76fa5754876a.png)

![image](https://user-images.githubusercontent.com/23094588/124495223-23d7d380-ddb8-11eb-8dfd-3f1d8ec2a055.png)


:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Crear una Nueva Editorial"
```

![image](https://user-images.githubusercontent.com/23094588/124495367-4ff35480-ddb8-11eb-8fc5-f9a60fc26450.png)

## ✅ 30 Modificar una Editorial

Vamos a hacer la funcionalidad de modificar una Editorial.

### Modificar el Controlador `src/Controller/EditorialesController.php`

Añadimos los siguientes métodos:

![image](https://user-images.githubusercontent.com/23094588/124500605-5be31480-ddc0-11eb-9a5b-eac864a23d13.png)

![image](https://user-images.githubusercontent.com/23094588/124500720-8af98600-ddc0-11eb-99bd-453e76578bd9.png)

### Modificar la plantilla `templates/editoriales/index.html.twig`

![image](https://user-images.githubusercontent.com/23094588/124500815-b8deca80-ddc0-11eb-9854-db855852f4c0.png)


### Crear la Nueva Plantilla `templates/editoriales/nueva.html.twig`

![image](https://user-images.githubusercontent.com/23094588/124500885-d7dd5c80-ddc0-11eb-91e3-52fa91989fa9.png)

### Salida de Pantallas

![image](https://user-images.githubusercontent.com/23094588/124501094-3dc9e400-ddc1-11eb-8788-be56d6433eb5.png)

![image](https://user-images.githubusercontent.com/23094588/124501218-6f42af80-ddc1-11eb-9ccd-65dce3fe0b99.png)

![image](https://user-images.githubusercontent.com/23094588/124501264-81245280-ddc1-11eb-8d26-966df5966c5d.png)


:eight_pointed_black_star: Subir a GIT

```sh
git status
git add .
git commit -m "Modificar una Editorial"
```

![image](https://user-images.githubusercontent.com/23094588/124501307-97caa980-ddc1-11eb-82b5-76fe1c50e958.png)


## ✅ 31 


![image](https://user-images.githubusercontent.com/23094588/124496828-3e12b100-ddba-11eb-9d5e-b078505ab197.png)






























