


OTRA.
![image](https://user-images.githubusercontent.com/23094588/124496828-3e12b100-ddba-11eb-9d5e-b078505ab197.png)

### SERVICIOS

#### Los servicios que se necesiten en mi servicio los INYECTO en el Construtor.

![image](https://user-images.githubusercontent.com/23094588/124551861-0b58cf00-de33-11eb-987f-ba950ed7069e.png)

Crear variable de clase que se usará en los métodos con el valor Inyectado

![image](https://user-images.githubusercontent.com/23094588/124552300-a487e580-de33-11eb-89d0-757dbe074a6c.png)

#### En el Controlador Llamamos al Servicio que hace la Lógica

![image](https://user-images.githubusercontent.com/23094588/124553379-f2511d80-de34-11eb-85c2-2bd94493914a.png)

El Servicio tiene que responder una respuesta que le llegará al Controlador. SEGUN LO QUE SE QUIERA DEVOLVER

Devolver solo el ID

![image](https://user-images.githubusercontent.com/23094588/124553701-57a50e80-de35-11eb-8c79-453ac145b9ac.png)


Devolver la Entidad Entera

![image](https://user-images.githubusercontent.com/23094588/124553760-6db2cf00-de35-11eb-8cca-ecd716cc90bd.png)

Un Array Asociativo

![image](https://user-images.githubusercontent.com/23094588/124554018-c97d5800-de35-11eb-8781-1745bb8ecb7e.png)

#### Para posibles fallos en el Flush hay dos opciones de Manejarlo:

1) Con TRY en el Servicio (Quitamos el del Controlador)

![image](https://user-images.githubusercontent.com/23094588/124554405-3a247480-de36-11eb-965a-8d9aa03232dc.png)

![image](https://user-images.githubusercontent.com/23094588/124554822-abfcbe00-de36-11eb-91bb-f00b831adec4.png)

2) Manejar la Excepción del fallo en el Servicio(flush) en el Controlador

![image](https://user-images.githubusercontent.com/23094588/124555164-0c8bfb00-de37-11eb-824c-3730b7643aba.png)


#### El Constructor necesita usar el Servicio ¿Comó le llega? INYECTANDOLO

![image](https://user-images.githubusercontent.com/23094588/124567029-e1f46f00-de43-11eb-864a-cc788662216b.png)

#### El Constructor es el encargado de recibir el REQUEST y recuperar los datos, que serán pasados al Servicio, NUNCA SE LE PASA EL REQUEST COMPLETO al Servicio para que el obtenga los datos, ES UNA TAREA DEL CONTROLADOR.


#### El Controlador si puede llamar al "Servicio Repository" por ejemplo:

![image](https://user-images.githubusercontent.com/23094588/124573281-af4d7500-de49-11eb-86c6-5bf74fdb14b2.png)

O

![image](https://user-images.githubusercontent.com/23094588/124573382-c7bd8f80-de49-11eb-8065-259a859e8b2d.png)


Cuando creo cosas en el Controlador ya lo debo mover a un Servicio, por ejemplo:

![image](https://user-images.githubusercontent.com/23094588/124573561-f3d91080-de49-11eb-9a2f-ddb80c58b577.png)

Este método es más discutible si se cambia o no a un Servicio:

![image](https://user-images.githubusercontent.com/23094588/124574192-8679af80-de4a-11eb-9a9c-6ff0fb223d1a.png)

### CLAVES

![image](https://user-images.githubusercontent.com/23094588/124796608-a5af3480-df51-11eb-9b80-6e73df6bb1bb.png)






