### Práctica de integración sobre tu ecommerce

## DESAFÍO COMPLEMENTARIO:

# Consigna

> Con base en el proyecto que venimos desarrollando, toca solidificar algunos procesos

# Aspectos a incluir

> Mover la ruta suelta <strong>/api/users/premium/:uid<strong> a un router específico para usuarios en /api/users/

![alt text](/img/image.png)

> Modificar el modelo de User para que cuente con una nueva propiedad “documents” 
> el cual será un array que contenga los objetos con las siguientes propiedades
>- name: String (Nombre del documento).
>- reference: String (link al documento).

![alt text](/img/image-1.png)

>No es necesario crear un nuevo modelo de Mongoose para éste.
>
>Además, agregar una propiedad al usuario llamada “last_connection”, la cual deberá modificarse cada vez que el
>usuario realice un proceso de login y logout

![alt text](/img/image-2.png)

>Crear un endpoint en el router de usuarios api/users/:uid/documents con el método POST que permita subir uno o
>múltiples archivos. Utilizar el middleware de Multer para poder recibir los documentos que se carguen y actualizar
>en el usuario su status para hacer saber que ya subió algún documento en particular.

![alt text](/img/image-3.png)


>El middleware de multer deberá estar modificado para que pueda guardar en diferentes carpetas los diferentes archivos que se suban.

>Si se sube una imagen de perfil, deberá guardarlo en una carpeta profiles, en caso de recibir la imagen de un producto, deberá guardarlo en una carpeta products, mientras que ahora al cargar un documento, multer los guardará en una carpeta documents.

![alt text](/img/image-4.png)

>Modificar el endpoint /api/users/premium/:uid   para que sólo actualice al usuario a premium si ya ha cargado los siguientes documentos:
>
> -Identificación, Comprobante de domicilio, Comprobante de estado de cuenta

![alt text](/img/image-5.png)

![alt text](/img/image-6.png)

![alt text](/img/image-7.png)

>Si el Usuario ya subio los documentos desaparece el link

![alt text](/img/image-8.png)