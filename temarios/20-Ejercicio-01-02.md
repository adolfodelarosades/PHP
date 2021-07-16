### Para el **`login-json`**

Le damos acceso para no logeados.

![image](https://user-images.githubusercontent.com/23094588/125641957-e001600e-7786-447e-a887-90295a2baa66.png)


Probando

![image](https://user-images.githubusercontent.com/23094588/125642116-917f6feb-ec6a-4be0-a257-548d36852362.png)

![image](https://user-images.githubusercontent.com/23094588/125642194-49dbb320-dddb-41a2-acd6-6e3d24148172.png)


El Token recuperado es:

eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJpYXQiOjE2MjYyNzM3MTAsImV4cCI6MTYyNjI3NzA3MCwicm9sZXMiOlsiUk9MRV9VU0VSIl0sInVzZXJuYW1lIjoiYWRvbGZvQGdtYWlsLmNvbSJ9.Dqh0jJeFxvfR6rv9mF1Jj-Mw9vBF_fd3SVAPxdif1N2wmSII93taqsmClppcGKrRT2nNpe2eE8cDMA4iB7x96YUQKRmCZH6YtpKnOK0K3g8HIoCAz4hYMlMG9jy9SvVGgOdZWoldxlwKM7NMTzFf_C9vsLCNh3fY8s1U8dPhtdlgU73eFoPvNVQiVvZwM5mlizqGvcMXI5tYBuPhjOSS2TBVXJ1w_Z_XI_3nrHTpGax_TNDDScb2xBQ-KlvCCld2WzbAHgkKj4HxhwTRRi4B0HjV3oPwFxXoU4jXnywfC5l8uahEjtQiHy3h056FBR3gWHhQGIMGhjcmX5NrT_ZQrQ

https://jwt.io/

![image](https://user-images.githubusercontent.com/23094588/125642835-917ff86a-0487-47d8-8edc-3fdfa57d6731.png)


Aquí podemos ver lo que se oculta en el TOKEN


Si intento entrar en http://localhost:8000/fondos

![image](https://user-images.githubusercontent.com/23094588/125643659-20f66e9e-7f72-4c13-acd5-d08648f5e736.png)


### DESDE UNA APLICACION ESXTERNA QUE MANDA LLAMAR EL json-lo

Debo pasar el TOKEN en cada llamada

Revisar 13/07/21


## 🔴 Bundle Alice Bundle

https://github.com/hautelook/AliceBundle

Pertite insertar registros a mogollon

Para poblar la BD.

El comando para instalar es :

**`composer require --dev hautelook/alice-bundle`**

![image](https://user-images.githubusercontent.com/23094588/125647193-2b7786fa-031f-489a-9611-aa666e09227a.png)

![image](https://user-images.githubusercontent.com/23094588/125647253-8da039a4-07e2-4783-9a1d-6c19f91b7a9e.png)


![image](https://user-images.githubusercontent.com/23094588/125647455-460d8d31-7a7c-4dbc-947a-6ba79b0bc816.png)


![image](https://user-images.githubusercontent.com/23094588/125647690-afd95322-62a0-4d42-9fa4-0255ab28576e.png)


Crear el Fixure

![image](https://user-images.githubusercontent.com/23094588/125650188-f9b4dab0-ff9f-41f5-9dd9-359214bb5442.png)

![image](https://user-images.githubusercontent.com/23094588/125651513-a46124c6-c5a9-432d-873f-f05bc698d257.png)


```
parameters:
    hash: $2y$13$KI/2bbjTMVrEmc.wtVe7dOelSDPyNaoiDl.zfwKZAqe82rz0yJDiW

App\Entity\User:
    user_admin:
        email: admin@admin.com
        roles: ["ROLE_ADMIN"]
        password: <{hash}>
    
    user_adolfo_admin:
        email: adolfoAdmin@gmail.com
        roles: ["ROLE_ADMIN"]
        password: <{hash}>

    user_carlos:
        email: adolfo@gmail.com
        roles: []
        password: <{hash}>

App\Entity\Editorial:
    editorial_{1..100}:
        nombre: <company()>

App\Entity\Autor:
    autor_{1..500}:
        nombre: <name()>
        tipo: 'PERSONA'
    autor_{501..600}:
        nombre: <company()>
        tipo: 'ENTIDAD'

App\Entity\Fondo:
    fondo_{1..1000}:
        titulo: <sentence()>
        isbn: <isbn13()>
        edicion: <numberBetween(1940, 2021)>
        publicacion: <numberBetween(1940, 2021)>
        categoria: <word()>
        editorial: '@editorial_*'
        autores: '<numberBetween(1, 3)>x @autor_*'
```

Ejecutar Comando

![image](https://user-images.githubusercontent.com/23094588/125649542-1170f561-e6a8-4323-bafa-8747c4380c71.png)

![image](https://user-images.githubusercontent.com/23094588/125650211-e01b02e2-3a3b-4a0a-b3cc-63e35070a49e.png)


En la BD

![image](https://user-images.githubusercontent.com/23094588/125650246-2112e390-a59c-43a8-9ad5-ad0a3116dea8.png)

![image](https://user-images.githubusercontent.com/23094588/125650341-d45436eb-255b-4d86-823d-2a9c6bc317b9.png)



![image](https://user-images.githubusercontent.com/23094588/125649824-b468a2ed-eb40-4649-be40-8c42b0e98ff3.png)

![image](https://user-images.githubusercontent.com/23094588/125651365-27e00311-adaa-43a9-af37-c2495e1b729e.png)

En la WEB


![image](https://user-images.githubusercontent.com/23094588/125654437-4d1f6de2-5334-42b6-ab59-28462ba5cea6.png)

![image](https://user-images.githubusercontent.com/23094588/125654512-67f27e98-2191-4c37-8e51-139e04e40cec.png)

![image](https://user-images.githubusercontent.com/23094588/125654567-a09fb8a6-79fb-4aa5-abfc-f5be054a94ce.png)

![image](https://user-images.githubusercontent.com/23094588/125655211-cd32a638-400b-4929-b28b-fda2735998ba.png)

Esto nos arroja 1102 Consultas en 461.24 ms

![image](https://user-images.githubusercontent.com/23094588/125656672-75f62ddd-09fc-48ca-a829-7bb4513c2d59.png)

En Datatable no muestra lo mismo solo muestra un Query

![image](https://user-images.githubusercontent.com/23094588/125656921-3678a727-f40b-43e6-8cc1-3aee20a2d194.png)

### GIT de Alice

![image](https://user-images.githubusercontent.com/23094588/125660646-c6c0b254-12cf-4566-9b53-97869ec9e496.png)

![image](https://user-images.githubusercontent.com/23094588/125660771-dd92a5dc-694f-4965-8385-e9934706a1f1.png)


## 🔴 OPTIMIZAR QUERIES

https://www.doctrine-project.org/projects/doctrine-orm/en/2.9/reference/query-builder.html#the-querybuilder

Añadir funcion en el Repositorio

![image](https://user-images.githubusercontent.com/23094588/125667571-122c9f7e-44da-409a-a88f-731c28c681b0.png)


Cambiar en la llamada

![image](https://user-images.githubusercontent.com/23094588/125667623-274e66e0-1ad8-45f2-9420-b30dae24001d.png)

(Tambien se puede cambiar en el Datatable)

Al Probar ya solo sale un Query

![image](https://user-images.githubusercontent.com/23094588/125667691-75eec3c3-fd35-4ff3-a9fe-7f4086cd75db.png)

Para mas Info

https://www.doctrine-project.org/projects/doctrine-orm/en/2.9/reference/dql-doctrine-query-language.html#doctrine-query-language

![image](https://user-images.githubusercontent.com/23094588/125667822-bebb2da6-410d-4da8-8fe6-199981b10588.png)



Comando para mostrar lo que tenemos instalado en el proyecto **`composer show --installed `**


GIT

![image](https://user-images.githubusercontent.com/23094588/125669134-41d3bb42-c209-4115-8615-6072bd5ceed2.png)

## 🔴 QUERY BUILDER

![image](https://user-images.githubusercontent.com/23094588/125670154-f4437dee-11a9-438b-a47d-d2d34d4f35c7.png)


![image](https://user-images.githubusercontent.com/23094588/125670736-393adfca-600a-47ed-a02b-c5c00e79084e.png)

Llamo el método


![image](https://user-images.githubusercontent.com/23094588/125671443-ca50e822-1b2a-413b-9251-be84d20c913e.png)


![image](https://user-images.githubusercontent.com/23094588/125671509-dadb763e-3d78-478f-acf0-0eb767cd580f.png)


GIT

![image](https://user-images.githubusercontent.com/23094588/125674385-58728313-cebc-4f60-8240-6477530b217b.png)





## 🔴 SQL

![image](https://user-images.githubusercontent.com/23094588/125670774-0f2b8f8a-5111-4776-8129-df5a23a6566a.png)

![image](https://user-images.githubusercontent.com/23094588/125674629-d6f22b9d-13e9-4548-8904-b7ee0e499f40.png)


OJO este query regresa 2050 resultados por los cruces

Hay que tratar los datos antes de devolverlos para que el proceso siga trabajando.

![image](https://user-images.githubusercontent.com/23094588/125674782-68610a25-71cc-4d90-9741-78f8395d5975.png)

![image](https://user-images.githubusercontent.com/23094588/125675458-83270e07-9e5c-4f2f-a33f-c8a0f4b0bf39.png)

## ✅ XX I18N

https://symfony.com/doc/current/translation.html

Existen dos formas de Traduccir:

* En las plantillas Twig
* En el código

Los diccionarios de traducciones se almacenan en:

![image](https://user-images.githubusercontent.com/23094588/125916729-fd2e8475-e5ca-4da8-b81b-86b1681ddacc.png)

Por ahora no tenemos ninguno.


#### Comando para ver las traducciones que nos faltan hacer en nuestros diccionarios.

**`php bin/console translation:update --dump-messages en`**

![image](https://user-images.githubusercontent.com/23094588/125915921-be59be24-9e72-4c8a-85d0-4187d86bd685.png)

![image](https://user-images.githubusercontent.com/23094588/125916025-4f681282-d9f7-406e-a982-a80638f6a513.png)

![image](https://user-images.githubusercontent.com/23094588/125916133-40346c7b-1f23-4ad8-92a0-7b02969101d0.png)

![image](https://user-images.githubusercontent.com/23094588/125916225-4192daab-b98a-4985-8e21-cea671d9c623.png)

Como aun no hemos usado la traducción no detecta texto por traducir.

### Empecemos por traducir la página Inicial.

![image](https://user-images.githubusercontent.com/23094588/125917084-57ee7baf-7986-40ec-ad06-9c3f0ac2a68f.png)

Esta página solo tiene dos textos: 

* **Gestión de Fondos**
* **Libros, Revistas, Documentales, Videos, Películas CDs, ...**

Vamos a la plantilla de esta página y vemos que tenemos:

![image](https://user-images.githubusercontent.com/23094588/125921728-8088bbdd-c79b-45bd-a5ce-38441c7e73d6.png)

Lo cambiamos por lo siguiente para usar las traducciones:

![image](https://user-images.githubusercontent.com/23094588/125924060-87cb5db8-3019-4c86-ab82-b439ed6636e3.png)

Por lo que si ejecutamos de nuevo el comando **`php bin/console translation:update --dump-messages en`** tenemos:

![image](https://user-images.githubusercontent.com/23094588/125924130-2eb7ea55-b3e1-4124-a651-b35e6b971ccc.png)

***Nos indica que tenemos tres textos sin traducir***

#### Comando para Crear los Archivos de Traducciones

**`php bin/console translation:update --force en`**

![image](https://user-images.githubusercontent.com/23094588/125925088-e84583cb-6bf6-4d8b-89af-e9625de5f1c6.png)

Crea en la carpeta **`translations`** los siguientes archivos:

![image](https://user-images.githubusercontent.com/23094588/125925214-7fe6a1ec-8c17-411e-a04f-871d5a233b45.png)

Vamos a realizar lo mismo pero para Español:

**`php bin/console translation:update --force es`**

![image](https://user-images.githubusercontent.com/23094588/125925515-5023bd6b-24c8-4458-8191-a0bf0668e535.png)

![image](https://user-images.githubusercontent.com/23094588/125925538-bfde2621-4f78-4482-8996-98b97ff72706.png)


Si abrimos el archivo **`messages+intl-icu.en.xlf`** que es el documento en Inglés tenemos:

![image](https://user-images.githubusercontent.com/23094588/125925864-94c5df66-631d-4e9b-a635-4924fd5a1cc1.png)


* **`source`** indica el texto original.
* **`target`** indica el texto traducido.

Vamos a realizar las traducciones:

![image](https://user-images.githubusercontent.com/23094588/125926456-8165fba9-747a-4884-bfa9-f3889a8468fc.png)

En el Documento de Español **`messages+intl-icu.es.xlf`** que lo tenemos así:

![image](https://user-images.githubusercontent.com/23094588/125926803-eb2d3667-96f3-43fd-ada2-94ce85f43062.png)

Simplemente quitamos las barras:

![image](https://user-images.githubusercontent.com/23094588/125926900-08f4f510-de3b-4055-8519-9a3fbf0d41c3.png)

#### Contamos con Archivos de Seguridad **`security.en.xlf`** y **`security.es.xlf`**

***Obsérvese que en estos documentos el Original siempre es el Inglés y la traducción es la que se va cambiando según el lenguaje***

![image](https://user-images.githubusercontent.com/23094588/125927233-3276dc19-b1d7-4e17-a6c2-9af9132f518b.png)

![image](https://user-images.githubusercontent.com/23094588/125927286-ace5c2d0-5aae-47b0-b2f6-95e8499ff751.png)

#### También Contamos con Archivos de Validación **`validators.en.xlf`** y **`validators.es.xlf`**

***Obsérvese que podemos mandar parámetros a los mensajes***

![image](https://user-images.githubusercontent.com/23094588/125927984-27f2ff51-8d2f-4283-bcc2-ded2865b10e9.png)

![image](https://user-images.githubusercontent.com/23094588/125928052-6fb40c26-f9c6-41f7-88f5-acfd8e283aec.png)

#### Cargar la Página 

Una vez hechas las traducciones ya se muestra en la Home por que por default Symphony esta en Inglés.

![image](https://user-images.githubusercontent.com/23094588/125929236-51a1b4de-ce35-45a6-8ca3-2a2dd6773225.png)

#### Ver Ayuda de Translation

![image](https://user-images.githubusercontent.com/23094588/125930862-f5d46788-4a27-4f5e-b819-27ddfe6efd67.png)

![image](https://user-images.githubusercontent.com/23094588/125930789-4402019d-4148-4ce6-b228-47263d976d43.png)

Nos indica que por default se esta usando Inglés y que se han traducido 3 textos.

### Vamos a Cambiar la Página de **`Quiénes somos`**

![image](https://user-images.githubusercontent.com/23094588/125932680-dfbcb58a-4ddb-486c-8aa1-dd0482ce8da7.png)

Si intentamos cargar la página tenemos:

![image](https://user-images.githubusercontent.com/23094588/125932745-d72f6f10-c013-451a-8e04-73b61dd53c0f.png)

Vemos que el texto **`Quiénes somos`** aparece en español pero el otro en Inglés.

Si vemos la ayuda de **Translation** que ahora aparece en rojo tenemos:

![image](https://user-images.githubusercontent.com/23094588/125932884-596ed105-4dcc-4fb4-a6de-c8fba68cc5d7.png)

Nos indica que se nos ha olvidado hacer una traducción que se ocupa dos veces. Y por otro lado podemos ver las definiciones que se usan y que ya esta traducida, por eso el texto ya nos aparece en Inglés.

![image](https://user-images.githubusercontent.com/23094588/125933069-856852d5-9e21-45fe-adad-4661f55f7ad9.png)

Podemos meterla manualmente o repetir los comandos para que lo meta por nosotros:

**`php bin/console translation:update --force en`**
**`php bin/console translation:update --force es`**

![image](https://user-images.githubusercontent.com/23094588/125933463-1699b850-b7d8-41db-a8b9-916a66be202c.png)

![image](https://user-images.githubusercontent.com/23094588/125933541-2fa4dda0-ec0e-4337-8073-bde7b5f12608.png)

Ha insertado los textos que nos faltan por traducir, en este caso ess solo uno:

![image](https://user-images.githubusercontent.com/23094588/125933654-7f0d24bf-f827-4c6f-8418-939f5c568ac0.png)

Hay que realizar las traducciones:

![image](https://user-images.githubusercontent.com/23094588/125933893-91a62971-e108-4a03-b293-b6b1edd8c6ea.png)

![image](https://user-images.githubusercontent.com/23094588/125934050-c12f5fef-e575-4584-ad80-75cdcd80f5fa.png)


Si vemos la página tenemos

![image](https://user-images.githubusercontent.com/23094588/125934173-35c3b38d-0c76-4434-816f-d9c2b2afef35.png)

![image](https://user-images.githubusercontent.com/23094588/125934241-f342bb8d-6758-4ec6-af3d-8e6a7d0d6875.png)

***Debemos repetir este proceso para todas nuestras páginas***

### Veamos el caso de la página `Login`

![image](https://user-images.githubusercontent.com/23094588/125935097-a2cc6d12-33ce-4cfb-900d-fefc565b32d6.png)

![image](https://user-images.githubusercontent.com/23094588/125935141-45b4e4ef-c6fa-4cea-bc31-f149250ba030.png)

***Observese que para los mensajes de error ya maneja algunos mensajes de la seguridad***

![image](https://user-images.githubusercontent.com/23094588/125937477-dcffa0c4-4e6a-4e16-b32b-7e679979cfd1.png)

#### Vamos a meter los mensajes para la traducción.

![image](https://user-images.githubusercontent.com/23094588/125939915-f4d0aab5-2f35-42dd-a3ba-5bef9f07095e.png)

![image](https://user-images.githubusercontent.com/23094588/125940061-8affe748-66a9-42b4-bf7b-89736e91a375.png)

Repetir los comandos para que lo meta por nosotros:

**`php bin/console translation:update --force en`**
**`php bin/console translation:update --force es`**

![image](https://user-images.githubusercontent.com/23094588/125940175-2e75c041-1ae6-4ee1-97a6-7319bd25c9d5.png)

![image](https://user-images.githubusercontent.com/23094588/125940238-c976f646-8c97-4b7b-8b40-e2474fd0ce94.png)

Vamos a meter las traducciones:

![image](https://user-images.githubusercontent.com/23094588/125940470-fdb5f7e7-acaf-4212-ac66-214133750346.png)

![image](https://user-images.githubusercontent.com/23094588/125940776-5f7b4a35-1183-4c7a-832c-a566d832e3db.png)


Si cargamos la página tenemos:

![image](https://user-images.githubusercontent.com/23094588/125952471-0a81bff8-5a13-46ae-9b91-9c2a71023250.png)


Finalmente vamos a cambar el Menú Inicial

![image](https://user-images.githubusercontent.com/23094588/125953354-7f59ad71-dcb1-4386-b960-2f4e46e80edd.png)


### MODIFICAR RUTAS PARA IDIOMAS

También es muy recurrida la técnica de poner las urls prefijadas con el idioma. En ese caso se configura así:

**`config/routes/annotations.yaml`**

![image](https://user-images.githubusercontent.com/23094588/125954742-6f089de9-00b1-4b01-a673-3dfa048e1957.png)

Le añadimos lo siguiente:

![image](https://user-images.githubusercontent.com/23094588/125954938-ed9e9e4d-e05a-4797-8586-8a70d0f59bd0.png)














**``**
**``**















