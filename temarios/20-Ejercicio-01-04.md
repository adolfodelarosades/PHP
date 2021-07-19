## XX Plantillas de Error

![image](https://user-images.githubusercontent.com/23094588/126192239-d9aa3dda-d6fc-4d74-9451-f2b510fba672.png)

Crear la Carpeta **`mkdir -p templates/bundles/TwigBundle/Exception`** y dentro el archivo  **`error404.html.twig`**

Si llamamos al URL **`http://localhost:8000/_error/404`** (HAY QUE ESTAR LOGEADO O AÑADIRLA EN SECURYTY **`- { path: ^/_error, roles: IS_AUTHENTICATED_ANONYMOUSLY }`**) tenemos lo que ayamos puesto en la plantilla **`error404.html.twig`**

![image](https://user-images.githubusercontent.com/23094588/126193429-dbad9c41-33cb-41cf-8dc8-77f05a01d108.png)

Muchas veces la Cache se queda Bloqueado y hay que limpiar la cache con **`php bin/console cache:clear`**







