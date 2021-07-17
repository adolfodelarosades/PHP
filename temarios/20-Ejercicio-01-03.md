## ✅ XX Paginación

### Realizamos el Query que realice la busqueda deseada y Paginado

En **`FondoRepository.php`** añadimos el siguiente método:

![image](https://user-images.githubusercontent.com/23094588/125985195-49d4639b-1f22-4160-a3de-08236ea0cd7b.png)

### Crear un Nuevo Controler

**`bin/console make:controller`**

![image](https://user-images.githubusercontent.com/23094588/125986974-a8a51522-a343-447a-8cf4-832d0603c090.png)

#### Código Controlador

![image](https://user-images.githubusercontent.com/23094588/126043686-d34c6560-56aa-4df3-b11d-c0dc2323c30e.png)

#### Añadir Parámetros en **`services.yaml`**

![image](https://user-images.githubusercontent.com/23094588/126043895-fda897f3-d039-4e06-98ba-5ac7d622c8aa.png)

#### Código Plantillas

![image](https://user-images.githubusercontent.com/23094588/126043712-d219d303-dcf8-4e20-9541-e97cb9274750.png)

![image](https://user-images.githubusercontent.com/23094588/126043725-c5f85714-9729-47ad-b0d6-73c22fa05c7f.png)

![image](https://user-images.githubusercontent.com/23094588/126043738-46be8139-42a3-44c9-ba38-f55f34f4fd25.png)

#### Sección Paginación

![image](https://user-images.githubusercontent.com/23094588/126043815-f0a109a3-2189-44e3-a140-3c15ed7ea53a.png)

#### Estilos

![image](https://user-images.githubusercontent.com/23094588/126043870-8d4d02e3-f5be-4246-92ec-bf4ac7cb4817.png)

#### Añadir Opción al Menú **`_menu.html.twig`**

Ninguna funciona bien no encuentra la Ruta.

![image](https://user-images.githubusercontent.com/23094588/126044117-686f4c29-60de-436a-85d3-7418895bce50.png)

![image](https://user-images.githubusercontent.com/23094588/126044635-911c2e87-9feb-4fdd-b784-7b0dd0cd26ca.png)


#### Probar la Aplicación, Un Error común ¿Por qué no me había salido?

![image](https://user-images.githubusercontent.com/23094588/125990330-b3d3e20f-dad8-4a85-b1f4-e70047d89eaa.png)

![image](https://user-images.githubusercontent.com/23094588/125990701-ca62ce22-1096-4d54-9351-d18cecbd8b3f.png)

#### Añadir **`__toString()`** a Entidades **`Editorial`** y **`Autor`**

![image](https://user-images.githubusercontent.com/23094588/126043984-c8bf1d1b-d636-41d8-b79f-8ffcad20cdda.png)

![image](https://user-images.githubusercontent.com/23094588/126043995-e66b0276-ec3c-49e3-b60b-0b784fec1c9f.png)

#### Probar la Aplicación

Al pulsar la Opción del Menú **`Fondos Paginado`** me sale esto:

![image](https://user-images.githubusercontent.com/23094588/126044682-4d376254-df4d-4f23-a61d-0b2d6526a0fb.png)

Se confunde con la Ruta **`http://localhost:8000/fondos/6`**

Manualmente pongo **`http://localhost:8000/fondos/paginados/id/1`** y se carga:

![image](https://user-images.githubusercontent.com/23094588/126044704-468e07ef-1bc3-478c-bcda-2150caada18e.png)

![image](https://user-images.githubusercontent.com/23094588/126044714-dfeff832-a1d3-4e87-adf3-3dad4af01398.png)

![image](https://user-images.githubusercontent.com/23094588/126044722-1fd064c1-4581-4482-86b1-09ded3e22f22.png)

![image](https://user-images.githubusercontent.com/23094588/126044726-905875c8-e71f-4b8d-b9df-df9746a5464b.png)

![image](https://user-images.githubusercontent.com/23094588/126044732-362534fe-f68b-4a78-845b-14dbdc7756d2.png)

Existe otro problema con al seleccionar la página 1 ya que el enlace que se arma no toma los valores

![image](https://user-images.githubusercontent.com/23094588/126044856-0698b4a6-8d6f-41e0-9c2f-212052520981.png)

![image](https://user-images.githubusercontent.com/23094588/126044872-2528300d-e688-4569-99fa-3901e341f3eb.png)

Si comento los valores por Default se componen ambos problemas.

![image](https://user-images.githubusercontent.com/23094588/126044943-fff7bed9-d9a2-4a56-ba95-3775c91be6c0.png)



#### GIT

![image](https://user-images.githubusercontent.com/23094588/126044750-2126bc55-6cbc-42f8-9bcf-d9ea486595ae.png)

![image](https://user-images.githubusercontent.com/23094588/126044796-651cc893-638f-43c8-b3f2-9628f29ecfcd.png)

![image](https://user-images.githubusercontent.com/23094588/126045292-84501804-c417-4357-9953-832b2eedbfaf.png)

