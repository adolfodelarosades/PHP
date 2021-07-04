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


