## HTTP/3

La capa HTTP realiza transportes al estilo HTTP, incluida la compresión del 
encabezado HTTP usando QPACK, que es muy similar a la compresión HTTP/2 llamada HPACK.

El algoritmo HPACK depende de una entrega *ordenada* de flujos, por lo que no fue
posible reutilizar eso para HTTP/3 sin modificaciones ya que QUIC ofrece
flujos que pueden ser entregados fuera de orden. QPACK puede ser visto como la
versión adaptada para QUIC de [HPACK](https://httpwg.org/specs/rfc7541.html).