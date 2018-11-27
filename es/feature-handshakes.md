# Saludos rápidos

QUIC ofrece configuraciones de conexión 0-RTT y 1-RTT, lo que significa que 
en el mejor de los casos QUIC no necesita viajes de ida y vuelta adicionales 
al configurar una nueva conexión. El mas rápido de esos dos, el saludo 0-RTT,
 solo funciona si ha habido una conexión establecida con un host y un secreto 
 de esa conexión ha sido almacenada en caché.

## Datos tempranos

QUIC permite que un cliente incluya datos que ya están en elsaludo 0-RTT. Esta 
característica permite que un cliente entregue datos al otro extremo lo más 
rápido posible, y eso, por supuesto, permite que el servidor responda y envíe 
datos de vuelta incluso antes.
