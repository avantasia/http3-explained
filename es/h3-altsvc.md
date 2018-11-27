# Alt-svc

La cabecera de servicio alternativo (Alt-svc :) y su correspondiente trama de 
HTTP/2 `ALT-SVC` no se crean específicamente para QUIC o HTTP/3. Son parte de un
mecanismo ya diseñado y creado para que un servidor le diga a un cliente: 
*"mira, ejecuto el mismo servicio en ESTE HOST utilizando ESTE PROTOCOLO en ESTE 
PUERTO "*. Ver detalles en [RFC 7838](https://tools.ietf.org/html/rfc7838).

Se recomienda para un cliente que reciba una respuesta Alt-svc de este tipo que, 
si lo soporta y quiere, se conecte a ese otro host en paralelo en segundo
plano - usando el protocolo especificado - y si es exitoso cambie sus
operaciones a eso en lugar de la conexión inicial.

Si la conexión inicial utiliza HTTP/2 o incluso HTTP/1, el servidor puede responder
e informar al cliente de que puede conectarse de nuevo y probar HTTP/3. Podría 
ser para el mismo host u otro que sepa servir ese origen. 
La información dada en dicha respuesta Alt-svc tiene un temporizador de expiración 
que hace que los clientes sean informados de eso durante un período de tiempo 
de forma que las conexiones y las solicitudes pueden ir directamente al host 
alternativo utilizando el protocolo alternativo sugerido.

## Ejemplo

Un servidor HTTP incluye un encabezado `Alt-Svc:` en su respuesta:

    Alt-Svc: h3=":50781"

Esto indica que HTTP/3 está disponible en el puerto UDP 50781 con el 
mismo nombre de host que se utilizó para obtener esta respuesta.

Un cliente puede intentar configurar una conexión QUIC a ese destino y
si tiene éxito, continuar comunicándose con el origen de esa forma en 
lugar de con la versión inicial de HTTP.