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





