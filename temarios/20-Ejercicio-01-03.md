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

## ✅ XX Ordenación ASC/DESC por Campos

Lo primero que tenemos que hacer es modificar **`FondoRepository.php`**

![image](https://user-images.githubusercontent.com/23094588/126143653-2e0f45ff-d8ee-4a79-bd26-b9504e2c9505.png)

Para Ordenar por Autores o Editorial se usan otras tablas por eso hay que usar su correspondiente Alias. Por otro lado también se recibe el parámetro para el tipo de Orden es decir ASC o DESC.

Modificamos el Controlador **`FondosPaginadosController.php`**

![image](https://user-images.githubusercontent.com/23094588/126144024-851da5da-39d2-4415-89ca-ff4e1ddf45af.png)

Añadimos el parámetro para el tipo de Orden es decir ASC o DESC.

En **`_menu.html.twig`** añadimos en nuevo parámetro.

![image](https://user-images.githubusercontent.com/23094588/126145579-5cf955a4-2e21-4e09-baec-a531eaa9b07e.png)

En **`_paginacion.html.twig`** añadimos en nuevo parámetro.

![image](https://user-images.githubusercontent.com/23094588/126145781-d1a5895b-dda1-4a93-9ada-f6fec9ef7e8f.png)

En **`templates/fondos_paginados/index.html.twig`** 

![image](https://user-images.githubusercontent.com/23094588/126146019-efc742c9-71b0-4710-b69e-0268668838fd.png)

![image](https://user-images.githubusercontent.com/23094588/126146162-81dd600f-4e47-4804-ac79-c7b3608aed9b.png)

![image](https://user-images.githubusercontent.com/23094588/126146256-ee2cf06b-1a2c-4eb6-b158-10b5802cbcf4.png)

Se subieron las imagenes **`sort_asc.png`**, **`sort_both.png`** y **`sort_desc.png`**


### Probando la Aplicación

![image](https://user-images.githubusercontent.com/23094588/126146448-09d3555b-4933-4a12-92df-ec839bf1b824.png)

![image](https://user-images.githubusercontent.com/23094588/126146487-0e78e11e-d8aa-4f98-877b-dc806febe230.png)

![image](https://user-images.githubusercontent.com/23094588/126146514-8865bf4c-c03e-47ae-b9eb-680963ef7302.png)

![image](https://user-images.githubusercontent.com/23094588/126146558-cf91ad60-b2a0-4afb-b504-853ba03b9682.png)

![image](https://user-images.githubusercontent.com/23094588/126146617-fae0d58f-c564-4e67-b300-e8b898164b70.png)

![image](https://user-images.githubusercontent.com/23094588/126146658-4f378a76-3ba2-4075-b326-3b820c194077.png)

![image](https://user-images.githubusercontent.com/23094588/126146713-34611357-2857-42e7-a5a0-bdd7b9ff0d26.png)

![image](https://user-images.githubusercontent.com/23094588/126146758-1e3193ae-1624-4451-ba17-3309d639d32e.png)

![image](https://user-images.githubusercontent.com/23094588/126146813-63218d37-606c-4170-aa99-69e50d61b693.png)

![image](https://user-images.githubusercontent.com/23094588/126146842-bd805d76-26fc-4299-880f-0ff076462a37.png)

### GIT

![image](https://user-images.githubusercontent.com/23094588/126146907-1e00b415-1cef-4dc1-a748-0b4d5ec53056.png)

![image](https://user-images.githubusercontent.com/23094588/126147064-4461df95-a14b-4055-9cf0-1c80c8696600.png)

