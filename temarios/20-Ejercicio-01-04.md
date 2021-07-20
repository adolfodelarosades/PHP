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

![image](https://user-images.githubusercontent.com/23094588/126272072-d1430114-2f1f-46fd-a3ee-806522b40dbf.png)

![image](https://user-images.githubusercontent.com/23094588/126199882-c410d1e6-0706-43c3-9c69-72cf887a58b7.png)

La plantilla Original esta en **`vendor/symfony/error-handler/Resources/views/error.html.php**`**

Podemos mejorar el diseño de la plantilla para **`error404.html.twig`**.

![image](https://user-images.githubusercontent.com/23094588/126272238-31a28b13-7eae-492a-a309-d80d667b2660.png)

Para hacerlo lo hemos tomado de una plantilla libre.

![image](https://user-images.githubusercontent.com/23094588/126273210-ddfef3ea-caec-4aa6-8daf-c6991a076647.png)

Hemos insertado el archivo **`sb-admin-2.min.css`** para el estilo.

Hasta ahora hemos probado a nivel DEV con **`http://localhost:8000/_error/404`** ya que por estar en modo desarrollo es la forma de ver como queda la plantilla por que sino la salida normal para un error 404 es:

![image](https://user-images.githubusercontent.com/23094588/126273546-f10c4933-d85d-4812-8ef8-5ae44dff34fe.png)

Si realmente queremos ver como se veria en PRODucción tenemos que cambiar un parámetro en **`.env.local`**:

![image](https://user-images.githubusercontent.com/23094588/126273770-a0592c08-a9e7-4070-b49e-d165daa47ed9.png)

lo cambiamos por **`prod`**

![image](https://user-images.githubusercontent.com/23094588/126273841-ed7f5346-b3c4-457a-8bf5-0c171eedf536.png)

Es posible que tengamos que limpiar la cache con **`php bin/console cache:clear`**:

![image](https://user-images.githubusercontent.com/23094588/126274122-c5f5daa3-1676-44c9-b444-34d20d4569b9.png)

Si ahora probamos nuevamente el enlace **`http://localhost:8000/ventas`** tenemos:

![image](https://user-images.githubusercontent.com/23094588/126274238-27c1e5ac-d53c-4752-a2b7-d49c188f06ef.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/126274314-a6fd1750-be4c-4dd7-ad9f-7603d35ab75a.png)

![image](https://user-images.githubusercontent.com/23094588/126274422-a8fc4670-ac24-433d-921f-bb787000f47e.png)





















