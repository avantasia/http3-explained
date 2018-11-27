## Transferencias de datos confiables

Si bien UDP no es un transporte confiable, QUIC agrega una capa encima de UDP 
que introduce confiabilidad. Ofrece retransmisiones de paquetes, control de la
congestión, ritmo y otras características que de lo contrario están presentes en TCP.

Los datos enviados a través de QUIC desde un punto final aparecerán en el otro 
extremo tarde o temprano, siempre y cuando se mantenga la conexión.