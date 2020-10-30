
<div style="text-align: center">

# Hypertext Transfer Protocol 

<div/>

##	Peticiones
#### GET 

solicita una representación del recurso especificado. Las solicitudes que usan GET solo deben recuperar datos.

#### HEAD
El método HEAD pide una respuesta idéntica a la de una petición GET, pero sin el cuerpo de la respuesta.

#### POST
El método POST se utiliza para enviar una entidad a un recurso en específico, causando a menudo un cambio en el estado o efectos secundarios en el servidor.

#### PUT
El modo PUT reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición.

#### DELETE
El método DELETE borra un recurso en específico.

#### CONNECT
El método CONNECT establece un túnel hacia el servidor identificado por el recurso.

#### OPTIONS
El método OPTIONS es utilizado para describir las opciones de comunicación para el recurso de destino.

#### TRACE
El método TRACE  realiza una prueba de bucle de retorno de mensaje a lo largo de la ruta al recurso de destino.

#### PATCH
El método PATCH  es utilizado para aplicar modificaciones parciales a un recurso.

##		Respuestas
<div style="text-align: justify">

Los códigos de estado de respuesta HTTP indican si una solicitud HTTP específica se ha completado correctamente. Las respuestas se agrupan en cinco clases:

#### -Respuestas informativas (100-199):

	100 Continuar
Esta respuesta provisional indica que todo está bien hasta ahora y que el cliente debe continuar con la solicitud o ignorar la respuesta si la solicitud ya ha finalizado.

	101 Protocolo de conmutación
Este código se envía en respuesta a un encabezado de solicitud de actualización del cliente e indica el protocolo al que está cambiando el servidor.

	102 Procesamiento (WebDAV)
Este código indica que el servidor ha recibido y está procesando la solicitud, pero aún no hay respuesta disponible.
	

#### -Respuestas satisfactorias (200-299)

	200 OK
La solicitud se ha realizado correctamente. El significado del éxito depende del método HTTP:
GET: el recurso se ha recuperado y se transmite en el cuerpo del mensaje.
HEAD: Los encabezados de la entidad están en el cuerpo del mensaje.
PUT o POST: el recurso que describe el resultado de la acción se transmite en el cuerpo del mensaje.
TRACE: El cuerpo del mensaje contiene el mensaje de solicitud recibido por el servidor.

	201 Creado
La solicitud se ha realizado correctamente y, como resultado, se ha creado un nuevo recurso. Esta suele ser la respuesta enviada después de las solicitudes POST o algunas solicitudes PUT.

	204 Sin contenido
No hay contenido para enviar para esta solicitud, pero los encabezados pueden ser útiles. El agente de usuario puede actualizar sus encabezados en caché para este recurso con los nuevos.

#### -Redireccionamientos (300–399)

	307 redireccionamiento temporal
El servidor envía esta respuesta para indicarle al cliente que obtenga el recurso solicitado en otro URI con el mismo método que se utilizó en la solicitud anterior. 

	308 Redirección permanente
Esto significa que el recurso ahora se encuentra permanentemente en otro URI, especificado por el encabezado Location: HTTP Response. Tiene la misma semántica que el código de respuesta HTTP 301 Moved Permanently, con la excepción de que el agente de usuario no debe cambiar el método HTTP utilizado: si se usó un POST en la primera solicitud, se debe usar un POST en la segunda solicitud.

#### -Errores del cliente (400–499)

	403 Prohibido 
El cliente no tiene derechos de acceso al contenido; es decir, no está autorizado, por lo que el servidor se niega a proporcionar el recurso solicitado.

	404 Not found 
El servidor no puede encontrar el recurso solicitado. En el navegador, esto significa que no se reconoce la URL. En una API, esto también puede significar que el punto final es válido pero el recurso en sí no existe. Los servidores también pueden enviar esta respuesta en lugar de 403 para ocultar la existencia de un recurso a un cliente no autorizado. Este código de respuesta es probablemente el más famoso debido a su frecuente aparición en la web.

#### -Errores del servidor (500–599)

	504 Tiempo de espera de puerta de enlace
Esta respuesta de error se da cuando el servidor actúa como puerta de enlace y no puede obtener una respuesta a tiempo.

	505 Versión HTTP no compatible 
La versión HTTP utilizada en la solicitud no es compatible con el servidor.
<div/>

