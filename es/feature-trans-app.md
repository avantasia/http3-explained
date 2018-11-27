## Transporte y nivel de aplicación

El protocolo IETF QUIC es un protocolo de transporte, sobre el que otros
protocolos de aplicación pueden ser utilizados. El protocolo de capa de 
aplicación inicial es HTTP/3 (h3).

La capa de transporte hace conexiones y flujos.

La versión heredada de Google de QUIC tenía transporte y HTTP pegados en
un solo multipropósito y era más un protocolo con la misión especial de 
enviar tramas http/2 sobre udp.
