
# How to Build a Login Form - Cómo Crear un Formulario de Inicio de Sesión

* Generando el formulario de inicio de sesión
* Finalización del formulario de inicio de sesión
* Control de mensajes de error
* Redirigir a la última página a la que se accedió con TargetPathTrait

> ℹ️ Si está buscando la opción de firewall **`form_login`**, [consulte Uso del proveedor de autenticación **`form_login`**](https://symfony.com/doc/current/security/form_login.html).

¿Listo para crear un formulario de inicio de sesión? Primero, asegúrese de haber seguido la [Guía de Seguridad](https://symfony.com/doc/current/security.html) principal para instalar la seguridad y crear su clase de usuario.

## Generando el formulario de inicio de sesión

La creación de un formulario de inicio de sesión potente se puede iniciar con el comando **`make:auth`** de [MakerBundle](https://symfony.com/doc/current/bundles/SymfonyMakerBundle/index.html). Dependiendo de su configuración, es posible que se le hagan diferentes preguntas y su código generado puede ser ligeramente diferente:

![image](https://user-images.githubusercontent.com/23094588/127173438-3d2c5a7a-46ce-4805-874d-f87fabf8b420.png)

> ℹ️ **Nuevo en la versión 1.8**: Se agregó soporte para la autenticación del formulario de inicio de sesión para **`make:auth`** en MakerBundle 1.8.

Esto genera lo siguiente: 

1) Rutas y controlador de inicio de sesión/cierre de sesión
2) Una plantilla que muestra el formulario de inicio de sesión
3) Una clase de [Guard authenticator](https://symfony.com/doc/current/security/guard_authentication.html) que procesa el envío de inicio de sesión y 
4) Actualiza el archivo de configuración de seguridad principal.

**Paso 1**. Las rutas y el controlador **`/login/`** **`/logout`**:
