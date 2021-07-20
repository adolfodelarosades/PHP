## XX Plantillas de Error

![image](https://user-images.githubusercontent.com/23094588/126192239-d9aa3dda-d6fc-4d74-9451-f2b510fba672.png)

Crear la Carpeta **`mkdir -p templates/bundles/TwigBundle/Exception`** y dentro el archivo  **`error404.html.twig`**

**ESTO ES SOLO PARA VER COMO SE VEN LAS PÁGINAS DE ERROR EN DESARROLLO POR QUE SI PROVOCAMOS UN ERROR REALMENTE NO SE VE, MUESTRA LA QUE TIENE SIEMPRE**

![image](https://user-images.githubusercontent.com/23094588/126196097-fa89eeda-2a96-46a7-95e3-97c774c44fb9.png)




Si llamamos al URL **`http://localhost:8000/_error/404`** (HAY QUE ESTAR LOGEADO O AÑADIRLA EN SECURYTY **`- { path: ^/_error, roles: IS_AUTHENTICATED_ANONYMOUSLY }`**) tenemos lo que ayamos puesto en la plantilla **`error404.html.twig`**

![image](https://user-images.githubusercontent.com/23094588/126193429-dbad9c41-33cb-41cf-8dc8-77f05a01d108.png)

Muchas veces la Cache se queda Bloqueado y hay que limpiar la cache con **`php bin/console cache:clear`**

Otra opción es mejor añadirla en en lugar de la opción **`- { path: ^/_error, roles: IS_AUTHENTICATED_ANONYMOUSLY }`**

![image](https://user-images.githubusercontent.com/23094588/126196296-29c72833-2aa1-42c6-aaa1-e51a4b8c8743.png)

Si no cambiamos las platillas se muestran así:

![image](https://user-images.githubusercontent.com/23094588/126199882-c410d1e6-0706-43c3-9c69-72cf887a58b7.png)

La plantilla Original esta en **`vendor/symfony/error-handler/Resources/views/error.html.php**`




