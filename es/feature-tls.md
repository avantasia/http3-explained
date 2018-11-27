## TLS 1.3

La seguridad de transporte utilizada en QUIC está utilizando TLS 1.3  ([RFC
8446](https://tools.ietf.org/html/rfc8446)) y nunca hay una conexión QUIC sin cifrado.

TLS 1.3 tiene varias ventajas en comparación con versiones anteriores de TLS, pero 
la principal razón para usarlo en QUIC es que 1.3 cambió el saludo para requerir menos
viajes de ida y vuelta. Esto reduce la latencia del protocolo.

La versión heredada de Google de QUIC usó una criptografía personalizada.