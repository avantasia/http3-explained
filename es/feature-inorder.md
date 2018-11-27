## ‎Entrega en orden

QUIC garantiza la entrega de flujos en orden, pero no entre flujos. Esto
significa que cada flujo enviará datos y mantendrá el orden de los datos, 
¡pero cada flujo puede llegar al destino en un orden diferente al que la 
la aplicación los envió en el extremo del envio!

Por ejemplo: los flujos A y B se transfieren de un servidor a un cliente. 
El flujo A se inicia primero y luego el flujo B. En QUIC, un paquete perdido 
solo afectaría a el(los) flujo(s) a los que pertenece el paquete perdido. 
Si el flujo A tiene un paquete perdido, y el flujo B no, el flujo B puede 
continuar sus transferencias y completarse mientras que el flujo A estará 
recibiendo su paquete perdido retransmitido. Esto no era posible con HTTP / 2.

Ilustrado aquí con un flujo amarillo y uno azul enviados entre dos puntos 
finales de QUIC sobre una sola conexión. Son independientes y pueden llegar 
en un orden diferente, pero cada flujo se entrega de manera confiable en orden.

![dos flujos de QUIC entre dos ordenadores](../images/quic-chain-streams.png)
