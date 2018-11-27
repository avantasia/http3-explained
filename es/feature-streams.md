## Múltiples flujos dentro de conexiones

De forma similar a SCTP, SSH y HTTP/2, QUIC presenta flujos lógicos separados dentro 
de las conexiones físicas. Una serie de flujos paralelos que pueden transferir datos
simultáneamente a través de una sola conexión sin afectar a los otros flujos.

Una conexión es una configuración negociada entre dos puntos finales de forma similar 
a cómo funciona una conexión TCP. Se realiza una conexión QUIC a un puerto UDP y una 
dirección IP, pero una vez establecida, la conexión está asociada por su "ID de conexión".

Sobre una conexión establecida, cualquiera de los lados puede crear flujos y enviar datos
al otro extremo. Los flujos se entregan en orden y son confiables, pero diferentes 
flujos pueden ser entregados fuera de orden.

QUIC ofrece control de flujo tanto en conexión como en flujos.

Ver más detalles en las secciones de [conexiones](quic-connections.md) y [flujos](quic-streams.md)