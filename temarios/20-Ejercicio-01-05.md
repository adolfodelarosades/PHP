## ✅ XX FORWARD

20/07/2021

Como trabaja el **`forward`** en vez de un **`redirec`**, parecieran lo mismo pero no trabajan igual, el **`forward`** es menos recomendable pero es más eficiente.

Con **`redirec`** hay dos llamadas al Server con **`forward`** solo una.

El **`forward`** puede provocar una URL no muy real.

(explicación 1er HORA)

## ✅ XX AUTORIZACIÓN

Autorización según el Rol, en código o en plantillas.

## ✅ XX SERIALIZADOR
(Explicación 2da Parte)

![image](https://user-images.githubusercontent.com/23094588/126366061-77487714-a204-4365-9ee8-ff038d8256a1.png)


Dos pasos 

1) Normalizar convertir los Objetos en Arrays
2) Convertirlo al formato deseado JSON, XML, CVS, etc.
(Si se hace manual)

Symphony tiene un Serializador que convierte Array de Objetos a JSON directamente.

Se inyecta el Servicio 

![image](https://user-images.githubusercontent.com/23094588/126366538-757cf265-eb79-4449-8940-7ad7defb0f7d.png)

Con PHP solo, medio medio

![image](https://user-images.githubusercontent.com/23094588/126366727-13ca65e3-3b69-4315-9769-9300c6e5d042.png)

Una respuesta bien con Symphony es:

![image](https://user-images.githubusercontent.com/23094588/126367052-cc97842a-e9bd-4db8-9158-74e29d489fa5.png)

Hay un error de Referencia Circular.

![image](https://user-images.githubusercontent.com/23094588/126367191-dbf78a71-7c6a-4af3-b881-b1a4664f7fd3.png)

Esto es por que los Autores tienen la propiedad Fondos, y vuelven a salir los Fondos del Autor, se hace un bucle.

Sino ubieramos hecho la relación inversa entre las entidades (fondos en el autor) no pasaría eso.

IGUAL PARA LA EDITORIAL.

![image](https://user-images.githubusercontent.com/23094588/126368168-c5560869-fbb6-47df-9c20-6b33306a0cd2.png)

Pero la solución no siempre puede ser quitar las propiedades a las Entidades.

![image](https://user-images.githubusercontent.com/23094588/126368477-3b10c919-7776-4637-85f4-ba7131653aed.png)

Usar Normailizadores y Encoders.

### Para deserializar un Objeto.

![image](https://user-images.githubusercontent.com/23094588/126368588-5a04acfd-e531-4c16-b29a-4872dc6eece6.png)

### Solución a las Referencias Circulares.

Lanza Exception **`CircularReferenceException`**

![image](https://user-images.githubusercontent.com/23094588/126369112-d2e411db-c053-47dc-b354-efaae1ab54b8.png)

![image](https://user-images.githubusercontent.com/23094588/126369796-e16cf765-a187-448b-b33d-cf58bfcb8b45.png)

Con PHP 8 se pueden usar los nameParameters.

![image](https://user-images.githubusercontent.com/23094588/126369903-8a2f10a3-bb67-4ca7-ac5e-98925cb5f0a4.png)

![image](https://user-images.githubusercontent.com/23094588/126380839-0e6146c7-396d-4991-a5be-bdcbbdedfd96.png)


















