## ✅ XX Plantillas de Error

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

### Ojo con Producción

Si nos logeamos nos muestra lo siguiente

![image](https://user-images.githubusercontent.com/23094588/126275069-c62f6458-d514-42e8-8d52-7f3f43804bb7.png)

Esto es por que establecimos **error** solo para DEV deberíamos añadir la ruta de los errores en la SECURITY.

Pues tampoco funciono **OJO CON ESTE CAMBIO EN PRODUCCION**

![image](https://user-images.githubusercontent.com/23094588/126275404-8187def4-1186-4470-bb61-0273d0b81c02.png)




## ✅ XX Otra forma de Usar la Plantillas de Error

Actualmente tenemos en **Fondos** lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/126278298-ee2fa276-00b5-499b-b8a6-b49945efd57e.png)

![image](https://user-images.githubusercontent.com/23094588/126278371-4a5788f6-1e92-47f9-aaaf-52be6eb4a567.png)

Esto pasa por que en el Controlador **`FondosController`** tenemos:

![image](https://user-images.githubusercontent.com/23094588/126278574-eec27c8c-c103-4feb-8275-bfa26195502a.png)

Cuando no encontramos un recurso lo mandamos a una plantilla común llamada **`comunes/recurso-no-encontrado.html.twig`** mandando como parámetro el mensaje a pintar.

En lugar de esto podemos lanzar una **Exception** por ejemplo **`createNotFoundException`** la cual lanza una excepción concreta que es **`NotFoundHttpException`** 

![image](https://user-images.githubusercontent.com/23094588/126279687-6655f77e-7fac-4c26-a69e-1e5b1150a214.png)

Esto es lo mismo que hacer:

![image](https://user-images.githubusercontent.com/23094588/126280130-a885cd02-da35-4c83-87ee-282822cd507a.png)

Symphone detecta la Excepción y manda una página 404.

Podemos manejar el error de dos formas mandando un status 200 y un mensaje de error personalizado(WEB) o redirigir a la plantilla del error 404, para un API se suele mandar un 404 cuando el recurso no se encuentra.

Probando el enlace **`http://localhost:8000/fondos/1`** que ya habíamos probado tenemos:

![image](https://user-images.githubusercontent.com/23094588/126281243-cb632ce6-7fef-4841-b67a-3c1ac5046312.png)

Una página 404 con el mensaje que mandamos.

Cualquier otra excepción que mandemos en lugar de las dos anteriores(que es la misma) mandan un error 500, error en el Servidor (BD caída, SQL mal construida, falta de permisos, etc).

![image](https://user-images.githubusercontent.com/23094588/126282528-842d2758-7478-4a74-b053-fe5b7abfa39a.png)

![image](https://user-images.githubusercontent.com/23094588/126282571-37c4dff9-720a-410f-b588-32379736557e.png)





























